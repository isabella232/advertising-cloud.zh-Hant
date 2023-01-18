---
title: Adobe廣告整合Adobe Audience Manager
description: 了解Adobe廣告與Adobe Audience Manager交換資料的不同方式。
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Adobe廣告整合Adobe Audience Manager

您可以透過下列方式整合Adobe廣告與Audience Manager。

## 同步Audience Manager和其他 [!DNL Adobe] 廣告鎖定目標的區段

[!DNL Search] 和DSP可提取廣告商或代理商的所有Audience Manager和其他內容的中繼資料、階層資料和不重複對象資料 [!DNL Adobe] 對象。 此獨特連線僅適用於使用Adobe廣告的行銷人員。 請參閱「[匯入Adobe Audience Manager區段以用於廣告鎖定目標](/help/integrations/audience-manager/import-audiences.md).&quot;

### 使用Audience Manager和其他 [!DNL Adobe] 要建立的區段 [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*選擇加入的廣告商 [!DNL Advertising Search] 僅限*

在[!DNL內 [!DNL Search]]您可以建立 [!DNL Google Ads] GoogleAudience Manager會使用您現有的客戶區段來比對來自使用者ID的受眾，這些區段具有 [!UICONTROL Adobe Media Optimizer (HTTP)] 和 [!UICONTROL Adobe Media Optimizer Batch Destination] 作為目的地。 ([!DNL Media Optimizer] 是[!DNL的舊名 [!DNL Search]])。 這包括發佈至Adobe Experience Cloud的Adobe Analytics區段，以及在Adobe Experience Cloud中使用 [!DNL People core service]. 如需詳細資訊，請參閱[!DNL中的產品內說明 [!DNL Search]]。

[客戶比對來自使用者ID的受眾](https://support.google.com/google-ads/answer/9199250) 類似網站標籤型受眾，但會將非PII ID指派給不重複受眾成員，以獲得比標準客戶比對和網站標籤型受眾更明顯的優點。

若要建立必要的使用者ID，您必須使用Adobe廣告JavaScript標籤 <!-- with a user ID parameter -->在您的網站上。 聯絡您的[!DNL [!DNL Search]]客戶團隊，以了解詳細資訊。

![區段建立程式](/help/integrations/assets/ad_search_user_id_pic.png)

建立對象後，即可在 [!DNL Google Ads] 行銷活動 [促銷活動層級或廣告群組層級的目標或排除](#audience-manager-targets).

### 使用Audience Manager和其他 [!DNL Adobe] 要定位或排除廣告的區段 {#audience-manager-targets}

* （透過[!DNL加入的廣告商） [!DNL Search]])您可以使用 [!DNL Google Ads] 對象 [使用 [!DNL Adobe] 區段](#audience-manager-google-audiences) 作為促銷活動層級或廣告群組層級的目標或排除 [!DNL Google Ads] 行銷活動。

* (具有DSP的廣告商)您可以使用現有的 [!DNL Adobe] 區段作為廣告版位的目標。 您可以選擇將區段納入可重複使用的對象中，以用作多個版位的目標或排除。

* （廣告商與廣告創意）您可以使用現有的 [!DNL Adobe] 區段作為廣告體驗中特定創意的目標。

>[!NOTE]
>
>如需如何在Audience Manager和Experience Cloud中建立對象的詳細資訊 [!DNL Audience Library] 介面和不同對象類型的常見使用案例，請參閱「[受眾建立選項](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## 傳送DSP媒體曝光資料至Audience Manager

*僅包含DSP的廣告商*

擁有Adobe Audience Manager的DSP客戶可使用像素呼叫來Audience Manager，從廣告促銷活動擷取資料。 然後，您可以使用促銷活動資料來建立規則型特徵，您可以用來定義新區段以啟用各種DSP使用案例，例如更進階的細分、頻率管理、行銷分析和報告深入分析。

請參閱「[傳送DSP媒體曝光資料至Adobe Audience Manager概述](/help/integrations/audience-manager/media-data-integration/overview.md)」以取得詳細資訊。

## 透過Audience Analytics，更深入了解網站活動

Adobe廣告客戶 [[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) 可將Adobe廣告追蹤的資料和Audience Manager區段傳送至 [!DNL Analytics] 以擴充網站活動的深入分析。

如需詳細資訊，請參閱[[!DNL Adobe][!DNL Audience Analytics] Adobe廣告客戶](/help/integrations/audience-manager/audience-analytics.md).&quot;
