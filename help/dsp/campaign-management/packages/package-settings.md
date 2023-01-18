---
title: 套件設定
description: 請參閱可用套件設定的說明。
feature: DSP Packages
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 0%

---

# 套件設定

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** 套件名稱。 長度上限為60個字元。

**[!UICONTROL Description]:** （選用）套件的說明。

**[!UICONTROL 3rd Party Billed Fees]:** （可選）要作為不計費成本跟蹤的靜態第三方費用：

>[!NOTE]
>
>可結算費用反映於 [!UICONTROL Net CPM] 量度。
* **[!UICONTROL CPM]:** 每1000次曝光的成本(CPM)。

* **[!UICONTROL CPM Description]:** CPM費用的說明。

您可以在 [刊登層級](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** （現有套件的唯讀）要放置和限制套件中版位的層級：

* **[!UICONTROL Package level pacing]:** 此步調策略的運作方式為步調和限定所有包含的版位， *群組*. 此策略可確保指定套件中的所有版位都能全面最佳化，並根據效能和規模將支出分配至選取的關鍵績效指標(KPI)。

* **[!UICONTROL Placement level pacing]:**  此步調策略的運作方式為步調調整，並限定所有包含的版位 *個別*. 最佳做法是只將此策略用於執行有保證的私有市場交易。

**[!UICONTROL Flight Dates]:** 包的開始日期和結束日期。

要選擇為包建立不均勻的調度，請選擇 *[!UICONTROL *Activate Custom Flighting]**並在 [!UICONTROL Flighting] 一節。 啟用自訂光源並儲存套件後，就無法停用自訂光源。

>[!NOTE]
>
>* 投放日期必須包含在促銷活動投放日期中。 此外，分配給此包的所有版位的投放日期必須包含在這些日期中。
> * 啟動自訂光源時，您無法編輯套件開始日期。


**[!UICONTROL Budget]:** （僅包級步調的包）總預算上限和預算間隔。

對於具有自訂光源的套件，預算間隔一律為 *[!UICONTROL All time]*. 對於沒有自定義指令碼的包，請指定預算間隔： *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* 或 *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** （僅具有包級別步調和動態利潤管理的包）包期間的預算總額。

**[!UICONTROL Optimization Goal]:** （僅包級步調的包）包的最佳化目標。 請參閱以下各個最佳化目標的說明： [最佳化目標及其使用方式](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goals]:** （僅包含自訂最佳化目標） [自訂目標](/help/dsp/optimization/custom-goal-about.md) 包。 如需自訂目標及使用這些目標之促銷活動的最佳實務，請參閱  [建立自訂目標的最佳作法](/help/dsp/optimization/custom-goal-best-practices.md) 和 [設定效能行銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md).

**[!UICONTROL Package Goal Type]:** （僅限具有自訂最佳化目標的套件）套件的用途。 此設定有助於確定如何最佳化套件：

* *[!UICONTROL Prospecting]:* 潛在客戶套件專注於贏取新客戶。

* *[!UICONTROL Retargeting]:* 重新定位套件著重於重新顯示先前的訪客或客戶。

* *[!UICONTROL Other]:* 其他用途。

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** （僅限具有自訂最佳化目標的套件）其歷史資料用作最佳化套件之輸入的其他套件。

**[!UICONTROL Target]:** （僅包級步調的包）目標目標，用於跟蹤效能。

>[!NOTE]
>
>此欄位僅是基準，不用於決策。

**[!UICONTROL Frequency Cap]:** （僅包級步調的包）唯一設備或人員的次數(取決於指定 [!UICONTROL Cross Device Level] 適用於促銷活動)可從套件提供廣告。 選項包括 *[!UICONTROL Unlimited]* 或每天、每週或每月的特定數量。

>[!NOTE]
>
>* 您可以在促銷活動、封裝和位置層級設定頻率上限。 DSP會遵循促銷活動階層中最嚴格的頻率上限。
>* 最佳實務是在封裝層級設定探礦和重新定位的頻率上限。
> * 頻率上限越高，支出和曝光次數越高，觸及範圍越低。 頻率上限較低會導致支出和曝光次數降低，但觸及率較高。


**[!UICONTROL Pace on]:** （僅包級步調的包）步調基於以下內容：

* *[!UICONTROL Budget]:* （預設）此選項在分配的包預算內提供盡可能多的曝光次數。

* *[!UICONTROL Impressions]:* 此選項會傳送曝光次數，直到在指定間隔內達到指定數量為止。 選取此選項時，請指定曝光次數和間隔： *總是，* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* 或 *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** （僅包層級步調的套件）如何在整個飛行中步調和傳遞：

* *[!UICONTROL Even]:* 在每次飛行中以50%的目標均勻地進行交付。

* *[!UICONTROL Slightly Ahead]:* （預設）加速傳送，使得在飛行期間中途完成55-65%。

* *[!UICONTROL Frontload]:* 加速運送，使得它在飛行途中完成65-75%。

* *[!UICONTROL Aggressive Frontload]:* 加速運送，使得75-85%的人在飛行途中完成。

**[!UICONTROL Intraday pacing]:** （僅限包裝層級步調的套件）如何在飛行期間以每天的時間來調整廣告投放：

* *[!UICONTROL Even]:* （預設）根據庫存可用性調整交貨規模。 一般而言，當拍賣量較高時，白天每小時傳送的廣告數量會較多，而早上和晚上傳送的廣告數量則會較少。

* *[!UICONTROL ASAP]:* 將傳送速度加快至 *平均*.

   >[!CAUTION]
   >
   >此選項可能對效能產生負面影響。 只有在您完全排定傳送的優先順序時才使用它，並且花費在效能最佳化上。

## [!UICONTROL Flighting]

(具有包級別步調和「[!UICONTROL Activate Custom Flighting]&quot;已啟用)在整體 [!UICONTROL Flight Dates] 在中指定 [!UICONTROL Goals & Budget] 區段。

對於每次飛行，輸入開始日期、結束日期和曝光次數的目標數量。 要添加另一個投放，請按一下 **[!UICONTROL Add Flight]**.

>[!MORELIKETHIS]
>
>* [關於套件管理](package-about.md)
>* [建立套件](package-create.md)
>* [編輯套件](package-edit.md)
>* [將版位附加到包](package-attach-placement.md)
>* [查看包的更改日誌](package-change-log.md)
>* [Campaign Management常見問題集](/help/dsp/campaign-management/campaign-management-faq.md)

