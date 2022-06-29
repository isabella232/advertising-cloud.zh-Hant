---
title: 手動建立交易ID詳細資訊
description: 瞭解如何手動輸入交易ID的詳細資訊。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: cd9763a7-99d4-4881-9df9-b4e24c55be0f
source-git-commit: 39f491a39bdc9d8dd820eb4c69594dda71d8b3c2
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# 手動建立交易ID詳細資訊

1. 在主菜單中，按一下 **[!UICONTROL Inventory]> [!UICONTROL Deals]。**

1. 在資料表上方，按一下 **[!UICONTROL Create]**，然後選擇 **[!UICONTROL Deal ID]**。

1. 輸入 [交易設定](deal-id-settings.md):

   1. 在 [!UICONTROL Deal ID basics] 部分，指定交易詳細資訊和可以訪問交易的廣告商。 對於有保證的交易，您還必須指定計畫的飛行日期和估計的印數，以僅用於跟蹤目的。

   1. (僅限管理員用戶；可選) [!UICONTROL Technical] 編輯預設設定。

   1. 按一下 **[!UICONTROL Save]**.

1. （僅限保證交易）選擇要用於交易的廣告，並建立預設的計畫保證(PG)放置。

   預設的PG設定可確保您的交易始終為每個投標請求返回投標。 如果您未建立預設的PG放置，則任何以此交易為目標的放置都不會進行出價，除非它們設定正確。 應始終建立預設PG放置。 在 [!UICONTROL Placements] 視圖，預設PG放置 [!UICONTROL Sub-type] 列值&quot;[!UICONTROL PG Default]&quot;

   您可以根據需要將交易用作附加配售中的庫存目標，但必須正確設定它們才能進行投標。

   1. 在 [!UICONTROL Ad & Campaign Selection] 設定，選擇將用於交易的廣告：

      1. 選擇廣告商、市場活動和廣告類型。 （可選）選擇用於篩選廣告的廣告狀態。

      1. 從可用廣告清單中，選中每個廣告旁邊的複選框以用於交易。

      1. 按一下 **[!UICONTROL Apply]**.
   1. 在放置設定螢幕中：

      1. 輸入放置名稱。

      1. （可選）編輯 [放置設定](/help/dsp/campaign-management/placements/placement-settings.md)包括覆蓋預設投標，該預設投標自動填入交易中的CPM值；更改日期範圍；或者附加更多廣告。

      該交易在「庫存目標」部分中自動成為目標。 所有其他目標選項均不適用。

      1. 按一下 **[!UICONTROL Create placement]**.



建立交易後，您可以將交易用作多次投放的庫存目標。

>[!NOTE]
>
> 您不需要將交易標籤發送給發佈者以進行驗證。

>[!TIP]
>
>* 在 [!UICONTROL Inventory] > [!UICONTROL Deals] 的 [!UICONTROL Pacing & Budget] 列顯示交易如何向指定的飛行日期和印象目標前進。
>
>* 如果交付時間不足或過長，請聯繫您的發行商，以調整它通過交易發送的數量。


>[!MORELIKETHIS]
>
>* [手動交易ID設定](deal-id-settings.md)
>* [設定計畫保證交易](programmatic-guaranteed-set-up.md)
>* [提交廣告，用於計畫保證處理 [!DNL FreeWheel]](freewheel-submit.md)
>* [關於寫程式擔保交易](programmatic-guaranteed-about.md)

<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->