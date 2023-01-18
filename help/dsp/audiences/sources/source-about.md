---
title: 關於從受眾來源啟用已驗證的區段
description: 了解如何從客戶資料平台擷取第一方區段。
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# 關於從受眾來源啟用已驗證的區段

<!-- Doesn't specifically explain what you can do in our UI -->
*測試版功能*

DSP可內嵌由客戶資料平台(CDP)內建的已驗證訊號所組成的第一方區段。 您可以使用擷取的區段作為版位的目標。

## [!DNL Adobe Real-Time Customer Data Profile]

DSP已與 [the [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html)，屬於Adobe Experience Platform。

在 [!DNL Real-time CDP], *目的地* 是與外部資料平台的連線，可順暢地啟動資料。 例如，您可以使用目的地來啟用已知客戶關係（例如雜湊電子郵件地址），以針對DSP所支援數位格式的目標廣告。

如需目的地的詳細資訊，請參閱Experience Platform [目的地指南](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html)，包括產品概觀、 [建立目標工作區](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) 和 [建立目標連線](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html)，和 [將資料啟用至目的地](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

### 搭配使用DSP整合的工作流程 [!DNL Real-time CDP] {#workflow-sources}

<!-- Make sure that titles make the distinctions clear -- everything can't be "Activate XXX." -->

1. [允許DSP將客戶資料區段轉譯為 [!DNL LiveRamp RampIDs]](source-durable-id.md) 在可買環境中識別。<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your DSP account team will perform this configuration. -->

1. [建立受眾來源](source-create.md) 若要將受眾匯入您的DSP帳戶或廣告商帳戶。

1. [設定 [!DNL Real-Time CDP] 目標連接Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).

如需其他支援，請連絡您的 [!DNL Adobe] 帳戶團隊或 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [向持久ID合作夥伴啟用已驗證的區段](source-durable-id.md)
>* [建立對象來源以啟用第一方對象](source-create.md)
>* [對象來源設定](source-settings.md)
>* [AdobeAdvertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [目的地目錄概觀](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [關於Audience Management](/help/dsp/audiences/audience-about.md)

