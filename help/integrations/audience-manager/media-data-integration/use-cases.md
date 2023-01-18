---
title: 使用案例
description: 了解與Audience Manager共用Advertising DSP媒體資料的使用案例
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# 在Adobe Audience Manager中擷取媒體曝光資料的使用案例

*僅具有Advertising DSP的廣告商*

*廣告商與Adobe廣告 — 僅Adobe Audience Manager整合*

以下是擷取Advertising DSP媒體曝光資料可讓您受益的一些方式 <!-- ad impression data? --> Audience Manager。

## 使用間隔和頻率管理

在Audience Manager中擷取曝光資料可讓您建立已接觸特定廣告或行銷活動之使用者的區段，以增強頻率管理。 如果您想要增加頻率，可將這些區段用於廣告鎖定目標，或如果想限制頻率，則可用於廣告隱藏。

此外，使用Audience Manager [!DNL Segment Builder]，您可以 [時近和頻率控制](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) 任意 [規則型特徵](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) 包含可操作的訊號。 例如，這可讓您限制媒體促銷活動中特定創意內容的使用者顯示次數。 讀取「[即時跨裝置隱藏功能](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)」以了解如何執行此操作。<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## 循序訊息

透過擷取曝光資料，您可以建立已公開至促銷活動或廣告的使用者區段，並使用此區段進行循序訊息傳送或隱藏。 例如，您可以重新鎖定看到創意內容的使用者 `123` 但並未透過展示創意內容來點擊或轉換 `456`.

若要在Audience Manager中執行此範例，請遵循下列步驟：<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. 建立特徵以擷取看到創意內容的使用者。

   例如，若要為特徵命名 `Creative Trait 123`，請使用下列特徵規則：

   `d_creative == 123 AND d_event == imp`

1. 建立特徵以擷取點按或轉換的使用者。

   例如，若要為此特徵命名 `Click and Converter`，請使用下列特徵規則：

   `d_event == click OR d_event=conv`

1. 建立區段，稱為 `Retarget Users` 填入看到創意內容的使用者 `123` 但未點按或轉換。 使用下列特徵規則：

   `Creative Trait 123 AND NOT Click and Converter`

1. 對應區段 `Retarget Users` 到目的地，並透過創意內容鎖定目的地中的使用者 `456`.

## [!DNL Adobe Audience Analytics] 和促銷活動曝光資料

一旦促銷活動曝光次數和點按資料可在Audience Manager內取得，您就可以建立向特定促銷活動或策略公開或互動之使用者的特徵和區段。 使用 [[!DNL Audience Analytics] 整合](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)，您的Audience Manager區段可與 [!DNL Analytics] 供進一步分析。 潛在使用案例包括：

* **DSP與 [!DNL Adobe Advertising Search] 廣告：** 標準 [[!DNL Analytics for Advertising] 整合](/help/integrations/analytics/overview.md) 不提供DSP與[!DNL之間互動的分析 [!DNL Search]]因為這兩個管道都使用遵循AMO ID歸因規則的AMO ID，而搜尋點選會覆寫顯示檢視。 在Audience Manager中建立DSP曝光區段後，您可以使用 [!DNL Audience Analytics] 分析DSP與[!DNL之間的互動 [!DNL Search]]廣告 [!DNL Analytics].

* **頻率分析：** 您可以根據使用者接觸到特定廣告或促銷活動的次數，在Audience Manager中建立區段。 接著，您可以分析Analytics中不同的曝光區段，以了解使用者行為隨DSP曝光數量而改變的情形。

## [!DNL Audience Optimization Reports]

您可以善用 [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) 識別促銷活動中區段的潛在績效機會。 這些報表將促銷活動曝光數、點按次數及轉換資料與區段量度結合，以提供以區段為中心的最佳化及有效的管道組合。

### 相關Audience Optimization報表的類型

| 報表 | 說明 |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] 報表](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | 依曝光次數和轉換率比較已對應和未對應的區段。 |
| [[!UICONTROL Trend Analysis and Volume Analysis] 報告]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | 傳回廣告維度範圍廣泛之曝光數、點進率和轉換的相關資料。 |
| [[!UICONTROL Optimal Frequency] 報表](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | 可協助您在提供的曝光次數與轉換次數之間找到最佳平衡。 它可讓您調整要顯示的曝光次數，再開始看到遞減的回報。 |
| [[!UICONTROL Unique User Reach] 報表](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | 泡泡圖，其中每個泡泡的大小與所選維度的不重複使用者人數成正比。 |

### 考量事項

* 若 [!DNL Audience Optimization Reports] 使用者擁有角色型存取控制(RBAC)，然後 [!DNL Adobe Customer Care] 必須設定廣告商ID與組織的Audience Manager資料來源整合程式碼之間的對應。 然後，管理員用戶就可以向不同的用戶提供RBAC權限。

* 中的轉換報告 [!DNL Audience Optimization Reports] 一般使用者需要進行一些設定。 使用者必須填入中繼資料檔案。

* [!DNL Audience Optimization Reports] 不支援對促銷活動中繼資料進行變更（例如促銷活動名稱或版位名稱）。

* 搜尋廣告的點按次數包含在 [!DNL Audience Optimization Reports] 只有在與曝光次數相關時才可以。 換言之，搜尋點按在曝光後會視為轉換。 因此，許多搜尋點按可能不會包含在 [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [傳送DSP媒體曝光資料至Adobe Audience Manager概述](overview.md)
>* [從Advertising DSP促銷活動收集點按和曝光資料](collect.md)

