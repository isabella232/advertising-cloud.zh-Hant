---
title: 跨設備解決方案
description: 瞭解有關跨設備功能的詳細資訊。
feature: DSP Introduction
exl-id: 29f8ec41-35a6-4a29-a638-82a2929a8fe6
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '1110'
ht-degree: 0%

---

# 跨設備解決方案

Advertising Cloud DSP整合 [!DNL LiveRamp] 和 [!DNL Adobe Device Co-op] 允許您將受眾擴展到個人的所有已知設備，而不只是您的品牌跟蹤的設備。 該整合還提供跨所有設備的頻率封蓋和屬性測量。

使用支援的基於人員的設備圖時，可以：

* 讓不同渠道和設備的受眾進行匹配，以向個人和家庭而不是設備投放廣告。
* 通過瞭解和限制個人間的頻率來平衡和暴露。
* Test策略，可以在不同頻道或設備間公開與轉換觀眾。

## 每個設備圖的優勢

* [!DNL Adobe Device Co-op]:
   * 提供參與Adobe廣告商的確定性和概率性資料的可選擇加入池
   * 提供由案頭和移動Web訪問者支援的強大Cookie ID連接
   * 包括主要來自美國和加拿大的資料
   * 沒有使用費

* [!DNL LiveRamp] 設備圖形：
   * 提供確定性資料池，包括離線客戶資料
   * 在cookie ID和移動設備ID之間提供均勻的覆蓋
   * 包括主要來自美國的資料
   * 免費進行頻率封頂和屬性測量
   * 價格為0.35美元的CPM，用於擴展印象(僅通過使用 [!DNL LiveRamp] 設備圖，而不是在目標受眾段中找到的設備上)

      費率反映在您的帳戶費率卡上。

## 基於人的頻率管理

基於人員的頻率管理允許您在人員級別指定頻率上限，而不是設備級別，以實現真正的媒體曝光控制。

### 激活基於人員的頻率管理

* **市場活動：** 建立新市場活動時，可以指定 [!UICONTROL Cross-Device Level] 的子菜單。 啟用「」[!UICONTROL Same Device]&quot;-> &quot;[!UICONTROL People]，並選擇一個設備圖形。 指定的設備圖用於在放置級別上的跨設備目標和在活動、包裝和放置級別上基於人的頻率管理。 頻率上限適用於所有已知設備。

有關詳細資訊，請參見 [市場活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)。

保存市場活動後，無法更改其 [!UICONTROL Cross Device Level] 的子菜單。

* **包：**  您可以選擇在包層設定附加頻率上限。 會DSP尊重市場活動等級中最嚴格的頻率限制。

* **放置：** 您可以選擇在放置層設定附加的頻率大寫。 會DSP尊重市場活動等級中最嚴格的頻率限制。

## 基於人的目標

基於人的目標使您能夠在台式機和移動設備上找到客戶。

### 激活基於人員的目標

* **市場活動：** 建立新市場活動時，可以指定 [!UICONTROL Cross-Device Level] 的子菜單。 啟用「」[!UICONTROL Same Device]&quot;-> &quot;[!UICONTROL People]，並選擇一個設備圖形。 指定的設備圖形用於在放置級別上的跨設備目標和基於人的頻率管理。

有關詳細資訊，請參見 [市場活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)。

* **放置：** 當您為市場活動中使用指定設備圖形的位置選擇受眾目標時， [!UICONTROL Cross-Device Targeting] 選項允許您將目標擴展到人員的所有已知設備（根據市場活動設定中指定的設備圖），甚至不在指定段中的設備。

### 設定基於人員的目標報告

您可以在自定義報告中包括以下度量：

* **擴展印象：** (在 [!UICONTROL Build Your Report] 節 [!UICONTROL Metrics] > [!UICONTROL Std. Metrics])通過利用設備圖形（在原始受眾段中找不到）提供的增量印象量。 此度量還用於計算與使用第三方設備圖形相關的適用費用。

   要確定某段時間內擴展印象的成本，請運行包含 [!UICONTROL Extended Impressions] 列，然後將擴展印數總數乘以0.00035美元(0.35/1000印數)。

   總成本亦包括於綜合 [!UICONTROL Billable Other Net Spend] 列 [!UICONTROL Metrics] > [!UICONTROL Spend])，儘管該指標還包括您可能添加的其他促銷費用。

* **設備圖形：** (在 [!UICONTROL Build Your Report] 節 [!UICONTROL Dimensions] > [!UICONTROL Campaign])特定市場活動、包或位置的所選設備圖表。

## 基於人的歸因度量

*僅具有Advertising Cloud轉換跟蹤的廣告商*

使用基於人的屬性，您可以在與媒體曝光發生的設備不同的設備上進行屬性轉換。 基於人的歸屬度測量可在DSPAdvertising Cloud Search和Advertising Cloud Creative為在其網站上實施了Advertising Cloud轉換像素的廣告商提供。

### 啟用基於人的屬性測量

如果要激活跨設備屬性測量，請與 [!DNL Adobe] 客戶團隊。 對於 [!DNL Adobe Device Co-op] 帳戶，您需要提供您的簽名 [!DNL Adobe Device Co-op] 合同和Experience Cloud [!DNL Organization ID] (以前稱 [!DNL IMS org ID])。

要查看廣告商帳戶是否配置為使用設備圖表進行屬性測量：

1. 在主菜單中，按一下 **[!UICONTROL Settings]>[!UICONTROL Advertiser]**。
1. 將游標置於廣告商行上，然後按一下 **[!UICONTROL Edit]**。
1. 在 [!UICONTROL Integrations] 的子目錄中，查看 [!UICONTROL Cross-Device Attribution] 設定處於活動狀態。

   對於主動整合，表示設備圖。

### 設定跨設備轉換屬性的轉換報告

#### 轉換報表設定

當設備圖被啟用用於屬性測量時， [!UICONTROL Conversion] 報告包括 [!UICONTROL Cross-Device Breakout] 設定，允許您為每個轉換度量包括最多三個單獨的列，包括：

* &lt;*轉換*>[!UICONTROL (tp)]:包括總轉換（人員總數），其中包括相同設備轉換和跨設備轉換（如果適用）。 在報告中， &quot;[!UICONTROL (tp)]&quot;被附加到轉換路徑中的轉換度量名稱、規則類型和轉換類型(例如，&quot;Responses(le)(tl)(tp))。

* &lt;*轉換*>[!UICONTROL (sd)]:（可選）僅包括在轉換路徑中僅跟蹤單個設備的轉換。 在報告中， &quot;[!UICONTROL (sd)]&quot;被附加到轉換路徑中的轉換度量名稱、規則類型和轉換類型(例如，&quot;Responses(le)(tl)(sd))。

* &lt;*轉換*>[!UICONTROL (xd)]:（可選）僅包括在轉換路徑中跟蹤多個設備的轉換。 在報告中， &quot;[!UICONTROL (xd)]&quot;被附加到轉換路徑中的轉換度量名稱、規則類型和轉換類型(例如，&quot;Responses(le)(tl)(xd))。

#### 如何解釋轉換報告

如果對跨設備的總轉換百分比進行排序([!UICONTROL (xd)]/[!UICONTROL (tl)])從高到低，您將瞭解驅動高於平均值的跨設備轉換的因素。 您可以使用此策略來告知您的創意或目標策略，以便將消息傳遞和引導投資與用戶行為相匹配。

* 包 — 查看哪些包驅動著最大的總轉換，哪些包具有較高的跨設備轉換百分比。 這可以幫助您瞭解重點支出的位置。

* 放置 — 比較放置效能和屬性（例如，移動Web廣告可能會推動案頭上的轉換）。 如果沒有用於屬性的設備圖表，您可能會錯過移動Web放置對案頭轉換的影響，或者，如果大多數用戶在案頭而不是移動Web上轉換，則可能會被隱藏。

* 廣告 — 發現哪些廣告會推動更高轉換率，並量化它們在Web瀏覽器和移動應用環境中的價值和影響。

* 站點 — 跨站點優化，而不是手動完全排除站點。 如果網站驅動跨設備轉換，則您可以看到在哪些設備上發生此行為。

* 交易 — 通過驗證哪些庫存交易提供跨設備轉換，然後確定是否應將目標擴展到這些交易中包括更多設備和渠道來改進手動優化。

>[!MORELIKETHIS]
>
>* [報告設定](/help/dsp/reports/report-settings.md)
>* [市場活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [包設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [放置設定](/help/dsp/campaign-management/placements/placement-settings.md)

