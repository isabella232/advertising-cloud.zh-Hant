---
title: 向 [!DNL FreeWheel]提交PG交易的廣告
description: 了解如何向FreeWheel上的發佈商申請程式化保證廣告的核准。
feature: Private Inventory, Deal IDs
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# 向FreeWheel提交程式化保證交易的廣告

*僅具有程式 [!DNL FreeWheel] 保證權限的帳戶*

一旦您[接受FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)上與發佈商進行的程式化保證交易（包括選擇廣告和建立用於交易的程式化保證預設位置），您必須將廣告提交給FreeWheel進行批准。

>[!PREREQUISITES]
>
>與您的Adobe帳戶團隊合作，確保您的[!DNL DSP]帳戶擁有使用[!DNL FreeWheel]程式化保證工作流程的權限。

1. 複製與FreeWheel交易搭配使用之廣告的廣告金鑰：

   1. 按一下促銷活動的名稱。

   1. 在子菜單中，按一下&#x200B;**[!UICONTROL Ads]**。

   1. 按一下廣告名稱旁的&#x200B;**[!UICONTROL ...]>[!UICONTROL Edit]**。

   1. 開啟廣告設定後，複製瀏覽器位址列所顯示URL中的英數字元廣告金鑰。

      例如，在下列URL中，廣告索引鍵為`3NtNC5ZbaGZtqbei8jD3`

      `https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads`

1. 將廣告提交至FreeWheel:

   1. 在[!UICONTROL Deals]檢視中，找出交易。

   1. 在交易行中，按一下![選項菜單](/help/dsp/assets/options-menu.png) **>[!UICONTROL submit to [!DNL FreeWheel]]**。

   1. 驗證交易ID，輸入在步驟1中複製的&#x200B;**[!UICONTROL Ad Key]**，然後按一下&#x200B;**[!UICONTROL Submit]**。

   廣告必須先提交並核准，才能執行。

1. [檢查廣告提交狀態](freewheel-check-status.md)。

>[!MORELIKETHIS]
>
>* [在FreeWheel中建立程式保證交易概述](freewheel-overview.md)
>* [在交易ID收件匣中接受交易](deal-id-inbox-accept.md)
>* [檢查程式化保證交 [!DNL FreeWheel] 易的廣告狀態](freewheel-check-status.md)
>* [FreeWheel廣告提交的錯誤代碼](freewheel-error-codes.md)

