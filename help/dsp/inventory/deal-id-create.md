---
title: 手動建立交易ID詳細資訊
description: 了解如何手動輸入交易ID的詳細資訊。
feature: Private Inventory, Deal IDs
exl-id: cd9763a7-99d4-4881-9df9-b4e24c55be0f
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# 手動建立交易ID詳細資訊

1. 在主菜單中，按一下「**[!UICONTROL Inventory]> [!UICONTROL Deals]」。**

1. 在資料表上，按一下&#x200B;**[!UICONTROL Create]**，然後選擇&#x200B;**[!UICONTROL Deal ID]**。

1. 輸入[交易設定](deal-id-settings.md):

   1. 在[!UICONTROL Deal ID basics]區段中，指定可存取交易的交易詳細資訊和廣告商。 對於有保證的交易，您還必須指定計畫的投放日期和估計的曝光數，僅用於追蹤目的。

   1. (僅管理員用戶；可選)在[!UICONTROL Technical]區段中，視需要編輯預設設定。

   1. 按一下 **[!UICONTROL Save]**.

1. （僅限保證交易）選取將用於交易的廣告，並建立預設的程式化保證(PG)位置。

   預設PG版位可確保您的交易一律會針對每個競標請求傳回出價。 如果您未建立預設的PG版位，則任何以交易為目標的版位，除非正確設定，否則不會出價。 您應一律建立預設的PG位置。 在[!UICONTROL Placements]檢視中，預設PG版位的欄位值為「[!UICONTROL PG Default]」。[!UICONTROL Sub-type]

   您可以選擇在附加版位中將交易用作庫存目標，但必須正確設定它們才能進行競標。

   1. 在[!UICONTROL Ad & Campaign Selection]設定中，選取將用於交易的廣告：

      1. 選取廣告商、促銷活動和廣告類型。

      1. 從可用廣告清單中，選取將用於交易的每個廣告旁的核取方塊。

      1. 按一下 **[!UICONTROL Apply]**.
   1. 在位置設定畫面中：

      1. 輸入版位名稱。

      1. （選用）編輯[版位設定](/help/dsp/campaign-management/placements/placement-settings.md)，包括覆寫預設出價，該出價會自動填入交易的CPM值；變更日期範圍；或附加更多廣告。

      在「庫存目標」部分自動定位交易。 所有其他定位選項皆不適用。

      1. 按一下 **[!UICONTROL Create placement]**.



建立交易後，您可以將交易用作多個版位的庫存目標。

>[!NOTE]
>
> 您不需要將交易標籤傳送給發佈商進行驗證。

>[!TIP]
>
>* 在[!UICONTROL Inventory] > [!UICONTROL Deals]檢視中， [!UICONTROL Pacing & Budget]欄顯示交易如何步調至指定的投放日期和曝光目標。
>
>* 如果傳送進度不佳或過於謹慎，請連絡您的發行商，以調整透過交易傳送的數量。


>[!MORELIKETHIS]
>
>* [手動交易ID設定](deal-id-settings.md)
>* [設定程式化保證交易](programmatic-guaranteed-set-up.md)
>* [提交程式保證交易的廣告 [!DNL FreeWheel]](freewheel-submit.md)
>* [關於程式化保證交易](programmatic-guaranteed-about.md)

