---
title: 實作 [!DNL Analytics for Advertising Cloud]的必要條件和重要資訊
description: 實作 [!DNL Analytics for Advertising Cloud]的必要條件和重要資訊
feature: Integration with Adobe Analytics
exl-id: 08e54e2b-ed9b-4489-8de5-ab1379b7133c
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# 實作[!DNL Analytics for Advertising Cloud]的必要條件和重要資訊

*廣告商與Advertising Cloud DSP和Advertising Cloud Search*

請先檢閱下列資訊，再將Advertising Cloud與Adobe Analytics整合。

## [!DNL Analytics]中報告Advertising Cloud資料的需求

* Experience CloudIdentity服務：`visitorAPI.js`版本2.0或更高版本
* 任何Adobe Analytics版本（包括[!DNL Prime]、[!DNL Premium]或[!DNL Ultimate]）
* Adobe Analytics:`appMeasurement.js`版本2.1或更高版本

>[!TIP]
>
>若要改善資料保真度，請使用具有CNAME支援的最新版Experience CloudIdentity Service，以及最新版的Analytics AppMeasurement for JavaScript。

## 與Advertising Cloud共用Analytics區段的需求

* Experience CloudIdentity服務：`visitorAPI.js`版本2.1或更高版本
* Adobe Analytics:`!DNL appMeasurement.js`版本1.8或更高版本

## 在Advertising Cloud中報告[!DNL Analytics]資料的需求

為Advertising Cloud實作團隊提供下列項目：

* [!DNL Analytics]報表套裝ID，將用於報告付費媒體活動以及饋送網站活動以在Advertising Cloud中最佳化和報告
* 公司的Experience Cloud組織ID（組織ID）。

您可以在Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html)的[摘要畫面中找到這兩個ID。

![Experience Cloud Debugger摘要畫面](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Advertising Cloud中的資料 {#lookback-a4adc}

因為[!DNL Analytics]資料會傳送至Advertising Cloud以進行報告和最佳化，因此資料會受到歸因規則的約束，包括針對Advertising Cloud中的廣告商設定的曝光和點擊回顧期間。

![Advertising Cloud中的廣告商層級回顧期間設定](/help/integrations/assets/a4adc-lookbacks.png)

* Advertising Cloud歸因點擊回顧期間：首次點按發生後的天數，點按可歸因於轉換。 預設情況下，此值為60天；最多90天
* Advertising Cloud歸因曝光回顧期間：廣告曝光發生後的天數，可將曝光歸因於轉換。 預設情況下，此值為14天；最多30天

   >[!NOTE]
   >
   > 曝光回顧期間是Advertising Cloud專屬的，而非[!DNL Analytics for Advertising Cloud]，報表。

[!DNL Analytics for Advertising Cloud] JavaScript會使用這些設定來判斷要將檢視項目或點進項目視為有效的距離。 如需如何判斷閱覽和點進次數的詳細資訊，請參閱「[Analytics使用的Advertising Cloud ID](ids.md)」。

## [!DNL Analytics]中的Advertising Cloud資料

[!DNL Analytics] 在Analytics點擊中設定Advertising Cloud ID(AMO ID)，但受廣告商的eVar持續性設定所限，該設定同時適用於點進和閱覽。永續性設定是在Advertising Cloud後端設定，您的Adobe帳戶管理員可加以變更。

* [!DNL Analytics for Advertising Cloud] eVar過期時間：AMO ID預設為60天

>[!NOTE]
>
>若要區隔不同時間範圍的資料，您可以[設定自訂區段](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html)，在Analysis Workspace中使用不同回顧期間。

## 支援的廣告環境

* 搜尋
* 顯示
* 影片
* 線上影片
* 原生

如需各個管道中最新支援的廣告環境，請聯絡您的Adobe客戶經理。

## 實作前須知

* 此整合不需額外付費，伺服器呼叫也不會產生額外的[!DNL Analytics]或Advertising Cloud費用。

* [!DNL Analytics for Advertising Cloud] 廣告伺服器不受限：任何廣告伺服器都可能提供閱覽或點進，而網站登入時會產生正確的ID。

* 整合只會將[!DNL Analytics]標準和自訂事件傳遞至Advertising Cloud，以便對後續付費媒體和廣告工作進行最佳化出價。 它不會將[!DNL Analytics]區段、計算量度和eVar傳遞至Advertising Cloud以進行競價最佳化。

* Advertising Cloud會根據使用者進入網站前所點按或檢視的最後一個廣告，根據Advertising Cloud中設定的[點按和檢視回顧視窗](#lookback-a4adc)，在[!DNL Analytics]內建立永久性ID。 如果網站訪客的設定檔內有兩種網站登入互動類型，且點按位於回顧期間內，則訪客的點進ID會覆寫網站報告的閱覽ID。

* [!DNL Analytics for Advertising Cloud] Adobe Analytics中的轉換追蹤使用可設定的追蹤回顧期間（預設為60天）。Advertising Cloud報表會反映整個追蹤回顧期間的網站轉換和參與。

* 支援所有廣告類型。 不過，並非所有廣告環境都受支援。

   例如，連線電視(CTV)廣告不會受到追蹤，因為CTV中不會發生點按，且同一部裝置上不會發生轉換。 不過，如果在案頭環境中檢視廣告，則可能會追蹤某些閱覽網站項目資料。

* [!DNL Analytics] 目前只會追蹤轉換，並將其歸因於相同裝置上的訪客。

* [!DNL Analytics for Advertising Cloud] 不支援應用程式內檢視轉換。

* 使用[!DNL Analytics]的伺服器端轉送實作的廣告商不支援閱覽追蹤。

### 補充ID

為網站實作Experience CloudIdentity服務後，包含[!DNL Analytics]或Advertising Cloud資料的點擊就會包含補充ID。

範例：`sdid=2F3C18E511F618CC-45F83E994AEE93A0`

為了精確資料整合，[!DNL Analytics for Advertising Cloud]活動用來傳送內容或記錄目標量度的所有Advertising Cloud呼叫，必須有共用相同補充ID的對應[!DNL Analytics]點擊。

在[!DNL Analytics]中進行疑難排解時，請務必確認[!DNL Analytics]點擊有補充ID。 在[Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html)中，您可以在Advertising Cloud標籤中看到此ID為`sdid`參數。

>[!NOTE]
>
> 此實作的運作方式與[!DNL Analytics for Target]整合類似。

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [適用於Analytics for Advertising Cloud的JavaScript程式碼](/help/integrations/analytics/javascript.md)

