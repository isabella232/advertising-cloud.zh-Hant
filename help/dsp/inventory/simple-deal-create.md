---
title: '"建立 [!UICONTROL Simple Ad Serving] 交易」'
description: 「了解如何為 [!UICONTROL Simple Ad Serving] 交易。」
feature: DSP Simple Ad Serving
exl-id: d8de85ec-616c-44ed-9a1a-cc25713ad4a4
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# 建立 [!UICONTROL Simple Ad Serving] 交易

1. 在主功能表中，按一下 **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. 在資料表格上方，按一下 **[!UICONTROL Create]**，然後選取 **[!UICONTROL Simple Ad Serving]**.

1. 輸入 [交易設定](simple-deal-settings.md):

   1. 在 [!UICONTROL Select Ad Source] 區段，指定發佈者、廣告商和促銷活動以及廣告類型的相關資訊，然後按一下 **[!UICONTROL Next]**.

   1. 在 [!UICONTROL Select Ad(s)] 區段中，指定要作為DSP中代理的廣告：

      1. 執行下列任一操作：

         * 針對現有廣告，選取要使用的廣告。

         * 若為新廣告，請建立Proxy [第三方廣告](/help/dsp/campaign-management/ads/ad-create-multiple.md).
      >[!NOTE]
      > DSP不提供您指定的廣告。 發佈者提供廣告。

      1. 按一下 **[!UICONTROL Next]**.
   1. 在摘要詳細資料中，編輯摘要詳細資料，然後按一下 **[!UICONTROL Next]**.

      DSP會自動產生名為「SAS位置 — &lt;*交易名稱*>，」。 在版位中，交易會自動定位於 [!UICONTROL Inventory Targets] 區段。 所有其他定位選項皆不適用。



1. 透過下列其中一種方式，將事件追蹤像素傳送至發佈者以進行實作：

   * （選用）從 [!UICONTROL Activate Tag with Publisher] 螢幕上，將交易標籤傳送給發佈商。

      完成上述步驟後，DSP會產生電子郵件訊息，供您傳送給發佈者。 該消息包括交易詳細資訊、用於檢索交易標籤的連結以及該連結的授權代碼。

      1. 查看交易詳細資訊，然後執行以下任一操作：

         * 若要將資訊貼到裝置上電子郵件應用程式中的電子郵件訊息中，請按一下 **[!UICONTROL Email & Done]** 並選取電子郵件應用程式。 此 [!UICONTROL CC:] 欄位已預先填入 [!DNL Adobe] 支援地址。 然後，您可以將訊息傳送給發佈者的適當聯絡人。

         * 若要將資訊複製到剪貼簿，請按一下 **[!UICONTROL Copy Email].** 然後，您可以手動將內容貼入電子郵件訊息中，並傳送給發佈商的適當連絡人。 您必須將副本(CC:)包含到 `publisher-support-global@adobe.com`. 複製完訊息後，按一下 **[!UICONTROL Email & Done]**.
      1. （如有必要）請向發佈商跟進，查看標籤是否包含適當的巨集，讓標籤與發佈商的廣告伺服器搭配使用。
   * （選用）手動將事件追蹤像素傳送至發佈者：

      1. 在 [!UICONTROL Deals] 檢視，按一下 ![選項功能表](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         事件像素包括 [!UICONTROL Clickthrough] 像素和 [!UICONTROL Impression] 像素。 視訊和音訊廣告也包含按完成四分位數的事件像素(來自 [!UICONTROL 25% Complete] to [!UICONTROL 100% Complete])。

      1. 複製事件追蹤像素並提供給您的發佈者。



>[!MORELIKETHIS]
>
>* [關於 [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] 設定](simple-deal-settings.md)
>* [查看交易的詳細報表](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
