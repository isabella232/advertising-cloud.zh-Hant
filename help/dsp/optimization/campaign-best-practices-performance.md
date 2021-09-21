---
title: 設定效能行銷活動的最佳實務
description: 了解設定以效能為中心的行銷活動的最佳實務，包括針對最低CPA或最高ROAS最佳化的刊登版位。
feature: DSP Optimization, DSP Best Practices
exl-id: fc64680d-9d1c-4f74-a8b9-2e9b670c00eb
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '1233'
ht-degree: 0%

---

# 設定效能行銷活動的最佳實務

Advertising Cloud能以最低的每次贏取成本(CPA)或最高的廣告投入報酬率(ROAS)，最佳化您以效能為中心的促銷活動。

請參閱下列效能促銷活動的最佳實務：

* 步驟1 — 定義目標
* 步驟2 — 定義策略
* 步驟3 — 建立套件
* 步驟4 — 建立放置結構
* 步驟5 — 使用正確的創意資產

## 步驟1 — 定義目標

請務必了解行銷活動的目標是達成盡可能高的ROAS或盡可能低的CPA。 對於促銷活動中的每個套件，您將相應地指定目標為&#x200B;*[!UICONTROL Highest ROAS - Custom Goal]*&#x200B;或&#x200B;*[!UICONTROL Lowest CPA - Custom Goal]*。

![最佳化目標](/help/dsp/assets/optimization-goals.png)

您也需要判斷將導向整體目標的成功事件，並據此建立自訂目標。 對於每個套件，您會指定要與使用[!DNL Adobe Sensei]的報表和演算法最佳化的整體最佳化目標搭配使用的自訂目標。 如需建立自訂目標的詳細資訊，請參閱[建立自訂目標的最佳實務](custom-goal-best-practices.md)。

![自訂目標](/help/dsp/assets/objective-goals.png)

## 步驟2 — 定義策略

### 探礦策略

漏斗上方的套件包括定位範圍非常廣的版位，可觸及新的淨消費者。

#### 探礦建議的放置策略

* 使用下列策略尋找可能轉換的新對象：

   * 來自資料管理平台(DMP)(例如Adobe Audience Manager)的相似建模。
   * 使用協力廠商資料的行為鎖定目標。
   * 內容鎖定。
   * 網站/類別定位。

* 使用運行網路(RON)目標：必須包括一系列網路版位，不鎖定受眾目標和廣泛的庫存目標。 這可讓[!DNL Adobe Sensei]演算法尋找可能有較新Cookie且尚未分類至受眾的有價值使用者。

### 重新定位策略

下層漏斗套件包含定位已造訪廣告商網頁或廣告商擁有CRM資料之使用者的位置。

#### 重新定位的建議刊登策略

* 如果廣告商是Adobe Analytics或Adobe Audience Manager客戶，則您可以建立第一方區段（例如首頁訪客、產品頁面或購物車放棄者），並將其用作Advertising Cloud中的版位目標。

* 請避免為目標對象版位指派太多預算。 一般規則是，每月每1,000名使用者預算30美元。

## 步驟3 — 建立套件

最佳實務是為漏斗上部的勘察作業和漏斗下部的重新定位作業分別建立套件。 最佳化會在套件層級進行，因此會收集套件中所有位置的效能資料。 因此，將配置分組到具有類似預期效能的包中。

![用於探礦和重新定位的單獨包示例](/help/dsp/assets/p-r.png)

此外，請使用下列設定。

### 目標與預算

* **步調與上限設定：** 若要選取CPA或ROAS最佳化目標，套件必須使用套件層級的步調。這可確保套件中的所有版位都經過最佳化，以根據效能和規模來分配支出，以符合所選目標。

* **投放日期：** （探礦套件）當您的促銷活動執行超過25天時，請使用 [!UICONTROL Activate Custom Flighting] 功能。首先，將前10天的定製飛行設定為所需每日預算的75%，以減少&#x200B;*學習階段*&#x200B;期間的支出。 然後設定預算余下的第二個自訂飛行。

   例如，如果您有$100,000可在30天內花費，則將第1班機（第1-10天）的預算設定為$25,000(75% x $100,000/30天= $2,500)。 使用2號航班（11-30天）的剩餘預算75,000美元。

* **預算：** DSP一律會嘗試在套件中的所有版位之間平均分配100%的套件預算。如果刊登版位的花費較低或沒有支出，建議設定刊登版位的預算上限，以允許將更多預算按比例分配給刊登版位。 校準預算更改需要24到48小時。

* **最佳化目標：** 根據套件目標，使用兩 *[!UICONTROL Highest ROAS]* 個效能最佳化目 *[!UICONTROL Lowest CPA]*&#x200B;標之一或。 這些目標會分別針對最高ROAS或最低CPA版位自動最佳化套件。

* **自訂目標：**
   * 如果新套件的目標與現有套件相同，您可以選擇連結現有套件，讓演算法可以使用現有的機器學習資料。
   * 輸入相應的[!UICONTROL Target CPA]或[!UICONTROL Target ROAS]。

* **步調填滿策略：** 選取此 *[!UICONTROL Even]* 選項，在整個飛行日期內以一致的步調來達到最佳效能目標。

   只有在您完全排定傳送的優先順序時，才使用&#x200B;*[!UICONTROL FrontLoad]*&#x200B;和&#x200B;*[!UICONTROL Aggressive Front Load]*&#x200B;步調，並且花費超過效能最佳化，因為這些策略可能會對您想要的效能KPI造成負面影響。

## 步驟4 — 建立放置結構

少就是多。 如果您每個套件設定的版位少於6個，則可用預算可以動態地轉移至效能最佳的版位。

此外，請務必將每個版位新增至包目標類型為&#x200B;*[!UICONTROL Prospecting]*&#x200B;或&#x200B;*[!UICONTROL Retargeting]*&#x200B;的包（如適用）。

以下是效能促銷活動的建議位置設定。

### 目標

您將在套件層級設定CPA或ROAS最佳化（請參閱步驟3 — 建立套件），但您可以新增其他版位層級設定。

* **最高競價：**
   * 如需探礦位置，請使用最低出價（5美元）。
   * 若要重新定位版位，請使用最高出價($12)。

* **出價前篩選器：** 盡可能減少或最好避免設定積極的出價前篩選器，而這會使版面無法達到規模。最佳實務包括：

   * 對每個版位使用一(1)個出價前篩選。 多個出價前篩選條件必須同時符合這兩項條件，以縮小規模。

   * 如果套用其他目標（例如對象、地理和網站目標），請考慮設定較不嚴格的競標前篩選。

請參閱[版位層級預先競價篩選及如何使用](/help/dsp/optimization/optimization-pre-bid-filters.md)中每個預先競價篩選的使用時機說明。

### 庫存

要最大化規模，請使用[!UICONTROL Public]（開放Exchange）和[!UICONTROL On Demand]庫存。

### 網站目標定位

* **[!UICONTROL Traffic Type]**: [!UICONTROL Websites] 僅限
* **[!UICONTROL Site Tier]**:  [!UICONTROL All sites]

### 對象鎖定

* **[!UICONTROL Included Audiences]:**
   * 若是探礦位置，請將類似的對象類別和類似的對象大小分組為一個位置。 然後，根據效能，執行下列其中一項操作：
      * 從現有版位移除表現欠佳的對象。
      * 將表現最佳的受眾移至個別版位，以更妥善地控制預算。
   * 若是重新定位版位，理想情況下，您應在每個版位中加入一個對象區段，以輕鬆控制出價和預算。

>[!NOTE]
>
>如果只能以一個版位觸及使用者，您的廣告會呈現最佳效果。 跨版位的使用者大量重疊，可能會造成競爭，進而產生持續增加出價的週期，進而提高每位使用者的成本。 因此，如果您包含多個對象，請確定這些對象不會由重疊的使用者/對象成員組成。
>
> 您可以在層級中建立對象，以避免重疊的對象，以便根據需要從版位中隱藏較高、更包容的層級。

* **[!UICONTROL Frequency Capping]:**
   * 若是探礦位置，請使用緊密的頻率上限（每天一次曝光）。
   * 若要重新定位版位，請將主要版位上限設為每天6-10個曝光數，將次要上限設為每小時一個曝光數。

* **[!UICONTROL Device Targeting]**:
   * 包括[!UICONTROL Computer]、[!UICONTROL Mobile]和[!UICONTROL Tablet]。
   * 由於定位和測量限制，請勿鎖定[!UICONTROL Firefox]和[!UICONTROL Safari]。 如需[!DNL Adobe][!DNL Safari ITP]支援的詳細資訊，請連絡您的Adobe帳戶管理員。
   * 如果您將行動網路流量作為目標，請停用除[!UICONTROL Chrome]和[!UICONTROL Edge]外的所有行動瀏覽器。

### 品牌安全與媒體品質

使用內容篩選、出價前欺詐封鎖及/或[!UICONTROL Ads.txt]篩選將限制您刊登版位的規模，但視需要使用。

## 步驟5 — 使用正確的創意資產

* 最佳實務是盡可能納入多個不重複廣告大小，以將觸及最大化。 通用顯示範本可讓您上傳任何標準顯示廣告大小。
* 請確定所有版位至少包含&#x200B;**&#x200B;所有主要顯示廣告大小（300x250、728x90、160x600、300x600、320x50和300x50）。
* 經常更新創作元素，以防止創作疲勞。

>[!MORELIKETHIS]
>
>* [套件設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [版位設定](/help/dsp/campaign-management/placements/placement-settings.md)
> * [DSP如何最佳化您的行銷活動](optimization-how-dsp-optimizes-campaigns.md)
>* [最佳化目標及其使用方式](optimization-goals.md)
>* [版位層級出價前篩選器及其使用方法](optimization-pre-bid-filters.md)
>* [Campaign啟動檢查清單](/help/dsp/campaign-management/campaign-launch-checklist.md)

