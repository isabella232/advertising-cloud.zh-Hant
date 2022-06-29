---
title: 設定計畫保證交易
description: 瞭解如何設定您與發行商談判的計畫保證(PG)交易。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 9e371606-5428-4635-9653-7dc43449e489
source-git-commit: 39f491a39bdc9d8dd820eb4c69594dda71d8b3c2
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# 設定計畫保證交易

*[僅支援供應端平台](programmatic-guaranteed-about.md)*

在您與受支援的發行商協商寫程式保證(PG)交易後，您可以使用以下DSP任一項來設定交易 [!DNL Deal ID inbox] 或手動輸入交易詳細資訊。

>[!NOTE]
>
> 對於PG交易，發佈者處理所有預算調整、預算上限和目標。 允許PG通過的所有SSPDSP確認發佈者可以設定預算上限。
>
> 與發行商建立方案保證協定 [!DNL FreeWheel] 需要額外的權限和步驟。 請參閱「」[中計畫保證交易設定概述 [!DNL FreeWheel]](freewheel-overview.md)的雙曲餘切值。

## 使用 [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

以下方法是 [!DNL FreeWheel]。 [!DNL Google Authorized Buyers], [!DNL Magnite DV+]。

1. [接受交易](deal-id-inbox-accept.md)。

1. 保存交易後，選擇將用於交易的廣告，並根據提示建立寫程式保證(PG)預設放置。

   為交易建立預設的PG位置是必須提供100%購買量的。 此類型的投標沒有目標，DSP因此可以將投標返回給發行商的每個投標請求。

   * 如果您接受單筆交易，則會自動重定向到PG預設放置建立工作流。

      全部 [!DNL FreeWheel] 交易被提議為單一交易。

   * 如果您接受具有多個PG交易ID的建議，請確定您需要建立的每個PG預設位置。 建立所有必需的放置後，將啟用「繼續」按鈕。

1. （可選）通過按一下 ![「選項」菜單](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**。

   交易可以針對支援任何媒體類型組合（如連接的電視、案頭和音頻）的多種放置。

## 手動設定計畫保證交易

將此方法用於所有其他SSP。

1. [手動設定交易ID詳細資訊](deal-id-create.md)。

1. 保存交易後，選擇將用於交易的廣告，並根據提示建立PG預設放置。

   為交易建立PG預設位置是必須提供100%購買量的。 此類型的投標沒有目標，DSP因此可以將投標返回給發行商的每個投標請求。

1. （可選）通過按一下 ![「選項」菜單](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**。

   交易可以針對支援任何媒體類型組合（如連接的電視、案頭和音頻）的多種放置。

>[!MORELIKETHIS]
>
>* [關於寫程式擔保交易](programmatic-guaranteed-about.md)
>* [計畫保證交易談判技巧](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [提交廣告，用於計畫保證處理 [!DNL FreeWheel]](freewheel-submit.md)
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [手動建立交易ID詳細資訊](deal-id-create.md)
>* [SSP合作夥伴](ssp-partners.md)
>* [庫存功能概覽](inventory-overview.md)

