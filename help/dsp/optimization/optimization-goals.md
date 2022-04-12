---
title: 優化目標及其使用方法
description: 參考可用的優化目標並查看何時使用這些目標。
feature: DSP Optimization
exl-id: 9bca09b5-9aa7-4009-a576-9b30cfddfd55
source-git-commit: dd41d184adf5eea463c3a7feb73e1c0858619830
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 優化目標及其使用方法

| 優化目標 | 說明 | 何時使用此目標 |
| -----------| ---------- | ---------- |
| [!UICONTROL Always Max Bid & Highest Clickthrough Rate] | 在包層優化中，預算分配將優先安排最高點擊率的職位安排。<br><br>如果支出目標得到實現，拍賣評估將優先考慮CTR。 提交的投標將始終是 [!UICONTROL Max Bid]但是，如果安置支出良好，預計的CTR閾值將變得更加嚴格。 | 市場活動類型：品牌<br><br>基準：最高點擊率<br><br>廣告類型：預卷、顯示<br><br><b>注：</b> 如果您有一個不需要超越的固定CPM目標和一個需要最大化的CTR目標，則使用此目標。 將「最大投標」設定為所需的CPM目標，DSP並在嘗試花費全部預算時實現盡可能最佳的CTR。 |
| [!UICONTROL Always Max Bid & Highest Completion Rate] | 通過一攬子優化，預算分配將優先安排最高完成率的安置。<br><br>如果支出目標得到實現，拍賣評估將優先選擇完成率。 提交的投標總是設定的「最大投標」，但是如果投資情況良好，預計的「完成率」閾值將變得更加嚴格。 | 市場活動類型：品牌<br><br>基準：最高完成率<br><br>廣告類型：僅預滾<br><br><b>注：</b> 如果您有一個不需要超越的固定CPM目標和一個需要最大化的完成率目標，則使用此目標。 將「最大投標」設定為所需的CPM目標，DSP並在嘗試花費全部預算時達到盡可能最佳的完成率。 |
| [!UICONTROL Always Max Bid & Highest Engagement Rate] | 在包級別優化中，預算分配將優先安排最高的簽約率。<br><br>如果支出目標得到實現，拍賣評估將優先確定訂婚率。 提交的出價將始終是設定的最大出價，但如果配售支出良好，預計的投入率門檻將變得更加嚴格。 | 市場活動類型：品牌<br><br>基準：最高訂約率<br><br>廣告類型：僅移動間隙<br><br><b>注：</b> 如果您有一個不需要超越的固定CPM目標和一個需要最大化的參與目標，則使用此目標。 將「最大投標」設定為所需的CPM目標，DSP並在嘗試花費全部預算時實現盡可能最佳的參與率。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (Adobe – GroupM)] | 在包層優化中，預算分配將優先安排可查看率最高的放置。<br><br>如果支出目標得到實現，拍賣評估將優先查看率。 提交的投標總是設定的「最大投標」，但如果投入得當，預計的可視性率閾值將變得更加嚴格。 | 市場活動類型：品牌<br><br>基準：最高可查看率<br><br>廣告類型：僅互動式預卷<br><br><b>注：</b> 此目標將始終使用放置級別的最大出價。<br><br>如果市場活動的「可視性敏感度」設定設定為「標準（連續2秒內視圖為廣告的50%）」，則市場活動將使用媒體評級委員會(MRC)可視性度量標準。 如果市場活動設定為「嚴格（視圖中廣告的100%和音頻的50%持續時間）」，則市場活動將使用GroupM可視性度量標準。 理想情況下，您應將市場活動設定與優化目標和投標前篩選器設定相匹配。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (Adobe – MRC)] | 在包層優化中，預算分配將優先安排可查看率最高的放置。<br><br>如果支出目標得到實現，拍賣評估將優先查看率。 提交的投標總是設定的「最大投標」，但如果投入得當，預計的可視性率閾值將變得更加嚴格。 | 市場活動類型：品牌<br><br>基準：最高可查看率<br><br>廣告類型：僅互動式預卷<br><br><b>注：</b> 此目標將始終使用放置級別的最大出價。<br><br>如果市場活動的「可視性敏感度」設定設定為「標準（連續2秒內視圖為廣告的50%）」，則市場活動將使用媒體評級委員會(MRC)可視性度量標準。 如果市場活動設定為「嚴格（視圖中廣告的100%和音頻的50%持續時間）」，則市場活動將使用GroupM可視性度量標準。 理想情況下，您應將市場活動設定與優化目標和投標前篩選器設定相匹配。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (IAS – MRC)] | 在包層優化中，預算分配將優先安排可查看率最高的放置。<br><br>如果支出目標得到實現，拍賣評估將優先查看率。 提交的投標總是設定的「最大投標」，但如果投入得當，預計的可視性率閾值將變得更加嚴格。 | 市場活動類型：品牌<br><br>基準：最高可查看率<br><br>廣告類型：僅互動式預卷<br><br><b>注：</b> 此目標將始終使用放置級別的最大出價。<br><br>當來自IAS的第三方資料通知算法時，此設定最有效。 僅當為市場活動啟用了IAS整合時才使用此目標。 |
| [!UICONTROL Highest ROAS – Custom Goal] | （僅在包級別提供）預算分配將優先安排廣告投放，廣告支出回報最高(ROAS)。<br><br>拍賣評估將確定ROAS的優先順序。 如果支出目標得到實現，DSP那麼將在降低企業業績管理與提高ROAS之間取得平衡。 | 市場活動類型：效能<br><br>基準：最高收入<br><br>廣告類型：顯示<br><br><b>注：</b> 有關詳細資訊，請參閱「設定績效市場活動的最佳做法」。 |
| [!UICONTROL Lowest CPA – Custom Goal] | （僅在一攬子級別提供）預算分配將優先安排最低註冊會計師的職位。<br><br>拍賣評估將優先考慮註冊會計師。 如果支出目標得到實現，DSP那麼將在降低企業業績管理與降低註冊會計師之間取得平衡。 | 市場活動類型：效能<br><br>基準：最低註冊會計師<br><br>廣告類型：顯示<br><br><b>注：</b> 有關詳細資訊，請參閱「設定績效市場活動的最佳做法」。 |
| [!UICONTROL Lowest Cost Per Click] | 通過一攬子優化，預算分配將優先安排最低CPC的安置。<br><br>拍賣評估將優先考慮中油。 如果支出目標得到實現，DSP那麼將在降低CPM和提高CTR之間取得平衡，以降低CPC。 | 市場活動類型：品牌<br><br>基準：高效CPM和最高點擊率<br><br>廣告類型：預卷、顯示<br><br><b>注：</b> 用這個目標實現最好的中國共產黨。 要確保最大CPM，請將其用作放置的最大標價。 |
| [!UICONTROL Lowest Cost Per Completion] | 通過一攬子優化，預算分配將優先安排每次完成時的最低成本。<br><br>拍賣評估將優先確定視頻完成率(VCR)。 如果支出目標得到實現，DSP則將在降低CPM與增加VCR之間取得平衡，以降低每次完成的成本。 | 市場活動類型：品牌<br><br>基準：高效CPM和最高完成率<br><br>廣告類型：僅預滾 |
| [!UICONTROL Lowest Cost Per Engagement] | 通過包級別優化，預算分配將優先安排最低的簽約率。<br><br>拍賣評估將優先確定訂婚率。 如果支出目標得到實現，DSP那麼將嘗試在降低企業業績管理與降低每次參與的成本之間取得平衡。 | 市場活動類型：品牌<br><br>基準：高效CPM和最高參與率<br><br>廣告類型：僅移動間隙 |
| [!UICONTROL Lowest CPM] | 在一攬子優化中，預算分配將優先安排最低的業績管理。<br><br>拍賣評估將優先考慮公司業績管理。 如果支出目標得到實現，DSP則企業業績管理將逐漸降低。 | 市場活動類型：品牌<br><br>基準：高效CPM<br><br>廣告類型：預卷、顯示、CTV、本機、音頻 |
| [!UICONTROL Lowest Cost Per View] | 與Lows CPM類似。 在一攬子優化中，預算分配將優先安排最低的業績管理。<br><br>拍賣評估將優先考慮公司業績管理。 如果支出目標得到實現，DSP則企業業績管理將逐漸降低。 | 市場活動類型：品牌<br><br>基準：高效CPM和最高點擊率<br><br>廣告類型：預卷、顯示 |
| [!UICONTROL Lowest vCPM (Adobe - GroupM)] | 通過一攬子優化，預算分配將優先安排最低的vCPM.<br><br>拍賣評估將優先考慮vCPM。 如果支出目標得到實現，DSP那麼將嘗試在降低CPM與提高可視性之間取得平衡。 | 市場活動類型：品牌<br><br>基準：高效CPM和最高vCPM<br><br>廣告類型：預卷、顯示<br><br><b>注：</b> 利用此目標實現盡可能最佳的vCPM。<br><br>要確保最大CPM，請將其用作放置的最大標價。 |
| [!UICONTROL Lowest vCPM (Adobe - MRC)] | 通過一攬子優化，預算分配將優先安排最低的vCPM.<br><br>拍賣評估將優先考慮vCPM。 如果支出目標得到實現，DSP那麼將嘗試在降低CPM與提高可視性之間取得平衡。 | 市場活動類型：品牌<br><br>基準：高效CPM和最高vCPM<br><br>廣告類型：預卷、顯示<br><br><b>注：</b> 利用此目標實現盡可能最佳的vCPM。<br><br>要確保最大CPM，請將其用作放置的最大標價。 |
| [!UICONTROL Lowest vCPM (IAS - MRC)] | 通過一攬子優化，預算分配將優先安排最低的vCPM.<br><br>拍賣評估將優先考慮vCPM。 如果支出目標得到實現，DSP那麼將嘗試在降低CPM與提高可視性之間取得平衡。 | 市場活動類型：品牌<br><br>基準：高效CPM和最高vCPM<br><br>廣告類型：預卷、顯示<br><br><b>注：</b> 利用此目標實現盡可能最佳的vCPM。<br><br>要確保最大CPM，請將其用作放置的最大標價。<br><br>當來自IAS的第三方資料通知算法時，此設定最有效。 僅當為市場活動啟用了IAS整合時才使用此目標。 |
| [!UICONTROL Lowest vCPM (Moat - GroupM)] | 通過一攬子優化，預算分配將優先安排最低的vCPM.<br><br>拍賣評估將優先考慮vCPM。 如果支出目標得到實現，DSP那麼將嘗試在降低CPM與提高可視性之間取得平衡。 | 市場活動類型：品牌<br><br>基準：高效CPM和最高vCPM<br><br>廣告類型：預卷、顯示<br><br><b>注：</b> 利用此目標實現盡可能最佳的vCPM。<br><br>要確保最大CPM，請將其用作放置的最大標價。<br><br>此設定在來自的第三方資料 [!DNL Moat] 正在通知算法。 僅當啟用 [!DNL Moat] 整合活動。 |
| [!UICONTROL Lowest vCPM (Moat - MRC)] | 通過一攬子優化，預算分配將優先安排最低的vCPM.<br><br>拍賣評估將優先考慮vCPM。 如果支出目標得到實現，DSP那麼將嘗試在降低CPM與提高可視性之間取得平衡。 | 市場活動類型：品牌<br><br>基準：高效CPM和最高vCPM<br><br>廣告類型：預卷、顯示<br><br><b>注：</b> 利用此目標實現盡可能最佳的vCPM。<br><br>要確保最大CPM，請將其用作放置的最大標價。<br><br>此設定在來自的第三方資料 [!DNL Moat] 正在通知算法。 僅當啟用 [!DNL Moat] 整合活動。 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [設定績效活動的最佳做法](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [位置級預投標過濾器及其使用方法](optimization-pre-bid-filters.md)
>* [市場活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)

