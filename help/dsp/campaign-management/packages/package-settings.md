---
title: 包設定
description: 請參閱可用包設定的說明。
feature: DSP Packages
exl-id: b4d415d1-86a5-40bd-b645-1709b267c174
source-git-commit: 4a699912468cd89efec0c1da9fdb6302ca93a3b4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 包設定

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** 包名稱。 最大長度為60個字元。

**[!UICONTROL Description]:** （可選）包的說明。

**[!UICONTROL 3rd Party Billed Fees]:** （可選）要作為不可計費成本跟蹤的靜態第三方費用：

>[!NOTE]
>
>計費費用反映於 [!UICONTROL Net CPM] 度量。
* **[!UICONTROL CPM]:** 每1000次印象(CPM)的成本。

* **[!UICONTROL CPM Description]:** CPM費的描述。

可以在 [放置級別](/help/dsp/campaign-management/placements/placement-settings.md)。

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** （現有包的只讀）在哪個級別加快和限制包中的放置：

* **[!UICONTROL Package level pacing]:** 此調整策略通過調整和限制所有包括的放置作為 *組*。 此策略確保整個優化給定包中的所有放置位置，根據效能和規模將支出分配到選定的關鍵績效指標(KPI)。

* **[!UICONTROL Placement level pacing]:**  此調整策略通過調整和限制所有包括的放置 *單獨*。 最佳做法是，僅使用此策略執行有保證的私有市場交易。

**[!UICONTROL Flight Dates]:** 包的開始日期和結束日期。

要（可選）為包建立不均勻的起飛，請選擇 *[!UICONTROL *Activate Custom Flighting]**在 [!UICONTROL Flighting] 的下界。 一旦啟用了自定義flight並保存了包，就無法禁用自定義flight。

>[!NOTE]
>
>* 航班日期必須包括在促銷航班日期中。 此外，分配給此包的所有放置的飛行日期必須包括在這些日期中。
> * 激活自定義照明時，無法編輯包的開始日期。


**[!UICONTROL Budget]:** （僅包級別調整的包）總預算上限和預算間隔。

對於具有自定義功能的包，預算間隔始終為 *[!UICONTROL All time]*。 對於沒有自定義功能的包，指定預算間隔： *[!UICONTROL All time]。* *[!UICONTROL Daily]。* *[!UICONTROL Monthly]。* 或 *[!UICONTROL Weekly]*。

**[!UICONTROL Gross Budget]:** （僅具有包級別調整和動態毛利管理的包）包持續時間的總預算上限。

**[!UICONTROL Optimization Goal]:** （僅包級調整的包）包的優化目標。 請參閱以下位置中每個優化目標的說明 [優化目標及其使用方法](/help/dsp/optimization/optimization-goals.md)。

**[!UICONTROL Custom Goals]:** （僅包含自定義優化目標的包） [自定義目標](/help/dsp/optimization/custom-goal-about.md) 包。 有關自定義目標和使用這些目標的市場活動的最佳做法的詳細資訊，請參見  [構建自定義目標的最佳做法](/help/dsp/optimization/custom-goal-best-practices.md) 和 [設定績效活動的最佳做法](/help/dsp/optimization/campaign-best-practices-performance.md)。

**[!UICONTROL Package Goal Type]:** （僅具有自定義優化目標的包）包的目的。 此設定有助於確定如何優化包：

* *[!UICONTROL Prospecting]:* 發現客戶的產品包側重於收購新客戶。

* *[!UICONTROL Retargeting]:* 重新定位軟體包的重點是重新暴露以前的訪問者或客戶。

* *[!UICONTROL Other]:* 所有其他目的。

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** （僅具有自定義優化目標的包）其歷史資料用作優化包的輸入的另一個包。

**[!UICONTROL Target]:** （僅包級調整的包）用於跟蹤效能的目標。

>[!NOTE]
>
>此欄位僅是基準，不用於決策。

**[!UICONTROL Frequency Cap]:** （僅包級別調節的包）唯一設備或個人的次數(取決於指定的 [!UICONTROL Cross Device Level])可從包中獲得廣告。 選項包括 *[!UICONTROL Unlimited]* 或每天、每週或每月的特定金額。

>[!NOTE]
>
>* 您可以在市場活動、包裝和放置層設定頻率上限。 尊DSP重市場活動層次中最嚴格的頻率上限。
>* 最佳做法是在一攬子級別為發現客戶和重新確定目標設定頻率上限。
> * 頻率上限越高，支出和印象就越高，但影響力越小。 低頻率上限導致支出和印象降低，但影響力更大。


**[!UICONTROL Pace on]:** （僅包級調步的包）調步基於：

* *[!UICONTROL Budget]:* （預設）此選項在分配的包預算內提供盡可能多的印象。

* *[!UICONTROL Impressions]:* 此選項在指定的時間間隔內達到指定數量之前提供印數。 選擇此選項時，指定印次數和間隔： *一直以來，* *[!UICONTROL Daily]。* *[!UICONTROL Monthly]。* 或 *[!UICONTROL Weekly]*。

**[!UICONTROL Pacing Fill Strategy]:** （僅包級調整的包）如何調整和交付：

* *[!UICONTROL Even]:* 在每次飛行中均勻交付，目標是在飛行前半段交付50%。

* *[!UICONTROL Slightly Ahead]:* （預設值）加快交貨速度，以便在飛行時間的一半內完成55-65%。

<!-- replaced with ASAP -->
* *[!UICONTROL Frontload]:* 加快交貨速度，使飛行中途完成65-75%。

* *[!UICONTROL Aggressive Frontload]:* 加快交貨速度，使75%-85%在飛行中途完成。

## [!UICONTROL Flighting]

(具有包級別調整和「」的包[!UICONTROL Activate Custom Flighting]「已啟用」)在整個 [!UICONTROL Flight Dates] 在 [!UICONTROL Goals & Budget] 的子菜單。

對於每個航班，輸入起始日期、終止日期和目標印數。 要添加另一個航班，請按一下 **[!UICONTROL Add Flight]**。

>[!MORELIKETHIS]
>
>* [關於包管理](package-about.md)
>* [建立包](package-create.md)
>* [編輯包](package-edit.md)
>* [將放置附加到包](package-attach-placement.md)
>* [關於Campaign Management的常見問題](/help/dsp/campaign-management/campaign-management-faq.md)

