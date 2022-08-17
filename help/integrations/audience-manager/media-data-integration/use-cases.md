---
title: 使用案例
description: 瞭解用於與Advertising Cloud DSP共用媒體資料的使用案例和Audience Manager
feature: Integration with Adobe Audience Manager
source-git-commit: 3980af19efa785c437cacbf479ca3eabbed73b1b
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 0%

---

# 在Adobe Audience Manager捕獲媒體曝光資料的使用案例

*僅包含Advertising Cloud DSP的廣告商*

*只有Advertising Cloud-Adobe Audience Manager整合的廣告商*

以下是捕獲Advertising Cloud DSP媒體曝光資料的一些方法 <!-- ad impression data? --> Audience Manager。

## 頻率和頻率管理

在Audience Manager中捕獲印象資料使您能夠通過建立已接觸特定廣告或市場活動的用戶段來增強頻率管理。 如果要增加頻率，可以將這些段用於廣告目標；如果要限制頻率，則可以使用廣告抑制。

另外，還有Audience Manager [!DNL Segment Builder]，您可以 [頻率和頻率控制](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) 任意 [基於規則的特徵](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) 包含可操作信號。 例如，這允許您限制用戶在媒體活動中顯示特定創意的次數。 已讀取「[即時跨設備抑制](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)學習如何做到。<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## 順序消息

通過捕獲印象資料，您可以建立一個用戶段，這些用戶已經接觸市場活動或廣告，並使用此段進行連續消息傳遞或抑制。 例如，您可以重新瞄準那些看到創意的用戶 `123` 但是沒有通過顯示其創造性來按一下或轉換 `456`。

要在Audience Manager中執行此示例，請執行以下步驟：<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. 建立一個特徵，以捕捉看到創意的用戶。

   例如，要命名特徵 `Creative Trait 123`，使用以下特性規則：

   `d_creative == 123 AND d_event == imp`

1. 建立特徵以捕獲按一下或轉換的用戶。

   例如，要命名此特性 `Click and Converter`，使用以下特性規則：

   `d_event == click OR d_event=conv`

1. 建立名為 `Retarget Users` 來填充那些 `123` 但未按一下或轉換。 使用以下特性規則：

   `Creative Trait 123 AND NOT Click and Converter`

1. 映射段 `Retarget Users` 到目標，目標用戶具有創造性 `456`。

## [!DNL Adobe Audience Analytics] 和市場活動暴露資料

在Audience Manager中提供活動印象和點擊資料後，您就可以建立接觸特定活動或策略或與之互動的用戶的特徵和部分。 與 [[!DNL Audience Analytics] 整合](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)，您的Audience Manager段可以與 [!DNL Analytics] 供進一步分析。 潛在使用案例包括：

* **廣告與Advertising Cloud SearchDSP廣告的互動分析：** 標準 [[!DNL Analytics for Advertising Cloud] 整合](/help/integrations/analytics/overview.md) 不提供與之間交互DSP的 [!DNL Search] 因為兩個通道都使用遵循AMO ID屬性規則的AMO ID，而搜索按一下將覆蓋顯示視圖。 通過在Audience ManagerDSP中建立曝光段，您可以使用 [!DNL Audience Analytics] 分析與之DSP間 [!DNL Search] 廣告 [!DNL Analytics]。

* **頻率分析：** 您可以根據用戶接觸特定廣告或市場活動的次數在Audience Manager中建立段。 然後，您可以分析分析中的不同暴露段，以查看用戶行為如何根據暴露數DSP量而改變。

## [!DNL Audience Optimization Reports]

你可以利用 [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) 確定市場活動中各細分市場的潛在表現機會。 這些報告將市場活動印象、按一下和轉換資料與段度量結合起來，以支援以段為中心的優化和有效的渠道組合。

### 相關Audience Optimization報表的類型

| 報告 | 說明 |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] 報告](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | 按印數和轉換率比較映射和未映射段。 |
| [[!UICONTROL Trend Analysis and Volume Analysis] 報告：9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | 返回有關廣告維度的印象、點擊率和轉換的資料。 |
| [[!UICONTROL Optimal Frequency] 報告](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | 幫助您發現服務印象數和轉換之間的最佳平衡。 它允許您調整要顯示的印數，然後開始看到遞減的回報。 |
| [[!UICONTROL Unique User Reach] 報告](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | 氣泡圖，其中每個氣泡的大小與所選維的唯一用戶數成正比。 |

### 注意事項

* 如果 [!DNL Audience Optimization Reports] 用戶具有基於角色的訪問控制(RBAC), [!DNL Adobe Customer Care] 必須配置廣告商ID與組織Audience Manager資料源整合代碼之間的映射。 然後，管理員用戶可以向不同用戶提供RBAC權限。

* 轉換報告 [!DNL Audience Optimization Reports] 需要最終用戶進行一些設定。 用戶必須填充元資料檔案。

* [!DNL Audience Optimization Reports] 不支援對市場活動元資料（如市場活動名稱或職位名稱）所做的更改。

* 搜索廣告的點擊量包含在 [!DNL Audience Optimization Reports] 只有與印象相關。 換句話說，搜索點擊被視為根據印象進行的轉換。 因此，許多搜索點擊可能不包括在 [!DNL Audience Optimization Reports]。

>[!MORELIKETHIS]
>
>* [向Adobe Audience Manager發送DSP媒體曝光資料概述](overview.md)
>* [收集Advertising Cloud DSP市場活動的點擊和印象資料](collect.md)

