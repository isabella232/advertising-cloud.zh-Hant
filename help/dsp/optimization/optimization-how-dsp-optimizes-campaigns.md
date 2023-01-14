---
title: DSP如何最佳化您的行銷活動
description: 了解DSP如何最佳化行銷活動中的套件。
feature: DSP Optimization
exl-id: 054582ef-b677-4725-b25c-b82bf3e5b43e
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Advertising DSP如何最佳化您的行銷活動

本頁概述DSP最佳化引擎(由 [!DNL Adobe Sensei]，會最佳化行銷活動中的套件。 如需手動最佳化行銷活動的秘訣和技巧，請連絡您的 [!DNL Adobe] 客戶團隊。 <!-- add link to trading playbook if we add it to help -->

套件最佳化目標分兩個層級運作：

* 對於每個包：DSP會根據版位對所選KPI的效能，為套件內的每個版位分配預算。

* 對於包中的每個放置/拍賣：DSP會計算每次拍賣的即時經濟KPI值，然後使用此值來判斷出價。

   >[!NOTE]
   >
   >經濟價值可以根據投資安排支出的好壞進行重大加權。 如果某次拍賣低於其支出目標，那麼它將獲准購買質量較低的拍賣。 如果一次拍賣能輕鬆達到其支出目標，那麼它將專注於質量更高的拍賣。

## 封裝最佳化

DSP可透過兩種基本方式最佳化您的傳送，提供20種變數以符合您的特定效能目標。 您可以選擇：

* 優先處理效能率

* 優先確定平衡成本效率與效能率的優先順序

請參閱 [最佳化目標及其使用方式](optimization-goals.md) 來判斷哪個最佳化目標可協助您達成KPI。

### 將效能率排為優先順序的包

對於將績效率排為優先順序的最佳化目標，DSP會預測每次拍賣的績效，並一律在「最高競價」出價。 適用最佳化目標的範例包括 [!UICONTROL Highest Viewability Rate], [!UICONTROL Highest Clickthrough Rate]等。

此最佳化模式在下列情況下運作良好：

* 您已經知道有效/可接受的CPM層級（例如歷史基準）。

* 您願意手動調整 [!UICONTROL Max Bid] 針對每個版位，在擴充功能方面遇到挑戰。

* 你把規模置於效率之上。

#### 步調邏輯 {#pacing-logic-performance}

* 如果支出速度加快，競標將變得更加有選擇性，這樣，你只會對預期有較高表現率的拍賣進行競標。

* 如果支出落後於速度，競標將變得不那麼有選擇性，這樣，你就會在拍賣會上競標，因為預計拍賣的成績會更低，以趕上步調一致的目標。

#### 清除價格/出價底紋 {#clearing-price-performance}

在DSP執行步調邏輯後，透過清算價格預測模型執行建議的出價。 如果預測指示出價可以以對獲勝率的最小降低來降低，則根據預測來降低出價。

### 將成本效率與效能率進行優先平衡的軟體包

對於某些最佳化目標，DSP會預測每次拍賣的績效並自動調整出價，絕不會超過配售 [!UICONTROL Max Bid]. 適用最佳化目標的範例包括 [!UICONTROL Lowest CPM], [!UICONTROL Lowest CPA], [!UICONTROL Lowest Cost per View], [!UICONTROL Lowest Cost per Click]等。

#### 步調邏輯 {#pacing-logic-balanced}

* 如果支出速度加快，DSP就會變得更加敏感價格，以更低的價格來換取中獎率，與步調一致的計畫。

* 如果效能量度也處於平衡狀態(除 [!UICONTROL Lowest CPM])，則預計KPI會混合到競標金額中。 因此，你會以更高的價格競拍，而這些拍賣預計會以「每次成本」為基礎更有成效。

* 如果支出落後於速度，DSP就會變得對價格不那麼敏感，並出價更高，直到 [!UICONTROL Max Bid]，用步調計畫取代贏率。

#### 清除價格/出價底紋 {#clearing-price-balanced}

在DSP執行步調邏輯後，透過清算價格預測模型執行建議的出價。 如果預測指示出價可以以對獲勝率的最小降低來降低，則根據預測來降低出價。

## 放置最佳化

版位預先出價篩選是確保高效能的最嚴格方式。 DSP會在不同廣告類型間策略性地使用出價前篩選，以達成每個套件中不同版位的效能目標。 您可以同時使用預先出價篩選器與封裝層級最佳化，或單獨使用。

>[!NOTE]
>
>可用的競標前篩選條件會依廣告類型而異。 例如，對於標準顯示版位，您可以依點進率和可檢視性來篩選，但不能依完成率篩選。

請參閱 [版位層級出價前篩選器及其使用方法](optimization-pre-bid-filters.md) 來判斷哪個出價前篩選器能協助您達成KPI。

>[!MORELIKETHIS]
>
>* [套件設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [版位設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [最佳化目標及其使用方式](optimization-goals.md)
>* [版位層級出價前篩選器及其使用方法](optimization-pre-bid-filters.md)
>* [效能疑難排解](/help/dsp/optimization/troubleshooting-performance.md)

