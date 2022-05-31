---
title: 關於從受眾源激活經過驗證的段
description: 瞭解如何從客戶資料平台接收第一方段。
feature: DSP Audiences
source-git-commit: aac60e8fddce1db3d0101a617fca3af970043648
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 關於從受眾源激活經過驗證的段

<!-- Doesn't specifically explain what you can do in our UI -->
*Beta功能*

Advertising Cloud DSP可以接收由在客戶資料平台(CDP)內構建的經過驗證的信號組成的第一方資料段。 可以將攝取的段用作放置的目標。

## [!DNL Adobe Real-Time Customer Data Profile]

DSP與 [這樣 [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html)是Adobe Experience Platform的一部分。

在 [!DNL Real-time CDP]。 *目的地* 是與外部資料平台的連接，允許無縫資料激活。 例如，您可以使用目標來激活已知的客戶關係（如散列電子郵件地址），以針對受支援的數字格式進行目標廣DSP告。

有關目標的詳細資訊，請參閱Experience Platform [目標指南](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html)，包括產品概述，說明 [建立目標工作區](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) 和 [建立目標連接](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html), [將資料激活到目標](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html)。

### 用於與整合DSP的工作流 [!DNL Real-time CDP] {#workflow-sources}

<!-- Make sure that titles make the distinctions clear -- everything can't be "Activate XXX." -->

1. [允許DSP將客戶資料段轉換為 [!DNL LiveRamp RampIDs]](source-durable-id.md) 在可愛的環境中可辨認的。<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your DSP account team will perform this configuration. -->

1. [建立受眾源](source-create.md) 將受眾導入您的DSP帳戶或廣告商帳戶。

1. [配置 [!DNL Real-Time CDP] 目標連接在Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)。<!-- Verify URL once it's published. -->

要獲得其他支援，請與 [!DNL Adobe] 客戶團隊 `adcloud-support@adobe.com`。

>[!MORELIKETHIS]
>
>* [從持久ID合作夥伴激活經過驗證的段](source-durable-id.md)
>* [建立受眾源以激活第一方受眾](source-create.md)
>* [受眾源設定](source-settings.md)
>* [Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [目標目錄概述](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [關於受眾管理](/help/dsp/audiences/audience-about.md)

