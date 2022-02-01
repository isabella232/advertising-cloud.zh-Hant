---
title: 如何優DSP化您的市場活動
description: 瞭解如何DSP優化您的市場活動中的包。
feature: DSP Optimization
exl-id: 054582ef-b677-4725-b25c-b82bf3e5b43e
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# 如何優DSP化您的市場活動

本頁概述了如何使用Advertising Cloud DSP優化引擎 [!DNL Adobe Sensei]，優化市場活動中的包。 有關如何手動優化活動的提示和技巧，請與 [!DNL Adobe] 客戶團隊。 <!-- add link to trading playbook if we add it to help -->

包優化目標在兩個級別運行：

* 對於每個包：根DSP據職位安排的績效，根據所選KPI將預算分配給包內的每個職位。

* 對於包中的每次放置/拍賣：計DSP算每次拍賣的每次投放的即時經濟KPI值，然後使用此值確定投標。

   >[!NOTE]
   >
   >經濟價值可以根據投資支出的好壞進行重大加權。 如果一家公司的投資目標落後，它將獲准購買質量較低的拍賣品。 如果一家公司能輕鬆實現其支出目標，那麼它將專注於質量更高的拍賣。

## 包優化

可以DSP通過兩種基本方式優化交付，20種變體可以與您的特定效能目標保持一致。 您可以選擇：

* 優先設定效能率

* 將成本效率與效能率進行優先平衡

請參閱 [優化目標及其使用方法](optimization-goals.md) 確定哪個優化目標將幫助您實現KPI。

### 優先設定效能率的包

對於優化目標，將效能率排DSP在優先位置，預測每次拍賣的效能，並始終以最大出價進行出價。 適用的優化目標示例包括 [!UICONTROL Highest Viewability Rate]。 [!UICONTROL Highest Clickthrough Rate]等等。

如果：

* 您已經知道有效/可接受的CPM級別（例如，歷史基準）。

* 您願意手動調整 [!UICONTROL Max Bid] 在擴展方面遇到挑戰時，

* 你將規模置於效率之上。

#### 起步邏輯 {#pacing-logic-performance}

* 如果支出速度加快，競價將變得更加有選擇性，因此你只會在預計會有較高表現的拍賣會上投標。

* 如果支出落後於速度，競價將變得不那麼有選擇性，這樣你就會在拍賣會上競拍，預計拍賣會的表現會更低，以便趕上競拍的節奏。

#### 結算價格/投標底紋 {#clearing-price-performance}

在執行起步邏輯後，DSP通過清算價格預測模型運行建議的出價。 如果預測指示出價可以以對贏率的最小減小來降低，則根據預測來降低出價。

### 將成本效率與效能率進行優先平衡的軟體包

對於某些優化目DSP標，預測每次拍賣的表現並自動調整出價，從不超過配售價格 [!UICONTROL Max Bid]。 適用的優化目標示例包括 [!UICONTROL Lowest CPM]。 [!UICONTROL Lowest CPA]。 [!UICONTROL Lowest Cost per View]。 [!UICONTROL Lowest Cost per Click]等等。

#### 起步邏輯 {#pacing-logic-balanced}

* 如果支出速度加快，DSP價格就會變得更敏感，競標金額會降低，以利用起步計畫來換取贏率。

* 如果也平衡了績效指標(除非 [!UICONTROL Lowest CPM])，然後將預測的KPI混合到投標金額中。 因此，你會以更高的價格競拍拍賣，預計「每筆成本」的拍賣會將更有成效。

* 如果支出落後於速度，DSP那麼價格就變得不那麼敏感，出價更高，甚至 [!UICONTROL Max Bid]用起步計畫來取消贏率。

#### 結算價格/投標底紋 {#clearing-price-balanced}

在執行起步邏輯後，DSP通過清算價格預測模型運行建議的出價。 如果預測指示出價可以以對贏率的最小減小來降低，則根據預測來降低出價。

## 放置優化

放置預投標濾波器是確保高效能的最嚴格方法。 在不同DSP的廣告類型中策略性地使用預投標過濾器，以跨每個包中的放置實現效能目標。 您可以同時使用預投標過濾器與封裝級優化或獨立使用。

>[!NOTE]
>
>可用的預標過濾器因廣告類型而異。 例如，對於標準顯示放置，可以通過按一下穿透率和可查看性進行篩選，但不能通過完成率進行篩選。

請參閱 [位置級預投標過濾器及其使用方法](optimization-pre-bid-filters.md) 確定哪種預投標篩選器將幫助您實現KPI。

>[!MORELIKETHIS]
>
>* [包設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [放置設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [優化目標及其使用方法](optimization-goals.md)
>* [位置級預投標過濾器及其使用方法](optimization-pre-bid-filters.md)
>* [排除效能故障](/help/dsp/optimization/troubleshooting-performance.md)

