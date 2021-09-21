---
title: 複製促銷活動
description: 了解如何複製行銷活動。
feature: DSP Campaigns
exl-id: 2bb4030d-22b0-4a16-aeed-35f64a19df6a
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# 複製促銷活動

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

複製促銷活動以建立具有類似設定的新促銷活動。 您可以：

* 複製原始廣告商或不同廣告商的促銷活動
* （可選）複製原始包和版位
* 修改新促銷活動的投放日期

如需未重複之版位設定清單，請參閱「[未重複的項目](#campaign-not-duplicated)」。

1. 在主菜單中，按一下&#x200B;**[!UICONTROL Campaigns]**。
1. 在促銷活動名稱旁，按一下&#x200B;**... >[!UICONTROL Duplicate]**。
1. 指定新的促銷活動設定：
   1. 輸入新促銷活動名稱和結束投放日期。
   1. （選用）變更預設設定。

      依預設，新促銷活動會指派給原始廣告商、有從當天開始的投放排程，且包含原始的套件和版位。

1. 按一下 **[!UICONTROL Submit]**.

## 未重複的項目 {#campaign-not-duplicated}

原始版位中的所有設定都會重複，但是：

* 實驗設定
* （如果您變更投放日期）自訂廣告排程
* （若未附加廣告）自訂廣告加權和排程
* 程式化保證(PG)交易的預設刊登版位和[!UICONTROL Simple Ad Serving]交易的刊登版位
* （如果您將版位複製到不同的促銷活動）:
   * 地理目標
   * 事件像素
   * 廣告
   * 版位層級[!DNL DoubleVerify Authentic Brand Safety]區段（會覆寫廣告商層級區段）

>[!MORELIKETHIS]
>
>* [關於促銷活動管理](campaign-about.md)
>* [建立促銷活動](campaign-create.md)
>* [編輯促銷活動](campaign-edit.md)
>* [促銷活動設定](campaign-settings.md)

