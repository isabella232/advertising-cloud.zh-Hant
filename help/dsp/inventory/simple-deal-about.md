---
title: 關於 [!UICONTROL Simple Ad Serving]
description: 瞭解 [!UICONTROL Simple Ad Serving] 使用事件跟蹤像素的交易。
feature: DSP Simple Ad Serving
exl-id: d65d1d8e-4d10-4d1d-86d3-f4457c29ae8d
source-git-commit: 05578e9252f0eec6dd4e003d317742007edb3351
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# 關於 [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] 為指定的發佈者和單個廣告類型提供有保證的、未決定的廣告交付和報告，使用單個專用位置。 使用 [!DNL Simple Ad Serving] 當您的發行商無法通過交易ID執行交易時。 所有目標、預算調整和上限設定以及頻率上限設定都由發佈者處理。 通過事件跟蹤像素執行這些交易。

與 [!UICONTROL Simple Ad Serving]每個廣告都由發佈者（站點服務者）直接提供，並DSP提供一個事件跟蹤像素發送給發佈者，發佈者需要實現像素並傳DSP送廣告。 根據清單類型，事件像素測量印象、點擊和視頻播放事件。

以下廣告類型可用：

* 台式機標準預卷
* 平板電腦和移動標準預卷
* 連接電視標準預卷
* 顯示
* 音頻

可以建立 [!UICONTROL Simple Ad Serving] 交易 [!UICONTROL Inventory] > [!UICONTROL Deals] 的子菜單。 自DSP動生成子類型為「」的放置[!DNL Simple ad serving]」。 該安排以交易為目標，但不允許進行更多目標、預算或頻率限制。 您只能編輯某些交易設定，如交易名稱、CPM、印象和航班日期。<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving] 配售不符合客戶的可用資金或市場活動和一攬子預算。 但是，支出會被跟蹤並計入這些預算。 即使CPM為0美元，也始終會跟蹤事件資料。

>[!MORELIKETHIS]
>
>* [建立 [!UICONTROL Simple Ad Serving] 交易](simple-deal-create.md)
>* [[!UICONTROL Simple Ad Serving] 設定](simple-deal-settings.md)
>* [查看事件跟蹤像素 [!UICONTROL Simple Ad Serving] 交易](simple-deal-show-pixels.md)

