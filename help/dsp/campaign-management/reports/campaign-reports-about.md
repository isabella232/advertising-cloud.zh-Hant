---
title: 關於平台內報表
description: 了解行銷活動管理檢視中包含的報表資料。
feature: DSP Campaign Data Views
exl-id: e9f7dafe-e0db-4fec-bf5b-858cbcfdde45
source-git-commit: c1441fb6fddf56a0f0346a967da49efa0fb602ff
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 0%

---

# 關於平台內報表

<!-- rename "About Performance Reports in Campaign Management Views?" -->
行銷活動管理檢視包含完整的報表資料。 可用報表可協助您識別成效良好的套件和版位，以及需要您注意的套件和版位。 快速動作按鈕也可讓您更有效率。

## 所有促銷活動清單

[!UICONTROL Campaigns]檢視會開啟，列出您帳戶內的所有促銷活動。 [!UICONTROL Subtotals]列顯示所有可見列中每個量度的總和或平均值。

![行銷活動清單](/help/dsp/assets/campaigns-list.png)

依預設，每個行銷活動列都包含步調和傳送量度。 步調量度包括[!UICONTROL Gross Spend (Lifetime)]，其中包含行銷活動中所有套件的實際目標上支出與預期目標上支出的量度，以便您一目瞭然地識別成效不佳的行銷活動。 您可以選擇[更改列視圖](column-view-change.md)或甚至[建立自定義列視圖](column-view-create.md)。

您可以進一步以其他方式自訂資料表](campaign-data-views-about.md)，並[篩選可見資料](campaign-data-filter.md)。[

若要檢視更詳細的促銷活動，請按一下促銷活動名稱。

## 單一促銷活動報告

在促銷活動中，您可以根據促銷活動實體篩選資料：[!UICONTROL Packages]、[!UICONTROL Placements]和[!UICONTROL Ads]。 您可以進一步[篩選可見資料](campaign-data-filter.md)，以僅包含您想查看的套件、版位或廣告。

![促銷活動實體索引標籤](/help/dsp/assets/campaign-subtabs.png)

在每個實體索引標籤中，每一列預設包含步調和傳送量度，但您可以[變更欄檢視](column-view-change.md)或甚至[建立自訂欄檢視](column-view-create.md)，以套用至促銷活動的所有子索引標籤。 您可以進一步使用其他方式自定義資料表](campaign-data-views-about.md)。 [每個資料表格都包含[!UICONTROL Subtotals]列，可顯示所有可見列中每個量度的總和或平均值。

對於每個促銷活動，您也可以使用三個度量來自訂時間序列趨勢圖，這些度量在每個實體檢視中都可用。 預設情況下，[!UICONTROL Net Spend]、[!UICONTROL Impressions]和[!UICONTROL Net CPM]的資料將包含在單獨的圖表中（網格圖表）。 您可以選擇變更量度。

![三個度量的獨立趨勢圖](/help/dsp/assets/trend-chart-separate.png)

您也可以選擇覆蓋這三個量度，以便輕鬆偵測異常和改善規模或效能的區域。

![覆蓋圖趨勢圖](/help/dsp/assets/trend-chart.png)

您可以依促銷活動[自訂趨勢圖](campaign-data-visualization-manage.md)，而相同的度量會保留在促銷活動的所有趨勢圖中。

### 位置檢查器

對於每個版位，您可以[開啟（詳細資訊檢視[!UICONTROL Inspector]）](placement-details-view.md)，其中包含下列深度資料：

* **[!UICONTROL Sites]:** 投放位置有曝光的所有網站。

   [!UICONTROL Sites]索引標籤包含搜尋和篩選功能、首頁面上可用的相同標準和自訂欄檢視選項，以及每列中的[!UICONTROL Exclude]按鈕，讓您可以快速將網站排除在位置之外。

* **[!UICONTROL Ads]:** 版位中的所有廣告。

   [!UICONTROL Ads]索引標籤包含搜尋和篩選功能、首頁面上可用的相同標準和自訂欄檢視選項，以及每一列的快速動作按鈕，例如[!UICONTROL Pause]（讓您可以快速暫停廣告）。

* **[!UICONTROL Frequency]:** 投放位置之每個廣告頻率層級的資料，包括：
   * 廣告頻率層級（例如「1」，適用於使用者曾看過廣告一次的所有例項）
   * 在指定頻率層級接收曝光數的裝置/瀏覽器或人員（取決於版位的指定[!UICONTROL Cross Device Level]）的預估不重複數量
   * 在指定頻率級別上的估計曝光次數
   * 指定頻率級別的估計平均頻率。 此值等於（估計曝光數）/（估計唯一值）。

* **[!UICONTROL Inventory]:** 以單一檢視定位之所有交易的資訊。

「清單」頁簽包括搜索和篩選功能、首頁上可用的相同標準和自定義列視圖選項以及每行中的快速操作按鈕，如「編輯」和「查看報告」。 「詳細目錄」索引標籤可顯示「拍賣」、「出價」、「贏率」等效能統計資料，以協助快速疑難排解。

# 疑難排解庫存

| 問題 | 可能的原因 | 要採取的動作 |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | 發佈商尚未開始傳送競標請求 | 請聯絡發佈商以啟用交易 |
|  | 交易設定問題，例如輸入錯誤的外部交易ID等。 | 確認交易詳細資訊並編輯交易 |
| [!UICONTROL Non-zero Auctions but no Bids] | 版位鎖定目標與來自交易的傳入競標請求不相符。 <br><br> 例如，版位可能針對的地理位置可能不同於根據交易要求的位置 | 適當地編輯位置設定，以避免與交易的定位不匹配 |
|  | 版位沒有交易要求的有效廣告或正確的媒體類型 | 建立/附加具有正確媒體類型的廣告至版位 |
|  | 職位安排沒有足夠的預算 | 適當編輯投放預算以允許對傳入的請求進行投標 |
|  | 版位投放日期與曝光傳送日期沒有根據交易而重疊 | 編輯投放日期 |
| [!UICONTROL Low Win Rate] | 刊登時的最高出價設定在交易所需的最低出價（下限或固定）以下 | 適當地編輯位置的最高競價 |
|  | 版位使用的出價前篩選條件有 | 降低預先出價篩選器的臨界值，以允許更多出價 |
|  | 刊登版位的對象鎖定限制太嚴 | 檢查指定的對象目標是否有足夠的作用中使用者，並盡可能擴展對象 |

![位置檢查器](/help/dsp/assets/placement-inspector-sites.png)

您可以將[!UICONTROL Sites]、[!UICONTROL Ads]或[!UICONTROL Frequency]標籤上的資料，以XLSM格式的報表形式，匯出至瀏覽器的預設下載資料夾。

### 其他類型的促銷活動層級報表

如需其他資料劃分，請檢視[來自[!UICONTROL Campaigns Classic]的舊版促銷活動層級報表頁面](/help/dsp/campaign-management/campaigns/campaign-view-report.md)。 舊版報表包含[!UICONTROL Geography]、[!UICONTROL Device]、[!UICONTROL Viewability]和[!UICONTROL Audience Performance]資料的區段。

>[!MORELIKETHIS]
>
>* [檢視版位的網站、廣告和頻率詳細資料](placement-details-view.md)
>* [關於促銷活動資料檢視](campaign-data-views-about.md)
>* [建立自訂欄檢視](column-view-create.md)
>* [更改列視圖](column-view-change.md)
>* [管理資料視覺效果](campaign-data-visualization-manage.md)
>* [從促銷活動管理檢視匯出資料](campaign-export-data.md)
>* [檢視促銷活動的詳細報表](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

