---
title: 設定績效活動的最佳做法
description: 瞭解設定注重績效的活動的最佳實踐，包括針對最低CPA或最高ROAS優化的職位安排。
feature: DSP Optimization, DSP Best Practices
exl-id: fc64680d-9d1c-4f74-a8b9-2e9b670c00eb
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '1232'
ht-degree: 0%

---

# 設定績效活動的最佳做法

Advertising Cloud可以優化注重績效的營銷活動，以便以最低的每次收購成本(CPA)或最高的廣告支出回報(ROAS)進行投放。

請參閱以下績效活動的最佳做法：

* 步驟1 — 定義目標
* 步驟2 — 定義策略
* 步驟3 — 建立包
* 步驟4 — 建立放置結構
* 步驟5 — 使用正確的創意資產

## 步驟1 — 定義目標

瞭解此活動的目標是實現盡可能高的ROA還是盡可能低的CPA，這一點很重要。 對於市場活動中的每個包，您將相應地指定目標目標，作為 *[!UICONTROL Highest ROAS - Custom Goal]* 或 *[!UICONTROL Lowest CPA - Custom Goal]*。

![優化目標](/help/dsp/assets/optimization-goals.png)

您還需要確定將導致總體目標的成功事件並相應地建立自定義目標。 對於每個包，您將指定一個自定義目標，以便與報告和算法優化的總體優化目標一起使用 [!DNL Adobe Sensei]。 有關建立自定義目標的詳細資訊，請參見 [構建自定義目標的最佳做法](custom-goal-best-practices.md)。

![自定義目標](/help/dsp/assets/objective-goals.png)

## 步驟2 — 定義策略

### 發現客戶的策略

上漏斗包包括非常廣泛的投放，以接觸淨新消費者。

#### 建議的探查位置策略

* 使用以下策略查找可能轉換的新受眾：

   * 從資料管理平台(DMP)(如Adobe Audience Manager)進行類似建模。
   * 使用第三方資料的行為目標。
   * 上下文目標。
   * 站點/類別目標。

* 使用網路運行(RON)目標：必須包括一系列網路佈局，不以受眾為目標，以廣泛的庫存為目標。 這允許 [!DNL Adobe Sensei] 算法，用於查找可能有較新Cookie的有價用戶，這些Cookie尚未被分類到受眾中。

### 重定目標策略

下漏斗包包括已訪問廣告商網頁或廣告商已為其提供CRM資料的目標用戶的定位。

#### 建議的重定位策略

* 如果廣告商是Adobe Analytics或Adobe Audience Manager的客戶，則您可以構建第一方網段（如首頁訪問者、產品頁面或購物車放棄者），並將它們用作Advertising Cloud的投放目標。

* 避免為針對受眾的安排分配過多的預算。 一般規定，每1 000個用戶每月預算30美元。

## 步驟3 — 建立包

最佳做法是為上漏斗物探和下漏斗物重定位建立單獨的包。 優化在包級別進行，以便將包內所有放置的效能資料匯集起來。 因此，集團配售於預期表現相若之組合。

![用於發現客戶和重新確定目標的單獨包示例](/help/dsp/assets/p-r.png)

另外，請使用以下設定。

### 目標和預算

* **起點和上限設定：** 要選擇CPA或ROAS優化目標，軟體包必須使用包級別調整。 這可確保優化包內的所有放置，以便根據效能和規模將支出分配到選定的目標。

* **航班日期：** （發現客戶包）當您的活動運行時間超過25天時，使用 [!UICONTROL Activate Custom Flighting] 的子菜單。 首先，將前10天的定製航班定在所需每日預算的75%左右，以減少在2014年12月31日 *學習階段*。 然後為預算的剩餘部分設定第二次定制航班。

   例如，如果您有100,000美元可以在30天內花費，則將第1次航班（第1-10天）的預算設定為$25,000（75% x $100,000/30天= $2,500）。 使用第2次航班（第11-30天）的剩餘預算75,000美元。

* **預算：** 總DSP是嘗試將100%的包預算平均分配到包中的所有位置。 如果職位安排的支出較少或沒有支出，我們建議為職位安排設定預算上限，以允許將更多預算分配給具有比例的職位安排。 允許24-48小時校準預算更改。

* **優化目標：** 使用兩種效能優化目標之一， *[!UICONTROL Highest ROAS]* 或 *[!UICONTROL Lowest CPA]*，具體取決於包目標。 這些目標分別自動優化最高ROAS或最低CPA配置的方案。

* **自定義目標：**
   * 如果新包與現有包具有相同的目標，則您可以選擇連結現有包，以便算法可以使用現有的機器學習資料。
   * 輸入相應的 [!UICONTROL Target CPA] 或 [!UICONTROL Target ROAS]。

* **調整填充策略：** 選擇 *[!UICONTROL Even]* 在整個飛行日期內協調一致，以最大限度地實現您的效能目標。

   使用 *[!UICONTROL FrontLoad]* 和 *[!UICONTROL Aggressive Front Load]* 只有在您完全排定交付優先順序並花費超過效能優化時才調整進度，因為這些策略可能會對您期望的效能KPI產生負面影響。

## 步驟4 — 建立放置結構

少就是多。 如果每個包可設定少於6個放置，則可用預算可以最輕鬆地動態切換到效能最佳的放置。

另外，確保將每個放置添加到包目標類型為 *[!UICONTROL Prospecting]* 或 *[!UICONTROL Retargeting]*。

以下是績效市場活動的推薦職位設定。

### 目標

您將在包級別配置CPA或ROAS優化（請參閱步驟3 — 建立包），但可以添加其他放置級別設定。

* **最大出價：**
   * 對於發現潛在客戶，請使用最低出價（5美元）。
   * 對於重定位置，請使用最高出價（12美元）。

* **預出價篩選器：** 最小化或理想地避免設定主動的預標過濾器，這會阻止放置達到規模。 最佳做法包括：

   * 每次放置使用一(1)個預投標過濾器。 多個投標前過濾器需要同時滿足這兩個條件，這會減少規模。

   * 考慮在應用附加目標（如受眾、地域和站點目標）的情況下設定較不嚴格的預標過濾器。

請參閱下列資訊的說明：何時使用每個預投標篩選器 [位置級預投標過濾器及其使用方法](/help/dsp/optimization/optimization-pre-bid-filters.md)。

### 庫存

要實現最大規模，請使用 [!UICONTROL Public] (Open Exchange)和 [!UICONTROL On Demand] 庫存。

### 站點目標

* **[!UICONTROL Traffic Type]**: [!UICONTROL Websites] 僅
* **[!UICONTROL Site Tier]**: [!UICONTROL All sites]

### 受眾目標

* **[!UICONTROL Included Audiences]:**
   * 對於發現潛在客戶的放映，將類似的受眾類別和類似的受眾規模分組為一個放映。 然後，根據效能，執行以下操作之一：
      * 從現有放映中刪除表現不佳的受眾。
      * 將表現最佳的觀眾移到單獨的位置，以更好地控制預算。
   * 對於重新定位投放，您最好在每個投放中包括一個受眾部分，以輕鬆控制投標和預算。

>[!NOTE]
>
>如果只能通過一個位置聯繫到用戶，您的廣告將發揮最佳效果。 用戶在不同位置之間的顯著重疊可能會導致競爭，這將產生一個不斷增加的出價的週期，從而推高每用戶的成本。 因此，如果您包括多個觀眾，請確保它們不由重疊的用戶/觀眾成員組成。
>
> 您可以通過在層中建立受眾來避免重疊的受眾，以便您可以根據需要從放置中抑制更高、更包容的層。

* **[!UICONTROL Frequency Capping]:**
   * 對於勘探位置，請使用緊密的頻率上限（每天一次印象）。
   * 對於重新定位放置，請將主放置上限設定為每天6-10次，將次放置上限設定為每小時1次。

* **[!UICONTROL Device Targeting]**:
   * 包括 [!UICONTROL Computer]。 [!UICONTROL Mobile], [!UICONTROL Tablet]。
   * 不瞄準 [!UICONTROL Firefox] 和 [!UICONTROL Safari] 因為目標和測量的限制。 聯繫您 [!DNL Adobe] 帳戶團隊的詳細資訊 [!DNL Adobe] 支援 [!DNL Safari ITP]。
   * 如果針對移動Web通信，則禁用除Web通信之外的所有移動瀏覽器 [!UICONTROL Chrome] 和 [!UICONTROL Edge]。

### 品牌安全與媒體質量

使用上下文過濾、投標前欺詐阻止和/或 [!UICONTROL Ads.txt] 篩選將限制放置的比例，但在需要時使用。

## 步驟5 — 使用正確的創意資產

* 最佳做法是盡可能多地加入獨特的廣告規模，以最大限度地擴大廣告覆蓋面。 通用顯示模板允許您上載任何標準顯示廣告大小。
* 確保所有放置都包含 *至少* 所有主顯示器和大小（300x250、728x90、160x600、300x600、320x50和300x50）。
* 經常更新創意，以防止創意疲勞。

>[!MORELIKETHIS]
>
>* [包設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [放置設定](/help/dsp/campaign-management/placements/placement-settings.md)
> * [如何優DSP化您的市場活動](optimization-how-dsp-optimizes-campaigns.md)
>* [優化目標及其使用方法](optimization-goals.md)
>* [位置級預投標過濾器及其使用方法](optimization-pre-bid-filters.md)
>* [市場活動啟動核對表](/help/dsp/campaign-management/campaign-launch-checklist.md)

