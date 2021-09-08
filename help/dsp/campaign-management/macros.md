---
title: Advertising Cloud DSP巨集
description: 參考可用的巨集以用於一般追蹤，以及追蹤第三方顯示廣告的點按次數。
feature: Ads
exl-id: e31cc2e5-ad1f-4555-a87b-0e4c3731fe5f
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# Advertising Cloud DSP巨集

宏是指令的簡短命令或速記，通常採用`${MACRO_NAME}`格式。 Advertising Cloud DSP廣告伺服器會在提供或點按廣告時執行巨集。

巨集最常用於販運第三方和自訂創意程式碼或中繼資料（例如第三方像素）。

## 一般追蹤巨集

視需要使用所有廣告和標籤類型的一般追蹤巨集來傳回特定資料。

| 巨集 | 說明 |
| --------------- | ---------------------- |
| `${USER_ID}` | 所有設備類型的用戶標識符。 |
| `${TM_RANDOM}` | 快捷人：1到1000000之間的隨機數 |
| `${TM_PLACEMENT_ID_NUM}` | 版位ID |
| `${TM_SITE_URL_URLENC}` | 競標請求中傳遞的URL;URL編碼 |
| `${TM_SITE_DOMAIN_URLENC}` | 從競標請求中的URL剖析的頁面子網域；URL編碼 |

{style=&quot;table-layout:auto&quot;}

## 按一下第三方顯示廣告的巨集

為了使用第三方顯示標籤準確追蹤廣告的點按次數，DSP需要顯示點按巨集。 只需要一個宏版本；相關巨集取決於標籤的類型。

| 巨集 | 說明 |
| --------------- | ---------------------- |
| `${TM_CLICK_URL}` | 可讓廣告伺服器追蹤及計算平台中廣告點按次數的重新導向URL |
| `${TM_CLICK_URL_URLENC}` | 重新導向URL，可讓需要URL編碼的廣告伺服器追蹤及計算平台中的廣告點按次數 |

{style=&quot;table-layout:auto&quot;}

當您：

* 從Advertising Cloud廣告伺服器合作夥伴<!-- [Needs PM confirmation.] -->匯出廣告標籤
* 直接在DSP中大量上傳[!DNL Flashtalking]或[!DNL Google DoubleClick for Advertisers]廣告標籤

如果您在建立顯示廣告時遺失點按巨集，DSP會顯示警告訊息，提示您在標籤的正確區域手動插入適當的顯示點按巨集。

>[!MORELIKETHIS]
>
>* [音訊廣告設定](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [音訊廣告設定](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [音訊廣告設定](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [音訊廣告設定](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [音訊廣告設定](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [音訊廣告設定](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)

