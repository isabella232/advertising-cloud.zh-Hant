---
title: 概觀 [!DNL Analytics for Advertising]
description: 概觀 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 0%

---

# 概觀 [!DNL Analytics for Advertising]

*廣告商與Advertising DSP及[!DNL Advertising Search]*

[!DNL Analytics for Advertising] 整合Adobe Analytics和Adobe廣告，以擴充及增強每項產品的功能。

整合可讓廣告商追蹤其中的點進和閱覽網站互動 [!DNL Analytics] 例如，讓品牌了解其廣告支出如何帶來網站參與和關鍵業務目標。

此外，Adobe廣告可存取大量的第一方資料， [!DNL Analytics] 收集使用 [!DNL Analytics] 標籤。 這可讓更健全的歷程管理、第一方再行銷和付費媒體網站報告。 Adobe廣告可進一步使用 [!DNL Analytics] 用於支出和競標最佳化的資料。

如果適當使用， [!DNL Analytics for Advertising] 模糊兩種傳統角色之間的界限：advertising journey management（透過廣告將使用者傳送至網站的行為），並透過web analytics了解該網站的參與度。

主要優點：

* 傳送 [!DNL Analytics] 區段直接Adobe廣告，以進行第一方網站再行銷。
* 使用 [!DNL Analytics] 將自訂和標準事件設為轉換訊號，以最佳化付費媒體廣告。
* 善用 [!DNL Analytics] Analysis Workspace，以更清楚了解網站登入點和造訪行為。
* 讓網路分析師與付費媒體團隊之間更密切的協作。
* 在中使用永續性Adobe廣告閱覽和點進ID [!DNL Analytics] 了解網站參與。
* 使用自訂量度、自訂維度以及將資料或像素匯出至廣告伺服器或其他DSP時無法實現的網站活動，增強Analysis Workspace中的傳統付費媒體報表。
* 善用 [!DNL Analytics] 程式碼，以在Adobe廣告中追蹤和最佳化。

>[!TIP]
>
> 觀看 [影片簡介 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## 將Analytics用於付費媒體報表

[!DNL Analytics for Advertising] 可讓您透過：

* 在中使用永續性Adobe廣告閱覽和點進ID [!DNL Analytics] 了解網站參與。
* 運用Analysis Workspace，更清楚了解網站登入點和造訪行為。 您可以存取付費媒體維度和事件資料，包括Adobe廣告促銷活動實體名稱（直至版位和廣告）及其相關量度，例如點按、曝光數和成本。

使用 [!DNL Analytics] 您的組織需要Experience Cloud登入才能存取Analysis Workspace，做為您的付費媒體報表工具。 您的Adobe廣告團隊會協助您將Adobe廣告資料對應至Analysis Workspace中的個別報表套裝。 您可以傳送Adobe廣告資料至任何報表套裝，但您應注意已對應至Adobe廣告的報表套裝，以及尚未對應的報表套裝。這可能會變更所報告的資料，視報表套裝而定。

[Adobe廣告ID [!DNL Analytics]](ids.md) 如同其他eVar，具有自訂的持續有效期。 依預設，在「Adobe廣告」實作期間，歸因回顧期間會設為60天。 若要變更此設定，請使用 [!DNL Adobe] 客戶團隊。

Adobe廣告維度會附加尾碼「(AMO ID)」(例如「廣告類型(AMO ID)」)。 請參閱「[AdobeAnalysis Workspace中的Advertising量度](advertising-metrics-in-analytics.md)「 」，以取得可用維度的清單。

>[!NOTE]
>
> 當您在 [!DNL Analytics]，請注意，量度和報表是根據 [!DNL Analytics]. 資料可能與您在其他報表系統（例如廣告伺服器報表）中看到的不同 [!DNL DSP] 報表或搜尋引擎報表。 若要了解 [!DNL Analytics]，您必須知道eVar資料何時過期、定義造訪的內容、上次接觸歸因與持續歸因總計的比較，以及其他因素。 如需詳細資訊，請參閱 [之間的預期資料差異 [!DNL Analytics] 和Adobe廣告](data-variances.md).

## 使用Analytics強化Adobe廣告促銷活動和Portfolio

無需任何額外像素， [!DNL Analytics for Advertising] 傳送兩個主要訊號給「Adobe廣告」，讓最佳化和更輕鬆的受眾細分：

* 要用作競標訊號的轉換量度：
   * 標準量度，例如 [!UICONTROL Revenue] 和 [!UICONTROL Cart Views].
   * 網站參與量度，例如頁面檢視和造訪量度。
   * 自訂收入量度。
   * 保留收入量度。
* 在中建立的區段 [!DNL Analytics] 並發佈至Experience Cloud。

   您可以使用 [!DNL Analytics] 中第一方網站重新定位的區段 [!DNL DSP] 付費搜索廣告。

   ([!DNL Search] 僅限)廣告商 [!DNL Analytics] 但不能Audience Manager也能建立Google網站標籤型對象（再行銷清單）和客戶比對對象（客戶清單），從 [!DNL Analytics] 共用給Experience Cloud的區段。

### 網站轉換量度作為競標訊號

您可以使用標準事件和自訂事件，來自 [!DNL Analytics] 在Adobe廣告中建立加權目標。 目標為您的競標決策提供資訊 [!DNL DSP] 套件和搜尋產品組合。

>[!NOTE]
>
> 您無法映射 [!DNL Analytics] Adobe廣告。

您的Adobe廣告團隊將協助您識別並對應適用於付費媒體績效的事件至Adobe廣告，這些事件將出現在 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

請參閱「[Adobe廣告中的Analytics量度](analytics-data-in-advertising.md)」，取得可用量度的清單。

### 網站重新定位的Analytics區段

Adobe廣告可擷取 [!DNL Analytics] 區段，以用於再行銷目的，以及 [!DNL Search] 廣告，使用的Experience Cloud對象整合 [!DNL Analytics] 和Experience Cloud。

若要存取 [!DNL Analytics] 區段，廣告商帳戶需要 [Experience CloudID服務](https://experienceleague.adobe.com/docs/id-service/using/home.html) 已啟用。 啟用ID服務時，所有Experience Cloud區段(包括 [!DNL Analytics] 發佈至Experience Cloud、在Adobe Audience Manager中建立的區段、在Experience Cloud中建立的區段，使用 [!DNL People core service]，以及在Adobe Experience Platform中建立並透過Audience Manager傳送至「Adobe廣告」的區段)，一經處理，即可在「Adobe廣告」中使用。

[!DNL Analytics] 區段會在24小時內提供，且會每天更新。

如需「Experience Cloud對象」服務的詳細資訊，請參閱 [Experience Cloud對象](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## 如何使用整合的範例

### 在Analysis Workspace中使用Adobe廣告資料

若要了解如何使用Adobe廣告資料在Analysis Workspace中建立視覺化報表，請參閱影片「[工作區和報表簡介](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### 建立AdobeAdvertising控制面板

若要了解如何根據您在Analysis Workspace中的目標追蹤Adobe廣告資料，請參閱影片「[使用Adobe Analytics建立AdobeAdvertising控制面板](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### 使用Adobe廣告ID進行網站項目分析

若要了解如何建立Adobe廣告網站項目報表，以監控一週中的某天、一天中的某天、瀏覽器以及地理位置的影響，請參閱影片「[建立Adobe廣告網站項目報表](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [影片：簡介 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [實作的必要條件和重要資訊 [!DNL Analytics for Advertising]](prerequisites.md)
>* [AdobeAnalytics使用的Advertising ID](ids.md)
>* [Analytics for Advertising的JavaScript程式碼](/help/integrations/analytics/javascript.md)
>* [之間的預期資料差異 [!DNL Analytics] 和Adobe廣告](data-variances.md)
>* [AdobeAnalysis Workspace中的Advertising量度](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe廣告中的資料](/help/integrations/analytics/analytics-data-in-advertising.md)

