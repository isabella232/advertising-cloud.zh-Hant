---
title: AdobeAnalysis Workspace中的Advertising量度
description: AdobeAnalysis Workspace中的Advertising量度
feature: Integration with Adobe Analytics
exl-id: d740bd19-c643-4917-9cfd-f9cf0affd07e
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# AdobeAnalysis Workspace中的Advertising量度

*廣告商與Adobe廣告 — 僅Adobe Analytics整合*

>[!NOTE]
>
>* Adobe廣告會將流量量度和維度傳遞至 [!DNL Analytics] 每日。
>* [!DNL Analytics] 擷取Adobe廣告即時點進和閱覽。


## 來自Adobe廣告的流量量度

>[!NOTE]
>
>中的所有Adobe廣告流量量度 [!DNL Analytics] 從「AMO」開始。

| 流量量度 | 說明 |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Adobe廣告曝光次數。 |
| [!UICONTROL AMO Clicks] | Adobe廣告點按總次數。 |
| [!UICONTROL AMO Cost] | Adobe廣告支出以報表套裝的貨幣計算。 |
| [!UICONTROL AMO ID Instance] | Adobe廣告ID的設定次數。 |
| [!UICONTROL AMO Minutes Viewed] | Adobe廣告影片被檢視的分鐘數。 |
| [!UICONTROL AMO Views] | 廣告上的檢視次數。 觀看者起始Adobe廣告影片時，即會計入檢視。 |
| [!UICONTROL AMO Views 25% Complete] | 至少25%的Adobe廣告影片觀看次數。 |
| [!UICONTROL AMO Views 50% Complete] | 觀看Adobe廣告影片至少50%的檢視次數。 |
| [!UICONTROL AMO Views 75% Complete] | 觀看Adobe廣告影片至少75%的檢視次數。 |
| [!UICONTROL AMO Views 100% Complete] | 觀看100%的Adobe廣告影片的檢視次數。 |
| [!UICONTROL AMO Viewable Impressions] | 根據放置配置可檢視的測量曝光次數。 |
| [!UICONTROL AMO Not Viewable Impressions] | 被判斷為無法檢視的曝光次數。 此值的計算方式為([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable ])。 |
| [!UICONTROL AMO Measurable Impressions] | 已成功初始化可視性檢測的曝光次數。 此值的計算方式為（有工具的曝光次數 — 無法測量的曝光次數）。 |

## 適用於Adobe廣告的實用自訂計算量度

請考慮為您的Adobe廣告資料建立下列量度。

* 點按至登陸頁面例項([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]):這是點按廣告並成功進入登陸頁面的人數百分比。
* 可測量比率([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* 可檢視曝光率([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* 每次檢視成本([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* 每次點按成本([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

## Adobe廣告Dimension

>[!NOTE]
>
>中的所有Adobe廣告維度 [!DNL Analytics] 後面接著「(AMO ID)」。

| Dimension | 適用的Adobe廣告資料 | 說明 |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] 和 [!DNL Search] 資料 | Advertising DSP或搜尋引擎名稱 |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] 和 [!DNL Search] 資料 | 帳戶名稱。 |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] 和 [!DNL Search] 資料 | RTB([!DNL DSP])或廣告網路名稱([!DNL Search]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] 和 [!DNL Search] 資料 | 促銷活動名稱。 |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] 和 [!DNL Search] 資料 | 套件([!DNL DSP])或產品組合([!DNL Search])名稱。 |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] 資料 | 版位名稱。 |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search] 資料 | 廣告群組名稱。 |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search] 資料 | 關鍵字。 |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search] 資料 | 搜尋符合類型。 |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search] 資料 | 關鍵字和符合類型。 |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] 和 [!DNL Search] 資料 | 廣告類型，例如 `text`, `video`, `display`，或 `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] 和 [!DNL Search] 資料 | 廣告類型([!DNL DSP])或廣告標題([!DNL Search])。 |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] 和 [!DNL Search] 資料 | 廣告說明([!DNL DSP])或廣告內文([!DNL Search])。 |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search] 資料 | 廣告中顯示的URL。 |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search] 資料 | 廣告的目標URL。 |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] 和 [!DNL Search] 資料 | 登錄頁面項目是閱覽或點進。 |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search] 資料 | 產品清單廣告的產品目標。 |

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Adobe廣告中的資料](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

