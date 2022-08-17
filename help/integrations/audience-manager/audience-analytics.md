---
title: '"[!DNL Adobe][!DNL Audience Analytics] Advertising Cloud客戶」'
description: 瞭解如何使用 [!DNL Adobe][!DNL Audience Analytics] 用於廣告使用案例
feature: Integration with Adobe Audience Manager
source-git-commit: d83e36847d0e14bc7e83106c0a221680060c2e58
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# [!DNL Adobe][!DNL Adobe] Advertising Cloud客戶

[[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) 是Adobe Audience Manager和Adobe Analytics的整合，允許Audience Manager客戶將資料段發送到 [!DNL Analytics] 以豐富有關站點活動的資訊。

Advertising Cloud客戶可通過 [!DNL Audience Analytics]。 整合允許您：

* 將Advertising Cloud暴露資料直接發送到 [!DNL Analytics] 確定上漏斗活動對下游站點活動的影響。

* 從上漏斗廣告中確定營銷渠道和站點入口點。

* 將整合與 [!DNL Analytics for Advertising Cloud] 將第三方人口部門 [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) 與 [!DNL Analytics for Advertising Cloud] 資料，以瞭解有關用戶配置檔案的更多見解。

   [!DNL Audience Marketplace] 通過「激活」訂閱模式提供對第三方資料源的訪問，該模式允許購買者將資料發送到目標。 如果資料在 [!DNL Analytics] 則不收取激活費。

* (Advertising Cloud DSP廣告商)添加更多曝光片段，以便獲得全面的旅程管理洞察力。

   Advertising Cloud DSP可以通過實施Adobe Experience Platform或Audience Manager印象跟蹤像素，將曝光資料作為可操作信號發送給Audience Manager。 將相同的資料轉發到 [!DNL Analytics] 啟用高級資料分析。 請參閱「」[Advertising Cloud與Adobe Audience Manager媒體資料整合概述](/help/integrations/audience-manager/media-data-integration/overview.md)的雙曲餘切值。

有關 [!DNL Audience Analytics]，包括其先決條件和工作流，請參見「[Audience Analytics概述](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)&quot;

## 如何使用示例 [!DNL Audience Analytics] 資料與Advertising Cloud資料

以下是如何在 [!DNL Analytics] [!DNL Analysis Workspace]。

### 請參閱上漏斗活動對下游活動的影響

使用Audience Manager暴露段查看上漏斗狀站點活動對下游站點活動的影響。 在跟蹤像素中包括Advertising Cloud或第三方宏ID，以跟蹤對詳細級別（從市場活動級別到用戶暴露的站點級別）的影響。

主要好處：

* 按漏斗/廣告類型跟蹤曝光和使用 [!DNL Audience Analytics] 確定入口率，並與客戶旅程的下一階段重疊。

* 確定上漏斗活動對下游站點活動的影響。

* 連接 [!DNL Analytics for Advertising Cloud]<!-- which doesn't include the last exposure event --> 和 [!DNL Audience Analytics] 資料 <!-- (which includes the user's last exposure event) --> 確定一個整體的到達現場的旅程。

以下是可在中建立的報告示例 [!DNL Analysis Workspace]。

![請參閱上漏斗活動對下游站點活動的影響](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### 使用 [!DNL Audience Analytics] 用於用戶配置檔案分析的第三方段資料

使用第三方Audience Manager段更詳細地分析用戶與站點的交互方式。 您可以根據來自第三方部門的配置檔案與媒體活動站點的關鍵績效指標的聯繫方式，使用這些資訊來確定要激活媒體的新的第三方受眾。

>[!TIP]
> 使用Audience Manager `Audiences ID` 和 `Audiences Name` 維 [!DNL Analytics]像其他任何維 [!DNL Analytics] 收集。

以下是可在中建立的報告示例 [!DNL Analysis Workspace]。

![使用第三方段豐富用戶配置檔案分析](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Advertising Cloud與Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

