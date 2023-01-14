---
title: '''[!DNL Adobe] [!DNL Audience Analytics] Adobe廣告客戶'
description: 了解如何使用 [!DNL Adobe] [!DNL Audience Analytics] 用於advertising的使用案例
feature: Integration with Adobe Audience Manager
exl-id: e05ba560-d3d5-4024-b1ba-956e878a2578
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] Adobe廣告客戶

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) 是Adobe Audience Manager與Adobe Analytics的整合，可讓Audience Manager客戶將區段傳送至 [!DNL Analytics] 以擴充網站活動的深入分析。

Adobe廣告客戶可透過以下方式獲益： [!DNL Audience Analytics]. 整合可讓您：

* 將Adobe廣告曝光資料直接傳送至 [!DNL Analytics] 以判斷上漏斗活動對下游網站活動的影響。

* 從漏斗上方曝光廣告中決定行銷管道和網站入口點。

* 將整合分層為 [!DNL Analytics for Advertising] 若要合併第三方人口統計區段，請從 [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) with [!DNL Analytics for Advertising] 資料，以取得使用者設定檔的更多深入分析。

   [!DNL Audience Marketplace] 透過「啟用」訂閱模型提供對協力廠商資料饋送的存取，讓購買者可將資料傳送至目的地。 若在 [!DNL Analytics] 目的地後，即不會收取啟動費。

* (具有Advertising DSP的廣告商)新增其他曝光區段，以獲得全方位的歷程管理分析。

   Advertising DSP可透過實作Adobe Experience Platform或Audience Manager曝光追蹤像素，將曝光資料傳送至Audience Manager，作為可操作的訊號。 將相同的資料轉送至 [!DNL Analytics] 啟用進階資料分析。 請參閱「[AdobeAdvertising Media資料與Adobe Audience Manager整合概述](/help/integrations/audience-manager/media-data-integration/overview.md)」以取得詳細資訊。

如需 [!DNL Audience Analytics]，包括其先決條件和工作流程，請參閱「[Audience Analytics概述](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## 使用方法範例 [!DNL Audience Analytics] 資料與Adobe廣告資料

以下範例說明如何在中使用合併的資料 [!DNL Analytics] [!DNL Analysis Workspace].

### 請參閱上漏斗活動對下游活動的影響

使用Audience Manager曝光區段來查看上漏斗網站活動對下游網站活動的影響。 在追蹤像素中加入Adobe廣告或第三方巨集ID，以追蹤對詳細層級（從促銷活動層級到使用者公開的網站層級）的影響。

主要優點：

* 依漏斗/廣告類型追蹤曝光次數和使用 [!DNL Audience Analytics] 以決定登入率，並與客戶歷程的下一階段重疊。

* 判斷上漏斗活動對下游網站活動的影響。

* Connect [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> 和 [!DNL Audience Analytics] 資料 <!-- (which includes the user's last exposure event) --> 以決定整個網站歷程。

以下是您可在中建立的報表範例 [!DNL Analysis Workspace].

![請參閱上漏斗活動對下游網站活動的影響](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### 使用 [!DNL Audience Analytics] 使用者設定檔分析的第三方區段資料

使用協力廠商Audience Manager區段，更詳細地分析使用者與您網站的互動方式。 您可以根據來自第三方區段的設定檔如何與媒體行銷活動網站的關鍵績效指標互動，使用資訊來判斷要啟用媒體的新第三方對象。

>[!TIP]
> 使用Audience Manager `Audiences ID` 和 `Audiences Name` 維度 [!DNL Analytics]，如同 [!DNL Analytics] 收集。

以下是您可在中建立的報表範例 [!DNL Analysis Workspace].

![使用協力廠商區段，以豐富使用者設定檔分析](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Adobe廣告整合Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

