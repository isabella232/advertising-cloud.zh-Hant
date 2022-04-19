---
title: 追加 [!DNL Analytics for Advertising Cloud] 宏到 [!DNL Flashtalking] 廣告標籤
description: 瞭解添加原因和方法 [!DNL Analytics for Advertising Cloud] 宏 [!DNL Flashtalking] ad標籤
feature: Integration with Adobe Analytics
source-git-commit: c95dc72fa42b47ecea0c27bd59a2df4cd9c20233
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# 追加 [!DNL Analytics for Advertising Cloud] 宏到 [!DNL Flashtalking] 廣告標籤

*只有Advertising Cloud-Adobe Analytics整合的廣告商*

*僅適用於Advertising Cloud DSP*

如果使用廣告標籤 [!DNL Flashtalking] 對於您的Advertising Cloud DSP廣告，將Advertising Cloud參數的分析附加到您的登錄頁URL。 參數記錄 `s_kwcid` 和 `ef_id` 查詢登錄頁URL中的字串參數，使Advertising Cloud能夠將廣告的點擊資料發送到Adobe Analytics。

使用宏 [!DNL Flashtalking] 以下類型的顯示和視頻廣告 [!DNL Analytics for Advertising Cloud] 實現：

* **廣告商 [!DNL Adobe] [!DNL Analytics for Advertising Cloud] 在其網站上實現的JavaScript代碼**:JavaScript代碼已記錄 `s_kwcid` 和 `ef_id` 查詢字串參數。 但是，當不支援第三方Cookie時，使用宏擴展了跟蹤以包括基於按一下的轉換。 最佳做法是將以下各節中的宏添加到廣告標籤中，以捕獲未通過JavaScript代碼捕獲的其他點擊式資料。

>[!NOTE]
>
>JavaScript代碼是僅在Cookie仍然可用時按一下跟蹤的解決方案。 一旦Cookie停止，就需要實施以下宏。

* **網站不使用廣告的廣告商 [!DNL Analytics for Advertising Cloud] JavaScript代碼，而是依賴 [!DNL Analytics] 伺服器端轉發僅用於點擊式資料** （沒有任何查看資料）:需要以下宏來報告您通過Advertising Cloud購買的廣告中的現場點擊活動。

## 顯示廣告標籤

在 [!DNL Flashtalking] 添加標籤設定，將以下宏添加到按一下URL的末尾 `Clicktag` 欄位：

```html
?[ftqs:[AdobeAMO]]
```

示例：  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

![示例 [!DNL Flashtalking] ad標籤設定](/help/integrations/assets/macro-flashtalking-display-ad.png)

## 視頻廣告標籤

在 [!DNL Flashtalking] 添加標籤設定，將以下宏添加到按一下URL的末尾 `Clicktag` 欄位：

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

示例：  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

![示例 [!DNL Flashtalking] ad標籤設定](/help/integrations/assets/macro-flashtalking-video-ad.png)

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising CloudID使用者 [!DNL Analytics]](/help/integrations/analytics/ids.md)


<!-- >* [Append [!DNL Analytics for Advertising Cloud] Macros to [!DNL Google Campaign Manager 360] Ad Tags](macros-google-campaign-manager.md) -->
