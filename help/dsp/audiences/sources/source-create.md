---
title: 建立對象來源以啟用第一方對象
description: 了解如何建立來源，將對象匯入您的帳戶或廣告商帳戶。
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# 建立對象來源以啟用第一方對象

*測試版功能*

<!-- Will this remain for admin users/Adobe account teams only? -->

建立來源以將受眾匯入您的DSP帳戶或廣告商帳戶。 目前，您可以從 [the [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html).

>[!NOTE]
>
>在您為 [!DNL Real-Time CDP]，您需要啟用 [!DNL Real-Time CDP] 對象，透過Adobe的Advertising DSP目的地 [!DNL Real-Time CDP] 開始匯入。 請參閱 [啟動工作流程中的步驟](source-about.md#workflow-sources).

1. 在主功能表中，按一下**[!UICONTROL Audiences] > [!UICONTROL Sources (BETA)].

1. 按一下 [!UICONTROL Add Source].

1. 在 [!UICONTROL Select a Type] ，請選擇源類型。

   *[!UICONTROL RT-CDP]*:此源類型，用於 [the [!DNL Adobe Real-Time Customer Data Profile]](source-about.md)，是唯一的選項。

1. 指定 [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* 或 *[!UICONTROL Account]*.

1. 輸入剩餘 [來源設定](source-settings.md).

   保留 [!UICONTROL Source Key] 即產生。 您稍後需要值。

1. 按一下 **[!UICONTROL Save]**.

1. 在Experience Platform中，使用 [!UICONTROL Source Key] 在DSP來源設定中產生。

如需啟動DSP目的地連線、選取區段及存取控制權限的指示，請參閱[Adobe Advertising Cloud DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

>[!MORELIKETHIS]
>
>* [對象來源設定](source-settings.md)
>* [關於從受眾來源啟用已驗證的區段](source-about.md)
>* [向持久ID合作夥伴啟用已驗證的區段](source-durable-id.md)<!-- title?-->
>* [Adobe Advertising Cloud DSP連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [關於Audience Management](/help/dsp/audiences/audience-about.md)

