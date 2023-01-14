---
title: 關於 [!UICONTROL Deal ID Inbox]
description: 了解 [!UICONTROL Deal ID inbox] 功能，可讓您接受您已與發佈商洽談的私人交易 [!DNL FreeWheel], [!DNL Google Authorized Buyers] (先前稱為 [!DNL AdX]), and [!DNL Magnite DV+] (原稱 [!DNL Rubicon])。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 0%

---

# 關於 [!UICONTROL Deal ID Inbox]

Advertising DSP [!UICONTROL Deal ID inbox] 可讓您快速設定DSP已透過供應端平台(SSP)從發佈商匯入的交易，因此您不必手動設定每筆交易。 您可以接受已與發佈商磋商的有保證和無保證的私人詳細目錄交易 [!DNL FreeWheel], [!DNL Google Authorized Buyers] (先前稱為 [!DNL AdX])和 [!DNL Magnite DV+] (原稱 [!DNL Rubicon]) [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising DSP是第一個與 [!DNL FreeWheel] API。

在 [!UICONTROL Deal ID inbox]，您可以在發佈商看到交易詳細資訊時查看，加快交易設定，並避免手動輸入錯誤。

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.
   
You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP每天在東部標準時間凌晨4:30自動重新整理所有交易詳細資訊。 也會重新整理所有 [!DNL FreeWheel] 交易及更新 [!DNL Google] 和 [!DNL Magnite DV+] 每小時。 您也可以隨時手動重新整理交易詳細資訊以填入新交易。

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>針對程式化保證交易，透過 [!DNL Google Authorized Buyers]，您必須交付至少90%的預算，否則您的帳戶將無法存取 [!DNL Google] 交易 [!UICONTROL Deal ID inbox].

## 實作 [!UICONTROL Deal ID Inbox]

若要在 [!UICONTROL Deal ID inbox]，您的SSP帳戶必須將貴組織的DSP帳戶對應至SSP帳戶。 DSP會與相關SSP共用組織的帳戶名稱。 請連絡您的 [!DNL Adobe] 客戶團隊以取得指示。

在交易洽談期間，請通知發佈商將交易傳送給您的購買者，而非父DSP帳戶。 交易識別碼可以是名稱或ID，視SSP而定。

## 您可以對交易採取的動作

* **審核交易** 確認SSP已傳送正確的發行者、投放日期、CPM和其他交易詳細資訊。 如果發佈商犯了錯誤，請在DSP外部與他們聯繫，以便他們能夠更正交易並重新發送。

* **接受交易** 檢閱後，且它們將不再顯示於 [!UICONTROL Deal ID inbox]. 接受的交易列於 [!UICONTROL Inventory] > [!UICONTROL Deals] 且已準備好在廣告商的版位中定位。

* **忽略交易** 不需要的或是主動的。 忽略的交易會移至 [!UICONTROL Ignored Deals] 標籤 [!UICONTROL Deal ID inbox]，可作為封存。 當您忽略交易時，DSP不會通知SSP和發佈商。

* **修改已接受交易的詳細資訊** 從 [!UICONTROL Inventory] > [!UICONTROL Deals] (不在 [!UICONTROL Deal ID inbox])。 同樣地，當發佈商傳送交易變更時，廣告商負責在 [!UICONTROL Inventory] > [!UICONTROL Deals] 因為 [!UICONTROL Deal ID inbox] 交易設定後，不會從SSP同步變更。

## 哪些類型的交易無法接受？

當交易清單未包含 ![接受](/help/dsp/assets/accept.png) 表徵圖或 [!UICONTROL Accept] 按鈕，您無法從 [!UICONTROL Deal ID inbox]. 反之，您可以 [手動建立交易ID詳細資訊](/help/dsp/inventory/deal-id-create.md).

您無法接受下列類型的交易：

* [!DNL Google] 不是美元的交易。

* [!DNL Magnite DV+] 非美元交易

* [!DNL FreeWheel] 不是你賬戶貨幣的交易。

* 在今天之前具有結束日期的交易。

* 舊 [!DNL Magnite DV+] 標示為「多種媒體類型」的交易。

交易細節包括交易無法接受的原因。

>[!MORELIKETHIS]
>
>* [在交易ID收件匣中接受交易](deal-id-inbox-accept.md)
>* [庫存功能概觀](inventory-overview.md)

