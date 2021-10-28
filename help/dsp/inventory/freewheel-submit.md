---
title: 提交PG交易的廣告以 [!DNL FreeWheel]
description: 了解如何向FreeWheel上的發佈商申請程式化保證廣告的核准。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: null
source-git-commit: c2caed80f0afc0cbe3572d01dc2c89f13ed13712
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 向FreeWheel提交程式化保證交易的廣告

*帳戶 [!DNL FreeWheel] 僅限程式保證權限*

一旦您 [接受與FreeWheel上的發佈商進行程式化保證的交易](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)，包括選取廣告和建立要用於交易的程式化保證預設位置，您必須將廣告提交至FreeWheel進行核准。

>[!PREREQUISITES]
>
>與您的 [!DNL Adobe] 帳戶團隊，確保您的 [!DNL DSP] 帳戶有權使用 [!DNL FreeWheel] 程式化保證的工作流程。

## 複製廣告金鑰以搭配 [!DNL FreeWheel] 交易 {#copy-ad-key}

1. 按一下促銷活動的名稱。

1. 在子菜單中，按一下 **[!UICONTROL Ads]**.

1. 按一下  **[!UICONTROL ...]>[!UICONTROL Edit]** 廣告名稱旁邊。

1. 開啟廣告設定後，複製瀏覽器位址列所顯示URL中的英數字元廣告金鑰。

例如，在下列URL中，廣告索引鍵為 `3NtNC5ZbaGZtqbei8jD3`

`https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads`

## 從 [!UICONTROL Ads] 檢視

1. [複製廣告的廣告金鑰](#copy-ad-key).

1. 在廣告名稱旁，按一下  **[!UICONTROL ...]>[!UICONTROL submit to FreeWheel]**.

1. 驗證交易ID，請輸入 [the **[!UICONTROL Ad Key]**](#copy-ad-key)，然後按一下&#x200B;**[!UICONTROL Submit]**.

   廣告必須先提交並核准，才能執行。

1. [檢查廣告提交狀態](freewheel-check-status.md).

## 從 [!UICONTROL Deals] 檢視

1. [複製廣告的廣告金鑰](#copy-ad-key).

1. 在主功能表中，按一下 **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. 在交易列中，按一下 ![選項功能表](/help/dsp/assets/options-menu.png) **>[!UICONTROL submit to FreeWheel]**.

1. 驗證交易ID，請輸入 [the **[!UICONTROL Ad Key]**](#copy-ad-key)，然後按一下&#x200B;**[!UICONTROL Submit]**.

   廣告必須先提交並核准，才能執行。

1. [檢查廣告提交狀態](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [在FreeWheel中建立程式保證交易概述](freewheel-overview.md)
>* [在交易ID收件匣中接受交易](deal-id-inbox-accept.md)
>* [檢查廣告的狀態 [!DNL FreeWheel] 程式化保證交易](freewheel-check-status.md)
>* [FreeWheel廣告提交的錯誤代碼](freewheel-error-codes.md)

