---
title: 版位設定
description: 請參閱可用版位設定的說明。
feature: DSP Placements
exl-id: 36097132-e589-4d49-bf86-54f61eae5b67
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '3418'
ht-degree: 0%

---

# 版位設定

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** 版位名稱。

>[!TIP]
>使用對您的情況有意義的命名慣例。 建議的命名慣例是「*\&lt;campaign name=&quot;&quot;>:\&lt;ad unit=&quot;&quot;>:\&lt;duration>:\&lt;targeting>*.&quot;

**[!UICONTROL Status]:** 版位狀態： *[!UICONTROL Active]* （預設）或 *[!UICONTROL Paused]*.

>[!TIP]
>最佳實務是暫停版位，直到您準備好啟動為止。

**[!UICONTROL Details]:** （唯讀）適用的廣告類型、建立或建立版位的帳戶，以及父促銷活動。 若要查看更多詳細資訊，請按一下 **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** 開啟現有版位範本清單。 若要從範本自動填入目標設定：

1. 執行下列任一操作：

   * 要從模板中重複使用所有目標，請選擇模板名稱旁的複選框。

   * 要從模板中重複使用單個目標類型，請展開模板名稱，並選擇要重複使用的目標類型旁邊的複選框。

1. 按一下 **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** （僅限視訊廣告格式）廣告持續時間和/或廣告規格，用於計算右側的「預測」投影。 欄位依廣告類型而異。

**[!UICONTROL Environment]:** （僅限通用視訊廣告格式）要納入作為位置目標的裝置環境（案頭、行動裝置、連線電視）。

**[!UICONTROL Placement tags]:** （可選）可協助您找出此位置的關鍵字或暱稱。

## 目標

**[!UICONTROL Package]:** （可選）分配了版位的包。 按一下 ![編輯](/help/dsp/assets/edit.png) 選擇和現有包或建立新包。 將版位指派給套件時， [!UICONTROL Goals] 小節會更新為包裝的投放日期、交付目標和預算。

**[!UICONTROL Flight Dates]:** 版位的開始日期和結束日期。 當版位處於作用中狀態且指派至作用中的套件或促銷活動時，已核准的廣告有資格在飛行期間執行。

預設會自動填入套件（若適用）或促銷活動的日期。

>[!NOTE]
>
>* 投放日期必須包含在促銷活動投放日期和包裝投放日期中。


### 指派給具有套件層級步調的套件的位置

**[!UICONTROL Placement Funding]:** 如何預算版位：

* *[!UICONTROL Optimize based on performance]:* 控制包級別的預算。
* *[!UICONTROL Set a fixed budget cap]:* 可讓您設定每日、每週、每月或全時版位預算。 輸入值和持續時間(*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*)。

**[!UICONTROL Max Bid]:** 1000次曝光的最高費用。

**[!UICONTROL Placement Pre-bid Filters]:** 最多必須符合五個KPI臨界值（例如最低可見度量或點進率），才能進行競標。 您可以使用出價前篩選器作為最佳化策略，但請了解每個規則都可能限制此版位競標的機會。 若要新增或編輯篩選器：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 執行下列任一操作：
   * 若要新增篩選器：
      1. 按一下 **[!UICONTROL Add Filter]**.
      1. 旁邊 **[!UICONTROL Only bid if]**，請選取量度，然後輸入值。
   * 若要移除篩選器，請按一下 **[!UICONTROL X]** 中。
1. 按一下 **[!UICONTROL Save]**.

請參閱「[版位層級出價前篩選器及其使用方法](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot;

### 所有其他版位

**[!UICONTROL Budget Goal]:** 總預算上限和預算間隔(*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*)。

**[!UICONTROL Gross Budget Goal]:** （僅限使用毛利管理的促銷活動中的刊登版位）總預算上限和預算間隔(*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*)。

**[!UICONTROL Optimization Goal]:**  套件的最佳化目標。 請參閱「[最佳化目標及其使用方式](/help/dsp/optimization/optimization-goals.md)」。

**[!UICONTROL Target Goal]:** 目標目標，用於追蹤效能。

>[!NOTE]
>
>此欄位僅是基準，不用於決策。

**[!UICONTROL Pace on]:** 哪些步調將基於：

* **[!UICONTROL Budget goal]:** （預設）此選項在分配的預算內提供盡可能多的曝光次數。

* **[!UICONTROL Impressions]:** 此選項會傳送曝光次數，直到在指定間隔內達到指定數量為止。 選取此選項時，請指定曝光次數和間隔： *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* 或 *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** 1000次曝光的最高費用。

**[!UICONTROL Flight pacing]:** （僅限具刊登版位層級步調的刊登版位）如何調整廣告投放速度：

* *[!UICONTROL Even]:* （預設值）在每次飛行中以50%的交貨目標均勻地進行交貨。

* *[!UICONTROL Slightly Ahead]:* （預設）加速傳送，使得在飛行期間中途完成55-65%。

* *[!UICONTROL Frontload]:* 加速運送，使得在飛行途中完成65-75%。

* *[!UICONTROL Aggressive Frontload]:* 加速運送，使得75-85%的航班在中途完成。

**[!UICONTROL Intraday pacing]:** （僅限具刊登版位層級步調的刊登版位）如何在飛行中逐日調整廣告投放速度：

* *[!UICONTROL Even]:* （預設）根據庫存可用性調整交貨規模。 一般而言，當拍賣量較高時，白天每小時傳送的廣告數量會較多，而早上和晚上傳送的廣告數量則會較少。

* *[!UICONTROL ASAP]:* （預設）將傳送速度加快至 *平均*.

   >[!CAUTION]
   >
   >此選項可能對效能產生負面影響。 只有在您完全排定傳送的優先順序時才使用它，並且花費在效能最佳化上。

**[!UICONTROL Placement Pre-bid Filters]:** （選用）最多必須符合五個篩選條件，才能進行競標。 您可以使用出價前篩選器作為最佳化策略，但請記住，每個規則都可能限制此版位可出價的機會。 若要新增或編輯篩選器：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 執行下列任一操作：
   * 若要新增篩選器：
      1. 按一下 **[!UICONTROL Add Filter]**.
      1. 旁邊 **[!UICONTROL Only bid if]**，請選取量度，然後輸入值。
   * 若要移除篩選器，請按一下 **[!UICONTROL X]** 中。
1. 按一下 **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** （選用）要在版位中包含或排除廣告的特定位置。 如果您未指定任何位置，則會鎖定所有位置。

>[!NOTE]
>
>城市和DMA位置無法用於Roku位置。

要指定位置：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 執行下列任一操作：
   * 要包括或排除國家、州、市、DMA、聯邦立法區或州立法區，請執行以下操作：
      1. 在左欄中選取位置類型。
      1. （視需要）按一下位置以展開。
      1. 在位置旁，按一下 *[!UICONTROL Include]* 將其納入目標或 *[!UICONTROL Exclude]* 將其排除為目標。
   * 要搜索郵遞區號並包括或排除所有選定結果：
      1. 按一下 **[!UICONTROL Search Postal Code]**.
      1. 選取國家。
      1. 輸入城市名稱，然後按一下 ![編輯](/help/dsp/assets/search.png).
      1. 按一下正確的搜索結果。
      1. 按一下 *[!UICONTROL Include All]* 將所有位置包括為目標或 *[!UICONTROL Exclude All]* 將所有位置排除為目標。
   * 要輸入或貼上郵遞區號，並包括或排除它們，請執行以下操作：
      1. 按一下 **[!UICONTROL Paste Postal Code]**.
      1. 選取國家。
      1. 輸入或貼上最多1000個郵遞區號。
每行包含一個郵遞區號，或輸入多個值（以逗號或分頁分隔）。
      1. 按一下 *[!UICONTROL Include All]* 將所有位置包括為目標或 *[!UICONTROL Exclude All]* 將所有位置排除為目標。
   * 從 [!UICONTROL Included] 或 [!UICONTROL Excluded] 清單，按一下 **[!UICONTROL X]** 位置旁邊。
1. 按一下 **[!UICONTROL Done]**.

>[!NOTE]
>
>* 並非所有國家/地區都有州、市或郵遞區號位置。
>* DMA（指定市場區域）、聯邦立法區和州立法區僅適用於美國地點。


## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** 要包括或排除作為目標的庫存來源。 對於大多數版位類型，預設會包含每種類型的所有庫存類型和所有來源。 針對 [!DNL Roku] 版位，必須指定庫存類型和來源。 您可以從下列庫存類型中選擇：

* [!UICONTROL Public]:（Roku除外的所有版位類型）DSP可存取的所有未結Exchange詳細目錄。 您可以包含和排除公用詳細目錄。

   您可以依來源或摘要來檢視清單。 當您依摘要檢視清單時，可以依摘要名稱、摘要金鑰或選取的特性標籤來搜尋。

* [!UICONTROL Private] | [!UICONTROL Roku Private]:您現有的私人交易（或現有的私人交易） [!DNL Roku] 交易 [!DNL Roku] 版位)與您已在DSP中設定的發佈者。 您可以包含但不能排除公用詳細目錄。

   您可以依關鍵字、索引鍵、交易ID或自訂標籤來搜尋清單。

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]:全部 [溢價，非擔保 [!UICONTROL On Demand] 詳細目錄](/help/dsp/inventory/on-demand-inventory-about.md) (或 [!UICONTROL On Demand] [!DNL] Roku交易 [!DNL Roku] 版位)，您已訂閱 [!DNL DSP]. 您可以包含和排除 [!UICONTROL On Demand] 詳細目錄。

   您可以依來源或摘要來檢視清單。 當您依摘要檢視清單時，可以依摘要名稱、摘要金鑰或選取的發佈者地區、類別標籤或特徵標籤進行搜尋。

要指定庫存目標定位：

* 若要排除庫存類型，請清除名稱旁的核取方塊。
* 要定位庫存類型，請執行以下操作：
   1. 選擇庫存類型名稱旁的複選框。
   1. （可選）將來源變更為包括：
      1. 按一下 ![編輯](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] 和 [!UICONTROL On Demand] 詳細目錄)按一下 *[!UICONTROL *View by Source]**或 **[!UICONTROL View by Feed]** 更改源的列出方式。
      1. （若適用）視需要篩選庫存。
      1. 指定要包括和排除的來源：
         * 若要包含 [!UICONTROL Public] 或 [!UICONTROL On Demand] 源，按一下 **[!UICONTROL Include]** 源名稱旁邊。
         * 要包括 [!UICONTROL Private] 來源：
            * 要在交易中包括所有庫存，請按一下 **[!UICONTROL Include all]** 在交易名稱旁邊。
            * 要包括單個庫存來源，請展開交易名稱，然後按一下來源名稱旁的複選框。
         * 若要排除 [!UICONTROL Public] 或 [!UICONTROL On ] 源，按一下 **[!UICONTROL Exclude]** 源名稱旁邊。
   1. （選用）若要將包含目標定位資訊的CSV檔案下載至瀏覽器的「下載」位置，請按一下 **[!UICONTROL Save & Export]**.
   1. 按一下 **[!UICONTROL Save]**.

>[!TIP]
>
>如果您訂閱 [!UICONTROL On Demand] 清單，但無法找到要定位的發行者或交易，然後檢查交易的狀態。 如需狀態的詳細資訊，請參閱 [關於 [!DNL On Demand] Premium庫存](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** （僅限視訊版位）排除傳出資料流流量。

外流廣告通常在內容上顯示為快顯視窗或填入內容（在原生體驗中），而非視訊播放器中的一般視訊廣告。

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** 要定位的流量類型。 選項包括 **[!UICONTROL Websites]** 和 **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]:** (可於 **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL Off]*)要定位的網站品質。 第1至第3層均為品牌安全，且已由DSP對應團隊審核及核准。

* *[!UICONTROL Tier 1]:* 國家認可的高級站點和應用程式。
* *[!UICONTROL Tier 2]:* 目標是第1層，以及比第1層更不為人所熟知的高質量站點和應用程式。
* *[!UICONTROL Tier 3]:* 鎖定第1至第2層，以及適合特定受眾的合法且品牌安全的網站和應用程式。 使用第3層進行觸及或資料目標鎖定購買。
* *[!UICONTROL All Sites]:* 目標層1-3和尚未篩選或分類的新庫存，您可以用於觸及。

>[!NOTE]
>
>詳細目錄是版位中的廣告單位。

>[!TIP]
>
>對於績效促銷活動，最佳實務是選取 *[!UICONTROL All Sites]*.

**[!UICONTROL Site Categories]:** (可選；可用時間 **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL Off]*)所選網站層級內的網站類別，以包含或排除（但不包括兩者）作為目標。 從DSP已根據網站主旨對應的垂直網站清單中選擇：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 指定要包括或排除的網站類別：
   * 要包括網站類別：
      1. 按一下 **[!UICONTROL Include categories]**.
      1. 選取每個要定位的類別旁的核取方塊。
   * 要排除網站類別：
      1. 按一下 **[!UICONTROL Exclude categories]**.
      1. 選取要排除之每個類別旁的核取方塊。
1. （選用）若要將包含目標定位資訊的CSV檔案下載至瀏覽器的「下載」位置，請按一下 **[!UICONTROL Export]**.
1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** (可選；可用時間 **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL Off]*)要排除的網站。 您可以搜尋和選取網站，或輸入或貼上網域名稱：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 指定網站：
   * 要搜索網站：
      1. 按一下 **[!UICONTROL Search]**.
      1. 輸入關鍵字、選擇站點層，和/或選擇站點類別。
      1. 在搜尋結果中，選取要排除的網站：
         * 若要排除個別網站，請選取其旁的核取方塊。
         * （可用結果超過50個時）若要排除前50個結果，請按一下 **[!UICONTROL Exclude these 50]**. 若要排除所有搜尋結果，請按一下 **[!UICONTROL Exclude these \<*NN *\>]**.
   * 要輸入域名，請執行以下操作：
      1. 按一下 **[!UICONTROL Paste]**.
      1. 在單行上輸入一個或多個域名。
      1. 按一下 **[!UICONTROL Exclude All]**.
1. 按一下 **[!UICONTROL Done]** 等你做完。

>[!NOTE]
>
>* 除了DSP外，也會套用帳戶層級和廣告商層級封鎖的網站清單 [全局阻止的站點清單](/help/dsp/introduction/features/brand-safety-media-quality.md)，包括廣告認為不安全的網站。
>* 被阻止的站點清單始終覆蓋目標站點清單。 如果版位同時排除和包含廣告的相同目標，則會排除該目標。


**[!UICONTROL Language]:** （選用）要定位的單一語言。

**[!UICONTROL Site List Preview]:** （唯讀）用於放置的所有已鎖定和已封鎖的網站。

您可以選擇將目標網站和封鎖網站的清單匯出為逗號分隔值(CSV)檔案。 若要匯出清單，請按一下 **[!UICONTROL Export full site list]**，然後根據瀏覽器的正常程式開啟或儲存檔案。

**[!UICONTROL Allow unscreened sites]:** （僅限標準顯示版位）啟用非稽核網站的廣告傳送。 當版位鎖定私人詳細目錄時，此選項可能會在封鎖的網站上傳送廣告。

**[!UICONTROL Paste list of targeted sites]:** 可讓您僅鎖定特定網站。 啟用此選項後，其他網站定位選項將被禁用。

**[!UICONTROL Sites]:** (可於 **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL On]*)要定位的網站。 您可以搜尋和選取網站，或輸入或貼上網域名稱：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 指定網站：
   * 要搜索網站：
      1. 按一下 **[!UICONTROL Search]**.
      1. 輸入關鍵字、選擇站點層，和/或選擇站點類別。
      1. 在搜尋結果中，選取要包含的網站：
         * 若要排除個別網站，請選取其旁的核取方塊。
         * （可用結果超過50個時）若要納入前50個結果，請按一下 **[!UICONTROL Include these 50]**. 要包括所有搜索結果，請按一下 **[!UICONTROL Include these \<*NN *\>]**.
   * 要輸入域名，請執行以下操作：
      1. 按一下 **[!UICONTROL Paste]**.
      1. 在單行上輸入一個或多個域名。
      1. 按一下 **[!UICONTROL Include All]**.
1. 按一下 **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** 版位的任何對象目標，包括 [協力廠商區段、第一方區段、Adobe區段、自訂區段和已儲存的對象](/help/dsp/audiences/audience-settings.md). 也會顯示所有選取區段和已儲存對象之間去重複化的對象總數與作用中的對象大小。 您可以選取現有對象、建立新對象以供稍後重複使用，或選取特定對象區段：

* 若要選取現有對象，請按一下 ![選擇](/help/dsp/assets/chevron-down.png) 下一頁 [!UICONTROL Included Audiences]，然後選取對象。
* 若要建立新對象，請按一下 ![選擇](/help/dsp/assets/chevron-down.png) 下一頁 [!UICONTROL Included Audiences]，然後選取 **[!UICONTROL + Create Audience]**. 如需指示，請參閱 [建立可重複使用的受眾](/help/dsp/audiences/reusable-audience-create.md)，從步驟3開始。
* 若要選取特定對象區段，請按一下 **[!UICONTROL Select segments for this placement only]**. 選取區段邏輯；如需指示，請參閱[建立可重複使用的受眾](/help/dsp/audiences/reusable-audience-create.md).&quot; 完成後，按一下 **儲存**.

**[!UICONTROL Excluded Audiences]:** 為版位排除的任何對象，包括 [協力廠商區段、第一方區段、Adobe區段、自訂區段和已儲存的對象](/help/dsp/audiences/audience-settings.md). 也會顯示所有已排除對象之已刪除重複的對象總計和作用中大小。 您可以選取現有對象或建立新對象，以便稍後重複使用：

* 若要選取現有對象，請按一下 ![選擇](/help/dsp/assets/chevron-down.png) 下一頁 [!UICONTROL Excluded Audiences]，然後選取對象。
* 若要建立新對象，請按一下 ![選擇](/help/dsp/assets/chevron-down.png) 下一頁 [!UICONTROL Excluded Audiences]，然後選取 **+建立對象**. 如需指示，請參閱 [建立可重複使用的受眾](/help/dsp/audiences/reusable-audience-create.md)，從步驟3開始。

**[!UICONTROL Cross Device Targeting]:** (當您選取至少一個區段或對象時，可用 [已針對以人物為基礎的跨裝置鎖定目標設定促銷活動](/help/dsp/campaign-management/campaigns/campaign-settings.md). 可讓您將目標延伸到所有人員的已知裝置（根據促銷活動設定中指定的裝置圖表），甚至不在指定區段的裝置。 視為促銷活動指定的圖表而定，可能需支付費用。 裝置圖表資料目前僅在北美地區提供。

**[!UICONTROL Placement Cap]:** （選用）不重複裝置或人員的次數(取決於指定 [!UICONTROL Cross Device Level] （針對促銷活動）將從版位提供廣告。 選項包括 *[!UICONTROL Unlimited]* 或每天、每週或每月的特定數量。

>[!NOTE]
>
> 您可以在促銷活動、封裝和位置層級設定頻率上限。 DSP將遵循促銷活動階層中最嚴格的頻率上限。

**[!UICONTROL Secondary Cap]:** (可選；包含數值時可用 [!UICONTROL Placement Cap])主要放置上限範圍內的其他限制。 選取曝光次數和時段（例如每12小時3次）。

**[!UICONTROL Day Parting]:** （選用）廣告可能執行的一週特定天數和一天中的時間。 要指定時段間隔：
1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 選取適用的時區。
1. 指定間隔：
   * 要選擇預設間隔，請按一下其中一個間隔按鈕。 選項包括*[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]*，或 *[!UICONTROL Prime]* (primetime)。
   * 若要手動選取間隔，請在儲存格內按一下，並可選擇拖曳以選取間隔。
1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (可選；可用於配置有 [!DNL Comscore] 和 [!DNL Grapeshot] 區段)特定區段名稱或ID [!DNL Comscore] 和 [!DNL Grapeshot] 包含作為目標。 此功能可能需額外付費。 若要啟用此功能並設定主題區段，請連絡您的 [!DNL Adobe] 客戶團隊。

要指定主題目標定位：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 指定要定位的區段：
   1. 在左欄中，選取合作夥伴(*[!UICONTROL Comscore]* 或 *[!UICONTROL Grapeshot]*)。
   1. 在輸入欄位中，輸入區段名稱或區段ID。
1. （選用）若要將包含主題資訊的CSV檔案下載至瀏覽器的「下載」位置，請按一下 **[!UICONTROL Export]**.
1. 按一下 **[!UICONTROL Save]**.

>[!TIP]
>
>* 主題目標定位會限製版位可競標的詳細目錄，因此，主題目標定位只適用於整體購買的一小部分。
>
>* 在上的區段內設定任何負面定位 [!DNL Comscore] 或 [!DNL Grapeshot].


**[!UICONTROL Device Targeting]:** （可選）要包括和排除作為目標的特定裝置資訊，包括裝置類型、製造商、作業系統、瀏覽器和連接類型。 要指定設備目標定位：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 指定要包含和排除的裝置詳細資訊：
   1. 在左欄中，選取類別。
   1. 指定目標：
      * 若要包含值，請按一下 **[!UICONTROL Include]** 值名稱旁。
      * 若要排除值，請按一下 **[!UICONTROL Exclude]** 值名稱旁。
1. （選用）若要將含有裝置定位資訊的CSV檔案下載至瀏覽器的「下載」位置，請按一下 **[!UICONTROL Export]**.
1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** （可選）特定網際網路服務提供者(ISP)，可納入或排除（但不包括兩者）作為目標。 要指定ISP目標：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 指定要包含或排除的ISP:
   * 要包括ISP:
      1. 按一下 **[!UICONTROL Include ISPs]**.
      1. （選用）依關鍵字篩選清單。
      1. 選取要鎖定的每個ISP旁的核取方塊。
   * 若要排除ISP:
      1. 按一下 **[!UICONTROL Exclude ISPs]**.
      1. （選用）依關鍵字篩選清單。
      1. 選取要排除的每個ISP旁的核取方塊。
1. （選用）若要下載CSV檔案（其中包含ISP目標定位資訊）至瀏覽器的「下載」位置，請按一下 **[!UICONTROL Export]**.
1. 按一下 **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** 類型 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]，和 [!DNL Peer39] 要套用的內容篩選。 系統會為新版位選取廣告商層級的預設值，但您可以變更設定：

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** （可選）預設要封鎖的一或多種庫存內容類型。 可能需支付額外費用。

* [!UICONTROL Peer 39]:

   * **目標站點包括：** （可選）預設要定位的一或多種庫存屬性類型。 可能需支付額外費用。

* [!UICONTROL ComScore]:

   * **阻止以下站點：** （可選）預設要封鎖的一或多種庫存屬性類型。 可能需支付額外費用。

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** （可選）預設要封鎖廣告的成人內容程度： *[!UICONTROL Do Not Block]* （預設）、 *[!UICONTROL Standard]*，或 *[!UICONTROL Strict]*. 可能需支付額外費用。

   * **[!UICONTROL Alcohol Content]:** （可選）預設要封鎖廣告的酒精含量程度： *[!UICONTROL Do Not Block]* （預設）、 *[!UICONTROL Standard]*，或 *[!UICONTROL Strict]*. 可能需支付額外費用。

**[!UICONTROL Pre-bid fraud blocking]:** 根據欺詐性流量和通過 [!DNL DoubleVerify], [!DNL Integral Ad Science]，和 [!DNL Peer39]. 系統會為新版位選取廣告商層級的預設值，但您可以變更設定：

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** 依預設，會封鎖所有100%無效流量，包括高位裝置上的新版位流量。 可能需支付額外費用。

   * **[!UICONTROL Also block sites with]:** （選用）預設情況下，會導致DSP封鎖廣告的額外欺詐和無效流量：  *[!UICONTROL None]* （預設值，不會封鎖其他流量）, *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*，或 *[!UICONTROL >25% Average Fraud/IVT levels]*. 可能需支付額外費用。

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** （選用）依預設會導致DSP封鎖廣告的一或多種欺詐類型： *[!UICONTROL Fraud]* （會以欺詐方式阻止所有網站）, *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*，和/或 *[!UICONTROL Fraud: Zero Ads]*. 可能需支付額外費用。

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** （可選）預設導致DSP封鎖廣告的可疑網站或應用程式活動類型： *[!UICONTROL None]* （預設值，不會根據可疑活動封鎖廣告）, *[!UICONTROL Suspicious Activity - High Risk]*，或 *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. 可能需支付額外費用。

**[!UICONTROL Ads.txt filtering]:**

哪一級 [Ads.txt](https://iabtechlab.com/ads-txt-about/) 透過運用每個發行者的「已授權數位賣家」清單來預先出價篩選。 系統會為新版位選取廣告商層級的預設值，但您可以變更設定：

* *[!UICONTROL Opt out of ads.txt (default)]*:向所有賣家購買庫存。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*:優先購買域授權的直銷商和經銷商的庫存。
* *[!UICONTROL Ads.txt sellers only]*:僅向域授權的直銷商和經銷商購買庫存。
* *[!UICONTROL Ads.txt sellers only]*:僅向域的授權直銷商購買庫存。

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** (以 [!UICONTROL DoubleVerify Authentic Brand Safety] 選項)啟用 [!DNL DoubleVerify Authentic Brand Safety]，這會使用為指定區段ID設定的自訂品牌安全規則來封鎖出價後曝光數。 DSP會向您收取帳戶，以了解在廣告商設定中指定之區段ID的使用情形。

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] 版位)經第三方追蹤廠商核准 [!DNL Roku] 包括 [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]，和 [!DNL Research Now].

**[!UICONTROL Event Pixels]:** （選用）依預設會附加至版位中所有新廣告的第三方事件追蹤像素。 若要指定事件像素：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 執行下列任一操作：
   * 若要選取現有像素，請選取像素列中的核取方塊。
   * 若要建立新像素：
      1. 按一下 **[!UICONTROL Create]**.
      1. 輸入以下資訊：
         * **[!UICONTROL Pixel name]:** 像素名稱；長度上限為500個字元。 使用可協助您輕鬆識別像素的名稱。
         * **[!UICONTROL Pixel event fires on]:** 觸發像素的事件。 可用事件會依廣告類型而異。
         * **[!UICONTROL Pixel type]:** 像素是否為 *[!UICONTROL IMG URL]* （1x1像素影像檔案）, *[!UICONTROL HTML]*，或 *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** 像素影像的URL。
      1. 按一下 **[!UICONTROL Create and attach]**.
   1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** （選用）轉換追蹤像素，預設會附加至版位中的所有新廣告。 若要指定轉換像素：

1. 按一下 ![編輯](/help/dsp/assets/edit.png).
1. 執行下列任一操作：
   * 若要選取現有像素，請選取像素列中的核取方塊。
   * 若要建立新像素：
      1. 按一下 **[!UICONTROL Create]**.
      1. 輸入以下資訊：
         * **[!UICONTROL Conversion pixel name]:** 像素名稱；長度上限為500個字元。 使用可協助您輕鬆識別像素的名稱。
         * **[!UICONTROL Conversion category]:** 轉換的類型。
         * **[!UICONTROL Impression conversion window]:** 廣告曝光發生後的天數，可將曝光歸因於轉換。 預設為30天。
         * **[!UICONTROL Click conversion window]:** 廣告點按發生後的天數，點按可歸因於轉換。 預設為30天。
         * **[!UICONTROL Notes]:** （可選）像素的說明或其他資訊。
      1. 按一下 **[!UICONTROL Create and attach]**.
      1. 在相關網頁上實作轉換像素：
         1. 在主功能表中，前往 **[!UICONTROL Resources]>[!UICONTROL Conversion pixels]**.
         1. 在像素列中，按一下 **[!UICONTROL edit]**.
         1. 複製 [!UICONTROL HTML Tag] 和 [!UICONTROL Flash Tag] 欄位，以提供給廣告商或網站連絡人。

            廣告商的IT部門或其他群組可能需要排程標籤部署，或接收相關通知。
   1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** （選用）靜態的第三方費用率，以每1000次曝光的不計費成本來追蹤。 除非您輸入不同值，否則新版位會自動套用套件層級預設值（若適用）。

>[!NOTE]
>
>可結算費用反映於 [!UICONTROL Net CPM] 量度。

>[!MORELIKETHIS]
>
>* [關於版位管理](placement-about.md)
>* [建立版位](placement-create.md)
>* [編輯位置](placement-edit.md)
>* [查看版位的更改日誌](placement-change-log.md)
>* [鍵盤快速鍵](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Campaign Management常見問題集](/help/dsp/campaign-management/campaign-management-faq.md)

