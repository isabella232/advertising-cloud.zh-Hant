---
title: 設定Adobe Target中Adobe廣告的A/B測試
description: 了解如何在 [!DNL Target] 針對您的DSP [!DNL Search] 廣告。
exl-id: 97055645-4b2f-4795-830d-9ce89ae2ad15
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '1654'
ht-degree: 0%

---

# 在Adobe Target中設定A/B測試以用於Advertising DSP和 [!DNL Advertising Search] 廣告

<!-- Add [!UICONTROL and [!DNL tags throughout as needed. -->

<!-- Break into sub-files, or just leave as one? -->

*僅具有Advertising DSP的廣告商*

Adobe廣告和Adobe Target可讓行銷人員更輕鬆地在付費媒體和站上訊息間提供個人化且互聯的體驗。 透過在產品之間共用訊號，您可以：

* 將客戶的廣告曝光度從DSP促銷活動連結至其站上體驗，借此降低網站落後率。

* 透過使用Adobe Audience Manager曝光資料和點按以摘要的Target對象，透過廣告訊息鏡像站上體驗，建立A/B測試。

* 透過Adobe Analytics中的簡單視覺效果，測量統一訊息對站上目標提升度的影響 [!DNL Target].

如需設定點進和閱覽追蹤、實作DSP與 [!DNL Target] 並設定A/B測試活動 [!DNL Analytics] Analysis Workspace以檢視測試資料。

如有其他問題，請聯繫adcloud_support@adobe.com。

## 必要條件

此使用案例需要下列產品和整合：

* [!DNL Target]

* [[!DNL Analytics] 廣告](/help/integrations/analytics/overview.md) 整合<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) 整合

* Audience Manager（僅適用於閱覽測試）

## 步驟1:設定點進架構 {#click-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![點進架構](/help/integrations/assets/target-ct-framework.png)

當您將DSP巨集新增至點進URL（使用者點按廣告並到達登錄頁面時顯示的URL）時，DSP會透過包含 ```${TM_PLACEMENT_ID}``` 在點進URL中。 此巨集會擷取英數字元放置金鑰，而非數值放置ID。

![點進URL附加至登陸頁面URL](/help/integrations/assets/target-ct-url.jpg)

### (僅限DSP)將DSP巨集新增至點進URL

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

在Flash談話或Google Campaign Manager 360中，手動更新每個廣告的點進URL，納入擷取AMO ID變數所需的巨集。 AMO ID變數可用來將點按資料傳送至Adobe Analytics，以及共用版位索引鍵以進行A/B測試。 如需指示，請參閱下列頁面：

* [附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤](/help/integrations/analytics/macros-flashtalking.md)

* [附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Google Campaign Manager 360] 廣告標籤](/help/integrations/analytics/macros-google-campaign-manager.md)

請連絡您的DSP帳戶團隊和Advertising解決方案群組(aac-advertising-solutions-group@adobe.com)，以擷取所需的版位金鑰並完成設定，並確保每個點進URL都已填入版位金鑰。

## 步驟2:使用Audience Manager設定閱覽架構 {#view-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![閱覽架構](/help/integrations/assets/targetr-vt-framework.png)

在您的廣告標籤和位置設定中新增Audience Manager曝光事件像素，您可以建立測試區段，以了解其他閱覽測試機會。

1. 在您的廣告標籤和DSP位置設定中實作Audience Manager曝光事件像素。

   有關說明，請參閱[從Advertising DSP促銷活動收集媒體曝光資料](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   請務必新增 [DSP巨集](/help/dsp/campaign-management/macros.md) 擷取您要讓曝光事件像素傳回的所有資料，包括 `${TM_PLACEMENT_ID_NUM}` ，以取得數值位置ID。

   >[!NOTE]
   >
   >點擊追蹤URL包含 `${TM_PLACEMENT_ID}` 用於字母數字放置鍵的宏，而不是 `${TM_PLACEMENT_ID_NUM}` ，以取得數值位置ID。

1. 從DSP曝光資料設定Audience Manager區段：

   1. 前往 **Audience Manager** > **對象資料** > **訊號**，然後選取 **搜尋** 標籤。

   1. 輸入 **金鑰** 和 **值** 用於決定區段使用者分組的層級的訊號。 使用 [受支援金鑰](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=en) 的值會與您新增至Audience Manager曝光事件像素的巨集對應。

      例如，若要針對特定版位將使用者分組，請使用 `d_placement` 鍵。 對於值，請使用DSP巨集擷取的實際數值放置ID(例如上方螢幕擷取畫面中的2501853) `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

      如果「總計」欄位顯示機碼值組的使用者計數，指出像素已正確放置且資料正在流動，則您可以繼續進行下一個步驟。
   ![搜尋訊號](/help/integrations/assets/target-am-signals.png)

1. [建立規則型特徵](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) 以在Audience Manager中建立區段。

   1. 為特徵命名，以便在測試活動中輕鬆識別。 將特徵儲存在您偏好的資料夾中。

   1. 從 **資料來源** 下拉式功能表，選取 **Ad Cloud**.

   1. 在運算式產生器中，新增 ```d_event``` 在「金鑰」欄位和 ```imp``` 在 **值** 欄位，選擇 **新增規則**，然後儲存特徵。

   ![規則型特徵的螢幕擷圖](/help/integrations/assets/target-am-trait.png)

1. 在Audience Manager中設定測試區段：

   1. 在頁面頂端，前往 **對象資料** > **特徵** 和搜尋完整特徵名稱。 選取特徵名稱旁的核取方塊，然後按一下 **建立區段**.

   1. 命名區段，選取 `Ad Cloud` 作為 **資料來源**，然後儲存區段。

      Audience Manager會自動將區段分割為控制組，該控制組接收標準著陸頁面體驗，以及測試組接收個人化的站上體驗。
   ![測試區段的螢幕擷圖](/help/integrations/assets/target-am-segment.png)

## 步驟3:在Target中設定「A/B測試」活動

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

下列指示會反白顯示DSP使用案例的相關資訊。 如需完整指示，請參閱[建立A/B測試](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)」

1. [登入Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. 從 **活動** 清單，按一下 **建立活動** > **A/B測試**.

   ![建立A/B測試活動](/help/integrations/assets/target-create-ab.png)

1. 在 **輸入活動URL***欄位，輸入測試的登錄頁面URL。

   ![輸入活動URL欄位](/help/integrations/assets/target-create-ab-url.png)

   >[!NOTE]
   >
   >您可以使用多個URL來測試閱覽網站項目。 如需詳細資訊，請參閱[多頁活動](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; 您可以透過建立 [網站登入報表](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) 中。

1. 在 **目標** 欄位，輸入測試的成功量度。

   >[!NOTE]
   >
   >確保 [!DNL Analytics] 在中以資料來源的形式啟用 [!DNL Target]，並選取正確的報表套裝。

1. 設定 **優先順序** to `High` 或 `999` 以防止在測試區段中的使用者收到錯誤的站上體驗時發生衝突。

1. 內 **報表設定**，請選取 **公司名稱** 和 **報表套裝** 已連線至您的DSP帳戶。

   如需其他報表秘訣，請參閱「[報告最佳實務和疑難排解](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

1. 在 **日期範圍** 欄位，輸入測試的適當開始和結束日期。

1. 新增對象至活動：

   1. 選擇 [區段，以測試閱覽對象](#view-through-framework).

      ![新增對象至活動](/help/integrations/assets/target-create-ab-audiences.png)

   1. 選擇 **網頁** > **登陸頁面** > **查詢**，並在 **值** 欄位來使用點進對象的Target查詢字串參數。

      ![目標點按對象的螢幕擷圖](/help/integrations/assets/target-click-audience.jpg)

1. 若 **流量分配方法**，選取 **手動（預設）** 並分開觀眾50/50。

1. 儲存活動。

1. 使用 [!DNL Target] [可視化體驗撰寫器](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) 變更A/B測試登錄頁面範本的設計。

   * 體驗A:請勿編輯，因為這是預設/控制著陸頁面體驗，不需個人化。

   * 體驗B:使用 [!DNL Target] 使用者介面，以根據測試中包含的資產（例如標題、復本、按鈕位置和創作元素）來自訂登錄頁面範本。
   >[!NOTE]
   >
   >例如，創意測試的創意測試使用案例，請連絡您的客戶團隊。

## 步驟4:設定您的 [!DNL Analytics for Target] Analysis Workspace [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T)是跨解決方案的整合，可讓廣告商建立 [!DNL Target] 活動 [!DNL Analytics] 轉換量度和受眾區段，然後使用 [!DNL Analytics] 作為報表來源時。 該活動的所有報表和區段都以 [!DNL Analytics] 資料收集。

如需 [!DNL Analytics for Target]，包括實作指示的連結，請參閱「[Adobe Analytics作為Adobe Target(A4T)的報表來源](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)」。

### 設定 [!DNL Analytics for Target] 面板

在Analysis Workspace中，設定 [!DNL Analytics for Target panel] 分析 [!DNL Target] 活動和體驗。 請記住以下關於報告的重要指針和資訊。

#### 量度

* 在工作區中建立面板，專用於執行測試的Adobe廣告促銷活動、套件或位置。 使用摘要視覺效果，在與Target測試效能相同的報表中顯示Adobe廣告量度。

* 優先使用站上量度（例如造訪和轉換）來測量效能。

* 了解來自Adobe廣告的匯總媒體量度（例如曝光數、點按和成本）無法與Target量度相符。

#### Dimension

以下維度與 [!DNL Analytics for Target]:

* **目標活動**:A/B測試的名稱

* **目標體驗**:活動內使用的登錄頁面體驗名稱

* **目標活動** > **體驗**:同一列的活動名稱和體驗名稱

### 疑難排解Analytics [!DNL Target] 資料

在Analysis Workspace中，如果您發現活動和體驗資料極少或未填入，請執行下列操作：

* 確認Target和Analytics使用相同的補充資料ID(SDID)。 您可以使用 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) 在促銷活動帶動使用者的登陸頁面上。

[Adobe偵錯工具中的補充資料ID(SDID)值](/help/integrations/assets/target-troubleshooting-sdid.png)

* 在相同的登陸頁面上，確認a)解決方案>目標下Adobe偵錯工具中顯示的主機名稱符合b)中顯示的追蹤伺服器 [!DNL Target] （位於「目標與設定>報表設定」下）。

   [!DNL Analytics For Target] 要求 [!DNL Analytics] 追蹤伺服器以在呼叫中傳送 [!DNL Target] 到 [!DNL Modstats] Analytics的資料收集伺服器。&lt;! — 只「到Analytics？」>

[Adobe偵錯工具中的主機名稱值](/help/integrations/assets/target-troubleshooting-hostname.png)

[Target中的追蹤伺服器值](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## 進一步閱讀

* [將Target與Analytics整合](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) — 說明如何在Analysis Workspace中設定Target報表。
* [A/B測試概觀](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html)  — 說明可用於DSP廣告的A/B測試活動。
* [體驗與選件](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html)  — 說明 [!DNL Target] 工具，以判斷DSP測試使用者要接觸到的站上內容。
* [訊號、特徵和區段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html)  — 定義一些可協助進行DSP檢視測試的Audience Manager工具。
* [Analytics for Advertising概觀](https://experienceleague.adobe.com/docs/advertising-cloud/integrations/analytics/overview.html)  — 推出Analytics for Advertising，可讓您追蹤Analytics例項中的點進和閱覽網站互動。

<!-- 
>[!MORELIKETHIS]
>
>* 
-->
