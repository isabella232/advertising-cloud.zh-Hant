---
title: 為何Adobe廣告和 [!DNL Marketing Channels]
description: 了解為何AMO ID追蹤的管道資料可能與 [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 4605dc7d-43d7-414f-a509-6096c6cf5fd2
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# 為何Adobe廣告和 [!DNL Marketing Channels]

*廣告商與Adobe廣告 — 僅Adobe Analytics整合*

使用者了解Adobe廣告與 [!DNL Marketing Channels] 資料集是「造成AMO ID和之間資料差異的原因」 [!DNL Marketing Channels]?&quot; 或者，有時候，「為什麼資料會中斷？ 我需要所有量度來比對所有報表。」 幸運的是，差異並不表示資料是「中斷」的，而是預期甚至期望的差異。 讓我們來看看為何以此方式設計整合。

這兩個資料集的主要使用案例不同：

* [!DNL Marketing Channels]:的主要使用案例 [!DNL Marketing Channels] 是使用通用的歸因模型來比較多個管道的資料。 分析師可使用 [!UICONTROL Marketing Channel] 維度，進一步了解管道彼此互動的方式。 此深入分析有助於推動宏觀層面決定如何投資於每個管道，並有助於深入分析每個管道的訪客如何與網站互動。

   此 [!DNL Analytics] [!UICONTROL Marketing Channel] 因此，維度已設定為擷取及追蹤所有通道。 [!DNL Marketing Channels] 也可以設定來擷取DSP閱覽和點進次數，而這與其他行銷管道相關。

* Adobe廣告AMO ID:Adobe廣告AMO ID資料的主要使用案例是饋送進階 [!DNL Adobe Sensei]競標算法。 這些演算法會自動做出每日數千個微層級的出價決策，以最大化廣告支出並達成 [!DNL DSP] 行銷活動或 [!DNL Search] 作品集。 演算法將促銷活動連結到的轉換資料越多，演算法就越能做出這些競標決策。

   若要收集此資料， [!DNL Analytics for Advertising] 整合會傳遞原始AMO ID，這些AMO ID可在Adobe Analytics的AMO ID維度中轉譯為點進和閱覽追蹤代碼，以自訂變數(eVar)或保留變數(rVar)的形式儲存。 其他管道的點進次數不會設定在AMO ID維度中，因此AMO ID維度無法追蹤來自這些其他管道的登入次數。 結果AMO ID會持續存在至 [!DNL Marketing Channels] 登入點。

如需Adobe廣告追蹤資料與 [!DNL Analytics] — 跟蹤的資料，請參閱[之間的預期資料差異 [!DNL Analytics] 和Adobe廣告](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [之間的預期資料差異 [!DNL Analytics] 和Adobe廣告](/help/integrations/analytics/data-variances.md)
>* [基礎 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [使用Adobe廣告ID來建立 [!DNL Marketing Channels] 處理規則](mc-ids.md)
>* [使用 [!DNL Analytics Marketing Channels] 與Adobe廣告資料](mc-ac-data.md)
>* [影片：使用 [!DNL Marketing Channels] AdobeAdvertising報表](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

