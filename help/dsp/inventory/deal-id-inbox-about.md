---
title: 關於 [!UICONTROL Deal ID Inbox]
description: 瞭解 [!UICONTROL Deal ID inbox] 功能，它允許您接受您已與發佈商就以下問題談判的私有協定 [!DNL FreeWheel], [!DNL Google Authorized Buyers] (前稱 [!DNL AdX]), and [!DNL Magnite DV+] （以前） [!DNL Rubicon])。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: 39f491a39bdc9d8dd820eb4c69594dda71d8b3c2
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# 關於 [!UICONTROL Deal ID Inbox]

DSP [!UICONTROL Deal ID inbox] 允許您快速設定Advertising Cloud DSP通過供應端平台(SSP)從發行商導入的交易，以便您不必手動設定每筆交易。 您可以接受您已與發佈商就以下問題進行協商的有保證和無保證的私有庫存交易 [!DNL FreeWheel]。 [!DNL Google Authorized Buyers] (前稱 [!DNL AdX])和 [!DNL Magnite DV+] （以前） [!DNL Rubicon]) [!UICONTROL Deal ID inbox]。

>[!NOTE]
>
>Advertising Cloud DSPDSP是第一個 [!DNL FreeWheel] API。

在 [!UICONTROL Deal ID inbox]，您可以在發佈者看到交易詳細資訊時查看交易詳細資訊，加快交易設定並避免手動輸入錯誤。

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.
   
You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

每天DSP在東部時間凌晨4時30分自動刷新所有交易詳細資訊。 它還刷新所有 [!DNL FreeWheel] 更新現有交易 [!DNL Google] 和 [!DNL Magnite DV+] 小時。 您還可以隨時人工刷新交易詳細資訊以填充新交易。

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>對於方案擔保交易， [!DNL Google Authorized Buyers]您必須至少交付90%的預算，否則您的帳戶將無法訪問 [!DNL Google] 交易 [!UICONTROL Deal ID inbox]。

## 執行 [!UICONTROL Deal ID Inbox]

要在 [!UICONTROL Deal ID inbox]，您的SSP帳戶必須將您組織的帳DSP戶映射到您的SSP帳戶。 將DSP與相關SSP共用組織的帳戶名。 聯繫您 [!DNL Adobe] 客戶團隊。

在交易談判期間，請讓發行商將交易發送給您的買家，而不是將交易發DSP送給父帳戶。 交易標識符可以是名稱或ID，具體取決於SSP。

## 您可以對交易採取的操作

* **審查交易** 驗證SSP是否已發送了正確的發佈者、飛行日期、CPM和其他交易詳細資訊。 如果出版商犯了錯誤，請在外面聯繫他們DSP，以便他們能夠更正並重新發送交易。

* **接受交易** 在審閱後，它們將不再出現在 [!UICONTROL Deal ID inbox]。 接受的交易列在 [!UICONTROL Inventory] > [!UICONTROL Deals] 並準備在廣告商的廣告投放中瞄準。

* **忽略交易** 不需要的或是主動的。 忽略的交易將移至 [!UICONTROL Ignored Deals] 中 [!UICONTROL Deal ID inbox]作為存檔。 在DSP忽略交易時不向SSP和發佈者發出警報。

* **修改已接受交易的詳細資訊** 從 [!UICONTROL Inventory] > [!UICONTROL Deals] (在 [!UICONTROL Deal ID inbox])。 同樣，當出版商向交易發送變更時，廣告商負責實施這些變更 [!UICONTROL Inventory] > [!UICONTROL Deals] 因為 [!UICONTROL Deal ID inbox] 在設定交易後不同步SSP中的更改。

## 哪些類型的交易不能接受？

當交易清單不包括 ![接受](/help/dsp/assets/accept.png) 表徵圖 [!UICONTROL Accept] 按鈕，您不能從 [!UICONTROL Deal ID inbox]。 相反，你可以 [手動建立交易ID詳細資訊](/help/dsp/inventory/deal-id-create.md)。

您無法接受以下類型的交易：

* [!DNL Google] 不是美元的交易。

* [!DNL Magnite DV+] 不以美元計價的交易

* [!DNL FreeWheel] 不以你的帳戶幣種表示的交易。

* 在今天之前結束的交易。

* 舊 [!DNL Magnite DV+] 被標為「多媒體類型」的交易。

交易細節包括交易無法接受的原因。

>[!MORELIKETHIS]
>
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [庫存功能概覽](inventory-overview.md)

