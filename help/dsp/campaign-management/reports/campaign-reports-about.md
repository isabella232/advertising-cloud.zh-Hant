---
title: 關於平台內報告
description: 瞭解市場活動管理視圖中包含的報告資料。
feature: DSP Campaign Data Views
exl-id: e9f7dafe-e0db-4fec-bf5b-858cbcfdde45
source-git-commit: 7d081583ff10675b515aafdd97ccb3053f19c32d
workflow-type: tm+mt
source-wordcount: '938'
ht-degree: 0%

---

# 關於平台內報告

<!-- rename "About Performance Reports in Campaign Management Views?" -->
市場活動管理視圖包括全面的報表資料。 可用的報告可幫助您確定效能良好的包和放置以及需要您注意的那些。 快速操作按鈕還可提高工作效率。

## 所有市場活動視圖

的 [!UICONTROL Campaigns] 「視圖」開啟一組績效資料圖表和帳戶內所有市場活動的清單。

### 圖表視圖 {#chart-view}

你可以 [自定義時間系列趨勢圖](campaign-data-visualization-manage.md) 使用三個指標在所有市場活動中執行。 預設情況下， [!UICONTROL Net Spend]。 [!UICONTROL Impressions], [!UICONTROL Net CPM] 包含在單獨的圖表（網格圖）中。 您可以根據需要更改度量。 要在時間系列趨勢圖中啟用小時資料，請將日期選擇更改為單日([!UICONTROL Today]。 [!UICONTROL Yesterday]或特定日)。

![三個指標的單獨趨勢圖](/help/dsp/assets/trend-chart-separate.png)

您還可以選擇覆蓋這三個指標，以便輕鬆檢測異常和要改進規模或效能的區域。

![覆蓋趨勢圖](/help/dsp/assets/trend-chart.png)

### 表視圖

![市場活動清單](/help/dsp/assets/campaigns-list.png)

預設情況下，每個市場活動行都包括調節和交付度量。 調整指標包括 [!UICONTROL Gross Spend (Lifetime)]，其中包括市場活動中所有一攬子計畫的實際目標支出與預期目標支出的衡量標準，因此您可以一目瞭然地確定業績不佳的市場活動。 您可以選擇 [更改列視圖](column-view-change.md) 甚至 [建立自定義列視圖](column-view-create.md)。

你可以 [自定義資料表](campaign-data-views-about.md) 以及 [篩選可見資料](campaign-data-filter.md)。

要查看更詳細的市場活動，請按一下市場活動名稱。

## 單個市場活動報告 {#single-campaign-reporting}

在市場活動中，您可以根據市場活動實體篩選資料： [!UICONTROL Packages]。 [!UICONTROL Placements], [!UICONTROL Ads]。 你可以 [篩選可見資料](campaign-data-filter.md) 只包括您想看的包裝、放置或廣告。

![市場活動實體頁籤](/help/dsp/assets/campaign-subtabs.png)

### 圖表視圖

對於每次活動， [自定義時間系列趨勢圖](campaign-data-visualization-manage.md) 具有三個度量，這些度量在每個實體視圖中可用。 在市場活動的所有趨勢圖中保留相同的指標。

查看 [關於跨市場活動指標的「圖表視圖」部分](#chart-view) 的子菜單。

### 表視圖

在每個實體頁籤中，每行預設都包括調步和傳遞度量，但您可以 [更改列視圖](column-view-change.md) 甚至 [建立自定義列視圖](column-view-create.md) 要應用於市場活動的所有子標籤。 你可以 [自定義資料表](campaign-data-views-about.md) 以其他方式。 每個資料表包括 [!UICONTROL Subtotals] 行，顯示所有可見行中每個度量的和或平均值。

### 放置 [!UICONTROL Inspector] {#placement-inspector}

對於每個位置， [開啟（詳細資訊視圖） [!UICONTROL Inspector])](placement-details-view.md)，包括以下深度資料：

* **[!UICONTROL Sites]:** 該網站的所有網站都有印象。

   的 [!UICONTROL Sites] 頁籤包括搜索和篩選功能、首頁上可用的相同標準和自定義列視圖選項，以及 [!UICONTROL Exclude] 按鈕，以便您可以從放置中快速排除站點。

* **[!UICONTROL Ads]:** 所有的廣告。

   的 [!UICONTROL Ads] 頁籤包括搜索和篩選功能、首頁上可用的相同標準和自定義列視圖選項以及每行中的快速操作按鈕，如 [!UICONTROL Pause] （這樣您就可以快速暫停廣告）。

* **[!UICONTROL Frequency]:** 放置的每個廣告頻率級別的資料，包括：
   * 廣告頻率級別（如用戶一次看到廣告的所有實例的「1」）
   * 估計的設備/瀏覽器或人員的唯一數量(取決於指定的 [!UICONTROL Cross Device Level] 在指定頻率級別接受印象
   * 在指定頻率級別上的印次估計數
   * 指定頻率電平的估計平均頻率。 此值等於（估計印數）/（估計單位）。

* **[!UICONTROL Inventory]:** 有關該位置所針對的所有交易的資訊。

   的 [!UICONTROL Inventory] 頁籤包括搜索和篩選功能、首頁上可用的相同標準和自定義列視圖選項以及每行中的快速操作按鈕，如 [!UICONTROL Edit] 和 [!UICONTROL View Report]。 的 [!UICONTROL Inventory] 頁籤通過顯示效能統計資訊來啟用快速故障排除 [!UICONTROL Auctions]。 [!UICONTROL Bids], [!UICONTROL Win Rate]。

#### 排除清單故障

| 問題 | 可能的原因 | 要採取的操作 |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | 發佈者尚未開始發送投標請求。 | 聯繫發行商以激活交易。 |
|  | 交易設定不正確，例如輸入了不正確的外部交易ID。 | 確認交易詳細資訊並編輯交易。 |
| [!UICONTROL Auctions but no Bids] | 配售目標與該交易的傳入投標請求不匹配。 <br><br> 例如，職位安排可能針對的是不符合交易資格的地理位置。 | 根據需要編輯放置目標，以避免目標不匹配。 |
|  | 該位置沒有具有交易所需媒體類型的活動廣告。 | 建立具有正確媒體類型的廣告並將其附加到位置。 |
|  | 該職位沒有足夠的預算。 | 增加安置預算以允許對傳入請求進行投標。 |
|  | 放行日期與交易的印象交付日期不重疊。 | 根據需要編輯放置的飛行日期。 |
| [!UICONTROL Low Win Rate] | 配售的最高出價（最低或固定）低於交易要求的最低出價。 | 增加職位安排 [!UICONTROL Max Bid] 按需要。 |
|  | 該置換使用限制投標的投標前過濾器。 | 降低預投標篩選器的閾值，以允許更多投標。 |
|  | 受眾針對該職位的限制性太強。 | 檢查指定的受眾目標是否具有足夠的活動用戶，並在可能時擴展受眾。 |

![放置檢查器](/help/dsp/assets/placement-inspector.png)

可以導出 [!UICONTROL Sites]。 [!UICONTROL Ads]或 [!UICONTROL Frequency] 的子菜單。

### 其它類型的市場活動層報告

對於其他資料斷開，請查看 [市場活動級報告頁](/help/dsp/campaign-management/campaigns/campaign-view-report.md)。 的 <!--legacy --> 報告包括部分 [!UICONTROL Geography]。 [!UICONTROL Device]。 [!UICONTROL Viewability], [!UICONTROL Audience Performance] 資料。

>[!MORELIKETHIS]
>
>* [查看位置的站點、廣告和頻率詳細資訊](placement-details-view.md)
>* [關於市場活動資料視圖](campaign-data-views-about.md)
>* [建立自定義列視圖](column-view-create.md)
>* [更改列視圖](column-view-change.md)
>* [管理資料可視化](campaign-data-visualization-manage.md)
>* [從Campaign Management視圖導出資料](campaign-export-data.md)
>* [查看市場活動的詳細報表](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

