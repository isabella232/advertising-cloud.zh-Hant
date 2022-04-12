---
title: 位置級預投標過濾器及其使用方法
description: 參考可用的位置級預投標過濾器，並查看如何使用這些過濾器。
feature: DSP Optimization
exl-id: c699e970-84ca-429b-8062-81804e6c9f21
source-git-commit: d17adc94a211992899e9f2eec6f9e13c16aa02c0
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# 位置級預投標過濾器及其使用方法

| 預投標篩選器 | 說明 | 何時使用此篩選器 |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | 為拍賣將導致點擊通過的概率設定最小預測閾值。 例如，如果將閾值設定為0.1%，則不會在拍賣中投標，除非點擊的預測概率大於或等於0.1%。<br><br><b>注：</b> 在優化目標之前應用篩選器。 因此，非常嚴格的過濾器可以防止花費。 | 當您具有用於點擊率(CTR)的最小KPI目標，並且不想在CTR低於閾值時花費預算時，請使用。 這個過濾器可能是相當限制性的，因此設定現實的目標很重要。 根據對職位安排的其他限制，0.03%至0.07%的目標通常是一個良好的起點。 您可以根據需要在站點級別優化此功能，以幫助改進指標。<br><br>如果您的目標是實現最小的CTR和最佳的CPM，則建議的設定是將 [!UICONTROL Click Through Rate] 具有優化目標&#39;&#39;的篩選器[!UICONTROL Lowest CPM]&quot; 如果目標是最大CPM，但沒有實現過度的實際好處，並且是最小CTR，則將 [!UICONTROL Click Through Rate] 具有優化目標&#39;&#39;的篩選器[!UICONTROL Always Max Bid + Highest CTR]可能更合適。 |
| [!UICONTROL 100% Completion Rate] | 設定在對印象進行投標之前必須滿足的所需最小完成率。 | 當市場活動的主要目標是完成率時，請使用此篩選器。 其他目標參數中的因子，但建議的起始百分比為65%。 |
| [!UICONTROL Player Size - Adobe] | 使用來自Advertising Cloud DSP的資料設定所需的最小播放器大小。 你會想到 [!UICONTROL Player Size] 滿足閾值。 | 用於確保使用中的資料交付全集播放器清DSP單。 |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | 使用來自的資料設定所需的最小播放器大小 [!DNL Moat] 或 [!DNL Integral Ad Science] ([!DNL IAS])。 你會想到 [!UICONTROL Player Size] 滿足閾值。 | 用於確保使用平台範圍提供全集播放器清點 [!DNL Moat] 或 [!DNL IAS] 資料。<br><br><b>注：</b> 僅當市場活動配置為使用時才使用此篩選器 [!DNL Moat] 或 [!DNL IAS] 資料。 |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | 使用Advertising Cloud DSP可視性數字和測量值設定所需的最小可視性百分比。 當達到指定的閾值時，你會以印象出價。<br><br><b>附註：</b><ul><li>如果市場活動 [!UICONTROL Viewability Sensitivity] 設定為「[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]」 [!DNL Media Rating Council] 市場活動使用(MRC)可查看性度量標準。 如果 [!UICONTROL Viewability Sensitivity] 設定為「[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]」 [!DNL GroupM] 市場活動使用可視性度量標準。</li><li>Adobe計量定義與第三方定義不同，因此可能與第三方資料存在細微差異。</li></ul> | 最佳做法是將優化目標和任何投標前篩選器設定與市場活動的匹配 [!UICONTROL Viewability Sensitivity] 的子菜單。 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [如何優DSP化您的市場活動](optimization-how-dsp-optimizes-campaigns.md)
>* [包設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [放置設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [市場活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [優化目標及其使用方法](optimization-goals.md)

