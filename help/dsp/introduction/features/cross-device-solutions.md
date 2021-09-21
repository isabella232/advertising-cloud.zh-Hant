---
title: 跨裝置解決方案
description: 進一步了解跨裝置功能。
feature: DSP Introduction
exl-id: 29f8ec41-35a6-4a29-a638-82a2929a8fe6
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '1111'
ht-degree: 0%

---

# 跨裝置解決方案

Advertising Cloud DSP與[!DNL LiveRamp]和[!DNL Adobe Device Co-op]的整合可讓您將對象延伸至人員的所有已知裝置，而不只是您的品牌追蹤的裝置。 整合也提供跨所有裝置的頻率限定和歸因測量。

使用支援的以人物為基礎的裝置圖表時，您可以：

* 比對跨管道和裝置的受眾，以將廣告傳送給人員和家庭，而非裝置。
* 了解並限定個人間的頻率，以平衡和曝光。
* 公開與轉換跨管道或裝置受眾的測試策略。

## 每個裝置圖表的優點

* [!DNL Adobe Device Co-op]:
   * 提供參與Adobe廣告商的決定性和可能性資料的選擇加入池
   * 提供由案頭和行動網站訪客提供技術支援的強大Cookie ID連線
   * 包括主要來自美國和加拿大的資料
   * 無使用費

* [!DNL LiveRamp] 裝置圖表：
   * 提供確定性資料池，包括離線客戶資料
   * 提供Cookie ID與行動裝置ID之間的平均涵蓋範圍
   * 包括主要來自美國的資料
   * 頻率限定和歸因測量可免費使用
   * 延伸曝光數的定價為$0.35 CPM（曝光數僅透過使用[!DNL LiveRamp]裝置圖表來傳送，而非透過目標受眾區段內找到的裝置傳送）

      該費率會反映在您的帳戶費率卡上。

## 以人物為基礎的頻率管理

以人物為基礎的頻率管理可讓您指定人員層級的頻率上限，而非裝置層級，以真正控制媒體曝光。

### 啟用以人物為基礎的頻率管理

* **促銷活動：** 當您建立新促銷活動時，可以指定 [!UICONTROL Cross-Device Level] 設定。啟用&quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People],&quot;並選取裝置圖表。 指定的裝置圖表可用於位置層級的跨裝置鎖定目標，以及行銷活動、封裝和位置層級的以人物為基礎的頻率管理。 頻率上限適用於人員的所有已知裝置。

如需詳細資訊，請參閱[促銷活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)。

儲存促銷活動後，就無法變更其[!UICONTROL Cross Device Level]設定。

* **套件：**  您可以選擇在套件層級設定其他頻率上限。DSP將遵循促銷活動階層中最嚴格的頻率上限。

* **版位：** 您可以選擇在版位層級設定其他頻率上限。DSP將遵循促銷活動階層中最嚴格的頻率上限。

## 以人物為基礎的定位

以人物為基礎的鎖定目標可讓您在案頭和行動裝置間尋找客戶。

### 啟用以人物為基礎的鎖定目標

* **促銷活動：** 當您建立新促銷活動時，可以指定 [!UICONTROL Cross-Device Level] 設定。啟用&quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People],&quot;並選取裝置圖表。 指定的裝置圖表可用於位置層級的跨裝置鎖定目標，以及以人物為基礎的頻率管理。

如需詳細資訊，請參閱[促銷活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)。

* **版位：** 當您使用指定裝置圖表為行銷活動中的版位選取對象目標時， [!UICONTROL Cross-Device Targeting] 選項可讓您將目標延伸到所有人員的已知裝置（根據行銷活動設定中指定的裝置圖表），甚至不在指定區段中的裝置。

### 設定以人物為基礎的定位報表

您可以在自訂報表中加入下列量度：

* **延伸曝光次數：** (在 [!UICONTROL Build Your Report]  [!UICONTROL Metrics]  >  [!UICONTROL Std. Metrics]下方的區段中)透過運用裝置圖表傳遞的增量曝光次數量（在原始受眾區段內找不到）。此量度也用於計算與使用協力廠商裝置圖表相關的適用費用。

   要確定某個時段內擴展曝光次數的成本，請運行包含[!UICONTROL Extended Impressions]列的自定義報告，然後將擴展曝光次數的總數乘以0.00035美元(0.35/1000曝光次數)。

   匯總成本也包含在[!UICONTROL Billable Other Net Spend]欄中（在[!UICONTROL Metrics] > [!UICONTROL Spend]下），不過該量度也包含您可能新增的其他促銷活動費用。

* **裝置圖表：** (在「 [!UICONTROL Build Your Report]  >  [!UICONTROL Dimensions]  [!UICONTROL Campaign]」下方的區段中)特定促銷活動、封裝或位置的選取裝置圖表。

## 以人物為基礎的歸因測量

*僅具有Advertising Cloud轉換追蹤的廣告商*

透過以人物為基礎的歸因，您可以歸因發生在媒體曝光所在裝置以外的不同裝置上的轉換。 DSP、Advertising Cloud Search和Advertising Cloud Creative中，有廣告商已在其網站上實作Advertising Cloud轉換像素，可使用以人物為基礎的歸因測量。

### 啟用以人物為基礎的歸因測量

如果您想要啟用跨裝置歸因測量，請連絡您的Adobe客戶經理。 對於[!DNL Adobe Device Co-op]帳戶，您需要提供您已簽署的[!DNL Adobe Device Co-op]合約和Experience Cloud[!DNL Organization ID]（先前稱為[!DNL IMS org ID]）。

若要查看廣告商帳戶是否已設定為使用裝置圖表進行歸因測量：

1. 在主菜單中，按一下「**[!UICONTROL Settings]>[!UICONTROL Advertiser]**」。
1. 將游標停留在廣告商行上，然後按一下&#x200B;**[!UICONTROL Edit]**。
1. 在廣告商設定的[!UICONTROL Integrations]區段中，查看[!UICONTROL Cross-Device Attribution]設定是否作用中。

   針對作用中的整合，會指出裝置圖表。

### 設定跨裝置轉換歸因的轉換報表

#### 轉換報表設定

為歸因測量啟用裝置圖表時，「[!UICONTROL Conversion]報表」會包含[!UICONTROL Cross-Device Breakout]設定，可讓您為每個轉換量度包含最多三個不同的欄，包括：

* &lt;>轉換&#x200B;*> [!UICONTROL (tp)]:包括總轉換次數（總人數），其中包括相同裝置轉換次數和跨裝置轉換次數（若適用）。*&#x200B;在報表中，「[!UICONTROL (tp)]」會附加至轉換路徑中的轉換量度名稱、規則類型和轉換類型(例如「回應(le)(tl)(tp)」)。

* &lt;>轉換&#x200B;*> [!UICONTROL (sd)]:（選用）僅包含轉換路徑中僅追蹤單一裝置的轉換。*&#x200B;在報表中，「[!UICONTROL (sd)]」會附加至轉換路徑中的轉換量度名稱、規則類型和轉換類型(例如「Responses(le)(tl)(sd)」)。

* &lt;>轉換&#x200B;*> [!UICONTROL (xd)]:（選用）僅包含在轉換路徑中追蹤超過一個裝置的轉換。*&#x200B;在報表中，「[!UICONTROL (xd)]」會附加至轉換路徑中的轉換量度名稱、規則類型和轉換類型(例如「回應(le)(tl)(xd)」)。

#### 如何解譯轉換報表

如果您將跨裝置([!UICONTROL (xd)]/[!UICONTROL (tl)])的轉換總數百分比從高到低排序，您將了解導致跨裝置轉換數高於平均水準的原因。 您可以利用此資訊來通知您的創意或目標策略，以符合訊息和管道投資與使用者行為。

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

