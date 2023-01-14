---
title: '"[!DNL Analytics] Adobe廣告中的資料」'
description: '"[!DNL Analytics] Adobe廣告中的資料」'
feature: Integration with Adobe Analytics
exl-id: 79fbc809-9965-41c1-971f-3652cc78fee3
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# [!DNL Analytics] Adobe廣告中的資料

*廣告商與Adobe廣告 — 僅Adobe Analytics整合*

## Analytics區段

在中建立的所有區段 [!DNL Analytics] 並發佈至Experience Cloud。

新區段需要24到48小時才會出現在Adobe廣告中。 現有區段的更新會在約8小時內同步。

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## 網站參與量度

>[!NOTE]
>
>* [!DNL Analytics] 將EF IDeVar的事件傳遞至Adobe廣告。  預設整合不支援將計算量度或其他維度(eVar)傳送至Adobe廣告。 不過，如果計算量度可在自訂事件中完全擷取，則Adobe廣告可以內嵌自訂事件。
>* [!DNL Analytics] 每小時將資料傳遞至Adobe廣告。


* [!UICONTROL Timespent_secs_1stvisit]:訪客首次造訪期間在網站上逗留的秒數。
* [!UICONTROL Timespent_secs_total]:點擊回顧期間內所有造訪在網站上逗留的總秒數。
* [!UICONTROL Pageviews_1stvisit]:訪客首次造訪期間網站的頁面檢視次數。
* [!UICONTROL Pageviews_total]:點擊回顧期間內，網站上所有造訪的頁面檢視總數。
* [[!UICONTROL Bounces] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]:次數 [!DNL Analytics] 收集 [!UICONTROL EF ID].

## 轉換量度

[!DNL Analytics] 每日傳遞轉換量度至Adobe廣告。

### 標準轉換量度

* [[!UICONTROL Revenue] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] 量度](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### 自訂轉換量度

這些量度是報表套裝專用的，因此每個客戶和報表套裝的可用量度會有所不同。

### 保留轉換量度

這些量度是報表套裝專用的，因此每個客戶和報表套裝的可用量度會有所不同。

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising]](overview.md)
>* [AdobeAnalysis Workspace中的Advertising量度](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)

