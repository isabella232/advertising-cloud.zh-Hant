---
title: 使用 [!DNL Marketing Channels] 使用Advertising Cloud資料
description: 了解如何在 [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
source-git-commit: 1ae45d0ceee2efc4fc52b86fd6737d4c7467a6ca
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 使用 [!DNL Analytics Marketing Channels] 使用Advertising Cloud資料

*僅具有Advertising Cloud-Adobe Analytics整合的廣告商*

同時使用Advertising Cloud和 [!DNL Marketing Channels] 報表，您就可獲得數位媒體如何影響網站活動的寶貴分析。

<!-- from video: By using Marketing Channels with your Advertising Cloud data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

下圖顯示Advertising Cloud和 [!DNL Marketing Channels] 追蹤組成一個訪客歷程的個別造訪。 Advertising Cloud報表 [!DNL Analytics] 僅限使用AMO ID透過Advertising Cloud販運的付費顯示和搜尋廣告。 不過， [!DNL Marketing Channels] 會追蹤中設定的所有通道 [!DNL Marketing Channels] 處理規則。

![Advertising Cloud和 [!DNL Marketing Channels] 追蹤訪客歷程中的個別造訪](/help/integrations/assets/a4adc-mc-sample-journey2.png)

在第一次瀏覽中，使用者透過電子郵件促銷活動進入網站，執行了10次頁面檢視，然後離開。 在第二次瀏覽中，使用者透過顯示廣告進入網站，執行10次頁面檢視，然後離開。 在第三次瀏覽中，使用者透過免費搜尋進入網站、執行五次頁面檢視、執行$250的轉換，然後在左邊。 請注意 [!DNL Marketing Channels] 和Advertising Cloud。 Advertising Cloud在此歷程中唯一追蹤的管道是 [!UICONTROL Display]. Advertising Cloud追蹤 [!UICONTROL Display] 管道造訪並將後續的參與資料（例如頁面檢視）和轉換歸因於該廣告的影響。 [!DNL Marketing Channels]，則可提供所有管道的完整檢視。

由於AMO ID會持續存在於訪客的歷程中，因此您可以使用AMO ID資料來了解Advertising Cloud對其他行銷管道的影響。 AMO ID [預設會持續60天](/help/integrations/analytics/overview.md)，但您可以視需要設定持續性。

## 如何結合Advertising Cloud和行銷管道資料以分析媒體效能

內 [!DNL Analytics]，您可以結合Advertising Cloud持續付費廣告資料和 [!DNL Marketing Channels] 全面的造訪資料，以便更好地分析您的媒體效能，進而更好地影響客戶歷程。

下列分析使用Advertising Cloud資料，顯示不同版本的顯示廣告如何影響網站轉換。 所有三欄都使用相同的轉換量度，但每一欄會呈現不同的動態：

* 第1欄會查看在訪客歷程中持續存在的AMO ID資料。 第1欄指出有641個應用程式開始，曾經透過閱覽或點進事件，與Advertising Cloud廣告連結。 這個觀點沒有其他觀點 [!DNL Marketing Channels] 歸因。

* 在 [!DNL Marketing Channels] 但是，資料集641個應用程式啟動會歸因於其他行銷管道。 最後兩欄會採用641個應用程式啟動，並將資料限制為 [!UICONTROL Display Click-Through] 和 [!UICONTROL Display View-Through] 管道，顯示上次接觸歸因模型中發生的轉換。

![顯示廣告如何影響網站轉換的範例](/help/integrations/assets/a4adc-mc-display-impact.png)

您可以更進一步進行此分析。 您可以依行銷管道進一步劃分Advertising Cloud列，以查看Advertising Cloud轉換歸因於641個應用程式啟動的位置。 您已知，其中5個轉換歸因於上次接觸顯示點進，19個歸因於上次接觸顯示檢視。 仍有617個應用程式開始歸因於其他行銷管道。 您可以將「上次接觸管道」維度拖放至Advertising Cloud DSP條列項目上方，以顯示其餘「應用程式開始」的管道屬性，並顯示「顯示」管道的跨管道影響。

![如何新增「上次接觸管道」維度](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

現在，您可以看到剩餘應用程式啟動的歸屬方式。 有357個上次接觸應用程式開始，且AMO ID持續存在，電子郵件的評分為。 使用此類型的分析，您可以了解Advertising Cloud顯示廣告在所有管道中所產生的影響。 只有一個資料集和歸因模型，就無法使用這種分析。

![顯示通道的跨通道影響範例](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

您可以使用「100%堆疊」的堆疊圖表集來顯示一段時間內的趨勢資料，進一步改善分析。 此視覺效果可讓您更輕鬆監控哪些上次接觸行銷管道受到顯示行銷活動的影響更大。

![顯示管道的趨勢跨管道影響範例](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [基礎 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [使用Advertising Cloud ID建立 [!DNL Marketing Channels] 處理規則](mc-ids.md)
>* [為何管道資料可能因Advertising Cloud和 [!DNL Marketing Channels]](mc-data-variances.md)
>* [影片：使用Advertising Cloud製作報表 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [概觀 [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md)

