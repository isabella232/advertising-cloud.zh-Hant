---
title: 概述 [!DNL Analytics for Advertising Cloud]
description: 概述 [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---

# 概述 [!DNL Analytics for Advertising Cloud]

*Advertising Cloud DSP和Advertising Cloud Search的廣告商*

[!DNL Analytics for Advertising Cloud] 整合Adobe Analytics和Adobe Advertising Cloud，以擴展和增強每種產品的功能。

這種整合使廣告商能夠跟蹤其中的點擊瀏覽和瀏覽網站交互 [!DNL Analytics] 例如，讓品牌瞭解其廣告支出如何帶來站點參與和關鍵業務目標。

此外，Advertising Cloud還可以訪問大量的第一方資料 [!DNL Analytics] 收集 [!DNL Analytics] 已在站點上標籤。 這允許更強健的行程管理、第一方再營銷和付費媒體站點報告。 Advertising Cloud可以進一步 [!DNL Analytics] 用於支出和投標優化的資料。

當被妥善雇用時， [!DNL Analytics for Advertising Cloud] 模糊兩種傳統角色之間的界限：廣告旅程管理（通過廣告將用戶發送到站點的行為），並通過web分析瞭解該站點參與。

主要好處：

* 發送 [!DNL Analytics] 直接分銷給Advertising Cloud，以進行第一方網站的再營銷。
* 使用 [!DNL Analytics] 將定制和標準事件用作優化付費媒體廣告的轉換信號。
* 利用 [!DNL Analytics] Analysis Workspace將更好地瞭解網站入口點和訪問行為。
* 實現網路分析員與付費媒體團隊之間更緊密的協作。
* 在中使用持久的Advertising Cloud查看和點擊ID [!DNL Analytics] 瞭解現場參與。
* 利用將資料或像素導出到廣告伺服器或其他伺服器時無法實現的自定義指標、自定義尺寸和站點活動，增強Analysis Workspace的傳統付費媒體報DSP告。
* 利用 [!DNL Analytics] 已在您網站上，用於跟蹤和優化Advertising Cloud。

>[!TIP]
>
> 觀看 [視頻簡介 [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics)。

## 使用分析進行付費媒體報告

[!DNL Analytics for Advertising Cloud] 通過允許您：

* 在中使用持久的Advertising Cloud查看和點擊ID [!DNL Analytics] 瞭解現場參與。
* 利用Analysis Workspace，更好地瞭解網站入口點和訪問行為。 您可以訪問付費媒體維和事件資料，包括Advertising Cloud市場活動實體名稱（直至投放和廣告）及其相關指標，如點擊量、印象和成本。

要使用 [!DNL Analytics] 作為付費媒體報告工具，您的組織需要Experience Cloud登錄，並且可以訪問Analysis Workspace。 您的Advertising Cloud團隊將幫助您將Advertising Cloud資料映射到Analysis Workspace的單個報告套件。 您可以將Advertising Cloud資料發送到任何報告套件，但您應該知道已映射到Advertising Cloud的報告套件和尚未映射的報告套件。根據報告套件的不同，這可能會更改報告的資料。

[Advertising CloudID [!DNL Analytics]](ids.md) 與其他eVar類似，具有自定義的持久過期。 預設情況下，在Advertising Cloud實施期間，屬性回望窗口設定為60天。 要更改此設定，請使用 [!DNL Adobe] 客戶團隊。

Advertising Cloud維後面附加尾碼「(AMO ID)」(如「Ad Type(AMO ID)」)。 請參閱「」[Advertising CloudAnalysis Workspace度量](advertising-cloud-metrics-in-analytics.md)&quot;（圖表）。

>[!NOTE]
>
> 查看Advertising Cloud資料（或任何資料集）時 [!DNL Analytics]，請注意，度量和報告基於在 [!DNL Analytics]。 資料可能與您在其他報告系統中看到的不同， [!DNL DSP] 報告或搜索引擎報告。 要瞭解 [!DNL Analytics]您需要知道eVar資料何時過期、什麼定義了訪問、什麼被視為最後一次訪問屬性與總持續屬性，以及其他因素。 有關詳細資訊，請參見 [預期資料差異 [!DNL Analytics] 和Advertising Cloud](data-variances.md)。

## 使用分析為Advertising Cloud活動和Portfolio提供動力

無需任何額外像素， [!DNL Analytics for Advertising Cloud] 通過向Advertising Cloud發送兩個主要信號，實現更好的優化和更方便的觀眾分割：

* 要用作投標信號的轉換度量：
   * 標準度量，如 [!UICONTROL Revenue] 和 [!UICONTROL Cart Views]。
   * 站點項目度量，如頁面視圖和訪問度量。
   * 自定義收入指標。
   * 保留收入指標。
* 建立於 [!DNL Analytics] 出版給Experience Cloud。

   您可以使用 [!DNL Analytics] 第一方站點重新定位的段 [!DNL DSP] 以及付費搜索廣告。

   (僅Advertising Cloud Search)廣告商 [!DNL Analytics] 但是，不能Audience Manager也從中建立基於Google網站標籤的受眾（重新營銷清單）和客戶匹配的受眾（客戶清單） [!DNL Analytics] 與Experience Cloud共用的段。

### 作為投標信號的站點轉換度量

您可以使用標準事件和自定義事件 [!DNL Analytics] 在Advertising Cloud建立加權目標。 目標為您的投標決策提供資訊 [!DNL DSP] 包和搜索包。

>[!NOTE]
>
> 無法從 [!DNL Analytics] 進入Advertising Cloud。

您的Advertising Cloud團隊將幫助您確定適用於付費媒體表現的事件並將其映射到Advertising Cloud，這些事件將出現在 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties]。

請參閱「」[Advertising Cloud分析指標](analytics-data-in-advertising-cloud.md)「 」，以查看可用度量的清單。

### 網站重定目標的分析段

Advertising Cloud可以 [!DNL Analytics] 分類，以作再營銷用途，用於Advertising Cloud DSP [!DNL Search] 使用本地Experience Cloud受眾的廣告 [!DNL Analytics] 和Experience Cloud。

訪問 [!DNL Analytics] 段，廣告商帳戶需要 [Experience CloudID服務](https://experienceleague.adobe.com/docs/id-service/using/home.html) 啟用。 啟用ID服務後，所有Experience Cloud段(包括在 [!DNL Analytics] 發佈至Experience Cloud，在Adobe Audience Manager建立的段，使用Experience Cloud建立的段 [!DNL People core service]以及在Adobe Experience Platform建立並通過Audience Manager發送到Advertising Cloud的片段)，在處理後即可在Advertising Cloud內獲得。

[!DNL Analytics] 24小時內提供，並每日更新。

有關Experience Cloud觀眾服務的詳細資訊，請參見 [Experience Cloud觀眾](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html)。

## 如何使用整合示例

### 在Analysis Workspace使用Advertising Cloud資料

要瞭解如何使用Advertising Cloud資料在Analysis Workspace建立可視報告，請參閱視頻「 」[工作區和報告簡介](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html)&quot;

### 建立Advertising Cloud儀表板

要瞭解如何根據Analysis Workspace的目標跟蹤Advertising Cloud資料，請參閱視頻「 」[使用Advertising Cloud建立Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html)&quot;

### 使用Advertising CloudID進行站點條目分析

要瞭解如何建立Advertising Cloud網站條目報告以監控一週中的一天、一天中的時間、瀏覽器和地理影響，請參閱視頻「 」[建立Advertising Cloud站點條目報告](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html)&quot;

>[!MORELIKETHIS]
>
>* [視頻：簡介 [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [實施的先決條件和關鍵資訊 [!DNL Analytics for Advertising Cloud]](prerequisites.md)
>* [Advertising Cloud分析使用的ID](ids.md)
>* [用於Advertising Cloud分析的JavaScript代碼](/help/integrations/analytics/javascript.md)
>* [預期資料差異 [!DNL Analytics] 和Advertising Cloud](data-variances.md)
>* [Advertising CloudAnalysis Workspace度量](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Advertising Cloud資料](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

