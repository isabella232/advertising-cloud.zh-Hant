---
title: Advertising Cloud DSP宏
description: 參考可用宏以進行常規跟蹤並跟蹤第三方顯示廣告的點擊量。
feature: DSP Ads
exl-id: e31cc2e5-ad1f-4555-a87b-0e4c3731fe5f
source-git-commit: fbadd81a34c375f00fa3e420ea3c46fc9143daf8
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# Advertising Cloud DSP宏

宏是指令的簡短命令或速記，通常遵循格式 `${MACRO_NAME}`。 創作代碼或點擊式URL中包含的宏會擴展為廣告伺服器能夠理解的較長代碼字串。 Advertising Cloud DSP廣告伺服器在提供或按一下廣告時執行宏。

Ad伺服器宏用於將重要資訊傳DSP遞給第三方Ad伺服器。 在販運第三方和自定義創作代碼或元資料（如第三方像素）期間，最常使用宏。

可以在任意位置手動插入宏，如在VAST標籤、任何URL中、或在第DSP三方事件像素中。 但是，每DSP個客戶端和夥伴都有不同的廣告標籤格式，因此宏應相應地插入標籤中的不同位置。 每次與新客戶機或合作夥伴合作時，請向他們詢問有關在他們的廣告標籤中插入宏的位置DSP文檔。

## 常規跟蹤宏

根據需要，在所有廣告和標籤類型中使用常規跟蹤宏來傳遞特定資料。

| 宏 | 替換說明 | 類型 |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | 帳戶ID。 | 整數 |
| `${TM_AD_ID}` | 廣告鍵(adKey)。 | 字串 |
| `${TM_AD_ID_NUM}` | 廣告ID。 | 整數 |
| `${TM_ADVERTISER_ID}` | 廣告商ID。 | 整數 |
| `${TM_CAMPAIGN_ID}` | 競選密鑰。 | 字串 |
| `${TM_CAMPAIGN_ID_NUM}` | 市場活動ID。 | 整數 |
| ` ${TM_CLICK_URL}` | 重定向URL，它使廣告伺服器能夠跟蹤和計數廣告點擊量。 當廣告服務時，如果用戶按一下它，則激活宏，並記錄並清點按一下以用於報告目的。 | 字串 |
| ` ${TM_CLICK_URL_URLENC}` | 編碼的重定向URL，使廣告伺服器能夠跟蹤和計數廣告點擊量。 當廣告服務時，如果用戶按一下它，則激活宏，並記錄並清點按一下以用於報告目的。 除非您正在建立第三方廣告，並且供應商需要URL編碼，否則不要使用此宏。 | 字串 |
| `${TM_FEED_ID}` | 媒體放置的鍵(feedKey)。 | 字串 |
| `${TM_FEED_ID_NUM}` | 媒體放置的ID。 | 整數 |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | 放置的站點鍵。 需要 [!DNL AppsFlyer] 按一下「跟蹤器」以獲取移動應用安裝廣告。<!-- should map to placement_site_key column of placement_site table --> | 字串 |
| `${TM_PLACEMENT_ID}` | 放置鍵(cpKey)。 | 字串 |
| `${TM_PLACEMENT_ID_NUM}` | 放置ID。 | 整數 |
| `${TM_RANDOM}` | 卡切巴斯特：1到100000之間的隨機數。 | 長 |
| `${TM_SESSION_ID}` | 會話的ID，它對應於廣告標籤的單個檢索。 | 字串 |
| `${TM_SITE_DOMAIN_URLENC}` | 從投標請求中的URL解析的頁面子域；URL編碼。 橫幅廣告不支援點擊播放廣告。 | 字串 |
| ` ${TM_SITE_NAME}` | 放置的站點名稱。 | 字串 |
| `${TM_SITE_URL_URLENC}` | 投標請求中傳遞的URL;URL編碼。 橫幅廣告不支援點擊播放廣告。 | 字串 |
| `${TM_SITE_ID_NUM}` | 放置的站點ID。 | 整數 |
| `${TM_TIMESTAMP}` | 指示自1970年1月1日午夜(00:00 UTC)以來已用秒數的Unix時間戳。 | 長 |
| ` ${TM_VIDEO_DURATION}` | 廣告視頻的持續時間（秒）。 | 整數 |

{style=&quot;table-layout:auto&quot;&quot;

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## 移動特定宏

| 宏 | 替換說明 | 類型 |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore])平台ID，它與設備的作業系統相對應：<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` 當平台不是上面的</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore])設備型號名稱，URL編碼。 | 字串 |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore])提供廣告的環境：<ul><li>`a` =移動應用程式</li><li>`b` =移動網站</li></ul> | 字串(`a` 或 `b`) |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen])平台ID，它與設備的作業系統相對應：<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` 當平台不是上面的</li></ul> | 字串 |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen])ad所在的設備類型：<ul><li>`TAB` =平板電腦</li><li>`PHN` =移動</li><li>`computer` =電腦</li></ul> | 字串 |
| `${UOO}` | ([!DNL Nielsen])用戶是否已選擇不進行廣告跟蹤：<ul><li>`1` （DNT標誌= 1）=用戶已選擇退出廣告跟蹤</li><li>`0` （DNT標誌= 0）=用戶已選擇加入廣告跟蹤</li></ul> | 整數(`0` 或 `1`) |
| `${TM_BUNDLE}` | 的 [!DNL iOS] 或 [!DNL Android] 應用商店包ID。 示例：com.zynga.wwf2.free或id804379658 | 字串 |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` 指示投標人是否確定投標請求來自歐盟並要求GDPR強制執行：<ul><li>`1` =應強制執行GDPR</li><li>`0` =不應強制執行GDPR</li></ul>`gdpr_consent=${GDPR_CONSENT}` 是入站投標請求中從供應夥伴傳遞的同意值：<ul><li>在大多數情況下，這是base64url編碼的同意字串或daisybit(例如：BN5lERiOMYEdiAKAWXEND1HoSBE6CAFAApAMgBkIDIgM0AgOJxAnQA)</li><li>`0` =未同意</li><li>`1` =同意</li></ul> | daisbit或整數 |

{style=&quot;table-layout:auto&quot;&quot;

## 按一下「第三方顯示廣告的宏」

要使用第三方顯示標籤準確跟蹤廣告的點擊量，DSP需要顯示按一下宏。 只需要一個宏版本；相關宏取決於標籤的類型。

| 宏 | 替換說明 | 類型 |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | 使廣告伺服器能夠跟蹤和計數平台中的廣告點擊量的重定向URL。 | 字串 |
| `${TM_CLICK_URL_URLENC}` | 重定向URL，它使需要URL編碼的廣告伺服器能夠跟蹤和計數平台中的廣告點擊量。 | 字串 |

{style=&quot;table-layout:auto&quot;&quot;

在DSP以下情況下，自動將顯示按一下宏插入第三方顯示標籤：

* 從Advertising Cloud廣告伺服器合作夥伴導出廣告標籤 <!-- [Needs PM confirmation.] -->
* 批量上載 [!DNL Flashtalking] 或 [!DNL Google DoubleClick for Advertisers] 直接將標籤放DSP在

如果在生成顯示廣告時缺少按一下宏，則DSP會顯示警告消息，提示您在標籤的正確區域手動插入適當的顯示按一下宏。

## 排除宏錯誤

在代碼中添加宏時，請確保使用宏的準確語法。 驗證宏時，檢DSP查宏是否與一個有效宏完全匹配。

如果宏名稱的開頭或結尾缺少字元，則會生成錯誤。 例如，在以下情況下，您將看到一條錯誤消息：

* 在宏名稱的開頭會忘記一個或多個字元，如 `${`。 如果不包括完整語法，則該條目將不被識別為有效宏。
* 宏不以有效字元集結尾，如 `}`。

>[!MORELIKETHIS]
>
>* [音頻廣告設定](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [連接的電視廣告設定](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [顯示廣告設定](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [移動廣告設定](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [本機廣告設定](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [預滾動廣告設定](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)

