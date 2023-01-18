---
title: 基礎 [!DNL Marketing Channels]
description: 了解關於 [!DNL Analytics Marketing Channels] the [!DNL Analytics for Advertising] 使用者應了解。
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# 基礎 [!DNL Analytics Marketing Channels]

*廣告商與Adobe廣告 — 僅Adobe Analytics整合*

本頁面說明 [!DNL Analytics Marketing Channels] the [!DNL Analytics for Advertising] 使用者需要了解。

如需 [!DNL Marketing Channels]，請參閱「[開始使用 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html).&quot;

## 概觀 [!DNL Marketing Channels]

[!DNL Marketing Channels] 是Adobe Analytics的重要功能。 [!DNL Marketing Channels] 報表會顯示客戶如何透過報告視窗到達您的網站，以及每個管道如何影響收入或站上行為。

請考量下列跨造訪歷程範例。 您網站的每次造訪都會以訪客所進入的行銷管道表示。 首次造訪也稱為首次接觸管道，是電子郵件。 瀏覽二時顯示為參與管道，免費搜尋則視為上次接觸管道。 如果您使用 [!UICONTROL Last Touch Attribution] with [!UICONTROL Attribution IQ]，免費搜尋將會獲得$250轉換事件的完整評分。 使用Experience CloudID服務，您可以將這些個別造訪連結在一起，讓單一訪客顯示一個歷程。

![行銷管道中的跨造訪轉換歷程範例](/help/integrations/assets/a4adc-mc-sample-journey.png)

使用 [!UICONTROL Marketing Channels] 處理規則，您可以建立邏輯集，以決定推動流量的管道，並在使用者造訪您的網站時追蹤每個管道。 例如， [!UICONTROL Email] 管道會以點按時產生的唯一追蹤代碼來指出，當Adobe Analytics記錄時，系統會將造訪分類為源自電子郵件行銷活動。

## 處理規則與行銷管道的設定方式

每次使用者造訪網站時，都會透過URL執行，使用者可按一下該URL或直接在位址列中輸入。 當使用者進入網站時， [!DNL Analytics] 會追蹤可用來判斷引導造訪的管道的資訊。

行銷人員通常會將查詢字串參數追蹤程式碼附加至管道URL，以協助追蹤管道對其網站的影響。 您可以設定 [!DNL Marketing Channels] 處理規則，以監聽特定追蹤參數和值，以判斷管道而不需任何其他追蹤。 例如，如果所有電子郵件促銷活動URL都遵循格式 `www.adobe.com?cid=email…` (其中URL包含查詢字串參數和值 `cid=email`)，然後您可以建立規則來監聽此追蹤程式碼，並將造訪分段到 [!UICONTROL Email] 頻道。

其他管道沒有可追蹤的URL路徑，需要進一步的邏輯才能識別。 例如， [!UICONTROL Earned Social]，而使用者點按另一個使用者在社交網路上有機共用的連結，則是重要的追蹤管道。 但行銷人員無法將查詢字串參數追蹤代碼附加至共用的URL。 在此情況下，您可以建立處理規則來監聽感興趣社交網路的反向連結網域，以及沒有付費追蹤代碼來判斷管道。 接著，在「行銷管道」報表中，將會以無償社交方式追蹤符合這些要求的造訪。

Adobe建議您與分析團隊合作，建立完整的 [!DNL Marketing Channels] 處理規則，以追蹤與您的業務相關的所有管道。 這麼做可讓您建立強大的歸因報表。

若要了解Adobe廣告對建立自訂行銷管道所需訊號的貢獻方式，請參閱「[使用Advertising ID來建立 [!DNL Marketing Channels] 規則](mc-ids.md).&quot;

>[!MORELIKETHIS]
>
>* [使用Adobe廣告ID來建立 [!DNL Marketing Channels] 處理規則](mc-ids.md)
>* [為何Adobe廣告和 [!DNL Marketing Channels]](mc-data-variances.md)
>* [使用 [!DNL Analytics Marketing Channels] 與Adobe廣告資料](mc-ac-data.md)
>* [影片：使用 [!DNL Marketing Channels] AdobeAdvertising報表](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [概觀 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)

