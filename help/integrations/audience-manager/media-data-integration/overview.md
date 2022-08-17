---
title: 向Adobe Audience Manager發送DSP媒體曝光資料概述
description: 瞭解如何使用Audience Manager事件像素捕獲Advertising Cloud DSP市場活動的印象級和點擊級資料
feature: Integration with Adobe Audience Manager
source-git-commit: e861fc53ba14d783c763b291cdc618e5f1d4124f
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# 向Adobe Audience Manager發送DSP媒體曝光資料概述

*僅包含Advertising Cloud DSP的廣告商*

*只有Advertising Cloud-Adobe Audience Manager整合的廣告商*

Advertising Cloud DSPAdobe Audience Manager的客戶可以使用Audience Manager事件像素來捕獲印象級資料和市場活動的點擊級DSP資料。 事件像素將資料作為可操作信號發送到Audience Manager。 這些信號支援DSP各種使用案例，如更高級的細分、頻率管理、市場分析和報告洞察力。

不DSP收你向Audience Manager發送這些信號。 但是，您會根據您的Audience Manager合同根據伺服器呼叫支付標準Audience Manager接收成本。 Audience Manager將刪除以兩種不同方式跟蹤的重複事件，以便每個事件只計費一次。

>[!NOTE]
>
> Audience Manager還支援從ad伺服器日誌檔案捕獲資料，這降低了靈活性。 本文檔不包括該過程。

## 主要優勢

* 市DSP場活動資料即時流入Audience Manager，您可以使用它來構建用於定義段的基於規則的特徵。

* 在用戶特徵和細分資格後，可立即進行細分，從而支援即時定向工作。

* 您可以利用市場活動資料進行以下使用案例：跨創意活動設定頻率上限、針對以前市場活動暴露的用戶以及分析下游站點行為和入口點。

* 聚合資料提供了市場活動績效的統一視圖，有助於確定自定義轉換路徑，並可用於改進通過Audience Manager導致轉換的事件順序 [!DNL Audience Optimization Reports] 或通過 [[!DNL Audience Analytics] 與Adobe Analytics](/help/integrations/audience-manager/audience-analytics.md)。

## 資料跟蹤方式

Audience Manager印象和按一下事件像素是基於cookie的。 這些像素不會捕獲在無cookie環境（如移動應用和連接的電視）中發生的事件。

### 印象跟蹤像素

Audience Manager在將1xl像素透明事件跟蹤像素附加到廣告時跟蹤廣告的印象資料。 每次向用戶提供廣告並由Web瀏覽器載入時，都載入事件像素。 像素從特定於客戶端的子域載入 [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html)，是用於Audience Manager的舊域，包含參數作為鍵值對。 事件調用收集印象和轉換資料並將其發送到Audience Manager資料收集伺服器。

### 按一下跟蹤像素

Audience Manager跟蹤點擊與印象類似，但是每次播放廣告時，它不會載入透明事件像素。 而是在廣告的點擊URL中跟蹤點擊資料。 該廣告指向的客戶端特定子域 [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html)，它是用於Audience Manager的舊域，用於由Audience Manager資料收集伺服器處理。 然後伺服器將用戶重定向到預期的登錄頁。 URL包含參數作為鍵值對。

>[!NOTE]
>
>如果您的組織使用 [!DNL Analytics] 跟蹤，則可能不需要Audience Manager按一下跟蹤。 Adobe Analytics捕獲點擊信號，並將其發送給Audience Manager [伺服器端轉發](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html)。

>[!MORELIKETHIS]
>
>* [收集Advertising Cloud DSP市場活動的點擊和印象資料](collect.md)
>* [使用案例](use-cases.md)

