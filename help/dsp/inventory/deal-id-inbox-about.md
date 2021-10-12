---
title: 關於[!UICONTROL Deal ID Inbox]
description: 了解[!UICONTROL Deal ID inbox]功能，該功能可讓您接受您已與 [!DNL FreeWheel], [!DNL Google Authorized Buyers] (formerly known as [!DNL AdX]), and [!DNL Magnite DV+] （先前為 [!DNL Rubicon]）的發佈商商議的私人交易。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: 8046ec79ec24f47fe33e49c6097e44dbba450f1f
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# 關於[!UICONTROL Deal ID Inbox]

DSP [!UICONTROL Deal ID inbox]可讓您快速設定Advertising Cloud DSP已透過供應端平台(SSP)從發佈商匯入的交易，因此您不必手動設定每筆交易。 您可以接受已與[!DNL FreeWheel]、[!DNL Google Authorized Buyers]（先前稱為[!DNL AdX]）和[!DNL Magnite DV+]（先前稱為[!DNL Rubicon]）的發行者就[!UICONTROL Deal ID inbox]、（先前稱為）進行協商的有擔保和非有擔保私人庫存交易。

>[!NOTE]
>
>Advertising Cloud DSP是第一個與[!DNL FreeWheel] API整合的DSP。

在[!UICONTROL Deal ID inbox]中，您可以在發佈商看到交易詳細資訊時查看，加快交易設定，並避免手動輸入錯誤。

DSP每天在東部標準時間凌晨4:30自動重新整理所有交易詳細資訊。 它也會每小時重新整理所有[!DNL FreeWheel]交易，並更新[!DNL Google]和[!DNL Magnite DV+]的現有交易。 您也可以隨時手動重新整理交易詳細資訊以填入新交易。

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>對於通過[!DNL Google Authorized Buyers]提供程式化擔保的交易，您必須交付至少90%的預算，否則您的帳戶將無法訪問[!UICONTROL Deal ID inbox]中的[!DNL Google]交易。

## 實作[!UICONTROL Deal ID Inbox]

若要在[!UICONTROL Deal ID inbox]中接收交易，您的SSP帳戶必須將貴組織的DSP帳戶對應至您的SSP帳戶。 DSP會與相關SSP共用組織的帳戶名稱。 如需指示，請連絡您的Adobe客戶經理。

在交易洽談期間，請通知發佈商將交易傳送給您的購買者，而非父DSP帳戶。 交易識別碼可以是名稱或ID，視SSP而定。

## 您可以對交易採取的動作

* **檢** 閱交易記錄，確認SSP已傳送正確的發行者、投放日期、CPM和其他交易詳細資料。如果發佈商犯了錯誤，請在DSP外部與他們聯繫，以便他們能夠更正並重新發送交易。

* **檢閱** 後接受交易，交易將不再顯示在 [!UICONTROL Deal ID inbox]中。接受的交易會列在[!UICONTROL Inventory] > [!UICONTROL Deals]中，且可在廣告商的版位中定位。

* **忽略** 不需要或未經請求的交易。忽略的交易會移至[!UICONTROL Deal ID inbox]內的[!UICONTROL Ignored Deals]標籤，作為封存。 當您忽略交易時，DSP不會通知SSP和發佈商。

* **修改已接受的交** 易的 [!UICONTROL Inventory] 詳細 [!UICONTROL Deals] 資訊>(不在 [!UICONTROL Deal ID inbox]中)。同樣地，當發佈商傳送交易變更時，廣告商會負責在[!UICONTROL Inventory] > [!UICONTROL Deals]中實作這些變更，因為在交易設定後，[!UICONTROL Deal ID inbox]不會從SSP同步變更。

## 哪些類型的交易無法接受？

當交易清單未包含![Accept](/help/dsp/assets/accept.png)圖示或[!UICONTROL Accept]按鈕時，您無法從[!UICONTROL Deal ID inbox]接受它。 相反地，您可以手動[建立交易ID詳細資訊](/help/dsp/inventory/deal-id-create.md)。

您無法接受下列類型的交易：

* [!DNL Google] 不是美元的交易。

* [!DNL Magnite DV+] 非美元交易

* [!DNL FreeWheel] 不是你賬戶貨幣的交易。

* 在今天之前具有結束日期的交易。

* 舊[!DNL Magnite DV+]交易標示為「多媒體類型」。

交易細節包括交易無法接受的原因。

>[!MORELIKETHIS]
>
>* [在交易ID收件匣中接受交易](deal-id-inbox-accept.md)
>* [庫存功能概觀](inventory-overview.md)

