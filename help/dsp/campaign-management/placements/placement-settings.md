---
title: 版位設定
description: 請參閱可用版位設定的說明。
feature: DSP Placements
exl-id: 36097132-e589-4d49-bf86-54f61eae5b67
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '3281'
ht-degree: 0%

---

# 版位設定

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** 版位名稱。

>[!TIP]
>使用對您的情況有意義的命名慣例。 建議的命名慣例是&quot;*\&lt;促銷活動名稱\>:\&lt;廣告單元\>:\&lt;持續時間\>:\&lt;目標定位\>*.&quot;

**[!UICONTROL Status]:** 版位狀態： *[!UICONTROL Active]* （預設值）或 *[!UICONTROL Paused]*。

>[!TIP]
>最佳實務是暫停版位，直到您準備好啟動為止。

**[!UICONTROL Details]:** （唯讀）適用的廣告類型、建立或建立版位的帳戶，以及父促銷活動。要查看更多詳細資訊，請按一下&#x200B;**[!UICONTROL Show more]**。

**[!UICONTROL Templates]:** 開啟現有版位範本清單。若要從範本自動填入目標設定：

1. 執行下列任一操作：

   * 要從模板中重複使用所有目標，請選擇模板名稱旁的複選框。

   * 要從模板中重複使用單個目標類型，請展開模板名稱，並選擇要重複使用的目標類型旁邊的複選框。

1. 按一下 **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** （僅限視訊廣告格式）廣告持續時間和/或廣告規格，用於計算右側的「預測」投影。欄位依廣告類型而異。

**[!UICONTROL Placement tags]:** （選用）可協助您找出此位置的關鍵字或暱稱。

## 目標

**[!UICONTROL Package]:** （選用）指派位置的套件。按一下![編輯](/help/dsp/assets/edit.png)以選擇和現有包或建立新包。 將投放位置分配給包時，[!UICONTROL Goals]部分將更新為包的投放日期、投放目標和預算。

**[!UICONTROL Flight Dates]:** 版位的開始日期和結束日期。當版位處於作用中狀態且指派至作用中的套件或促銷活動時，已核准的廣告有資格在飛行期間執行。

預設會自動填入套件（若適用）或促銷活動的日期。

>[!NOTE]
>
>* 投放日期必須包含在促銷活動投放日期和包裝投放日期中。


### 指派給具有套件層級步調的套件的位置

**[!UICONTROL Placement Funding]:** 如何為版位預算：

* *[!UICONTROL Optimize based on performance]:* 控制包層的預算。
* *[!UICONTROL Set a fixed budget cap]:* 可讓您設定每日、每週、每月或所有時間的版位預算。輸入值和持續時間(*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*)。

**[!UICONTROL Max Bid]:** 最多需要支付1000次曝光數。

**[!UICONTROL Placement Pre-bid Filters]:** 最多5個KPI臨界值（例如最低可見度量或點進率）必須符合，才會進行競標。您可以使用出價前篩選器作為最佳化策略，但請了解每個規則都可能限制此版位競標的機會。 若要新增或編輯篩選器：

1. 按一下「![編輯](/help/dsp/assets/edit.png)」。
1. 執行下列任一操作：
   * 若要新增篩選器：
      1. 按一下 **[!UICONTROL Add Filter]**.
      1. 在&#x200B;**[!UICONTROL Only bid if]**&#x200B;旁，選取量度，然後輸入值。
   * 若要移除篩選器，請按一下篩選器列中的&#x200B;**[!UICONTROL X]**。
1. 按一下 **[!UICONTROL Save]**.

請參閱「[版位層級預先競價篩選及如何使用](/help/dsp/optimization/optimization-pre-bid-filters.md)」中每個預先競價篩選的說明。

### 所有其他版位

**[!UICONTROL Budget Goal]:** 預算總額上限和預算間隔(*[!UICONTROL All time]*、 *[!UICONTROL Daily]*、 *[!UICONTROL Weekly]*、 *[!UICONTROL Monthly]*)。

**[!UICONTROL Gross Budget Goal]:** （僅限使用毛利管理的促銷活動中的刊登版位）總預算上限和預算間隔(*[!UICONTROL All time]*、 *[!UICONTROL Daily]*、 *[!UICONTROL Weekly]*、 *[!UICONTROL Monthly]*)。

**[!UICONTROL Optimization Goal]:**  套件的最佳化目標。請參閱「[最佳化目標及如何使用](/help/dsp/optimization/optimization-goals.md)」中每個最佳化目標的說明。

**[!UICONTROL Target Goal]:** 用於追蹤效能的目標目標。

>[!NOTE]
>
>此欄位僅是基準，不用於決策。

**[!UICONTROL Pace on]:** 步調將以下各項為基礎：

* **[!UICONTROL Budget goal]:** （預設）此選項在分配的預算內提供盡可能多的曝光次數。

* **[!UICONTROL Impressions]:** 此選項會傳送曝光數，直到在指定間隔內達到指定數量為止。選取此選項時，請指定曝光次數和間隔：*[!UICONTROL All time]、* *[!UICONTROL Daily]、* *[!UICONTROL Monthly]、*&#x200B;或&#x200B;*[!UICONTROL Weekly]*。

**[!UICONTROL Max Bid]:** 最多需要支付1000次曝光數。

**[!UICONTROL Pacing Fill Strategy]:** （僅具有套件層級步調的套件）如何調整廣告投放速度：

* *[!UICONTROL Even]:* （預設值）在每次飛行中以50%的傳送目標均勻地進行傳送。

* *[!UICONTROL Frontload]:* 加速運送，使其在飛行途中完成65-75%。

* *[!UICONTROL Aggressive Frontload]:* 加速運送，使得75-85%的運送在中途完成。

**[!UICONTROL Placement Pre-bid Filters]:** （選用）最多必須符合五個篩選條件，才會發生競標。您可以使用出價前篩選器作為最佳化策略，但請記住，每個規則都可能限制此版位可出價的機會。 若要新增或編輯篩選器：

1. 按一下「![編輯](/help/dsp/assets/edit.png)」。
1. 執行下列任一操作：
   * 若要新增篩選器：
      1. 按一下 **[!UICONTROL Add Filter]**.
      1. 在&#x200B;**[!UICONTROL Only bid if]**&#x200B;旁，選取量度，然後輸入值。
   * 若要移除篩選器，請按一下篩選器列中的&#x200B;**[!UICONTROL X]**。
1. 按一下 **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** （選用）要在版位中包含或排除廣告的特定位置。如果您未指定任何位置，則會鎖定所有位置。

>[!NOTE]
>
>城市和DMA位置無法用於Roku位置。

要指定位置：

1. 按一下「![編輯](/help/dsp/assets/edit.png)」。
1. 執行下列任一操作：
   * 要包括或排除國家、州、市、DMA、聯邦立法區或州立法區，請執行以下操作：
      1. 在左欄中選取位置類型。
      1. （視需要）按一下位置以展開。
      1. 在位置旁，按一下&#x200B;*[!UICONTROL Include]*&#x200B;將其納入為目標，或按一下&#x200B;*[!UICONTROL Exclude]*&#x200B;將其排除為目標。
   * 要搜索郵遞區號並包括或排除所有選定結果：
      1. 按一下 **[!UICONTROL Search Postal Code]**.
      1. 選取國家。
      1. 輸入城市名稱，然後按一下「![編輯](/help/dsp/assets/search.png)」。
      1. 按一下正確的搜索結果。
      1. 按一下&#x200B;*[!UICONTROL Include All]*&#x200B;將所有位置納入目標，或按一下&#x200B;*[!UICONTROL Exclude All]*&#x200B;將所有位置排除為目標。
   * 要輸入或貼上郵遞區號，並包括或排除它們，請執行以下操作：
      1. 按一下 **[!UICONTROL Paste Postal Code]**.
      1. 選取國家。
      1. 輸入或貼上最多1000個郵遞區號。
每行包含一個郵遞區號，或輸入多個值（以逗號或分頁分隔）。
      1. 按一下&#x200B;*[!UICONTROL Include All]*&#x200B;將所有位置納入目標，或按一下&#x200B;*[!UICONTROL Exclude All]*&#x200B;將所有位置排除為目標。
   * 要從[!UICONTROL Included]或[!UICONTROL Excluded]清單中刪除位置，請按一下右列中位置旁邊的&#x200B;**[!UICONTROL X]**。
1. 按一下 **[!UICONTROL Done]**.

>[!NOTE]
>
>* 並非所有國家/地區都有州、市或郵遞區號位置。
>* DMA（指定市場區域）、聯邦立法區和州立法區僅適用於美國地點。


## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** 要包含或排除作為目標的庫存來源。對於大多數版位類型，預設會包含每種類型的所有庫存類型和所有來源。 對於[!DNL Roku]版位，必須指定庫存類型和來源。 您可以從下列庫存類型中選擇：

* [!UICONTROL Public]:（Roku除外的所有版位類型）Advertising Cloud可存取的所有未結Exchange詳細目錄。您可以包含和排除公用詳細目錄。

   您可以依來源或摘要來檢視清單。 當您依摘要檢視清單時，可以依摘要名稱、摘要金鑰或選取的特性標籤來搜尋。

* [!UICONTROL Private] |  [!UICONTROL Roku Private]:您與已在DSP中設定的發 [!DNL Roku] 布商 [!DNL Roku] 的現有私人交易（或現有的刊登版位私人交易）。您可以包含但不能排除公用詳細目錄。

   您可以依關鍵字、索引鍵、交易ID或自訂標籤來搜尋清單。

* [!UICONTROL On Demand] |  [!UICONTROL Roku On Demand]:您 [已訂閱的所 [!UICONTROL On Demand] 有優質、非保](/help/dsp/inventory/on-demand-inventory-about.md) 證存貨 [!UICONTROL On Demand] [!DNL] (或 [!DNL Roku] Roku針對配售進行交易) [!DNL DSP]。您可以包含和排除[!UICONTROL On Demand]庫存。

   您可以依來源或摘要來檢視清單。 當您依摘要檢視清單時，可以依摘要名稱、摘要金鑰或選取的發佈者地區、類別標籤或特徵標籤進行搜尋。

要指定庫存目標定位：

* 若要排除庫存類型，請清除名稱旁的核取方塊。
* 要定位庫存類型，請執行以下操作：
   1. 選擇庫存類型名稱旁的複選框。
   1. （可選）將來源變更為包括：
      1. 按一下「![編輯](/help/dsp/assets/edit.png)」。
      1. （[!UICONTROL Public]和[!UICONTROL On Demand]詳細目錄）按一下&#x200B;*[!UICONTROL *View by Source]**或&#x200B;**[!UICONTROL View by Feed]**&#x200B;以變更來源的列出方式。
      1. （若適用）視需要篩選庫存。
      1. 指定要包括和排除的來源：
         * 要包括[!UICONTROL Public]或[!UICONTROL On Demand]源，請按一下源名稱旁的&#x200B;**[!UICONTROL Include]**。
         * 要包含[!UICONTROL Private]源，請執行以下操作：
            * 要在交易中包括所有庫存，請按一下交易名稱旁的&#x200B;**[!UICONTROL Include all]**。
            * 要包括單個庫存來源，請展開交易名稱，然後按一下來源名稱旁的複選框。
         * 要排除[!UICONTROL Public]或[!UICONTROL On ]源，請按一下源名稱旁的&#x200B;**[!UICONTROL Exclude]**。
   1. （選用）若要將包含目標定位資訊的CSV檔案下載至瀏覽器的「下載」位置，請按一下「**[!UICONTROL Save & Export]**」。
   1. 按一下 **[!UICONTROL Save]**.

>[!TIP]
>
>如果您訂閱[!UICONTROL On Demand]詳細目錄，但找不到要鎖定的發行者或交易，請檢查交易狀態。 有關狀態的詳細資訊，請參閱[關於 [!DNL On Demand] Premium Inventory](/help/dsp/inventory/on-demand-inventory-about.md)。

**[!UICONTROL Exclude out-stream]:** （僅限視訊版位）排除傳出資料流流量。

外流廣告通常在內容上顯示為快顯視窗或填入內容（在原生體驗中），而非視訊播放器中的一般視訊廣告。

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** 要定位的流量類型。選項包括&#x200B;**[!UICONTROL Websites]**&#x200B;和&#x200B;**[!UICONTROL Apps]**。

**[!UICONTROL Site tier]:** (適 **[!UICONTROL Paste list of targeted sites]** 用於 *[!UICONTROL Off]*&#x200B;時)要定位的網站品質。第1至第3層均為品牌安全，且已由DSP對應團隊審核及核准。

* *[!UICONTROL Tier 1]:* 國家認可的進階網站和應用程式。
* *[!UICONTROL Tier 2]:* 目標是第1層，以及比第1層更不為人所熟知的優質站點和應用程式。
* *[!UICONTROL Tier 3]:* 鎖定第1層至第2層，以及適合特定受眾的合法且品牌安全的網站和應用程式。使用第3層進行觸及或資料目標鎖定購買。
* *[!UICONTROL All Sites]:* 定位尚未篩選或分類的第1至第3層和新庫存，您可將其用於觸及。

>[!NOTE]
>
>詳細目錄是版位中的廣告單位。

>[!TIP]
>
>對於績效促銷活動，最佳實務是選取&#x200B;*[!UICONTROL All Sites]*。

**[!UICONTROL Site Categories]:** (選用；當是 **[!UICONTROL Paste list of targeted sites]** 時可 *[!UICONTROL Off]*&#x200B;用)所選網站層級內的網站類別，以包含或排除（但不包括兩者）作為目標。從Advertising Cloud已根據網站主旨對應的垂直網站清單中選擇：

1. 按一下「![編輯](/help/dsp/assets/edit.png)」。
1. 指定要包括或排除的網站類別：
   * 要包括網站類別：
      1. 按一下 **[!UICONTROL Include categories]**.
      1. 選取每個要定位的類別旁的核取方塊。
   * 要排除網站類別：
      1. 按一下 **[!UICONTROL Exclude categories]**.
      1. 選取要排除之每個類別旁的核取方塊。
1. （選用）若要將包含目標定位資訊的CSV檔案下載至瀏覽器的「下載」位置，請按一下「**[!UICONTROL Export]**」。
1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** (選用；可在 **[!UICONTROL Paste list of targeted sites]** 時 *[!UICONTROL Off]*&#x200B;使用)要排除的網站。您可以搜尋和選取網站，或輸入或貼上網域名稱：

1. 按一下「![編輯](/help/dsp/assets/edit.png)」。
1. 指定網站：
   * 要搜索網站：
      1. 按一下 **[!UICONTROL Search]**.
      1. 輸入關鍵字、選擇站點層，和/或選擇站點類別。
      1. 在搜尋結果中，選取要排除的網站：
         * 若要排除個別網站，請選取其旁的核取方塊。
         * （可用結果超過50個時）若要排除前50個結果，請按一下「**[!UICONTROL Exclude these 50]**」。 若要排除所有搜尋結果，請按一下「**[!UICONTROL Exclude these \<*NN *\>]**」。
   * 要輸入域名，請執行以下操作：
      1. 按一下 **[!UICONTROL Paste]**.
      1. 在單行上輸入一個或多個域名。
      1. 按一下 **[!UICONTROL Exclude All]**.
1. 完成後，按一下&#x200B;**[!UICONTROL Done]**。

>[!NOTE]
>
>* 除了Advertising Cloud DSP [全域封鎖的網站清單](/help/dsp/introduction/features/brand-safety-media-quality.md)外，也會套用帳戶層級和廣告商層級封鎖的網站清單，其中包含廣告認為不安全的網站。
>* 被阻止的站點清單始終覆蓋目標站點清單。 如果版位同時排除和包含廣告的相同目標，則會排除該目標。


**[!UICONTROL Language]:** （選用）要定位的單一語言。

**[!UICONTROL Site List Preview]:** （唯讀）此位置的所有已鎖定和已封鎖的網站。

您可以選擇將目標網站和封鎖網站的清單匯出為逗號分隔值(CSV)檔案。 要導出清單，請按一下&#x200B;**[!UICONTROL Export full site list]**，然後根據瀏覽器的常規過程開啟或保存該檔案。

<!-- **[!UICONTROL Allow unscreened sites]:** (XXX placements only) Allows you to XXXX.   Optional available for https://advertising.adobe.com/configurator/placement/edit/2432022 -->

**[!UICONTROL Paste list of targeted sites]:** 可讓您僅鎖定特定網站。啟用此選項後，其他網站定位選項將被禁用。

**[!UICONTROL Sites]:** (在 **[!UICONTROL Paste list of targeted sites]** 時 *[!UICONTROL On]*&#x200B;可用)要定位的網站。您可以搜尋和選取網站，或輸入或貼上網域名稱：

1. 按一下「![編輯](/help/dsp/assets/edit.png)」。
1. 指定網站：
   * 要搜索網站：
      1. 按一下 **[!UICONTROL Search]**.
      1. 輸入關鍵字、選擇站點層，和/或選擇站點類別。
      1. 在搜尋結果中，選取要包含的網站：
         * 若要排除個別網站，請選取其旁的核取方塊。
         * （可用結果超過50個時）若要納入前50個結果，請按一下「**[!UICONTROL Include these 50]**」。 要包括所有搜索結果，請按一下&#x200B;**[!UICONTROL Include these \<*NN *\>]**。
   * 要輸入域名，請執行以下操作：
      1. 按一下&#x200B;**[!UICONTROL Paste]**。
      1. 在單行上輸入一個或多個域名。
      1. 按一下 **[!UICONTROL Include All]**.
1. 按一下 **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** 版位的任何對象目標，包 [括第三方區段、第一方區段、Adobe區段、自訂區段和已儲存的對象](/help/dsp/audiences/audience-settings.md)。也會顯示所有選取區段和已儲存對象之間去重複化的對象總數與作用中的對象大小。 您可以選取現有對象、建立新對象以供稍後重複使用，或選取特定對象區段：

* 若要選取現有對象，請按一下![選取[!UICONTROL Included Audiences]旁的](/help/dsp/assets/chevron-down.png)，然後選取對象。
* 若要建立新對象，請按一下![選取[!UICONTROL Included Audiences]旁的](/help/dsp/assets/chevron-down.png)，然後選取&#x200B;**[!UICONTROL + Create Audience]**。 如需相關指示，請參閱從步驟3開始的[建立可重複使用的對象](/help/dsp/audiences/reusable-audience-create.md)。
* 若要選取特定對象區段，請按一下&#x200B;**[!UICONTROL Select segments for this placement only]**。 選取區段邏輯；如需指示，請參閱「[建立可重複使用的對象](/help/dsp/audiences/reusable-audience-create.md)」中的步驟6。 完成後，按一下&#x200B;**Save**。

**[!UICONTROL Excluded Audiences]:** 為版位排除的任何對象，包括具有第 [三方區段、第一方區段、Adobe區段、自訂區段和已儲存對象的對象](/help/dsp/audiences/audience-settings.md)。也會顯示所有已排除對象之已刪除重複的對象總計和作用中大小。 您可以選取現有對象或建立新對象，以便稍後重複使用：

* 若要選取現有對象，請按一下![選取[!UICONTROL Excluded Audiences]旁的](/help/dsp/assets/chevron-down.png)，然後選取對象。
* 若要建立新受眾，請按一下![選取[!UICONTROL Excluded Audiences]旁的](/help/dsp/assets/chevron-down.png)，然後選取&#x200B;**+建立受眾**。 如需相關指示，請參閱從步驟3開始的[建立可重複使用的對象](/help/dsp/audiences/reusable-audience-create.md)。

**[!UICONTROL Cross Device Targeting]:** (當您至少選取一個區段或對象，且促銷活 [動已設定為以人物為基礎的跨裝置鎖定目標時可用](/help/dsp/campaign-management/campaigns/campaign-settings.md)。可讓您將目標延伸到所有人員的已知裝置（根據促銷活動設定中指定的裝置圖表），甚至不在指定區段的裝置。 視為促銷活動指定的圖表而定，可能需支付費用。 裝置圖表資料目前僅在北美地區提供。

**[!UICONTROL Placement Cap]:** （選用）從版位向不重複裝置或人員(視指 [!UICONTROL Cross Device Level]定而定)提供廣告的次數。選項包括&#x200B;*[!UICONTROL Unlimited]*&#x200B;或每天、每週或每月的特定數量。

>[!NOTE]
>
> 您可以在促銷活動、封裝和位置層級設定頻率上限。 DSP將遵循促銷活動階層中最嚴格的頻率上限。

**[!UICONTROL Secondary Cap]:** (選用；包含數值時可用) [!UICONTROL Placement Cap]主要放置上限範圍內的其他限制。選取曝光次數和時段（例如每12小時3次）。

**[!UICONTROL Day Parting]:** （選用）一週中的特定天數，以及可執行廣告的一天中的時間。要指定時段間隔：
1. 按一下「![編輯](/help/dsp/assets/edit.png)」。
1. 選取適用的時區。
1. 指定間隔：
   * 要選擇預設間隔，請按一下其中一個間隔按鈕。 選項包括*[!UICONTROL Weekends]**、*[!UICONTROL Weekdays]*、*[!UICONTROL Morning]*、*[!UICONTROL Lunch]*、*[!UICONTROL Dinner]*&#x200B;或&#x200B;*[!UICONTROL Prime]*（黃金時段）。
   * 若要手動選取間隔，請在儲存格內按一下，並可選擇拖曳以選取間隔。
1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (選用；可供設定了和區 [!DNL Comscore] 段的廣 [!DNL Grapeshot] 告商使用)來自和的特定區段名稱 [!DNL Comscore] 或ID, [!DNL Grapeshot] 以包含作為目標。此功能可能需額外付費。 若要啟用此功能並設定主題區段，請連絡您的Adobe客戶經理。

要指定主題目標定位：

1. 按一下「![編輯](/help/dsp/assets/edit.png)」。
1. 指定要定位的區段：
   1. 在左欄中，選取合作夥伴（*[!UICONTROL Comscore]*&#x200B;或&#x200B;*[!UICONTROL Grapeshot]*）。
   1. 在輸入欄位中，輸入區段名稱或區段ID。
1. （選用）若要將包含主題資訊的CSV檔案下載至瀏覽器的「下載」位置，請按一下「**[!UICONTROL Export]**」。
1. 按一下 **[!UICONTROL Save]**.

>[!TIP]
>
>* 主題鎖定目標會限製版位可競標的詳細目錄，因此，主題鎖定目標只適用於整體購買的一小部分。
>
>* 在[!DNL Comscore]或[!DNL Grapeshot]的區段內設定任何負定位。


**[!UICONTROL Device Targeting]:** （選用）要納入和排除作為目標的特定裝置資訊，包括裝置類型、製造商、作業系統、瀏覽器和連線類型。要指定設備目標定位：

1. 按一下「![編輯](/help/dsp/assets/edit.png)」。
1. 指定要包含和排除的裝置詳細資訊：
   1. 在左欄中，選取類別。
   1. 指定目標：
      * 若要包含值，請按一下值名稱旁的&#x200B;**[!UICONTROL Include]**。
      * 若要排除值，請按一下值名稱旁的&#x200B;**[!UICONTROL Exclude]**。
1. （選用）若要將含有裝置定位資訊的CSV檔案下載至瀏覽器的「下載」位置，請按一下「**[!UICONTROL Export]**」。
1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** （選用）要納入或排除（但不能同時包括和排除）的特定網際網路服務提供者(ISP)作為目標。要指定ISP目標：

1. 按一下「![編輯](/help/dsp/assets/edit.png)」。
1. 指定要包含或排除的ISP:
   * 要包括ISP:
      1. 按一下 **[!UICONTROL Include ISPs]**.
      1. （選用）依關鍵字篩選清單。
      1. 選取要鎖定的每個ISP旁的核取方塊。
   * 若要排除ISP:
      1. 按一下 **[!UICONTROL Exclude ISPs]**.
      1. （選用）依關鍵字篩選清單。
      1. 選取要排除的每個ISP旁的核取方塊。
1. （可選）若要將含有ISP目標定位資訊的CSV檔案下載至瀏覽器的「下載」位置，請按一下「**[!UICONTROL Export]**」。
1. 按一下 **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** 要套用的 [!DNL Comscore]、 [!DNL DoubleVerify]、 [!DNL Integral Ad Science]和內 [!DNL Peer39] 容篩選類型。系統會為新版位選取廣告商層級的預設值，但您可以變更設定：

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** （選用）預設要封鎖的一或多種庫存內容類型。可能需支付額外費用。

* [!UICONTROL Peer 39]:

   * **目標網站為：** （選用）預設要定位的一或多種庫存屬性類型。可能需支付額外費用。

* [!UICONTROL ComScore]:

   * **封鎖網站：** （選用）預設要封鎖的一或多種庫存屬性類型。可能需支付額外費用。

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** （選用）預設要封鎖廣告的成人內容程度： *[!UICONTROL Do Not Block]* （預設）、  *[!UICONTROL Standard]*&#x200B;或 *[!UICONTROL Strict]*。可能需支付額外費用。

   * **[!UICONTROL Alcohol Content]:** （選用）依預設要封鎖廣告的酒精含量程度： *[!UICONTROL Do Not Block]* （預設）、  *[!UICONTROL Standard]*&#x200B;或 *[!UICONTROL Strict]*。可能需支付額外費用。

**[!UICONTROL Pre-bid fraud blocking]:** 根據透過、和測量的欺詐性流量和可疑活動而封鎖 [!DNL DoubleVerify]的 [!DNL Integral Ad Science]網站類 [!DNL Peer39]型。系統會為新版位選取廣告商層級的預設值，但您可以變更設定：

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** 依預設，會封鎖所有100%無效的流量，包括高位裝置上的新版位流量。可能需支付額外費用。

   * **[!UICONTROL Also block sites with]:** （選用）預設情況下，會導致DSP封鎖廣告的額外詐騙和無效流量層級：  *[!UICONTROL None]* （預設值，不會封鎖其他流量）、  *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*、  *[!UICONTROL >4% Average Fraud/IVT levels]*、  *[!UICONTROL >6% Average Fraud/IVT levels]*、  *[!UICONTROL >10% Average Fraud/IVT levels]*&#x200B;或 *[!UICONTROL >25% Average Fraud/IVT levels]*。可能需支付額外費用。

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** （選用）依預設會導致DSP封鎖廣告的一或多種欺詐類型： *[!UICONTROL Fraud]* （這會以欺詐方式封鎖所有網站）、 *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*&#x200B;和/或 *[!UICONTROL Fraud: Zero Ads]*。可能需支付額外費用。

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** （選用）預設會導致DSP封鎖廣告的可疑網站或應用程式活動類型： *[!UICONTROL None]* （預設值，不會根據可疑活動封鎖廣告）、 *[!UICONTROL Suspicious Activity - High Risk]*&#x200B;或 *[!UICONTROL Suspicious Activity - High or Moderate Risk]*。可能需支付額外費用。

**[!UICONTROL Ads.txt filtering]:**

透過運用每個發佈商的「已授權數位銷售商」清單，以預先出價篩選要使用的[Ads.txt](https://iabtechlab.com/ads-txt-about/)層級。 系統會為新版位選取廣告商層級的預設值，但您可以變更設定：

* *[!UICONTROL Opt out of ads.txt (default)]*:向所有賣家購買庫存。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*:優先購買域授權的直銷商和經銷商的庫存。
* *[!UICONTROL Ads.txt sellers only]*:僅向域授權的直銷商和經銷商購買庫存。
* *[!UICONTROL Ads.txt sellers only]*:僅向域的授權直銷商購買庫存。

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** (以選項設定的廣 [!UICONTROL DoubleVerify Authentic Brand Safety] 告商)啟用， [!DNL DoubleVerify Authentic Brand Safety]這會使用針對指定區段ID設定的自訂品牌安全規則來封鎖出價後曝光數。DSP會向您收取帳戶，以了解在廣告商設定中指定之區段ID的使用情形。

## [!UICONTROL Tracking]

>[!NOTE]
>
>（[!DNL Roku]版位）由[!DNL Roku]核准的第三方追蹤廠商包括[!DNL Acxiom]、[!DNL comScore]、[!DNL Data Plus Math]、[!DNL Experian]、[!DNL Factual]、[!DNL Kantar]、[!DNL Marketing Evolution]、[!DNL Neustar]、[!DNL Nielsen]、[!DNL Nielsen Catalina Solutions]、[!DNL NinthDecimal]、[!DNL Oracle]、[!DNL Placed]、[!DNL Polk]和[!DNL Research Now]。

**[!UICONTROL Event Pixels]:** （選用）協力廠商事件追蹤像素，預設會附加至版位中的所有新廣告。若要指定事件像素：

1. 按一下「![編輯](/help/dsp/assets/edit.png)」。
1. 執行下列任一操作：
   * 若要選取現有像素，請選取像素列中的核取方塊。
   * 若要建立新像素：
      1. 按一下 **[!UICONTROL Create]**.
      1. 輸入以下資訊：
         * **[!UICONTROL Pixel name]:** 像素名稱；長度上限為500個字元。使用有助於輕鬆識別像素的名稱。
         * **[!UICONTROL Pixel event fires on]:** 觸發像素的事件。可用事件會依廣告類型而異。
         * **[!UICONTROL Pixel type]:** 像素是(1x1 *[!UICONTROL IMG URL]* 像素影像檔案)、 *[!UICONTROL HTML]*&#x200B;還是 *[!UICONTROL JavaScript URL]*。
         * **[!UICONTROL Pixel URL]:** 像素影像的URL。
      1. 按一下 **[!UICONTROL Create and attach]**.
   1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** （選用）轉換追蹤像素，預設會附加至版位中的所有新廣告。若要指定轉換像素：

1. 按一下「![編輯](/help/dsp/assets/edit.png)」。
1. 執行下列任一操作：
   * 若要選取現有像素，請選取像素列中的核取方塊。
   * 若要建立新像素：
      1. 按一下 **[!UICONTROL Create]**.
      1. 輸入以下資訊：
         * **[!UICONTROL Conversion pixel name]:** 像素名稱；長度上限為500個字元。使用有助於輕鬆識別像素的名稱。
         * **[!UICONTROL Conversion category]:** 轉換的類型。
         * **[!UICONTROL Impression conversion window]:** 發生廣告曝光後的天數，可將曝光歸因於轉換。預設為30天。
         * **[!UICONTROL Click conversion window]:** 發生廣告點按後，該點按可歸因於轉換的天數。預設為30天。
         * **[!UICONTROL Notes]:** （選用）像素的說明或其他資訊。
      1. 按一下 **[!UICONTROL Create and attach]**.
      1. 在相關網頁上實作轉換像素：
         1. 在主菜單中，轉到&#x200B;**[!UICONTROL Resources]>[!UICONTROL Conversion pixels]**。
         1. 在像素行中，按一下&#x200B;**[!UICONTROL edit]**。
         1. 視需要複製[!UICONTROL HTML Tag]和[!UICONTROL Flash Tag]欄位中的值，以提供給廣告商或網站連絡人。

            廣告商的IT部門或其他群組可能需要排程標籤部署，或接收相關通知。
   1. 按一下 **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** （選用）靜態的第三方費用率，以每千次曝光的不計費成本來追蹤。除非您輸入不同值，否則新版位會自動套用套件層級預設值（若適用）。

>[!NOTE]
>
>可計費費用反映在[!UICONTROL Net CPM]量度中。

>[!MORELIKETHIS]
>
>* [關於版位管理](placement-about.md)
>* [建立版位](placement-create.md)
>* [編輯位置](placement-edit.md)
>* [鍵盤快速鍵](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [關於Campaign管理的常見問題集](/help/dsp/campaign-management/campaign-management-faq.md)

