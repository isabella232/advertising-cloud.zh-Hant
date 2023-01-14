---
title: 跨裝置解決方案
description: 進一步了解跨裝置功能。
feature: DSP Introduction
exl-id: 29f8ec41-35a6-4a29-a638-82a2929a8fe6
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 0%

---

# 跨裝置解決方案

Advertising DSP與 [!DNL LiveRamp] 可讓您將對象延伸至人員的所有已知裝置，而不只是您的品牌已追蹤的裝置。 整合也提供跨所有裝置的頻率限定和歸因測量。

使用支援的以人物為基礎的裝置圖表時，您可以：

* 比對跨管道和裝置的受眾，以將廣告傳送給人員和家庭，而非裝置。
* 了解並限定個人間的頻率，以平衡和曝光。
* 公開與轉換跨管道或裝置受眾的測試策略。

## 優點 [!DNL LiveRamp] 裝置圖表

* 提供確定性資料池，包括離線客戶資料

* 提供Cookie ID與行動裝置ID之間的平均涵蓋範圍

* 包括主要來自美國的資料

* 頻率限定和歸因測量可免費使用

* 延伸曝光數(僅透過使用 [!DNL LiveRamp] 裝置圖表，而非在目標受眾區段內找到的裝置上)

   該費率會反映在您的帳戶費率卡上。

## 以人物為基礎的頻率管理

以人物為基礎的頻率管理可讓您指定人員層級的頻率上限，而非裝置層級，以真正控制媒體曝光。

### 啟用以人物為基礎的頻率管理

* **促銷活動：** 當您建立新促銷活動時，可以指定 [!UICONTROL Cross-Device Level] 設定。 啟用「[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People]，並選取裝置圖表。 指定的裝置圖表可用於位置層級的跨裝置鎖定目標，以及行銷活動、封裝和位置層級的以人物為基礎的頻率管理。 頻率上限適用於人員的所有已知裝置。

如需詳細資訊，請參閱 [促銷活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md).

儲存促銷活動後，便無法變更其 [!UICONTROL Cross Device Level] 設定。

* **套件：**  您可以選擇在封裝層級設定其他頻率上限。 DSP將遵循促銷活動階層中最嚴格的頻率上限。

* **版位：** 您可以選擇在放置層級設定其他頻率上限。 DSP將遵循促銷活動階層中最嚴格的頻率上限。

## 以人物為基礎的定位

以人物為基礎的鎖定目標可讓您在案頭和行動裝置間尋找客戶。

### 啟用以人物為基礎的鎖定目標

* **促銷活動：** 當您建立新促銷活動時，可以指定 [!UICONTROL Cross-Device Level] 設定。 啟用「[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People]，並選取裝置圖表。 指定的裝置圖表可用於位置層級的跨裝置鎖定目標，以及以人物為基礎的頻率管理。

如需詳細資訊，請參閱 [促銷活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **版位：** 使用指定的裝置圖表為行銷活動中的版位選取對象目標時， [!UICONTROL Cross-Device Targeting] 選項可讓您將目標延伸到所有人員的已知裝置（根據促銷活動設定中指定的裝置圖表），甚至不在指定區段的裝置。

### 設定以人物為基礎的定位報表

您可以在自訂報表中加入下列量度：

* **延伸曝光次數：** (在 [!UICONTROL Build Your Report] 一節 [!UICONTROL Metrics] > [!UICONTROL Std. Metrics])運用裝置圖表所傳遞的增量曝光次數量（在原始受眾區段內找不到）。 此量度也用於計算與使用協力廠商裝置圖表相關的適用費用。

   若要判斷某時段內延伸曝光次數的成本，請執行包含 [!UICONTROL Extended Impressions] 欄，然後將擴展曝光總數乘以0.00035美元(0.35/1000曝光數)。

   總成本亦包括於 [!UICONTROL Billable Other Net Spend] 欄（在下） [!UICONTROL Metrics] > [!UICONTROL Spend])，但該量度也包含您可能新增的其他促銷活動費用。

* **裝置圖表：** (在 [!UICONTROL Build Your Report] 一節 [!UICONTROL Dimensions] > [!UICONTROL Campaign])特定促銷活動、套件或位置的所選裝置圖表。

## 以人物為基礎的歸因測量

*僅追蹤Adobe廣告轉換的廣告商*

透過以人物為基礎的歸因，您可以歸因發生在媒體曝光所在裝置以外的不同裝置上的轉換。 您可在各DSP中使用以人物為基礎的歸因測量， [!DNL Adobe Advertising Creative]，和 [!DNL Adobe Advertising Search] 若廣告商已在其網站上實作「Adobe廣告轉換像素」。

### 啟用以人物為基礎的歸因測量

如果您想要啟用跨裝置歸因測量，請連絡您的 [!DNL Adobe] 客戶團隊。

### 設定跨裝置轉換歸因的轉換報表

#### 轉換報表設定

裝置圖表啟用歸因測量時， [!UICONTROL Conversion] 報表包括 [!UICONTROL Cross-Device Breakout] 設定，可讓您為每個轉換量度包含最多三個不同的欄，包括：

* &lt;*轉換*>[!UICONTROL (tp)]:包括總轉換次數（總人數），其中包括相同裝置轉換次數和跨裝置轉換次數（若適用）。 在報告中，「[!UICONTROL (tp)]「 」會附加至轉換路徑中的轉換量度名稱、規則類型和轉換類型(例如「回應(le)(tl)(tp)」)。

* &lt;*轉換*>[!UICONTROL (sd)]:（選用）僅包含轉換路徑中僅追蹤單一裝置的轉換。 在報告中，「[!UICONTROL (sd)]「 」會附加至轉換路徑中的轉換量度名稱、規則類型和轉換類型(例如「回應(le)(tl)(sd)」)。

* &lt;*轉換*>[!UICONTROL (xd)]:（選用）僅包含在轉換路徑中追蹤超過一個裝置的轉換。 在報告中，「[!UICONTROL (xd)]「 」會附加至轉換路徑中的轉換量度名稱、規則類型和轉換類型(例如「回應(le)(tl)(xd)」)。

#### 如何解譯轉換報表

如果您排序的是跨裝置轉換總數的百分比([!UICONTROL (xd)]/[!UICONTROL (tl)])從高到低，您將了解推動高於平均水準的跨裝置轉換的因素。 您可以利用此資訊來通知您的創意或目標策略，以符合訊息和管道投資與使用者行為。

* 套件 — 查看哪些套件促成最多的總轉換，以及哪些套件具有高百分比的跨裝置轉換。 這可協助您了解要聚焦於何處。

* 版位 — 比較版位效能和歸因（例如，行動網路廣告可能會在案頭推動轉換）。 若沒有用于歸因的裝置圖表，您可能會遺漏行動版網站版位對案頭轉換的影響，或是如果大部分的使用者在案頭轉換，而非行動版網路，則可能會隱藏。

* 廣告 — 探索哪些廣告能促進更高的轉換，並量化其價值及在網頁瀏覽器和行動應用程式環境中的影響。

* 網站 — 跨網站最佳化，而非手動完全排除網站。 如果網站推動跨裝置轉換，您便可查看此行為發生的裝置。

* 交易 — 驗證哪些庫存交易可提供跨裝置轉換，然後決定是否應將目標擴展至這些交易中包含更多裝置和管道，借此改善手動最佳化。

>[!MORELIKETHIS]
>
>* [報表設定](/help/dsp/reports/report-settings.md)
>* [促銷活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [套件設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [版位設定](/help/dsp/campaign-management/placements/placement-settings.md)

