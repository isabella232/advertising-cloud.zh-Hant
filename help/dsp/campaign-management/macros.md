---
title: Advertising Cloud DSP巨集
description: 參考可用的巨集以用於一般追蹤，以及追蹤第三方顯示廣告的點按次數。
feature: DSP Ads
exl-id: e31cc2e5-ad1f-4555-a87b-0e4c3731fe5f
source-git-commit: b3fc18cf84713adcff5a4208db537b03904cfa08
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 0%

---

# Advertising Cloud DSP巨集

宏是指令的簡稱或簡稱，通常遵循格式 `${MACRO_NAME}`. 創意程式碼或點進URL中包含的巨集，會展開為廣告伺服器可了解的較長程式碼字串。 Advertising Cloud DSP廣告伺服器會在提供或點按廣告時執行巨集。

廣告伺服器巨集對於將重要資訊傳遞至DSP或協力廠商廣告伺服器很實用。 巨集最常用於販運第三方和自訂創意程式碼或中繼資料（例如第三方像素）。

您可以在任何地方手動插入巨集，例如在VAST標籤、任何URL中，或在DSP或第三方事件像素中。 不過，每個DSP用戶端和合作夥伴都有不同的廣告標籤格式，因此巨集應插入標籤中的不同位置。 每次您與新用戶端或合作夥伴合作時，請向對方索取相關檔案，說明要在哪些位置插入巨集，而這些巨集會在其廣告標籤中DSP流量。

## 一般追蹤巨集

視需要使用所有廣告和標籤類型的一般追蹤巨集來傳回特定資料。

| 巨集 | 替換說明 | 類型 |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | 帳戶ID。 | 整數 |
| `${TM_AD_ID}` | 廣告金鑰(adKey)。 | 字串 |
| `${TM_AD_ID_NUM}` | 廣告ID。 | 整數 |
| `${TM_ADVERTISER_ID}` | 廣告商ID。 | 整數 |
| `${TM_CAMPAIGN_ID}` | 促銷活動金鑰。 | 字串 |
| `${TM_CAMPAIGN_ID_NUM}` | 促銷活動ID。 | 整數 |
| ` ${TM_CLICK_URL}` | 重新導向URL，可讓廣告伺服器追蹤及計算廣告點按次數。 提供廣告時，如果使用者點按廣告，則會啟動巨集，並記錄點按並計入以用於報表用途。 | 字串 |
| ` ${TM_CLICK_URL_URLENC}` | 編碼的重新導向URL，可讓廣告伺服器追蹤及計算廣告點按。 提供廣告時，如果使用者點按廣告，則會啟動巨集，並記錄點按並計入以用於報表用途。 除非您要建立協力廠商廣告，且您的廠商需要URL編碼，否則請勿使用此巨集。 | 字串 |
| `${TM_FEED_ID}` | 媒體放置的索引鍵(feedKey)。 | 字串 |
| `${TM_FEED_ID_NUM}` | 媒體投放的ID。 | 整數 |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | 版位的網站索引鍵。 需要 [!DNL AppsFlyer] 按一下行動應用程式安裝廣告的追蹤器。<!-- should map to placement_site_key column of placement_site table --> | 字串 |
| `${TM_PLACEMENT_ID}` | 位置鍵(cpKey)。 | 字串 |
| `${TM_PLACEMENT_ID_NUM}` | 版位ID。 | 整數 |
| `${TM_RANDOM}` | 快捷人：1到1000000之間的隨機數。 | long |
| `${TM_SESSION_ID}` | 工作階段的ID，與廣告標籤的單一擷取相對應。 | 字串 |
| `${TM_SITE_DOMAIN_URLENC}` | 從競標請求中的URL剖析的頁面子網域；URL編碼。 橫幅廣告中不支援點按播放廣告。 | 字串 |
| ` ${TM_SITE_NAME}` | 版位的網站名稱。 | 字串 |
| `${TM_SITE_URL_URLENC}` | 競標請求中傳遞的URL;URL編碼。 橫幅廣告中不支援點按播放廣告。 | 字串 |
| `${TM_SITE_ID_NUM}` | 版位的網站ID。 | 整數 |
| `${TM_TIMESTAMP}` | Unix時間戳記，指出自1970年1月1日午夜(00:00 UTC)以來經過的秒數。 | long |
| ` ${TM_VIDEO_DURATION}` | 廣告視訊的持續時間（以秒為單位）。 | 整數 |

{style=&quot;table-layout:auto&quot;}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## 行動專屬巨集

| 巨集 | 替換說明 | 類型 |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore])平台ID，此ID對應至裝置的作業系統：<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` 當平台為上述任一值時</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore])裝置型號名稱，以URL編碼。 | 字串 |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore])提供廣告的環境：<ul><li>`a` =行動應用程式</li><li>`b` =行動網站</li></ul> | 字串(`a` 或 `b`) |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen])平台ID，此ID對應至裝置的作業系統：<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` 當平台為上述任一值時</li></ul> | 字串 |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen])廣告檢視器所在的裝置類型：<ul><li>`TAB` =平板電腦</li><li>`PHN` = mobile</li><li>`computer` =電腦</li></ul> | 字串 |
| `${UOO}` | ([!DNL Nielsen])使用者是否已選擇退出廣告追蹤：<ul><li>`1` （DNT標幟= 1）=使用者已選擇退出廣告追蹤</li><li>`0` （DNT標幟= 0）=使用者已選擇加入廣告追蹤</li></ul> | 整數(`0` 或 `1`) |
| `${TM_BUNDLE}` | 此 [!DNL iOS] 或 [!DNL Android] 應用程式商店套件ID。 範例：com.zynga.wwf2.free或id804379658 | 字串 |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` 指出競標者是否判定競標請求來自歐盟來源且需要GDPR強制執行：<ul><li>`1` =應強制執行GDPR</li><li>`0` =不應強制執行GDPR</li></ul>`gdpr_consent=${GDPR_CONSENT}` 是傳入競標請求中從供應合作夥伴傳遞的同意值：<ul><li>在大多數情況下，這是base64url編碼的同意字串或daisybit(範例：BN5lERiOMYEdiAKAWXEND1HoSBE6CAFAApAMgBkIDIgM0AgOJxAnQA)</li><li>`0` =未同意</li><li>`1` =同意</li></ul> | daisybit或整數 |

{style=&quot;table-layout:auto&quot;}

## 按一下第三方顯示廣告的巨集

為了使用第三方顯示標籤準確追蹤廣告的點按次數，DSP需要顯示點按巨集。 只需要一個宏版本；相關巨集取決於標籤的類型。

| 巨集 | 替換說明 | 類型 |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | 可讓廣告伺服器追蹤及計算平台中廣告點按次數的重新導向URL。 | 字串 |
| `${TM_CLICK_URL_URLENC}` | 重新導向URL，可讓需要URL編碼的廣告伺服器追蹤及計算平台中的廣告點按次數。 | 字串 |

{style=&quot;table-layout:auto&quot;}

當您執行下列動作時，DSP會自動在協力廠商顯示標籤中插入顯示點按巨集：

* 從Advertising Cloud廣告伺服器合作夥伴匯出廣告標籤 <!-- [Needs PM confirmation.] -->
* 大量上傳 [!DNL Flashtalking] 或 [!DNL Google DoubleClick for Advertisers] 直接在DSP中的廣告標籤

如果您在建立顯示廣告時遺失點按巨集，DSP會顯示警告訊息，提示您在標籤的正確區域手動插入適當的顯示點按巨集。

## 疑難排解巨集錯誤

將巨集新增至程式碼時，請務必使用巨集的確切語法。 驗證巨集時，DSP會檢查該巨集是否與其中一個有效巨集完全相符。

如果宏名稱的開頭或結尾缺少字元，則會產生錯誤。 例如，若出現下列情況，您會看到錯誤訊息：

* 您會在巨集名稱的開頭忘記一或多個字元，例如 `${`. 如果您未包含完整語法，則無法將該項目辨識為有效的巨集。
* 巨集的結尾不是有效的字元集，例如 `}`.

>[!MORELIKETHIS]
>
>* [音訊廣告設定](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [已連接的電視廣告設定](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [顯示廣告設定](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [行動廣告設定](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [原生廣告設定](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [前段廣告設定](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [通用視訊廣告設定](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)

