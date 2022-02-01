---
title: 建立 [!UICONTROL Simple Ad Serving] 交易
description: 瞭解如何為 [!UICONTROL Simple Ad Serving] 成交。
feature: DSP Simple Ad Serving
exl-id: d8de85ec-616c-44ed-9a1a-cc25713ad4a4
source-git-commit: 3e47fec28a17cb64de42309c0368293e1ef1cdea
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# 建立 [!UICONTROL Simple Ad Serving] 交易

1. 在主菜單中，按一下 **[!UICONTROL Inventory]> [!UICONTROL Deals]。**

1. 在資料表上方，按一下 **[!UICONTROL Create]**，然後選擇 **[!UICONTROL Simple Ad Serving]**。

1. 輸入 [交易設定](simple-deal-settings.md):

   1. 在 [!UICONTROL Select Ad Source] 部分，指定有關發佈者、廣告商和市場活動以及廣告類型的資訊，然後按一下 **[!UICONTROL Next]**。

   1. 在 [!UICONTROL Select Ad(s)] 部分，指定要用作代理的廣告DSP:

      1. 執行下列任一操作：

         * 對於現有廣告，選擇要使用的廣告。

         * 對於新廣告，建立代理 [第一方廣告](/help/dsp/campaign-management/ads/ad-create.md) 或 [第三方廣告](/help/dsp/campaign-management/ads/ad-create-third-party.md)。
      >[!NOTE]
      > 不DSP會真正為你指定的廣告服務。 發行商將提供廣告。

      1. 按一下 **[!UICONTROL Next]**.
   1. 在源詳細資訊中，編輯源詳細資訊，然後按一下 **[!UICONTROL Next]**。

      Advertising Cloud DSP自動生成名為「SAS放置 — &lt;*交易名稱*>，」。 在放置中，交易將自動定位在 [!UICONTROL Inventory Targets] 的子菜單。 所有其他目標選項均不適用。



1. 通過以下任一方式將事件跟蹤像素發送到發佈伺服器以實施：

   * （可選） [!UICONTROL Activate Tag with Publisher] 螢幕，將交易標籤發送給發佈者。

      完成以前步驟後，DSP將生成一封電子郵件，您可以將其發送給發佈者。 該消息包括交易詳細資訊、從中檢索交易標籤的連結和該連結的授權代碼。

      1. 複查交易詳細資訊，然後執行以下任一操作：

         * 要將資訊貼上到設備上電子郵件應用程式中的電子郵件消息中，請按一下 **[!UICONTROL Email & Done]** 並選擇電子郵件應用程式。 的 [!UICONTROL CC:] 欄位中 [!DNL Adobe] 支援地址。 然後，您可以將消息發送給發佈者的相應聯繫人。

         * 要將資訊複製到剪貼簿，請按一下 **[!UICONTROL Copy Email]。** 然後，您可以手動將內容貼上到電子郵件中，並將其發送給發佈者的相應聯繫人。 必須將副本（抄送：）包含到 `publisher-support-global@adobe.com`。 複製完消息後，按一下 **[!UICONTROL Email & Done]**。
      1. （如有必要）跟蹤發佈者，查看標籤是否包含相應的宏，以便該標籤與發佈者的廣告伺服器一起使用。
   * （可選）手動將事件跟蹤像素發送到發佈者：

      1. 在 [!UICONTROL Deals] 視圖，按一下 ![「選項」菜單](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**。

         事件像素包括 [!UICONTROL Clickthrough] 像素和 [!UICONTROL Impression] 像素。 視頻和音頻廣告還包括按完成四分之一(從 [!UICONTROL 25% Complete] 至 [!UICONTROL 100% Complete])。

      1. 複製事件跟蹤像素，並將它們提供給發佈者。



>[!MORELIKETHIS]
>
>* [關於 [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] 設定](simple-deal-settings.md)
>* [查看事件跟蹤像素 [!UICONTROL Simple Ad Serving] 交易](simple-deal-show-pixels.md)

