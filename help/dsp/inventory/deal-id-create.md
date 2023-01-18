---
title: 手動建立交易ID詳細資訊
description: 了解如何手動輸入交易ID的詳細資訊。
feature: DSP Private Inventory, DSP Deal IDs
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# 手動建立交易ID詳細資訊

1. 在主功能表中，按一下 **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. 在資料表格上方，按一下 **[!UICONTROL Create]**，然後選取 **[!UICONTROL Deal ID]**.

1. 輸入 [交易設定](deal-id-settings.md):

   1. 在 [!UICONTROL Deal ID basics] 區段中，指定交易詳細資訊以及可存取交易的廣告商。 對於有保證的交易，您還必須指定計畫的投放日期和估計的曝光次數，僅用於追蹤目的。

   1. (僅管理員用戶；選用)在 [!UICONTROL Technical] 區段，視需要編輯預設設定。

   1. 按一下 **[!UICONTROL Save]**.

1. （僅限保證交易）選取要用於交易的廣告，並建立預設的程式化保證(PG)位置。

   預設PG版位可確保您的交易一律會針對每個競標請求傳回競標。 如果您未建立預設的PG版位，則任何以交易為目標的版位都不會出價，除非設定正確。 您應一律建立預設的PG位置。 在 [!UICONTROL Placements] 檢視，預設PG版位具有 [!UICONTROL Sub-type] 列值&quot;[!UICONTROL PG Default].&quot;

   您可以選擇在附加版位中將交易用作庫存目標，但必須正確設定它們才能進行競標。

   1. 在 [!UICONTROL Ad & Campaign Selection] 設定中，選擇用於交易的廣告：

      1. 選取廣告商、促銷活動和廣告類型。 （可選）選擇要據以篩選廣告的廣告狀態。

      1. 從可用廣告清單中，選取用於交易的每個廣告旁的核取方塊。

      1. 按一下 **[!UICONTROL Apply]**.
   1. 在位置設定畫面中：

      1. 輸入版位名稱。

      1. （選用）編輯 [版位設定](/help/dsp/campaign-management/placements/placement-settings.md)，包括覆寫預設出價，該出價會自動填入交易的CPM值；變更日期範圍；或附加更多廣告。

      在「庫存目標」部分自動定位交易。 所有其他定位選項皆不適用。

      1. 按一下 **[!UICONTROL Create placement]**.



建立交易後，您可以將交易用作多個版位的庫存目標。

>[!NOTE]
>
> 您不需要將交易標籤傳送給發佈商進行驗證。

>[!TIP]
>
>* 在 [!UICONTROL Inventory] > [!UICONTROL Deals] 檢視， [!UICONTROL Pacing & Budget] 欄顯示交易進度如何達到指定的飛行日期和曝光目標。
>
>* 如果傳送進度不佳或過於謹慎，請連絡您的發行商，以調整透過交易傳送的數量。


>[!MORELIKETHIS]
>
>* [手動交易ID設定](deal-id-settings.md)
>* [設定程式化保證交易](programmatic-guaranteed-set-up.md)
>* [提交程式保證交易的廣告 [!DNL FreeWheel]](freewheel-submit.md)
>* [關於程式化保證交易](programmatic-guaranteed-about.md)

<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->