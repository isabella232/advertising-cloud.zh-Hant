---
title: 概觀 [!DNL Analytics for Advertising Cloud]
description: 概觀 [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: bfbfc293ad04b294c813ce7c8a11200e70fc812f
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---

# 概觀 [!DNL Analytics for Advertising Cloud]

*廣告商與Advertising Cloud DSP和Advertising Cloud Search*

[!DNL Analytics for Advertising Cloud] 整合Adobe Analytics和Adobe Advertising Cloud以擴充及增強每項產品的功能。

整合可讓廣告商追蹤其中的點進和閱覽網站互動 [!DNL Analytics] 例如，讓品牌了解其廣告支出如何帶來網站參與和關鍵業務目標。

此外，Advertising Cloud還可存取大量第一方資料， [!DNL Analytics] 收集使用 [!DNL Analytics] 標籤。 這可讓更健全的歷程管理、第一方再行銷和付費媒體網站報告。 Advertising Cloud可進一步使用 [!DNL Analytics] 用於支出和競標最佳化的資料。

如果適當使用， [!DNL Analytics for Advertising Cloud] 模糊兩種傳統角色之間的界限：advertising journey management（透過廣告將使用者傳送至網站的行為），並透過web analytics了解該網站的參與度。

主要優點：

* 傳送 [!DNL Analytics] 區段直接匯入Advertising Cloud，以進行第一方網站再行銷。
* 使用 [!DNL Analytics] 將自訂和標準事件設為轉換訊號，以最佳化付費媒體廣告。
* 善用 [!DNL Analytics] Analysis Workspace，以更清楚了解網站登入點和造訪行為。
* 讓網路分析師與付費媒體團隊之間更密切的協作。
* 在中使用永續性Advertising Cloud閱覽和點進ID [!DNL Analytics] 了解網站參與。
* 使用自訂量度、自訂維度以及將資料或像素匯出至廣告伺服器或其他DSP時無法實現的網站活動，增強Analysis Workspace中的傳統付費媒體報表。
* 善用 [!DNL Analytics] 已在您網站上的程式碼，以在Advertising Cloud中追蹤和最佳化。

>[!TIP]
>
> 觀看 [影片簡介 [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## 將Analytics用於付費媒體報表

[!DNL Analytics for Advertising Cloud] 可讓您透過：

* 在中使用永續性Advertising Cloud閱覽和點進ID [!DNL Analytics] 了解網站參與。
* 運用Analysis Workspace，更清楚了解網站登入點和造訪行為。 您可以存取付費媒體維度和事件資料，包括Advertising Cloud促銷活動實體名稱（包括版位和廣告）及其相關量度，例如點按、曝光數和成本。

使用 [!DNL Analytics] 您的組織需要Experience Cloud登入才能存取Analysis Workspace，做為您的付費媒體報表工具。 您的Advertising Cloud團隊會協助您將Advertising Cloud資料對應至Analysis Workspace中的個別報表套裝。 您可以傳送Advertising Cloud資料至任何報表套裝，但請注意已對應至Advertising Cloud的報表套裝，以及未對應的報表套裝。這可能會變更所報告的資料，視報表套裝而定。

[Advertising Cloud ID [!DNL Analytics]](ids.md) 如同其他eVar，具有自訂的持續有效期。 依預設，在Advertising Cloud實作期間，歸因回顧期間會設為60天。 若要變更此設定，請使用 [!DNL Adobe] 客戶經理。

Advertising Cloud維度會附加尾碼「(AMO ID)」(例如「廣告類型(AMO ID)」)。 請參閱「[Advertising CloudAnalysis Workspace量度](advertising-cloud-metrics-in-analytics.md)「 」，以取得可用維度的清單。

>[!NOTE]
>
> 當您在以下位置檢視Advertising Cloud資料（或任何資料集）時 [!DNL Analytics]，請注意，量度和報表是根據 [!DNL Analytics]. 資料可能與您在其他報表系統（例如廣告伺服器報表）中看到的不同 [!DNL DSP] 報表或搜尋引擎報表。 若要了解 [!DNL Analytics]，您必須知道eVar資料何時過期、定義造訪的內容、上次接觸歸因與持續歸因總計的比較，以及其他因素。 如需詳細資訊，請參閱 [之間的預期資料差異 [!DNL Analytics] 和Advertising Cloud](data-variances.md).

## 使用Analytics強化Advertising Cloud促銷活動和Portfolio

無需任何額外像素， [!DNL Analytics for Advertising Cloud] 將兩個主要訊號傳送至Advertising Cloud，讓最佳化和更輕鬆地劃分對象：

* 要用作競標訊號的轉換量度：
   * 標準量度，例如 [!UICONTROL Revenue] 和 [!UICONTROL Cart Views].
   * 網站參與量度，例如頁面檢視和造訪量度。
   * 自訂收入量度。
   * 保留收入量度。
* 在中建立的區段 [!DNL Analytics] 並發佈至Experience Cloud。

   您可以使用 [!DNL Analytics] 中第一方網站重新定位的區段 [!DNL DSP] 付費搜索廣告。

   (僅限Advertising Cloud Search)廣告商 [!DNL Analytics] 但不能Audience Manager也能建立Google網站標籤型對象（再行銷清單）和客戶比對對象（客戶清單），從 [!DNL Analytics] 共用給Experience Cloud的區段。

### 網站轉換量度作為競標訊號

您可以使用標準事件和自訂事件，來自 [!DNL Analytics] 在Advertising Cloud建立加權目標。 目標為您的競標決策提供資訊 [!DNL DSP] 套件和搜尋產品組合。

>[!NOTE]
>
> 您無法映射 [!DNL Analytics] 進入Advertising Cloud。

您的Advertising Cloud團隊將協助您識別並對應適用於付費媒體效能的事件，並將這些事件顯示在Advertising Cloud中 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

請參閱「[Advertising Cloud中的Analytics量度](analytics-data-in-advertising-cloud.md)」，取得可用量度的清單。

### 網站重新定位的Analytics區段

Advertising Cloud可以擷取 [!DNL Analytics] 區段，以用於再行銷用途，Advertising Cloud DSP和 [!DNL Search] 廣告，使用的Experience Cloud對象整合 [!DNL Analytics] 和Experience Cloud。

若要存取 [!DNL Analytics] 區段，廣告商帳戶需要 [Experience CloudID服務](https://experienceleague.adobe.com/docs/id-service/using/home.html) 已啟用。 啟用ID服務時，所有Experience Cloud區段(包括 [!DNL Analytics] 發佈至Experience Cloud、在Adobe Audience Manager中建立的區段、在Experience Cloud中建立的區段，使用 [!DNL People core service]、和在Adobe Experience Platform中建立並透過Audience Manager傳送至Advertising Cloud的區段)，一經處理，即可在Advertising Cloud中使用。

[!DNL Analytics] 區段會在24小時內提供，且會每天更新。

如需「Experience Cloud對象」服務的詳細資訊，請參閱 [Experience Cloud對象](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## 如何使用整合的範例

### 在Analysis Workspace中使用Advertising Cloud資料

若要了解如何使用Advertising Cloud資料在Analysis Workspace中建立視覺化報表，請參閱影片「[工作區和報表簡介](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### 建立Advertising Cloud控制面板

若要了解如何根據您在Analysis Workspace中的目標追蹤Advertising Cloud資料，請參閱影片「[使用Advertising Cloud建立Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### 使用Advertising Cloud ID進行網站登入分析

若要了解如何建立Advertising Cloud網站項目報表來監控星期幾、每日時間、瀏覽器和地理位置的影響，請參閱影片「[建立Advertising Cloud網站項目報表](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [影片：簡介 [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [實作的必要條件和重要資訊 [!DNL Analytics for Advertising Cloud]](prerequisites.md)
>* [Advertising Cloud使用的ID](ids.md)
>* [適用於Analytics for Advertising Cloud的JavaScript程式碼](/help/integrations/analytics/javascript.md)
>* [之間的預期資料差異 [!DNL Analytics] 和Advertising Cloud](data-variances.md)
>* [Advertising CloudAnalysis Workspace量度](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Advertising Cloud中的資料](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

