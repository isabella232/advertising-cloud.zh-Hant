---
title: 適用於 [!DNL Analytics for Advertising Cloud]
description: 適用於 [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: 26709071be0fffb43bb3fa4666c6fa52229ad5be
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---

# 適用於 [!DNL Analytics for Advertising Cloud]

*僅具有Advertising Cloud-Adobe Analytics整合的廣告商*

*僅包含Advertising Cloud DSP的廣告商*

對於Advertising Cloud DSP, [!DNL Analytics for Advertising Cloud] 整合會追蹤閱覽和點進網站的互動。 您的網頁上的標準Adobe Analytics程式碼會追蹤點進造訪；the [!DNL Analytics] 程式碼會擷取登陸頁面URL中的AMO ID和EF ID參數，並在各自保留的eVar中追蹤這些參數。 您可以在網頁中部署兩行JavaScript程式碼，以追蹤閱覽造訪。

在造訪網站的第一個頁面檢視中，Advertising Cloud JavaScript程式碼會檢查訪客之前是否曾檢視或點按過廣告。 如果使用者先前透過點進方式進入網站，或未看到廣告，則會忽略訪客。 如果訪客看過廣告，且未在 [點按回顧期間](/help/integrations/analytics/prerequisites.md#lookback-a4adc) 在Advertising Cloud中設定，則Advertising Cloud JavaScript程式碼會使用 [Experience CloudID服務](https://experienceleague.adobe.com/docs/id-service/using/home.html) 產生補充ID(`SDID`)，可將Advertising Cloud的資料匯整至訪客的Adobe Analytics點擊。 Adobe Analytics接著會查詢Advertising Cloud，找出與廣告曝光度相關聯的AMO ID和EF ID。 AMO ID和EF ID接著會填入各自的eVar中。 這些值會持續指定的期間（預設為60天）。

[!DNL Analytics] 傳送網站流量量度（例如頁面檢視、造訪和逗留時間）和 [!DNL Analytics] 以EF ID為索引鍵，將自訂或標準事件每小時轉換為Advertising Cloud 。 這些 [!DNL Analytics] 然後，透過Advertising Cloud歸因系統執行量度，將轉換連結至點按和曝光記錄。

>[!NOTE]
>
>Advertising Cloud JavaScript追蹤邏輯發生在Adobe端，因此對頁面載入時間幾乎沒有影響。
>
>相反地， [!DNL DCM] 資料連接器 [!DNL Analytics] (使用 [!DNL Google Campaign Manager 360])(針對Advertising Cloud DSP)。 用戶端連結會降低頁面載入速度，並增加資料遺失的風險。 這是因為 [!DNL Analytics] JavaScript必須Ping [!DNL DoubleClick] 等待 [!DNL DoubleClick] 若要傳回上次點按/曝光資料至 [!DNL Analytics]. 當 [!DNL DSP] 團隊設定 [!DNL DCM] data connector，您必須指定您願意延遲頁面的時間。

## 部署JavaScript程式碼

JavaScript程式庫包含兩行，允許 [!DNL Analytics] 和Advertising Cloud互相溝通。 若 [!DNL Analytics for Advertising Cloud] 整合在Advertising Cloud實作期間完成，您應已收到此程式碼，其中包含如何部署的指示。

如果您尚未取得程式碼，請聯絡Advertising Cloud支援團隊。

### 程式碼的放置位置

此 [!DNL Analytics for Advertising Cloud] JavaScript函式必須位於Experience CloudID服務之後，而位於Analytics應用程式測量程式碼之前，以便提供補充ID(`SDID`)可包含在Analytics呼叫中。

![程式碼放置](/help/integrations/assets/a4adc-code-placement.png)

### 驗證程式碼部署

您可以使用任何封包嗅探器類型的工具(例如 [!DNL Charles], [!DNL Fiddler]，或 [!DNL Chrome Developer Tools])，比較前往Advertising Cloud的請求與前往 [!DNL Analytics]，如下所述。

#### 如何確認程式碼 [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. 開啟 [!DNL Chrome Developer Tools] 並按一下 **網路** 標籤。
1. 載入包含 [!DNL Analytics for Advertising Cloud] JavaScript。
1. 篩選 [!UICONTROL Network] 標籤 `last` 並檢閱兩列：

   ![上次篩選](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * 第一列是對JavaScript程式庫的呼叫，並且會加上標題 `last-event-tag-latest.min.js`.
   * 第二行是傳送要求至Advertising Cloud的呼叫。 開頭如下： `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      如果您沒有看到對Advertising Cloud的呼叫，則可能不是您造訪的第一個頁面檢視。 為了測試之用，您可以移除Cookie，這樣下次呼叫就會是對應造訪的第一個頁面檢視：

      1. 在「應用程式」標籤上，找到 `adcloud` cookie，並確認cookie包含 `_les_v` （上次造訪），其值為 `y` 以及30分鐘後到期的UTC紀元時間戳記。
      1. 刪除 `ad cloud` cookie並重新整理頁面。
1. 篩選 `/b/ss` 來查看Analytics點擊。

   ![篩選 `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. 比較兩次點擊之間的ID值。 除了Analytics點擊中的報表套裝ID（緊接在後的URL路徑）之外，所有值都會位於查詢字串參數中 `/b/ss/`.

   | ID | Analytics參數 | Advertising Cloud參數 |
   |--- |--- |--- |
   | Experience CloudIMS組織 | `mcorgid` | `_les_imsOrgid` |
   | 補充資料ID | sdid | `_les_sdid` |
   | Analytics報表套裝 | 之後的值 `/b/ss/` | `_les_rsid` |
   | Experience Cloud訪客ID | mid | `_les_mid` |

   如果ID值相符，則確認JavaScript實施。 Advertising Cloud會 [!DNL Analytics] 伺服器任何點進或閱覽追蹤詳細資料（如果存在）。

#### 如何確認程式碼 [!DNL Adobe Experience Cloud Debugger]

1. 開啟 [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html) 在首頁上。
1. 前往 [!UICONTROL Network] 標籤。
1. 在 [!UICONTROL Solutions Filter] 按一下 [!UICONTROL Advertising Cloud] 和 [!UICONTROL Analytics].
1. 在 [!UICONTROL Request URL – Hostname] 參數行，查找 `lasteventf-tm.everesttech.net`.
1. 在 [!UICONTROL Request – Parameters*] 列，稽核產生的訊號，類似於「[如何確認程式碼 [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * 檢查以確定 `SDID` 參數符合 `Supplemental Data ID` 在Adobe Analytics篩選器中。
   * 如果程式碼未產生，請檢查以確定Advertising Cloud Cookie已移除 [!UICONTROL Application] 標籤。 移除後，重新整理頁面並重複此程式。

   ![稽核 [!DNL Analytics for Advertising Cloud] 中的JavaScript程式碼 [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [實作的必要條件和重要資訊 [!DNL Analytics for Advertising Cloud]](prerequisites.md)

