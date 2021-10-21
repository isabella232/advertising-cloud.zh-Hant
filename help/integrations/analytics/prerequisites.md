---
title: 實作的必要條件和重要資訊 [!DNL Analytics for Advertising Cloud]
description: 實作的必要條件和重要資訊 [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 08e54e2b-ed9b-4489-8de5-ab1379b7133c
source-git-commit: bfbfc293ad04b294c813ce7c8a11200e70fc812f
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%

---

# 實作的必要條件和重要資訊 [!DNL Analytics for Advertising Cloud]

*廣告商與Advertising Cloud DSP和Advertising Cloud Search*

請先檢閱下列資訊，再將Advertising Cloud與Adobe Analytics整合。

## 中報告Advertising Cloud資料的需求 [!DNL Analytics]

* Experience CloudIdentity服務： `visitorAPI.js` 2.0版或更高版本
* 任何版本的Adobe Analytics(包括 [!DNL Prime], [!DNL Premium]，或 [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` 2.1版或更高版本

>[!TIP]
>
>若要改善資料保真度，請使用具有CNAME支援的最新版Experience CloudIdentity Service，以及最新版的Analytics AppMeasurement for JavaScript。

## 與Advertising Cloud共用Analytics區段的需求

* Experience CloudIdentity服務： `visitorAPI.js` 2.1版或更高版本
* Adobe Analytics: `!DNL appMeasurement.js` 1.8版或更高版本

## 報告需求 [!DNL Analytics] Advertising Cloud中的資料

為Advertising Cloud實作團隊提供下列項目：

* 此 [!DNL Analytics] 報表套裝ID，用於報告付費媒體活動以及饋送網站活動以最佳化Advertising Cloud和報告
* 公司的Experience Cloud組織ID（組織ID）。

您可以在 [Adobe Experience Cloud Debugger的摘要畫面](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html).

![Experience Cloud Debugger摘要畫面](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Advertising Cloud中的資料 {#lookback-a4adc}

因為 [!DNL Analytics] 資料會傳送至Advertising Cloud以進行報告和最佳化，且資料會受到針對Advertising Cloud中的廣告商設定的歸因規則所限制，包括曝光和點擊回顧期間。

![Advertising Cloud中的廣告商層級回顧期間設定](/help/integrations/assets/a4adc-lookbacks.png)

* Advertising Cloud歸因點擊回顧期間：首次點按發生後的天數，點按可歸因於轉換。 預設情況下，此值為60天；最多90天
* Advertising Cloud歸因曝光回顧期間：廣告曝光發生後的天數，可將曝光歸因於轉換。 預設情況下，此值為14天；最多30天

   >[!NOTE]
   >
   > 曝光回顧期間是Advertising Cloud專屬，而非 [!DNL Analytics for Advertising Cloud]，報告。

此 [!DNL Analytics for Advertising Cloud] JavaScript會使用這些設定來判斷要將檢視項目或點進項目視為有效的距離。 如需如何判斷閱覽和點進的詳細資訊，請參閱「[Advertising Cloud使用的ID](ids.md).&quot;

## Advertising Cloud資料 [!DNL Analytics]

[!DNL Analytics] 在Analytics點擊中設定Advertising Cloud ID(AMO ID)，但受廣告商的eVar持續性設定所限，該設定同時適用於點進和閱覽。 永續性設定是在Advertising Cloud後端設定，而您的 [!DNL Adobe] 客戶經理可以變更。

* [!DNL Analytics for Advertising Cloud] eVar過期時間：AMO ID預設為60天

>[!NOTE]
>
>若要劃分不同時間範圍的資料，您可以 [設定自訂區段](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) Analysis Workspace中有不同回顧期間。

## 支援的廣告環境

* 搜尋
* 顯示
* 影片
* 線上影片
* 原生

請連絡您的 [!DNL Adobe] 客戶經理，了解每個管道中最新支援的廣告環境。

## 實作前須知

* 此整合不需額外付費，伺服器呼叫也不會產生額外費用 [!DNL Analytics] 或Advertising Cloud費。

* [!DNL Analytics for Advertising Cloud] 廣告伺服器不受限：任何廣告伺服器都可能提供閱覽或點進，而網站登入時會產生正確的ID。

* 整合僅通過 [!DNL Analytics] 標準和自訂事件傳送至Advertising Cloud，以最佳化後續付費媒體和廣告工作的出價。 沒通過 [!DNL Analytics] 區段、計算量度和eVar轉至Advertising Cloud，以進行競標最佳化。

* Advertising Cloud會在中建立永久性ID [!DNL Analytics] 根據使用者進入網站前所點按或檢視的最後一個廣告，根據 [點按和檢視回顧期間](#lookback-a4adc) 在Advertising Cloud中設定。 如果網站訪客的設定檔內有兩種網站登入互動類型，且點按位於回顧期間內，則訪客的點進ID會覆寫網站報告的閱覽ID。

* [!DNL Analytics for Advertising Cloud] Adobe Analytics中的轉換追蹤使用可設定的追蹤回顧期間（預設為60天）。 Advertising Cloud報表會反映整個追蹤回顧期間的網站轉換和參與。

* 支援所有廣告類型。 不過，並非所有廣告環境都受支援。

   例如，連線電視(CTV)廣告不會受到追蹤，因為CTV中不會發生點按，且同一部裝置上不會發生轉換。 不過，如果在案頭環境中檢視廣告，則可能會追蹤某些閱覽網站項目資料。

* [!DNL Analytics] 目前只會追蹤轉換，並將其歸因於相同裝置上的訪客。

* [!DNL Analytics for Advertising Cloud] 不支援應用程式內檢視轉換。

* 使用的伺服器端轉送實作的廣告商不支援閱覽追蹤 [!DNL Analytics].

### 補充ID

為網站實作「Experience Cloud身分識別服務」後，會出現包含資料的點擊 [!DNL Analytics] 或Advertising Cloud包含補充ID。

範例： `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

為了精確整合資料， [!DNL Analytics for Advertising Cloud] 傳送內容或記錄目標量度的活動必須具有對應的 [!DNL Analytics] 點擊會共用相同的補充ID。

當您在 [!DNL Analytics]，請務必確認是否有 [!DNL Analytics] 點擊。 在 [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html)，您可以在Advertising Cloud標籤中看到此ID作為 `sdid` 參數。

>[!NOTE]
>
> 此實作的運作方式與 [!DNL Analytics for Target] 整合。

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [適用於Analytics for Advertising Cloud的JavaScript程式碼](/help/integrations/analytics/javascript.md)

