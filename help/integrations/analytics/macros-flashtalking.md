---
title: 附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤
description: 了解新增原因及方式 [!DNL Analytics for Advertising] 巨集 [!DNL Flashtalking] 廣告標籤
feature: Integration with Adobe Analytics
exl-id: 4b060668-723c-4cd2-b70e-409501ec67de
source-git-commit: 04b57aec29e2d737bc33375614137543bead240c
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# 附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤

*廣告商與Adobe廣告 — 僅Adobe Analytics整合*

*僅適用於Advertising DSP*

如果您使用來自 [!DNL Flashtalking] 對於您的Advertising DSP廣告，將Analytics for Advertising參數附加至您的登陸頁面URL。 參數記錄 `s_kwcid` 和 `ef_id` 登錄頁面URL中的查詢字串參數，讓Adobe廣告可將廣告的點按資料傳送至Adobe Analytics。

使用宏 [!DNL Flashtalking] 顯示廣告和視訊廣告，適用於下列類型 [!DNL Analytics for Advertising] 實作：

* **廣告商與 [!DNL Adobe] [!DNL Analytics for Advertising] 在其網站上實作的JavaScript程式碼**:JavaScript程式碼已記錄 `s_kwcid` 和 `ef_id` 查詢字串參數。 不過，使用巨集會延伸追蹤功能，在不支援第三方Cookie時納入點擊式轉換。 最佳實務是將下列區段中的巨集新增至您的廣告標籤，以擷取未透過JavaScript程式碼擷取的其他點進資料。

>[!NOTE]
>
>JavaScript程式碼是只有在Cookie仍可用時，才能用於點擊追蹤的解決方案。 Cookie停止後，就需要實作下列巨集。

* **網站不使用 [!DNL Analytics for Advertising] JavaScript程式碼，而是依賴 [!DNL Analytics] 僅限點進資料的伺服器端轉送** （不含任何閱覽資料）:若要報告從您透過Adobe廣告購買的廣告所驅動的站上點按活動，需要下列巨集。

## 顯示廣告標籤

在 [!DNL Flashtalking] 廣告標籤設定中，將下列巨集附加至 `Clicktag` 欄位：

```html
?[ftqs:[AdobeAMO]]
```

範例：  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

## 視訊廣告標籤

在 [!DNL Flashtalking] 廣告標籤設定中，將下列巨集附加至 `Clicktag` 欄位：

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

範例：  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising]](overview.md)
>* [Adobe廣告ID：使用者 [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Google Campaign Manager 360] 廣告標籤](/help/integrations/analytics/macros-google-campaign-manager.md)

