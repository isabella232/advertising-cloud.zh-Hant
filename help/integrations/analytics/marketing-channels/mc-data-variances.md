---
title: 為何Advertising Cloud和 [!DNL Marketing Channels]之間的通道資料可能有所不同
description: 了解為何AMO ID追蹤的管道資料可能與 [!DNL Analytics Marketing Channels]追蹤的管道資料不同。
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# 為何Advertising Cloud和[!DNL Marketing Channels]之間的通道資料可能有所不同

*僅具有Advertising Cloud-Adobe Analytics整合的廣告商*

使用者若了解Advertising Cloud與[!DNL Marketing Channels]資料集的整合，常會遇到以下問題：「什麼會造成AMO ID與[!DNL Marketing Channels]之間的資料差異？」 或者，有時候，「為什麼資料會中斷？ 我需要所有量度來比對所有報表。」 幸運的是，差異並不表示資料是「中斷」的，而是預期甚至期望的差異。 讓我們來看看為何以此方式設計整合。

這兩個資料集的主要使用案例不同：

* [!DNL Marketing Channels]:的主要使用案例 [!DNL Marketing Channels] 是使用通用的歸因模型來比較多個管道的資料。分析師可以使用[!UICONTROL Marketing Channel]維度，進一步洞察管道彼此互動的方式。 此深入分析有助於推動宏觀層面決定如何投資於每個管道，並有助於深入分析每個管道的訪客如何與網站互動。

   因此， [!DNL Analytics] [!UICONTROL Marketing Channel]維配置為捕獲和跟蹤所有通道。 [!DNL Marketing Channels] 也可以設定來擷取Advertising Cloud DSP閱覽和點進次數，而這與其他行銷管道相關。

* Advertising Cloud AMO ID:Advertising Cloud AMO ID資料的主要使用案例是饋送Advertising Cloud的進階[!DNL Adobe Sensei]競標演算法。 演算法會自動做出每日數千個微層級的出價決策，以最大化廣告支出並達成[!DNL DSP]促銷活動或[!DNL Search]產品組合的目標。 演算法將促銷活動連結到的轉換資料越多，演算法就越能做出這些競標決策。

   為了收集此資料，[!DNL Analytics for Advertising Cloud]整合會傳遞原始AMO ID，這些AMO ID可在Adobe Analytics的AMO ID維度中轉譯為點進和閱覽追蹤代碼(以自訂變數(eVar)或保留變數(rVar)的形式儲存)。 其他管道的點進次數不會設定在AMO ID維度中，因此AMO ID維度無法追蹤來自這些其他管道的登入次數。 結果AMO ID會持續存在至[!DNL Marketing Channes]l登入點。

如需Advertising Cloud追蹤資料與[!DNL Analytics]追蹤資料之間可能資料差異的詳細資訊，請參閱「[ [!DNL Analytics] 與Advertising Cloud](../data-variances.md)之間的預期資料差異」。

>[!MORELIKETHIS]
>
>* [和之間的預期 [!DNL Analytics] 資料差異Advertising Cloud](/help/integrations/analytics/data-variances.md)
>* [基礎 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [使用Advertising Cloud ID建立 [!DNL Marketing Channels] 處理規則](mc-ids.md)
>* [ [!DNL Analytics Marketing Channels] 搭配Advertising Cloud資料使用](mc-ac-data.md)
>* [影片：使用Advertising Cloud製作報表 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

