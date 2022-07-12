---
title: 放置設定
description: 請參閱可用放置設定的說明。
feature: DSP Placements
exl-id: 36097132-e589-4d49-bf86-54f61eae5b67
source-git-commit: ef8e13dc5f94ead81191862dbb37c17ae762682d
workflow-type: tm+mt
source-wordcount: '3301'
ht-degree: 0%

---

# 放置設定

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** 放置名稱。

>[!TIP]
>使用適合您情況的命名約定。 建議的命名約定是「*\&lt;campaign name=&quot;&quot;>:\&lt;ad unit=&quot;&quot;>:\&lt;duration>:\&lt;targeting>*&quot;

**[!UICONTROL Status]:** 放置狀態： *[!UICONTROL Active]* （預設）或 *[!UICONTROL Paused]*。

>[!TIP]
>最佳做法是暫停放置，直到您準備好啟動它。

**[!UICONTROL Details]:** （只讀）適用的廣告類型、建立或建立職位安排的帳戶以及父市場活動。 要查看更多詳細資訊，請按一下 **[!UICONTROL Show more]**。

**[!UICONTROL Templates]:** 開啟現有放置模板的清單。 要從模板自動填充目標設定：

1. 執行下列任一操作：

   * 要重新使用模板中的所有目標，請選中模板名稱旁邊的複選框。

   * 要從模板中重用單個目標類型，請展開模板名稱，然後選中要重用的目標類型旁邊的複選框。

1. 按一下 **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** （僅視頻廣告格式）廣告持續時間和/或廣告規格，用於計算右側的預測投影。 欄位因廣告類型而異。

**[!UICONTROL Placement tags]:** （可選）用於幫助您定位此位置的關鍵字或暱稱。

## 目標

**[!UICONTROL Package]:** （可選）分配了放置的包。 按一下 ![編輯](/help/dsp/assets/edit.png) 選擇和現有包或建立新包。 將放置指定給包時， [!UICONTROL Goals] 此部分將更新為航班日期、交貨目標和包中的預算。

**[!UICONTROL Flight Dates]:** 放置的開始日期和結束日期。 當放置處於活動狀態並分配給活動的包裝或市場活動時，批准的廣告有資格在飛行期間運行。

預設情況下，包（如果適用）或市場活動的日期將自動填充。

>[!NOTE]
>
>* 飛行日期必須包括在活動飛行日期和包裝飛行日期中。


### 分配給具有包級別調整的包的放置

**[!UICONTROL Placement Funding]:** 如何預算職位安排：

* *[!UICONTROL Optimize based on performance]:* 在包級別控制預算。
* *[!UICONTROL Set a fixed budget cap]:* 允許您設定每日、每週、每月或全時的職位安排預算。 輸入值和持續時間(*[!UICONTROL All time]*。 *[!UICONTROL Daily]*。 *[!UICONTROL Weekly]*。 *[!UICONTROL Monthly]*)。

**[!UICONTROL Max Bid]:** 最多要付1000個印象。

**[!UICONTROL Placement Pre-bid Filters]:** 最多5個KPI閾值（例如最小可查看性度量或點擊率），必須滿足這些閾值才能進行投標。 您可以將投標前篩選器用作優化策略，但要瞭解，每個規則都可能限制此配售可以投標的機會。 要添加或編輯篩選器：

1. 按一下 ![編輯](/help/dsp/assets/edit.png)。
1. 執行下列任一操作：
   * 要添加篩選器：
      1. 按一下 **[!UICONTROL Add Filter]**.
      1. 旁邊 **[!UICONTROL Only bid if]**，選擇度量，然後輸入值。
   * 要刪除篩選器，請按一下 **[!UICONTROL X]** 的子菜單。
1. 按一下 **[!UICONTROL Save]**.

請參閱「」中每個預投標篩選器的說明[位置級預投標過濾器及其使用方法](/help/dsp/optimization/optimization-pre-bid-filters.md)&quot;

### 所有其他放置

**[!UICONTROL Budget Goal]:** 總預算上限和預算間隔(*[!UICONTROL All time]*。 *[!UICONTROL Daily]*。 *[!UICONTROL Weekly]*。 *[!UICONTROL Monthly]*)。

**[!UICONTROL Gross Budget Goal]:** （僅限使用毛利管理的市場活動中的放置）總預算上限和預算間隔(*[!UICONTROL All time]*。 *[!UICONTROL Daily]*。 *[!UICONTROL Weekly]*。 *[!UICONTROL Monthly]*)。

**[!UICONTROL Optimization Goal]:**  包的優化目標。 請參閱「」中每個優化目標的說明[優化目標及其使用方法](/help/dsp/optimization/optimization-goals.md)。

**[!UICONTROL Target Goal]:** 目標目標，用於跟蹤效能。

>[!NOTE]
>
>此欄位僅是基準，不用於決策。

**[!UICONTROL Pace on]:** 調步將基於：

* **[!UICONTROL Budget goal]:** （預設）此選項在分配的預算內提供盡可能多的印象。

* **[!UICONTROL Impressions]:** 此選項在指定的時間間隔內達到指定數量之前提供印數。 選擇此選項時，指定印次數和間隔： *[!UICONTROL All time]。* *[!UICONTROL Daily]。* *[!UICONTROL Monthly]。* 或 *[!UICONTROL Weekly]*。

**[!UICONTROL Max Bid]:** 最多要付1000個印象。

**[!UICONTROL Pacing Fill Strategy]:** （僅包級調整的包）如何調整和交付：

* *[!UICONTROL Even]:* （預設）在每次飛行中均勻地執行交付，目標是在飛行前半段執行50%的交付。

* *[!UICONTROL Frontload]:* 加快交貨速度，在飛行中途完成65-75%。

* *[!UICONTROL Aggressive Frontload]:* 加快交貨速度，在飛行中途完成75-85%。

**[!UICONTROL Placement Pre-bid Filters]:** （可選）最多必須滿足五個篩選條件才能進行投標。 您可以將投標前篩選器用作優化策略，但請記住，每個規則都可能限制此配售可以投標的機會。 要添加或編輯篩選器：

1. 按一下 ![編輯](/help/dsp/assets/edit.png)。
1. 執行下列任一操作：
   * 要添加篩選器：
      1. 按一下 **[!UICONTROL Add Filter]**.
      1. 旁邊 **[!UICONTROL Only bid if]**，選擇度量，然後輸入值。
   * 要刪除篩選器，請按一下 **[!UICONTROL X]** 的子菜單。
1. 按一下 **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** （可選）要在放置中包括或排除廣告的特定位置。 如果未指定任何位置，則所有位置都是目標位置。

>[!NOTE]
>
>城市和DMA位置不適用於Roku放置。

要指定位置：

1. 按一下 ![編輯](/help/dsp/assets/edit.png)。
1. 執行下列任一操作：
   * 要包括或排除國家、州、市、DMA、聯邦立法區或州立法區：
      1. 在左欄中選擇位置類型。
      1. （根據需要）按一下某個位置展開它。
      1. 在位置旁邊，按一下 *[!UICONTROL Include]* 將其作為目標或 *[!UICONTROL Exclude]* 將其排除為目標。
   * 要搜索郵遞區號並包括或排除所有選定結果，請執行以下操作：
      1. 按一下 **[!UICONTROL Search Postal Code]**.
      1. 選擇國家/地區。
      1. 輸入城市名稱，然後按一下 ![編輯](/help/dsp/assets/search.png)。
      1. 按一下正確的搜索結果。
      1. 按一下 *[!UICONTROL Include All]* 將所有位置作為目標或 *[!UICONTROL Exclude All]* 將所有位置排除為目標。
   * 要輸入或貼上郵遞區號，並包括或排除所有郵遞區號：
      1. 按一下 **[!UICONTROL Paste Postal Code]**.
      1. 選擇國家/地區。
      1. 輸入或貼上最多1000個郵遞區號。
每行包含一個郵遞區號，或輸入多個以逗號或制表符分隔的值。
      1. 按一下 *[!UICONTROL Include All]* 將所有位置作為目標或 *[!UICONTROL Exclude All]* 將所有位置排除為目標。
   * 從 [!UICONTROL Included] 或 [!UICONTROL Excluded] 清單，按一下 **[!UICONTROL X]** 的子菜單。
1. 按一下 **[!UICONTROL Done]**.

>[!NOTE]
>
>* 並非所有國家/地區都有州、市或郵遞區號位置。
>* DMA（指定市場區）、聯邦立法區和州立法區僅可在美國提供。


## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** 要包括或排除作為目標的庫存來源。 對於大多數放置類型，預設情況下包括所有庫存類型和每種類型的所有來源。 對於 [!DNL Roku] 放置，您必須指定庫存類型和來源。 您可以從以下類型的庫存中進行選擇：

* [!UICONTROL Public]:（除Roku外的所有放置類型）Advertising Cloud有權訪問的所有開放交換庫存。 您可以包括和排除公用清單。

   您可以按源或源查看清單。 按饋送查看清單時，可以按饋送名稱、饋送密鑰或選定的特徵標籤進行搜索。

* [!UICONTROL Private] | [!UICONTROL Roku Private]:您現有的私有交易（或現有的私有交易） [!DNL Roku] 交易 [!DNL Roku] 與您所設定的出版商合DSP作。 您可以包括但不排除公共庫存。

   您可以按關鍵字、鍵、交易ID或自定義標籤搜索清單。

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]:全部 [溢價，無擔保 [!UICONTROL On Demand] 庫存](/help/dsp/inventory/on-demand-inventory-about.md) 或 [!UICONTROL On Demand] [!DNL] Roku交易 [!DNL Roku] 配售) [!DNL DSP]。 可以包括和排除 [!UICONTROL On Demand] 庫存。

   您可以按源或源查看清單。 按源查看清單時，可以按源名稱、源鍵或選定的發佈者區域、類別標籤或特徵標籤進行搜索。

要指定庫存目標，請執行以下操作：

* 要排除庫存類型，請清除名稱旁邊的複選框。
* 要瞄準庫存類型：
   1. 選中庫存類型名稱旁邊的複選框。
   1. （可選）更改源以包括：
      1. 按一下 ![編輯](/help/dsp/assets/edit.png)。
      1. ([!UICONTROL Public] 和 [!UICONTROL On Demand] 清單)按一下 *[!UICONTROL *View by Source]**或 **[!UICONTROL View by Feed]** 更改源的清單方式。
      1. （如果適用）根據需要篩選庫存。
      1. 指定要包括和排除的源：
         * 要包括 [!UICONTROL Public] 或 [!UICONTROL On Demand] 源，按一下 **[!UICONTROL Include]** 的子菜單。
         * 要包括 [!UICONTROL Private] 源：
            * 要在交易中包括所有庫存，請按一下 **[!UICONTROL Include all]** 地址欄。
            * 要包括單個庫存來源，請展開交易名稱，然後按一下來源名稱旁邊的複選框。
         * 排除 [!UICONTROL Public] 或 [!UICONTROL On ] 源，按一下 **[!UICONTROL Exclude]** 的子菜單。
   1. （可選）要將包含目標資訊的CSV檔案下載到瀏覽器的「下載」位置，請按一下 **[!UICONTROL Save & Export]**。
   1. 按一下 **[!UICONTROL Save]**.

>[!TIP]
>
>如果您訂閱 [!UICONTROL On Demand] 清單，但找不到要瞄準的發佈者或交易，然後檢查交易的狀態。 有關狀態的詳細資訊，請參閱 [關於 [!DNL On Demand] 高級庫存](/help/dsp/inventory/on-demand-inventory-about.md)。

**[!UICONTROL Exclude out-stream]:** （僅視頻放置）排除流出流量。

外流廣告通常在內容上顯示為彈出窗口或填充到內容中（在本地體驗中），而不是像視頻播放器中的常規視頻廣告那樣出現。

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** 目標通信的類型。 選項包括 **[!UICONTROL Websites]** 和 **[!UICONTROL Apps]**。

**[!UICONTROL Site tier]:** (當 **[!UICONTROL Paste list of targeted sites]** 是 *[!UICONTROL Off]*)目標站點的質量。 第1至第3層都是品牌安全的，並經過地圖編製小組的審DSP核和批准。

* *[!UICONTROL Tier 1]:* 具有全國認知度的高級站點和應用程式。
* *[!UICONTROL Tier 2]:* 目標是第1層，以及比第1層更不為人所知的高質量站點和應用程式。
* *[!UICONTROL Tier 3]:* 目標是第1至2層，以及符合特定用戶需要的合法且品牌安全的站點和應用程式。 使用第3層進行訪問或資料目標購買。
* *[!UICONTROL All Sites]:* 目標層1-3和未經過篩選或分類的新庫存，您可以使用這些庫存進行訪問。

>[!NOTE]
>
>庫存特定於放置中的廣告單位。

>[!TIP]
>
>對於績效市場活動，最佳做法是選擇 *[!UICONTROL All Sites]*。

**[!UICONTROL Site Categories]:** (可選；可用 **[!UICONTROL Paste list of targeted sites]** 是 *[!UICONTROL Off]*)所選站點層中的站點類別，以包括或排除（但不包括兩者）作為目標。 從Advertising Cloud根據站點主題映射的垂直站點清單中進行選擇：

1. 按一下 ![編輯](/help/dsp/assets/edit.png)。
1. 指定要包括或排除的站點類別：
   * 要包括站點類別：
      1. 按一下 **[!UICONTROL Include categories]**.
      1. 選中每個目標類別旁邊的複選框。
   * 要排除站點類別，請執行以下操作：
      1. 按一下 **[!UICONTROL Exclude categories]**.
      1. 選中要排除的每個類別旁邊的複選框。
1. （可選）要將包含目標資訊的CSV檔案下載到瀏覽器的「下載」位置，請按一下 **[!UICONTROL Export]**。
1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** (可選；可用 **[!UICONTROL Paste list of targeted sites]** 是 *[!UICONTROL Off]*)要排除的站點。 您可以搜索和選擇站點，或輸入或貼上域名：

1. 按一下 ![編輯](/help/dsp/assets/edit.png)。
1. 指定站點：
   * 要搜索站點，請執行以下操作：
      1. 按一下 **[!UICONTROL Search]**.
      1. 輸入關鍵字、選擇站點層和/或選擇站點類別。
      1. 在搜索結果中，選擇要排除的站點：
         * 要排除單個站點，請選中其旁邊的複選框。
         * （當50個以上結果可用時）要排除前50個結果，請按一下 **[!UICONTROL Exclude these 50]**。 要排除所有搜索結果，請按一下 **[!UICONTROL Exclude these \<*非&#x200B;*\>]**。
   * 要輸入域名：
      1. 按一下 **[!UICONTROL Paste]**.
      1. 在單獨的行上輸入一個或多個域名。
      1. 按一下 **[!UICONTROL Exclude All]**.
1. 按一下 **[!UICONTROL Done]** 你完事了。

>[!NOTE]
>
>* 除Advertising Cloud DSP外，還應用帳戶級和廣告商級被阻止的網站清單 [全局阻止的站點清單](/help/dsp/introduction/features/brand-safety-media-quality.md)包括廣告認為不安全的網站。
>* 阻止的站點清單始終覆蓋目標站點清單。 如果放置既排除廣告又包括同一廣告目標，則排除該目標。


**[!UICONTROL Language]:** （可選）要目標的單種語言。

**[!UICONTROL Site List Preview]:** （只讀）放置的所有目標站點和被阻止的站點。

可以選擇將目標站點和被阻止站點的清單導出為逗號分隔值(CSV)檔案。 要導出清單，請按一下 **[!UICONTROL Export full site list]**，然後根據瀏覽器的常規過程開啟或保存檔案。

**[!UICONTROL Allow unscreened sites]:** （僅限標準顯示放置）在非審核站點上啟用廣告交付。 當放置目標為私人庫存時，此選項可在被阻止的站點上投放廣告。

**[!UICONTROL Paste list of targeted sites]:** 允許您僅針對特定站點。 啟用此選項後，其他站點目標選項將被禁用。

**[!UICONTROL Sites]:** (當 **[!UICONTROL Paste list of targeted sites]** 是 *[!UICONTROL On]*)目標站點。 您可以搜索和選擇站點，或輸入或貼上域名：

1. 按一下 ![編輯](/help/dsp/assets/edit.png)。
1. 指定站點：
   * 要搜索站點，請執行以下操作：
      1. 按一下 **[!UICONTROL Search]**.
      1. 輸入關鍵字、選擇站點層和/或選擇站點類別。
      1. 在搜索結果中，選擇要包括的站點：
         * 要排除單個站點，請選中其旁邊的複選框。
         * （當50個以上結果可用時）要包括前50個結果，請按一下 **[!UICONTROL Include these 50]**。 要包括所有搜索結果，請按一下 **[!UICONTROL Include these \<*非&#x200B;*\>]**。
   * 要輸入域名：
      1. 按一下 **[!UICONTROL Paste]**。
      1. 在單獨的行上輸入一個或多個域名。
      1. 按一下 **[!UICONTROL Include All]**.
1. 按一下 **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** 該職位的任何受眾目標，包括 [第三方段、第一方段、Adobe段、自定義段和已保存的受眾](/help/dsp/audiences/audience-settings.md)。 還會顯示所有選定段和已保存受眾的總和和活動的重複資料消除受眾大小。 您可以選擇現有受眾，建立稍後可以重新使用的新受眾，或選擇特定受眾群：

* 要選擇現有受眾，請按一下 ![選擇](/help/dsp/assets/chevron-down.png) 下 [!UICONTROL Included Audiences]，然後選擇觀眾。
* 要建立新受眾，請按一下 ![選擇](/help/dsp/assets/chevron-down.png) 下 [!UICONTROL Included Audiences]，然後選擇 **[!UICONTROL + Create Audience]**。 有關說明，請參見 [建立可重用的受眾](/help/dsp/audiences/reusable-audience-create.md)，從步驟3開始。
* 要選擇特定受眾段，請按一下 **[!UICONTROL Select segments for this placement only]**。 選擇段邏輯；有關說明，請參閱「」中的步驟6[建立可重用的受眾](/help/dsp/audiences/reusable-audience-create.md)&quot; 完成後，按一下 **保存**。

**[!UICONTROL Excluded Audiences]:** 要排除的播放對象，包括與 [第三方段、第一方段、Adobe段、自定義段和已保存的受眾](/help/dsp/audiences/audience-settings.md)。 還顯示所有排除的受眾的總和和活動的重複資料消除受眾大小。 您可以選擇現有受眾或建立新受眾，以後可以重新使用：

* 要選擇現有受眾，請按一下 ![選擇](/help/dsp/assets/chevron-down.png) 下 [!UICONTROL Excluded Audiences]，然後選擇觀眾。
* 要建立新受眾，請按一下 ![選擇](/help/dsp/assets/chevron-down.png) 下 [!UICONTROL Excluded Audiences]，然後選擇 **+建立受眾**。 有關說明，請參見 [建立可重用的受眾](/help/dsp/audiences/reusable-audience-create.md)，從步驟3開始。

**[!UICONTROL Cross Device Targeting]:** (當您至少選擇一個段或受眾和 [為基於人的跨設備目標配置活動](/help/dsp/campaign-management/campaigns/campaign-settings.md)。 允許您將目標擴展到人員的所有已知設備（根據市場活動設定中指定的設備圖表），甚至不在指定段中的設備。 根據市場活動指定的圖表，可以適用費用。 設備圖形資料目前僅在北美可用。

**[!UICONTROL Placement Cap]:** （可選）唯一設備或人員的次數(取決於指定的 [!UICONTROL Cross Device Level])將從該位置獲得廣告。 選項包括 *[!UICONTROL Unlimited]* 或每天、每週或每月的特定金額。

>[!NOTE]
>
> 您可以在市場活動、包裝和放置層設定頻率上限。 會DSP尊重市場活動等級中最嚴格的頻率限制。

**[!UICONTROL Secondary Cap]:** (可選；包含數字時可用 [!UICONTROL Placement Cap])在主放置帽的界限內附加限制。 選擇印數和時間段（例如每12小時3次）。

**[!UICONTROL Day Parting]:** （可選）一週中特定的天數和一天中可能運行廣告的時間。 要指定日分隔間隔：
1. 按一下 ![編輯](/help/dsp/assets/edit.png)。
1. 選擇適用的時區。
1. 指定間隔：
   * 要選擇預設間隔，請按一下其中一個間隔按鈕。 選項包括*[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*。 *[!UICONTROL Morning]*。 *[!UICONTROL Lunch]*。 *[!UICONTROL Dinner]*&#x200B;或 *[!UICONTROL Prime]* （黃金時段）。
   * 要手動選擇間隔，請在單元格內按一下，然後可選擇拖動以選擇間隔。
1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (可選；可用於配置有 [!DNL Comscore] 和 [!DNL Grapeshot] 段)特定段名稱或ID [!DNL Comscore] 和 [!DNL Grapeshot] 作為目標。 此功能可能需要額外費用。 要激活此功能並設定主題段，請與 [!DNL Adobe] 客戶團隊。

要指定主題目標：

1. 按一下 ![編輯](/help/dsp/assets/edit.png)。
1. 指定目標段：
   1. 在左欄中，選擇合作夥伴(*[!UICONTROL Comscore]* 或 *[!UICONTROL Grapeshot]*)。
   1. 在輸入欄位中，輸入段名稱或段ID。
1. （可選）要將包含主題資訊的CSV檔案下載到瀏覽器的「下載」位置，請按一下 **[!UICONTROL Export]**。
1. 按一下 **[!UICONTROL Save]**.

>[!TIP]
>
>* 主題目標限制了放置位置可以投標的庫存，因此，僅將主題目標用於購買總量的一小部分。
>
>* 在上的段內設定任何負目標 [!DNL Comscore] 或 [!DNL Grapeshot]。


**[!UICONTROL Device Targeting]:** （可選）特定設備資訊，包括設備類型、製造商、作業系統、瀏覽器和連接類型，以包括和排除作為目標。 要指定設備目標：

1. 按一下 ![編輯](/help/dsp/assets/edit.png)。
1. 指定要包括和排除的設備詳細資訊：
   1. 在左欄中，選擇類別。
   1. 指定目標：
      * 要包括值，請按一下 **[!UICONTROL Include]** 值名稱旁邊。
      * 要排除值，請按一下 **[!UICONTROL Exclude]** 值名稱旁邊。
1. （可選）要將帶有設備目標資訊的CSV檔案下載到瀏覽器的「下載」位置，請按一下 **[!UICONTROL Export]**。
1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** （可選）特定網際網路服務提供商(ISP)要麼包括或排除（但不包括兩者）作為目標。 要指定ISP目標：

1. 按一下 ![編輯](/help/dsp/assets/edit.png)。
1. 指定要包括或排除的ISP:
   * 要包括ISP:
      1. 按一下 **[!UICONTROL Include ISPs]**.
      1. （可選）按關鍵字篩選清單。
      1. 選中每個目標ISP旁邊的複選框。
   * 要排除ISP:
      1. 按一下 **[!UICONTROL Exclude ISPs]**.
      1. （可選）按關鍵字篩選清單。
      1. 選中要排除的每個ISP旁邊的複選框。
1. （可選）要將ISP目標資訊的CSV檔案下載到瀏覽器的「下載」位置，請按一下 **[!UICONTROL Export]**。
1. 按一下 **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** 類型 [!DNL Comscore]。 [!DNL DoubleVerify]。 [!DNL Integral Ad Science], [!DNL Peer39] 要應用的上下文篩選器。 已為新廣告投放選擇廣告商級預設值，但您可以更改以下設定：

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** （可選）預設情況下要阻止的一種或多種類型的庫存上下文。 可能需要額外收費。

* [!UICONTROL Peer 39]:

   * **目標站點：** （可選）預設情況下目標的一種或多種庫存屬性類型。 可能需要額外收費。

* [!UICONTROL ComScore]:

   * **阻止以下站點：** （可選）預設情況下要阻止的一種或多種庫存屬性類型。 可能需要額外收費。

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** （可選）預設情況下要阻止廣告的成人內容的程度： *[!UICONTROL Do Not Block]* （預設值）, *[!UICONTROL Standard]*&#x200B;或 *[!UICONTROL Strict]*。 可能需要額外收費。

   * **[!UICONTROL Alcohol Content]:** （可選）預設情況下要阻止廣告的酒精含量程度： *[!UICONTROL Do Not Block]* （預設值）, *[!UICONTROL Standard]*&#x200B;或 *[!UICONTROL Strict]*。 可能需要額外收費。

**[!UICONTROL Pre-bid fraud blocking]:** 根據通過測量的欺詐性流量和可疑活動來阻止的站點類型 [!DNL DoubleVerify]。 [!DNL Integral Ad Science], [!DNL Peer39]。 已為新廣告投放選擇廣告商級預設值，但您可以更改以下設定：

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** 預設情況下，會阻止所有100%的無效通信，包括快取設備上的通信，以用於新放置。 可能需要額外收費。

   * **[!UICONTROL Also block sites with]:** （可選）預設情況下會導致阻止廣告的額DSP外欺詐和無效流量：  *[!UICONTROL None]* （預設值，不阻止其他通信）, *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*。 *[!UICONTROL >4% Average Fraud/IVT levels]*。 *[!UICONTROL >6% Average Fraud/IVT levels]*。 *[!UICONTROL >10% Average Fraud/IVT levels]*&#x200B;或 *[!UICONTROL >25% Average Fraud/IVT levels]*。 可能需要額外收費。

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** （可選）預設情況下導致阻止廣告的DSP一種或多種欺詐： *[!UICONTROL Fraud]* （它阻止所有站點存在欺詐） *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*，和 *[!UICONTROL Fraud: Zero Ads]*。 可能需要額外收費。

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** （可選）預設情況下導致阻止廣告的可疑網DSP站或應用活動類型： *[!UICONTROL None]* （預設，不根據可疑活動阻止廣告）, *[!UICONTROL Suspicious Activity - High Risk]*&#x200B;或 *[!UICONTROL Suspicious Activity - High or Moderate Risk]*。 可能需要額外收費。

**[!UICONTROL Ads.txt filtering]:**

哪個級別 [Ads.txt](https://iabtechlab.com/ads-txt-about/) 通過利用每個出版商的授權數字銷售商清單來使用的預報價過濾。 已為新廣告投放選擇廣告商級預設值，但您可以更改以下設定：

* *[!UICONTROL Opt out of ads.txt (default)]*:向所有賣家購買存貨。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*:優先購買域授權直銷商和轉銷商的庫存。
* *[!UICONTROL Ads.txt sellers only]*:僅從域的授權直銷商和轉銷商購買庫存。
* *[!UICONTROL Ads.txt sellers only]*:僅從域的授權直銷商購買庫存。

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** (配置有 [!UICONTROL DoubleVerify Authentic Brand Safety] 選項)啟用 [!DNL DoubleVerify Authentic Brand Safety]，它使用為指定段ID配置的自定義品牌安全規則阻止投標後印象。 為DSP廣告商設定中指定的段ID向帳戶開單以瞭解使用情況。

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] 放置)第三方跟蹤供應商已獲得批准 [!DNL Roku] 包括 [!DNL Acxiom]。 [!DNL comScore]。 [!DNL Data Plus Math]。 [!DNL Experian]。 [!DNL Factual]。 [!DNL Kantar]。 [!DNL Marketing Evolution]。 [!DNL Neustar]。 [!DNL Nielsen]。 [!DNL Nielsen Catalina Solutions]。 [!DNL NinthDecimal]。 [!DNL Oracle]。 [!DNL Placed]。 [!DNL Polk], [!DNL Research Now]。

**[!UICONTROL Event Pixels]:** （可選）預設情況下將附加到放置中所有新廣告的第三方事件跟蹤像素。 要指定事件像素：

1. 按一下 ![編輯](/help/dsp/assets/edit.png)。
1. 執行下列任一操作：
   * 要選擇現有像素，請選中像素行中的複選框。
   * 要建立新像素：
      1. 按一下 **[!UICONTROL Create]**.
      1. 輸入以下資訊：
         * **[!UICONTROL Pixel name]:** 像素名稱；最大長度為500個字元。 使用有助於輕鬆識別像素的名稱。
         * **[!UICONTROL Pixel event fires on]:** 觸發像素觸發的事件。 可用事件因廣告類型而異。
         * **[!UICONTROL Pixel type]:** 像素是否為 *[!UICONTROL IMG URL]* （1x1像素影像檔案）, *[!UICONTROL HTML]*&#x200B;或 *[!UICONTROL JavaScript URL]*。
         * **[!UICONTROL Pixel URL]:** 像素影像的URL。
      1. 按一下 **[!UICONTROL Create and attach]**.
   1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** （可選）預設情況下將附加到放置中所有新廣告的轉換跟蹤像素。 要指定轉換像素：

1. 按一下 ![編輯](/help/dsp/assets/edit.png)。
1. 執行下列任一操作：
   * 要選擇現有像素，請選中像素行中的複選框。
   * 要建立新像素：
      1. 按一下 **[!UICONTROL Create]**.
      1. 輸入以下資訊：
         * **[!UICONTROL Conversion pixel name]:** 像素名稱；最大長度為500個字元。 使用有助於輕鬆識別像素的名稱。
         * **[!UICONTROL Conversion category]:** 轉換類型。
         * **[!UICONTROL Impression conversion window]:** 廣告印象後的天數，其中印象可歸因於轉換。 預設值為30天。
         * **[!UICONTROL Click conversion window]:** 廣告按一下後的天數，在該天數內，按一下可歸屬於轉換。 預設值為30天。
         * **[!UICONTROL Notes]:** （可選）有關像素的說明或其他資訊。
      1. 按一下 **[!UICONTROL Create and attach]**.
      1. 在相關網頁上實現轉換像素：
         1. 在主菜單中，轉到 **[!UICONTROL Resources]>[!UICONTROL Conversion pixels]**。
         1. 在像素行中，按一下 **[!UICONTROL edit]**。
         1. 複製 [!UICONTROL HTML Tag] 和 [!UICONTROL Flash Tag] 欄位，根據需要向廣告商或網站聯繫人提供。

            廣告商的IT部門或其他組可能需要安排標籤部署，或獲得有關標籤部署的資訊。
   1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** （可選）靜態第三方費用率，以每1000個印次的不可計費成本進行跟蹤。 除非輸入其他值，否則在適用時，將自動應用包層預設值來新建放置。

>[!NOTE]
>
>計費費用反映於 [!UICONTROL Net CPM] 度量。

>[!MORELIKETHIS]
>
>* [關於放置管理](placement-about.md)
>* [建立放置](placement-create.md)
>* [編輯放置](placement-edit.md)
>* [鍵盤快捷鍵](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [關於Campaign Management的常見問題](/help/dsp/campaign-management/campaign-management-faq.md)

