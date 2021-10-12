---
title: 設定程式化保證交易
description: 了解如何設定您與發佈商商議的程式化保證(PG)交易。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 9e371606-5428-4635-9653-7dc43449e489
source-git-commit: 8046ec79ec24f47fe33e49c6097e44dbba450f1f
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# 設定程式化保證交易

*[僅支援的供應端平台](programmatic-guaranteed-about.md)*

在您與受支援的發佈商協商程式化保證(PG)交易後，您可以使用[!DNL Deal ID inbox]或手動輸入交易詳細資訊，在DSP內設定交易。

>[!NOTE]
>
> 針對PG交易，發佈商會處理所有預算調整、預算上限和目標定位。 所有允許PG透過DSP的SSP都會確認發佈者可以設定預算上限。
>
> 在[!DNL FreeWheel]上與發佈者設定程式化保證交易需要額外的權限和步驟。 如需詳細資訊，請參閱「 [!DNL FreeWheel]](freewheel-overview.md)中設定程式化保證交易概述」。[

## 使用[!DNL Deal ID Inbox]設定程式化保證交易 {#pg-setup-deal-id-inbox}

這是[!DNL FreeWheel]、[!DNL Google Authorized Buyers]和[!DNL Magnite DV+]慣用的方法。

1. [接受交易](deal-id-inbox-accept.md)。

1. 儲存交易後，選取將用於交易的廣告，並依照提示建立程式化保證(PG)預設位置。

   必須為交易建立預設的PG位置，才能提供100%的購買。 此類型的版位沒有定位，因此DSP可以傳回出版商的每個競標請求。

   * 如果您接受單筆交易，系統會自動將您重新導向至PG預設版位建立工作流程。

      所有[!DNL FreeWheel]交易均以單一交易提出。

   * 如果您接受具有多個PG交易ID的建議書，請識別您需要建立的每個PG預設版位。 建立所有必要版位後，會啟用「繼續」按鈕。

1. （選用）以其他非PG版位鎖定PG交易。

## 手動設定程式化保證交易

此方法適用於所有其他SSP。

1. [手動設定交易ID詳細資訊](deal-id-create.md)。

1. 儲存交易後，選取將用於交易的廣告，並建立PG預設版位（如提示）。

   必須為交易建立PG預設位置，才能提供100%的購買。 此類型的版位沒有定位，因此DSP可以傳回出版商的每個競標請求。

1. （選用）以其他非PG版位鎖定PG交易。

>[!MORELIKETHIS]
>
>* [關於程式化保證交易](programmatic-guaranteed-about.md)
>* [談判程式保證交易的技巧](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [提交程式保證交易的廣告 [!DNL FreeWheel]](freewheel-submit.md)
>* [在交易ID收件匣中接受交易](deal-id-inbox-accept.md)
>* [手動建立交易ID詳細資訊](deal-id-create.md)
>* [SSP合作夥伴](ssp-partners.md)
>* [庫存功能概觀](inventory-overview.md)

