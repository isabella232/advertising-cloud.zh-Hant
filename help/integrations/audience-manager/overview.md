---
title: Advertising Cloud與Adobe Audience Manager
description: 瞭解Advertising Cloud與Adobe Audience Manager交換資料的不同方式。
feature: Integration with Adobe Audience Manager
source-git-commit: c761c96b32171bcfba12ed4a39235e6e8b6f6d34
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Advertising Cloud與Adobe Audience Manager

您可以通過以下方式將Advertising Cloud與Audience Manager相融合。

## 同步Audience Manager和其他 [!DNL Adobe] 廣告目標的段

Advertising Cloud Search和Advertising Cloud DSP可以為廣告商或代理機構的所有Audience Manager和其他收集元資料、層次資料和唯一的受眾資料 [!DNL Adobe] 觀眾。 這種獨特的連接僅供使用Advertising Cloud的營銷人員使用。 請參閱「」[導入Adobe Audience Manager段以進行廣告定位](/help/integrations/audience-manager/import-audiences.md)&quot;

### 使用Audience Manager和其他 [!DNL Adobe] 要建立的段 [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*具有 [!DNL Advertising Cloud Search] 僅*

在 [!DNL Search]，您可以建立 [!DNL Google Ads] Google客戶使用現有Audience Manager段匹配用戶ID的受眾 [!UICONTROL Adobe Media Optimizer (HTTP)] 和 [!UICONTROL Adobe Media Optimizer Batch Destination] 作為目的地。 ([!DNL Media Optimizer] 是Advertising Cloud Search的原名。) 這包括發佈給Adobe Experience Cloud的Adobe Analytics分部，以及使用 [!DNL People core service]。 有關詳細資訊，請參閱 [!DNL Search]。

[客戶與用戶ID的受眾匹配](https://support.google.com/google-ads/answer/9199250) 像基於網站標籤的受眾一樣工作，但會將非PII ID分配給唯一的受眾成員，以獲得比標準客戶匹配和基於網站標籤的受眾更明顯的好處。

要建立必要的用戶ID，必須使用Advertising CloudJavaScript標籤 <!-- with a user ID parameter -->在你的網站上。 請聯繫您的Advertising Cloud Search客戶團隊以瞭解更多資訊。

![段建立過程](/help/integrations/assets/ad_search_user_id_pic.png)

建立受眾後，您可以在 [!DNL Google Ads] 活動 [市場活動級或廣告組級目標或排除](#audience-manager-targets)。

### 使用Audience Manager和其他 [!DNL Adobe] 目標或排除廣告的段 {#audience-manager-targets}

* (具有 [!DNL Search])可以使用 [!DNL Google Ads] 觀眾 [建立時 [!DNL Adobe] 段](#audience-manager-google-audiences) 作為市場活動級別或廣告組級別目標或排除項 [!DNL Google Ads] 活動。

* (Advertising Cloud DSP的廣告商)您可以使用現有 [!DNL Adobe] 作為廣告投放的目標。 您可以選擇將段包括在可重複使用的受眾中，您可以將這些段用作多個放置的目標或排除。

* (Advertising Cloud Creative的廣告商)您可以使用現有 [!DNL Adobe] 作為廣告體驗中特定創意的目標。

>[!NOTE]
>
>有關如何在Audience Manager和Experience Cloud中建立受眾的詳細資訊 [!DNL Audience Library] 介面和不同受眾類型的常用用例，請參見「[受眾建立選項](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html)&quot;

## 將介DSP質暴露資料發送到Audience Manager

*僅包DSP含*

Advertising Cloud DSPAdobe Audience Manager客戶可以通過對Audience Manager的像素呼叫從廣告活動中獲取資料。 然後，您可以使用市場活動資料構建基於規則的特性，您可以使用這些特性定義新的細分段，以啟用各種使用案例DSP，如更高級的細分、頻率管理、市場營銷分析和報告洞察力。

請參閱「」[向Adobe Audience Manager發送DSP媒體曝光資料概述](/help/integrations/audience-manager/media-data-integration/overview.md)的雙曲餘切值。

## 通過Audience Analytics更深入地瞭解網站活動

Advertising Cloud客戶 [[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) 可以將Advertising Cloud跟蹤的資料和Audience Manager段發送到 [!DNL Analytics] 以豐富有關站點活動的資訊。

有關詳細資訊，請參閱「」[[!DNL Adobe][!DNL Audience Analytics] Advertising Cloud客戶](/help/integrations/audience-manager/audience-analytics.md)&quot;
