---
title: 實作的必要條件和重要資訊 [!DNL Analytics for Advertising]
description: 實作的必要條件和重要資訊 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 08e54e2b-ed9b-4489-8de5-ab1379b7133c
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# 實作的必要條件和重要資訊 [!DNL Analytics for Advertising]

*廣告商與Advertising DSP及[!DNL Advertising Search]*

請先檢閱下列資訊，再將Adobe廣告與Adobe Analytics整合。

## 報告Adobe廣告資料的需求，於 [!DNL Analytics]

* 以下任一項：
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Experience CloudIdentity服務： `visitorAPI.js` 2.0版或更高版本
* 任何版本的Adobe Analytics(包括 [!DNL Prime], [!DNL Premium]，或 [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` 2.1版或更高版本

>[!TIP]
>
>若要改善資料保真度，請使用每個程式庫的最新版本。

## 與Adobe廣告共用Analytics區段的需求

* Experience CloudIdentity服務： `visitorAPI.js` 2.1版或更高版本
* Adobe Analytics: `!DNL appMeasurement.js` 1.8版或更高版本

## 報告需求 [!DNL Analytics] Adobe廣告中的資料

為Adobe廣告實作團隊提供下列項目：

* 此 [!DNL Analytics] 報表套裝ID，用於報告付費媒體活動以及饋送網站活動以最佳化Adobe廣告中的報表
* 公司的Experience Cloud組織ID（組織ID）。

您可以在 [Adobe Experience Cloud Debugger的摘要標籤](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Experience Cloud Debugger摘要畫面](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Adobe廣告中的資料 {#lookback-a4adc}

因為 [!DNL Analytics] 資料會傳送至「Adobe廣告」以進行報表和最佳化，則資料會受到「Adobe廣告」中為廣告商設定的歸因規則所限制，包括曝光和點擊回顧期間。

![Adobe廣告中的廣告商層級回顧期間設定](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe廣告歸因點擊回顧期間：首次點按發生後的天數，點按可歸因於轉換。 預設情況下，此值為60天；最多90天
* Adobe廣告歸因曝光回顧期間：廣告曝光發生後的天數，可將曝光歸因於轉換。 預設情況下，此值為14天；最多30天

   >[!NOTE]
   >
   > 曝光回顧期間是Adobe廣告專屬的，而非 [!DNL Analytics for Advertising]，報告。

此 [!DNL Analytics for Advertising] JavaScript會使用這些設定來判斷要將檢視項目或點進項目視為有效的距離。 如需如何判斷閱覽和點進的詳細資訊，請參閱「[AdobeAnalytics使用的Advertising ID](ids.md).&quot;

## Adobe廣告資料，於 [!DNL Analytics]

[!DNL Analytics] 在Analytics點擊內設定Adobe廣告ID(AMO ID)，但以廣告商的eVar持續性設定為限，此設定會同時套用至點進和閱覽。 永續性設定是在Adobe廣告後端設定，而您的 [!DNL Adobe] 客戶團隊可以變更。

* [!DNL Analytics for Advertising] eVar過期時間：AMO ID預設為60天

>[!NOTE]
>
>若要劃分不同時間範圍的資料，您可以 [設定自訂區段](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) Analysis Workspace中有不同回顧期間。

## 支援的廣告環境

* 搜尋
* 顯示
* 影片
* 線上影片
* 原生

請連絡您的 [!DNL Adobe] 客戶團隊，了解每個管道中最新支援的廣告環境。

## 實作前須知

* Adobe廣告實作團隊會設定整合。

* 此整合不需額外付費，伺服器呼叫也不會產生額外費用 [!DNL Analytics] 或Adobe廣告費。

* [!DNL Analytics for Advertising] 廣告伺服器不受限：任何廣告伺服器都可能提供閱覽或點進，而網站登入時會產生正確的ID。

* 整合僅通過 [!DNL Analytics] 標準和自訂事件來Adobe廣告，以最佳化後續付費媒體和廣告工作的出價。 沒通過 [!DNL Analytics] 區段、計算量度和eVar，以Adobe廣告以進行競標最佳化。

* Adobe廣告會在內建立永久性ID [!DNL Analytics] 根據使用者進入網站前所點按或檢視的最後一個廣告，根據 [點按和檢視回顧期間](#lookback-a4adc) 在Adobe廣告中設定。 如果網站訪客的設定檔內有兩種網站登入互動類型，且點按位於回顧期間內，則訪客的點進ID會覆寫網站報告的閱覽ID。

* [!DNL Analytics for Advertising] Adobe Analytics中的轉換追蹤使用可設定的追蹤回顧期間（預設為60天）。 Adobe廣告報表反映整個追蹤回顧期間的網站轉換和參與。

* 支援所有廣告類型。 不過，並非所有廣告環境都受支援。

   例如，連線電視(CTV)廣告不會受到追蹤，因為CTV中不會發生點按，且同一部裝置上不會發生轉換。 不過，如果在案頭環境中檢視廣告，則可能會追蹤某些閱覽網站項目資料。

* [!DNL Analytics] 目前只會追蹤轉換，並將其歸因於相同裝置上的訪客。

* [!DNL Analytics for Advertising] 不支援應用程式內檢視轉換。

* 使用的伺服器端轉送實作的廣告商不支援閱覽追蹤 [!DNL Analytics].

### 補充ID

為網站實作「Experience Cloud身分識別服務」後，會出現包含資料的點擊 [!DNL Analytics] 或Adobe廣告包含補充ID。

範例： `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

為了精確整合資料， [!DNL Analytics for Advertising] 傳送內容或記錄目標量度的活動必須具有對應的 [!DNL Analytics] 點擊會共用相同的補充ID。

當您在 [!DNL Analytics]，請務必確認是否有 [!DNL Analytics] 點擊。 在 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)，您可以在「Adobe廣告」標籤中看到此ID作為 `sdid` 參數。

>[!NOTE]
>
> 此實作的運作方式與 [!DNL Analytics for Target] 整合。

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising]](overview.md)
>* [Analytics for Advertising的JavaScript程式碼](/help/integrations/analytics/javascript.md)

