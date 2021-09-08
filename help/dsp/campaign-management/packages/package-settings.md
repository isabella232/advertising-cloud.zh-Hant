---
title: 套件設定
description: 請參閱可用套件設定的說明。
feature: Packages
exl-id: b4d415d1-86a5-40bd-b645-1709b267c174
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 0%

---

# 套件設定

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** 套件名稱。長度上限為60個字元。

**[!UICONTROL Description]:** （選用）套件的說明。

**[!UICONTROL 3rd Party Billed Fees]:** （選用）要以非計費成本追蹤的靜態第三方費用：

>[!NOTE]
>
>可計費費用反映在[!UICONTROL Net CPM]量度中。
* **[!UICONTROL CPM]:** 每1000次曝光的成本(CPM)。

* **[!UICONTROL CPM Description]:** CPM費用的說明。

您可以覆寫[placement level](/help/dsp/campaign-management/placements/placement-settings.md)的封裝層級設定。

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** （現有套件的唯讀）要放置和限制套件中版位的層級：

* **[!UICONTROL Package level pacing]:** 此步調策略的運作方式為以群組形式調整所有包含的 *版位*。此策略可確保指定套件中的所有版位都能全面最佳化，並根據效能和規模將支出分配至選取的關鍵績效指標(KPI)。

* **[!UICONTROL Placement level pacing]:**  此步調策略的運作方式為個別調整和限定所有包含的 *版位*。最佳做法是只將此策略用於執行有保證的私有市場交易。

**[!UICONTROL Flight Dates]:** 套件的開始日期和結束日期。

要選擇為包建立不均勻的調度飛行，請選擇&#x200B;*[!UICONTROL *Activate Custom Flighting]**並在下面的[!UICONTROL Flighting]部分設定自定義飛行。 啟用自訂光源並儲存套件後，就無法停用自訂光源。

>[!NOTE]
>
>* 投放日期必須包含在促銷活動投放日期中。 此外，分配給此包的所有版位的投放日期必須包含在這些日期中。
> * 啟動自訂光源時，您無法編輯套件開始日期。


**[!UICONTROL Budget]:** （僅包級別調整的包）總預算上限和預算間隔。

對於具有自訂光源的套件，預算間隔一律為&#x200B;*[!UICONTROL All time]*。 對於沒有自定義指令碼的包，請指定預算間隔：*[!UICONTROL All time]、* *[!UICONTROL Daily]、* *[!UICONTROL Monthly]、*&#x200B;或&#x200B;*[!UICONTROL Weekly]*。

**[!UICONTROL Gross Budget]:** （僅包含包層級調整和動態利潤管理）包期間的預算總額。

**[!UICONTROL Optimization Goal]:** （僅具有套件層級步調的套件）套件的最佳化目標。請參閱[最佳化目標及如何使用](/help/dsp/optimization/optimization-goals.md)中每個最佳化目標的說明。

**[!UICONTROL Custom Goals]:** (僅限具有自訂最佳化目標的套 [件)](/help/dsp/optimization/custom-goal-about.md) 套件的自訂目標。如需關於使用自訂目標和促銷活動的最佳實務的詳細資訊，請參閱[建立自訂目標的最佳實務](/help/dsp/optimization/custom-goal-best-practices.md)和[設定效能促銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md)。

**[!UICONTROL Package Goal Type]:** （僅限具有自訂最佳化目標的套件）套件的用途。此設定有助於確定如何最佳化套件：

* *[!UICONTROL Prospecting]:* 潛在客戶套件著重於贏取新客戶。

* *[!UICONTROL Retargeting]:* 重新定位套件會著重於重新顯示先前的訪客或客戶。

* *[!UICONTROL Other]:* 所有其他用途。

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** （僅限具有自訂最佳化目標的套件）其歷史資料用作最佳化套件之輸入的其他套件。

**[!UICONTROL Target]:** （僅限具有套件層級步調的套件）目標，用於追蹤效能。

>[!NOTE]
>
>此欄位僅是基準，不用於決策。

**[!UICONTROL Frequency Cap]:** （僅具有封裝層級步調的封裝）從封裝中可提供廣告的唯一裝置或人員(視指 [!UICONTROL Cross Device Level]定而定)的次數。選項包括&#x200B;*[!UICONTROL Unlimited]*&#x200B;或每天、每週或每月的特定數量。

>[!NOTE]
>
>* 您可以在促銷活動、封裝和位置層級設定頻率上限。 DSP會遵循促銷活動階層中最嚴格的頻率上限。
>* 最佳實務是在封裝層級設定探礦和重新定位的頻率上限。
> * 頻率上限越高，支出和曝光次數越高，觸及範圍越低。 頻率上限較低會導致支出和曝光次數降低，但觸及率較高。


**[!UICONTROL Pace on]:** （僅包含套件層級步調的套件）步調所根據的：

* *[!UICONTROL Budget]:* （預設）此選項可在已分配的套件預算內提供盡可能多的曝光次數。

* *[!UICONTROL Impressions]:* 此選項會傳送曝光數，直到在指定間隔內達到指定數量為止。選取此選項時，請指定曝光次數和間隔：*所有時間，* *[!UICONTROL Daily]、* *[!UICONTROL Monthly]、*&#x200B;或&#x200B;*[!UICONTROL Weekly]*。

**[!UICONTROL Pacing Fill Strategy]:** （僅具有套件層級步調的套件）如何調整廣告投放速度：

* *[!UICONTROL Even]:* 在每次飛行中均勻地進行交付，目標為上半段交付量的50%。

* *[!UICONTROL Slightly Ahead]:* （預設值）加速傳送，使得在飛行期間中途完成55-65%。

* *[!UICONTROL Frontload]:* 加速運送，使其在飛行途中完成65-75%。

* *[!UICONTROL Aggressive Frontload]:* 加速運送，使得75-85%的作業在飛行途中完成。

## [!UICONTROL Flighting]

（具有包層步調且啟用「[!UICONTROL Activate Custom Flighting]」的包）在[!UICONTROL Goals & Budget]部分中指定的整體[!UICONTROL Flight Dates]內自定義飛行週期。

對於每次飛行，輸入開始日期、結束日期和曝光次數的目標數量。 要添加另一個飛行，請按一下&#x200B;**[!UICONTROL Add Flight]**。

>[!MORELIKETHIS]
>
>* [關於套件管理](package-about.md)
>* [建立套件](package-create.md)
>* [編輯套件](package-edit.md)
>* [將版位附加到包](package-attach-placement.md)
>* [關於Campaign管理的常見問題集](/help/dsp/campaign-management/campaign-management-faq.md)

