---
title: 重複版位
description: 了解如何複製一或多個版位。
feature: DSP Placements
exl-id: d22a61a8-4f1b-41ee-b4fb-3124bec81a2f
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%

---

# 重複版位

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

複製一或多個版位以建立具有類似設定的版位。 您可以：

* 製作多個版位重複項目
* 在原始廣告商和促銷活動內或不同廣告商和促銷活動內復製版位
* （適用於原始促銷活動內的重複版位）（可選）複製原始廣告
* 修改新版位的狀態和投放日期

如需未重複之版位設定清單，請參閱「[未重複的項目](#placement-not-duplicated)」。

1. 在主菜單中，按一下&#x200B;**[!UICONTROL Campaigns]**。
1. 按一下促銷活動的名稱。
1. 在子菜單中，按一下&#x200B;**[!UICONTROL Placements]**。
1. 執行下列任一操作：
   * 要複製一個位置，請按一下包名稱旁的&#x200B;**[!UICONTROL ...]>[!UICONTROL Duplicate]**。
   * 若要複製多個版位：
      1. 選取每個要複製之版位旁的核取方塊。
      1. 在批量操作工具欄中，按一下&#x200B;**[!UICONTROL Duplicate]**。
1. 指定新版位設定：
   1. （單一版位）輸入新版位名稱。
   1. 在&#x200B;**[!UICONTROL Choose Package (Required)]**&#x200B;菜單中，選擇父包或**[!UICONTROL No package]*。
   1. （選用）變更預設設定。

   設定會套用至所有選取的版位。

   依預設，新版位會用於原始廣告類型、指派給原始廣告商和行銷活動、有從當天開始的航班排程、已暫停，且不包含原始廣告。

   建立多個版位時，新版位名稱會依序使用慣例&lt;*original_placement_name #N*>附加一個數字，例如「我的版位#2」。

1. 按一下 **[!UICONTROL Submit]**.

## 未重複的項目 {#placement-not-duplicated}

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
>* [關於版位管理](placement-about.md)
>* [建立版位](placement-create.md)
>* [編輯位置](placement-edit.md)
>* [版位設定](placement-settings.md)

