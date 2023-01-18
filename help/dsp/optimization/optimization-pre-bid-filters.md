---
title: 版位層級出價前篩選器及其使用方法
description: 參考可用的版位層級預先出價篩選條件，並了解如何使用。
feature: DSP Optimization
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# 版位層級出價前篩選器及其使用方法

| 競標前篩選 | 說明 | 何時使用此篩選器 |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | 為拍賣導致點進的機率設定最小預測閾值。 例如，如果您將臨界值設為0.1%，則除非點按的預測機率大於或等於0.1%，否則您不會在拍賣上出價。<br><br><b>注意：</b> 篩選器會在最佳化目標之前套用。 因此，非常嚴格的篩選能防止支出。 | 當您的點進率(CTR)有最低KPI目標，且CTR低於臨界值時不想花費預算時，請使用。 此篩選條件可能具有相當的限制，因此設定實際目標很重要。 根據對版位的其他限制，.03-.07%的目標通常是一個好的起點。 您可以視需要在網站層級將這項功能最佳化，以協助改善量度。<br><br>如果您的目標是達到最低CTR和最佳可能的CPM，則建議的設定是結合 [!UICONTROL Click Through Rate] 使用最佳化目標「[!UICONTROL Lowest CPM].&quot; 如果您的目標是沒有超額實現真正好處的最大CPM，以及最小CTR，則配對 [!UICONTROL Click Through Rate] 使用最佳化目標「[!UICONTROL Always Max Bid + Highest CTR]「可能更合適。 |
| [!UICONTROL 100% Completion Rate] | 設定在曝光出價前必須符合的必要最低完成率。 | 當促銷活動的主要目標為完成率時，請使用此篩選。 其他定位參數中的因數，但建議的起始百分比為65%。 |
| [!UICONTROL Player Size - Adobe] | 使用DSP的資料，設定所需的最小播放器大小。 您會在 [!UICONTROL Player Size] 符合臨界值。 | 使用，確保您使用DSP的資料提供完整集播放器詳細目錄。 |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | 使用來自的資料，設定所需的最小播放器大小 [!DNL Moat] 或 [!DNL Integral Ad Science] ([!DNL IAS])。 您會在 [!UICONTROL Player Size] 符合臨界值。 | 使用確保您使用全平台提供完整集播放器詳細目錄 [!DNL Moat] 或 [!DNL IAS] 資料。<br><br><b>注意：</b> 只有在將促銷活動設定為使用時，才使用此篩選 [!DNL Moat] 或 [!DNL IAS] 資料。 |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | 使用DSP可檢視性數字和測量，設定所需的最小可檢視性百分比。 您會在符合指定臨界值時，對曝光進行出價。<br><br><b>附註：</b><ul><li>如果促銷活動的 [!UICONTROL Viewability Sensitivity] 設定為「[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]，」 [!DNL Media Rating Council] (MRC)促銷活動會使用可檢視性測量標準。 若 [!UICONTROL Viewability Sensitivity] 設定為「[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]，」 [!DNL GroupM] 促銷活動會使用「可檢視性測量標準」。</li><li>Adobe測量定義與協力廠商定義不同，因此與協力廠商資料可能會有細微差異。</li></ul> | 最佳實務是將最佳化目標及任何出價前篩選設定與促銷活動的相符 [!UICONTROL Viewability Sensitivity] 設定。 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [DSP如何最佳化您的行銷活動](optimization-how-dsp-optimizes-campaigns.md)
>* [套件設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [版位設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [促銷活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [最佳化目標及其使用方式](optimization-goals.md)

