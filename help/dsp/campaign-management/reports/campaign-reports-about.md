---
title: 關於平台內報表
description: 了解行銷活動管理檢視中包含的報表資料。
feature: DSP Campaign Data Views
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# 關於平台內報表

<!-- rename "About Performance Reports in Campaign Management Views?" -->
行銷活動管理檢視包含完整的報表資料。 可用報表可協助您識別成效良好的套件和版位，以及需要您注意的套件和版位。 快速動作按鈕也可讓您更有效率。

## 所有促銷活動檢視

此 [!UICONTROL Campaigns] 檢視會開啟一組效能資料圖表，以及帳戶內所有促銷活動的清單。

### 圖表視圖 {#chart-view}

您可以 [自定義時間序列趨勢圖](campaign-data-visualization-manage.md) 使用三個量度來檢視所有促銷活動。 依預設， [!UICONTROL Net Spend], [!UICONTROL Impressions]，和 [!UICONTROL Net CPM] 都包含在單獨的圖表（網格圖表）中。 您可以選擇變更量度。 若要在時間序列趨勢圖中啟用每小時資料，請將日期選擇變更為單日([!UICONTROL Today], [!UICONTROL Yesterday]，或特定日期)。

![三個度量的獨立趨勢圖](/help/dsp/assets/trend-chart-separate.png)

您也可以選擇覆蓋這三個量度，以便輕鬆偵測異常和改善規模或效能的區域。

![覆蓋圖趨勢圖](/help/dsp/assets/trend-chart.png)

### 表格檢視

![行銷活動清單](/help/dsp/assets/campaigns-list.png)

依預設，每個行銷活動列都包含步調和傳送量度。 步調量度包括 [!UICONTROL Gross Spend (Lifetime)]，包括行銷活動中所有套件的實際目標上支出與預期目標上支出的量度，因此您可以一眼就識別成效不佳的行銷活動。 您可以選擇 [更改列視圖](column-view-change.md) 或 [建立自訂欄檢視](column-view-create.md).

您可以進一步 [自訂資料表](campaign-data-views-about.md) 以及 [篩選可見資料](campaign-data-filter.md).

若要檢視更詳細的促銷活動，請按一下促銷活動名稱。

## 單一促銷活動報告 {#single-campaign-reporting}

在促銷活動中，您可以根據促銷活動實體篩選資料： [!UICONTROL Packages], [!UICONTROL Placements]，和 [!UICONTROL Ads]. 您可以進一步 [篩選可見資料](campaign-data-filter.md) 僅包含您想要查看的套件、版位或廣告。

![促銷活動實體索引標籤](/help/dsp/assets/campaign-subtabs.png)

### 圖表視圖

對於每個促銷活動，您可以 [自定義時間序列趨勢圖](campaign-data-visualization-manage.md) 包含三個量度，可在每個實體檢視中使用。 促銷活動的所有趨勢圖表中，都會保留相同的量度。

請參閱 [跨促銷活動量度的「圖表檢視」區段](#chart-view) 以取得更多資訊。

### 表格檢視

在每個實體索引標籤中，每一列預設包含步調和傳送量度，但您可以 [更改列視圖](column-view-change.md) 或 [建立自訂欄檢視](column-view-create.md) 以套用至促銷活動的所有子標籤。 您可以進一步 [自訂資料表](campaign-data-views-about.md) 以其他方式。 每個資料表都包含 [!UICONTROL Subtotals] 列，其中顯示所有可見列中每個量度的總和或平均值。

### 版位 [!UICONTROL Inspector] {#placement-inspector}

對於每個版位，您可以 [開啟（詳細資訊檢視） [!UICONTROL Inspector])](placement-details-view.md)，包含下列深入資料：

* **[!UICONTROL Sites]:** 投放位置有曝光的所有網站。

   此 [!UICONTROL Sites] 索引標籤包含搜尋和篩選功能、首頁面上可用的相同標準和自訂欄檢視選項，以及 [!UICONTROL Exclude] 按鈕，以便快速從版位中排除網站。

* **[!UICONTROL Ads]:** 版位中的所有廣告。

   此 [!UICONTROL Ads] 索引標籤包含搜尋和篩選功能、首頁面上可用的相同標準和自訂欄檢視選項，以及每列中的快速動作按鈕，例如 [!UICONTROL Pause] （以便您快速暫停廣告）。

* **[!UICONTROL Frequency]:** 投放位置之每個廣告頻率層級的資料，包括：
   * 廣告頻率層級（例如「1」，適用於使用者曾看過廣告一次的所有例項）
   * 預估的裝置/瀏覽器或人員不重複數量(取決於指定 [!UICONTROL Cross Device Level] （適用於促銷活動），在指定頻率層級接收曝光數
   * 在指定頻率級別上的估計曝光次數
   * 指定頻率級別的估計平均頻率。 此值等於（估計曝光數）/（估計唯一值）。

* **[!UICONTROL Inventory]:** 投放位置所定位之所有交易的相關資訊。

   此 [!UICONTROL Inventory] 標籤可顯示效能統計資訊，如 [!UICONTROL Auctions], [!UICONTROL Bids]，和 [!UICONTROL Win Rate]. 索引標籤包含搜尋和篩選功能、首頁面上可用的相同標準和自訂欄檢視選項，以及每列中的快速動作按鈕，包括 [!UICONTROL Edit], [!UICONTROL View Report]，和 [[!UICONTROL Auction Insights] 進一步疑難排解](/help/dsp/inventory/private-deal-auction-insights.md).

#### 疑難排解庫存

| 問題 | 可能的原因 | 要採取的動作 |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | 發佈商尚未開始傳送競標請求。 | 請聯絡發佈商以啟動交易。 |
|  | 交易設定不正確，例如輸入錯誤的外部交易ID。 | 確認交易詳細資訊並編輯交易。 |
| [!UICONTROL Auctions but no Bids] | 版位定位不符合交易傳入的競標請求。 <br><br> 例如，版位可能會鎖定不符合交易資格的地理位置。 | 視需要編輯投放目標，以避免目標不匹配。 |
|  | 版位沒有交易所需媒體類型的作用中廣告。 | 建立廣告，並將具有正確媒體類型的廣告附加至版位。 |
|  | 這個職位沒有足夠的預算。 | 增加投放預算，以允許對傳入的請求進行投標。 |
|  | 版位投放日期與交易的曝光傳送日期不重疊。 | 視需要編輯版位的投放日期。 |
| [!UICONTROL Low Win Rate] | 配售的最高出價（最低或固定）低於交易要求的最低出價。 | 增加版位 [!UICONTROL Max Bid] 視需要。 |
|  | 刊登版位使用限制競標的預先出價篩選條件。 | 降低預先出價篩選器的臨界值，以允許更多出價。 |
|  | 版位的對象鎖定目標限制太嚴格。 | 檢查指定的對象目標是否有足夠的作用中使用者，並盡可能展開對象。 |

![位置檢查器](/help/dsp/assets/placement-inspector.png)

您可以匯出 [!UICONTROL Sites], [!UICONTROL Ads]，或 [!UICONTROL Frequency] 以XLSM格式的報表形式，將標籤定位至瀏覽器的預設下載資料夾。

### 其他類型的促銷活動層級報表

對於其他資料劃分，請檢視 [行銷活動層級報表頁面](/help/dsp/campaign-management/campaigns/campaign-view-report.md). 此 <!--legacy --> 報告中包含 [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability]，和 [!UICONTROL Audience Performance] 資料。

>[!MORELIKETHIS]
>
>* [檢視版位的網站、廣告和頻率詳細資料](placement-details-view.md)
>* [關於促銷活動資料檢視](campaign-data-views-about.md)
>* [建立自訂欄檢視](column-view-create.md)
>* [更改列視圖](column-view-change.md)
>* [管理資料視覺效果](campaign-data-visualization-manage.md)
>* [從Campaign Management檢視匯出資料](campaign-export-data.md)
>* [檢視促銷活動的詳細報表](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

