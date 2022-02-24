---
title: '"[!DNL Analytics] Advertising Cloud資料」'
description: '"[!DNL Analytics] Advertising Cloud資料」'
feature: Integration with Adobe Analytics
exl-id: 79fbc809-9965-41c1-971f-3652cc78fee3
source-git-commit: 2c94b6c02b4e24878639dd9edbc0455e1751f679
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# [!DNL Analytics] Advertising Cloud資料

*只有Advertising Cloud-Adobe Analytics整合的廣告商*

## 分析段

建立的所有段 [!DNL Analytics] 出版給Experience Cloud。

新節目在Advertising Cloud需要24-48個小時。 對現有段的更新將在大約八小時內同步。

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## 站點項目指標

>[!NOTE]
>
>* [!DNL Analytics] 將EF IDeVar的事件傳遞到Advertising Cloud。  預設整合不支援將計算的度量或其他維(eVars)發送到Advertising Cloud。 但是，如果計算的度量可以在自定義事件中完全捕獲，則Advertising Cloud可以接收自定義事件。
>* [!DNL Analytics] 每小時向Advertising Cloud傳送資料。


* [!UICONTROL Timespent_secs_1stvisit]:訪問者首次訪問時在站點上花費的秒數。
* [!UICONTROL Timespent_secs_total]:按一下回望窗口內所有訪問站點所花費的總秒數。
* [!UICONTROL Pageviews_1stvisit]:訪問者首次訪問期間站點上的頁面視圖數。
* [!UICONTROL Pageviews_total]:按一下回望窗口內所有訪問站點上的頁面視圖總數。
* [[!UICONTROL Bounces] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]:那次 [!DNL Analytics] 收集 [!UICONTROL EF ID]。

## 轉換度量

[!DNL Analytics] 每天將轉換指標傳遞給Advertising Cloud。

### 標準轉換度量

* [[!UICONTROL Revenue] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] 度量](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### 自定義轉換度量

這些指標是特定於報告套件的，因此每個客戶和報告套件的可用指標各不相同。

### 保留轉換度量

這些指標是特定於報告套件的，因此每個客戶和報告套件的可用指標各不相同。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising CloudAnalysis Workspace度量](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)

