---
title: 最佳化目標及其使用方式
description: 參考可用的最佳化目標，並查看其使用時機。
feature: DSP Optimization
exl-id: 9bca09b5-9aa7-4009-a576-9b30cfddfd55
source-git-commit: 75ec6f54271542d56e0d16fbb7aa92ebcf00d765
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 最佳化目標及其使用方式

| 最佳化目標 | 說明 | 何時使用此目標 |
| -----------| ---------- | ---------- |
| [!UICONTROL Always Max Bid & Highest Clickthrough Rate] | 透過套件層級最佳化，預算分配會以最高點進率來排列版位優先順序。<br><br>如果支出目標實現，拍賣評估將優先處理CTR。提交的出價一律為[!UICONTROL Max Bid]設定，但如果投放投入良好，預計的CTR臨界值將變得更嚴格。 | 促銷活動類型：品牌推廣<br><br>基準：最高點進率<br><br>廣告類型：前段、顯示<br><br><b>注意：</b>如果您有不需要超越的固定CPM目標和需要最大化的CTR目標，請使用此目標。 將「最高競價」設為所需的CPM目標，DSP在嘗試花費全部預算時，會達到最佳的CTR。 |
| [!UICONTROL Always Max Bid & Highest Completion Rate] | 在套件層級最佳化中，預算分配會以最高完成率來排列版位優先順序。<br><br>如果支出目標達到，拍賣評估將優先處理完成率。提交的出價一律為設定的「最高出價」，但如果刊登版位花費不錯，預計的「完成率」臨界值將會更嚴格。 | 促銷活動類型：品牌推廣<br><br>基準：最高完成率<br><br>廣告類型：僅前段<br><br><b>注意：</b>如果您有不需要超越的固定CPM目標和需要最大化的完成率目標，請使用此目標。 將「最高競價」設為所需的CPM目標，DSP在嘗試花費全部預算時，會達到盡可能最佳的完成率。 |
| [!UICONTROL Always Max Bid & Highest Engagement Rate] | 透過套件層級最佳化，預算分配會以最高參與率來排列版位優先順序。<br><br>如果支出目標實現，拍賣評估將優先處理參與率。提交的出價將始終是設定的「最高出價」，但如果投資方案支出良好，預計的參與率閾值將變得更加嚴格。 | 促銷活動類型：品牌推廣<br><br>基準：最高參與率<br><br>廣告類型：僅限行動插入式連結<br><br><b>注意：</b>如果您有不需要超越的固定CPM目標以及需要最大化的參與目標，請使用此目標。 將「最高競價」設為所需的CPM目標，DSP將在嘗試花費完整預算時達到最佳的參與率。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (Adobe – GroupM)] | 透過套件層級最佳化，預算分配會以最高可檢視率來排列版位優先順序。<br><br>如果支出目標達到，拍賣評估將優先考慮可見度。提交的出價一律為設定的「最高出價」，但如果刊登版位花費不錯，預計的可見度臨界值會更嚴格。 | 促銷活動類型：品牌推廣<br><br>基準：最高可檢視率<br><br>廣告類型：僅互動式前段<br><br><b>注意：</b>此目標將一律使用版位層級的「最高競價」。<br><br>如果促銷活動的「可見度」設定設為「標準」（連續2秒檢視廣告的50%），則促銷活動會使用媒體評等委員會(MRC)可見度測量標準。如果促銷活動設為「嚴格（50%持續期間內檢視和音訊的廣告100%）」，則促銷活動會使用GroupM可見度測量標準。 理想情況下，您應將促銷活動設定與最佳化目標及出價前篩選設定相符。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (Adobe – MRC)] | 透過套件層級最佳化，預算分配會以最高可檢視率來排列版位優先順序。<br><br>如果支出目標達到，拍賣評估將優先考慮可見度。提交的出價一律為設定的「最高出價」，但如果刊登版位花費不錯，預計的可見度臨界值會更嚴格。 | 促銷活動類型：品牌推廣<br><br>基準：最高可檢視率<br><br>廣告類型：僅互動式前段<br><br><b>注意：</b>此目標將一律使用版位層級的「最高競價」。<br><br>如果促銷活動的「可見度」設定設為「標準」（連續2秒檢視廣告的50%），則促銷活動會使用媒體評等委員會(MRC)可見度測量標準。如果促銷活動設為「嚴格（50%持續期間內檢視和音訊的廣告100%）」，則促銷活動會使用GroupM可見度測量標準。 理想情況下，您應將促銷活動設定與最佳化目標及出價前篩選設定相符。 |
| [!UICONTROL Always Max Bid & Highest Viewability Rate (IAS – MRC)] | 透過套件層級最佳化，預算分配會以最高可檢視率來排列版位優先順序。<br><br>如果支出目標達到，拍賣評估將優先考慮可見度。提交的出價一律為設定的「最高出價」，但如果刊登版位花費不錯，預計的可見度臨界值會更嚴格。 | 促銷活動類型：品牌推廣<br><br>基準：最高可檢視率<br><br>廣告類型：僅互動式前段<br><br><b>注意：</b>此目標將一律使用版位層級的「最高競價」。<br><br>當來自IAS的第三方資料通知演算法時，此設定最有效。只有在已為促銷活動啟用IAS整合時，才使用此目標。 |
| [!UICONTROL Highest ROAS – Custom Goal] | （僅適用於套件層級）預算分配會優先處理廣告投入報酬率最高(ROAS)的刊登版位。<br><br>拍賣評估將優先處理ROAS。如果支出目標已達成，DSP將平衡降低CPM與提高ROAS。 | 促銷活動類型：效能<br><br>基準：最高收入<br><br>廣告類型：顯示<br><br><b>注意：</b>如需詳細資訊，請參閱「設定效能促銷活動的最佳實務」。 |
| [!UICONTROL Lowest CPA – Custom Goal] | （僅適用於套件層級）預算分配將優先處理CPA最低的版位。<br><br>拍賣評估將優先考慮註冊會計師。如果支出目標已達成，DSP將在降低CPM與降低CPA之間取得平衡。 | 促銷活動類型：效能<br><br>基準：最低CPA<br><br>廣告類型：顯示<br><br><b>注意：</b>如需詳細資訊，請參閱「設定效能促銷活動的最佳實務」。 |
| [!UICONTROL Lowest Cost Per Click] | 透過套件層級最佳化，預算分配會以最低CPC來排定版位優先順序。<br><br>拍賣評估將優先考慮中油。如果支出目標已達成，DSP將平衡降低CPM與提高CTR以嘗試降低CPC。 | 促銷活動類型：品牌推廣<br><br>基準：有效CPM和最高點進率<br><br>廣告類型：前段、顯示<br><br><b>注意：</b>使用此目標來達成最佳可能的CPC。 若要保證最大CPM，請將其用作版位的「最高競價」。 |
| [!UICONTROL Lowest Cost Per Completion] | 在套件層級最佳化中，預算分配將以最低的每次完成成本排列位置優先順序。<br><br>拍賣評估將優先處理視訊完成率(VCR)。如果支出目標正在實現，DSP將在降低CPM與增加VCR之間取得平衡，以降低每次完成的成本。 | 促銷活動類型：品牌推廣<br><br>基準：有效CPM和最高完成率<br><br>廣告類型：僅限前段 |
| [!UICONTROL Lowest Cost Per Engagement] | 透過套件層級最佳化，預算分配會以最低的參與率來排定刊登版位優先順序。<br><br>拍賣評估將優先考慮參與率。如果支出目標正在實現，DSP將嘗試在降低CPM與降低每次參與成本之間取得平衡。 | 促銷活動類型：品牌推廣<br><br>基準：有效CPM和最高參與率<br><br>廣告類型：僅限行動插入式 |
| [!UICONTROL Lowest CPM] | 透過套件層級最佳化，預算分配會以最低的CPM優先排列版位。<br><br>拍賣評估會優先處理CPM。如果支出目標已達成，則DSP會逐步降低CPM。 | 促銷活動類型：品牌推廣<br><br>基準：有效的CPM<br><br>廣告類型：前段、顯示、CTV、原生、音訊 |
| [!UICONTROL Lowest Cost Per View] | 操作方式與最低CPM類似。 透過套件層級最佳化，預算分配會以最低的CPM優先排列版位。<br><br>拍賣評估會優先處理CPM。如果支出目標已達成，則DSP會逐步降低CPM。 | 促銷活動類型：品牌推廣<br><br>基準：有效CPM和最高點進率<br><br>廣告類型：前段、顯示 |
| [!UICONTROL Lowest vCPM (Adobe - GroupM)] | 透過套件層級最佳化，預算分配會以最低的vCPM優先排列版位。<br><br>拍賣評估會優先處理vCPM。如果支出目標已達成，DSP將嘗試在降低CPM與提高可檢視性之間取得平衡。 | 促銷活動類型：品牌推廣<br><br>基準：有效的CPM和最高vCPM<br><br>廣告類型：前段、顯示<br><br><b>注意：</b>使用此目標來達成最佳的vCPM。<br><br>若要保證最大CPM，請將其用作版位的「最高競價」。 |
| [!UICONTROL Lowest vCPM (Adobe - MRC)] | 透過套件層級最佳化，預算分配會以最低的vCPM優先排列版位。<br><br>拍賣評估會優先處理vCPM。如果支出目標已達成，DSP將嘗試在降低CPM與提高可檢視性之間取得平衡。 | 促銷活動類型：品牌推廣<br><br>基準：有效的CPM和最高vCPM<br><br>廣告類型：前段、顯示<br><br><b>注意：</b>使用此目標來達成最佳的vCPM。<br><br>若要保證最大CPM，請將其用作版位的「最高競價」。 |
| [!UICONTROL Lowest vCPM (IAS - MRC)] | 透過套件層級最佳化，預算分配會以最低的vCPM優先排列版位。<br><br>拍賣評估會優先處理vCPM。如果支出目標已達成，DSP將嘗試在降低CPM與提高可檢視性之間取得平衡。 | 促銷活動類型：品牌推廣<br><br>基準：有效的CPM和最高vCPM<br><br>廣告類型：前段、顯示<br><br><b>注意：</b>使用此目標來達成最佳的vCPM。<br><br>若要保證最大CPM，請將其用作版位的「最高競價」。<br><br>當來自IAS的第三方資料通知演算法時，此設定最有效。只有在已為促銷活動啟用IAS整合時，才使用此目標。 |
| [!UICONTROL Lowest vCPM (Moat - GroupM)] | 透過套件層級最佳化，預算分配會以最低的vCPM優先排列版位。<br><br>拍賣評估會優先處理vCPM。如果支出目標已達成，DSP將嘗試在降低CPM與提高可檢視性之間取得平衡。 | 促銷活動類型：品牌推廣<br><br>基準：有效的CPM和最高vCPM<br><br>廣告類型：前段、顯示<br><br><b>注意：</b>使用此目標來達成最佳的vCPM。<br><br>若要保證最大CPM，請將其用作版位的「最高競價」。<br><br>當來自協力廠商的資料通知演算法時，此 [!DNL Moat] 設定的運作效果最佳。只有在已為促銷活動啟用[!DNL Moat]整合時，才使用此目標。 |
| [!UICONTROL Lowest vCPM (Moat - MRC)] | 透過套件層級最佳化，預算分配會以最低的vCPM優先排列版位。<br><br>拍賣評估會優先處理vCPM。如果支出目標已達成，DSP將嘗試在降低CPM與提高可檢視性之間取得平衡。 | 促銷活動類型：品牌推廣<br><br>基準：有效的CPM和最高vCPM<br><br>廣告類型：前段、顯示<br><br><b>注意：</b>使用此目標來達成最佳的vCPM。<br><br>若要保證最大CPM，請將其用作版位的「最高競價」。<br><br>當來自協力廠商的資料通知演算法時，此 [!DNL Moat] 設定的運作效果最佳。只有在已為促銷活動啟用[!DNL Moat]整合時，才使用此目標。 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [設定效能行銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [版位層級出價前篩選器及其使用方法](optimization-pre-bid-filters.md)
>* [促銷活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)

