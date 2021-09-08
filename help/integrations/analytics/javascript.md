---
title: ' [!DNL Analytics for Advertising Cloud]的JavaScript程式碼'
description: ' [!DNL Analytics for Advertising Cloud]的JavaScript程式碼'
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---

# [!DNL Analytics for Advertising Cloud]的JavaScript程式碼

*僅具有Advertising Cloud-Adobe Analytics整合的廣告商*

*僅包含Advertising Cloud DSP的廣告商*

若為Advertising Cloud DSP,[!DNL Analytics for Advertising Cloud]整合會追蹤閱覽和點進網站互動。 您的網頁上的標準Adobe Analytics程式碼會追蹤點進造訪；[!DNL Analytics]程式碼會擷取登陸頁面URL中的AMO ID和EF ID參數，並在各自保留的eVar中追蹤這些參數。 您可以在網頁中部署兩行JavaScript程式碼，以追蹤閱覽造訪。

在造訪網站的第一個頁面檢視中，Advertising Cloud JavaScript程式碼會檢查訪客之前是否曾檢視或點按過廣告。 如果使用者先前透過點進方式進入網站，或未看到廣告，則會忽略訪客。 如果訪客在Advertising Cloud內設定的[點擊回顧期間](/help/integrations/analytics/prerequisites.md#lookback-a4adc)內看見廣告且未透過點進進入網站，則Advertising Cloud JavaScript程式碼會使用[Experience CloudID服務](https://experienceleague.adobe.com/docs/id-service/using/home.html)產生補充ID(`SDID`)，用於將來自Advertising Cloud的資料拼接至訪客的Adobe Analytics點擊。 Adobe Analytics接著會查詢Advertising Cloud，找出與廣告曝光度相關聯的AMO ID和EF ID。 AMO ID和EF ID接著會填入各自的eVar中。 這些值會持續指定的期間（預設為60天）。

[!DNL Analytics] 以EF ID為索引鍵，每小時傳送網站流量量度(例如頁面檢視、造 [!DNL Analytics]  訪和逗留時間)以及任何自訂或標準事件至Advertising Cloud。接著，這些[!DNL Analytics]量度會透過Advertising Cloud歸因系統執行，將轉換連結至點按和曝光記錄。

>[!NOTE]
>
>Advertising Cloud JavaScript追蹤邏輯發生在Adobe端，因此對頁面載入時間幾乎沒有影響。
>
>相反地，用戶端會執行[!DNL DCM]資料連接器至[!DNL Analytics]（使用[!DNL Google Campaign Manager 360]）的Advertising Cloud DSP邏輯。 用戶端連結會降低頁面載入速度，並增加資料遺失的風險。 發生此情況是因為[!DNL Analytics] JavaScript必須Ping [!DNL DoubleClick] ，並等待[!DNL DoubleClick]將上次點按/曝光資料傳回[!DNL Analytics]。 當您的[!DNL DSP]團隊設定[!DNL DCM]資料連接器時，您必須指定您願意延遲頁面的時間。

## 部署JavaScript程式碼

JavaScript程式庫包含兩行，可讓[!DNL Analytics]和Advertising Cloud彼此通訊。 如果在Advertising Cloud實作期間完成[!DNL Analytics for Advertising Cloud]整合，您應該已收到此程式碼，其中包含如何部署的指示。

如果您尚未取得程式碼，請聯絡Advertising Cloud支援團隊。

### 程式碼的放置位置

[!DNL Analytics for Advertising Cloud] JavaScript函式必須在Experience CloudID服務之後、在Analytics應用程式測量程式碼之前，才能在Analytics呼叫中加入補充ID(`SDID`)。

![程式碼放置](/help/integrations/assets/a4adc-code-placement.png)

### 驗證程式碼部署

您可以使用任何封包Sniffer類型的工具（例如[!DNL Charles]、[!DNL Fiddler]或[!DNL Chrome Developer Tools]），比較前往Advertising Cloud的請求與前往[!DNL Analytics]的請求之間四個ID的值，以執行驗證，如下所述。

#### 如何使用[!DNL Chrome Developer Tools]確認程式碼 {#validate-js-chrome}

1. 開啟[!DNL Chrome Developer Tools]，然後按一下&#x200B;**Network**&#x200B;頁簽。
1. 載入包含[!DNL Analytics for Advertising Cloud] JavaScript的網站頁面。
1. 依`last`篩選[!UICONTROL Network]標籤並檢閱兩列：

   ![上次篩選](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * 第一行是對JavaScript程式庫的呼叫，其標題為`last-event-tag-latest.min.js`。
   * 第二行是傳送要求至Advertising Cloud的呼叫。 開頭如下：`_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      如果您沒有看到對Advertising Cloud的呼叫，則可能不是您造訪的第一個頁面檢視。 為了測試之用，您可以移除Cookie，這樣下次呼叫就會是對應造訪的第一個頁面檢視：

      1. 在「應用程式」標籤上，找出`adcloud` Cookie，並確認Cookie包含值`y`的`_les_v`（上次造訪），以及30分鐘後到期的UTC紀元時間戳記。
      1. 刪除`ad cloud` Cookie並重新整理頁面。
1. 篩選`/b/ss`以查看Analytics點擊。

   ![篩選  `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. 比較兩次點擊之間的ID值。 除了Analytics點擊中的報表套裝ID（緊接在`/b/ss/`之後的URL路徑）之外，所有值都會位於查詢字串參數中。

   | ID | Analytics參數 | Advertising Cloud參數 |
   |--- |--- |--- |
   | Experience CloudIMS組織 | `mcorgid` | `_les_imsOrgid` |
   | 補充資料ID | sdid | `_les_sdid` |
   | Analytics報表套裝 | `/b/ss/`之後的值 | `_les_rsid` |
   | Experience Cloud訪客ID | mid | `_les_mid` |

   如果ID值相符，則確認JavaScript實施。 Advertising Cloud會傳送[!DNL Analytics]伺服器任何點進或閱覽追蹤詳細資料（若有）。

#### 如何使用[!DNL Adobe Experience Cloud Debugger]確認程式碼

1. 在首頁上開啟[[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html)。
1. 前往[!UICONTROL Network]標籤。
1. 在[!UICONTROL Solutions Filter]工具列中，按一下[!UICONTROL Advertising Cloud]和[!UICONTROL Analytics]。
1. 在[!UICONTROL Request URL – Hostname]參數行中，找到`lasteventf-tm.everesttech.net`。
1. 在[!UICONTROL Request – Parameters*]列中，稽核產生的訊號，類似「[How to Confirm the Code with [!DNL Chrome Developer Tools]](#validate-js-chrome)」中的步驟3。
   * 檢查以確定`SDID`參數符合Adobe Analytics篩選器中的`Supplemental Data ID`。
   * 如果程式碼未產生，則檢查以確定Advertising Cloud Cookie已在[!UICONTROL Application]標籤中移除。 移除後，重新整理頁面並重複此程式。

   ![審核 [!DNL Analytics for Advertising Cloud] 中的JavaScript程式碼  [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [實作的必要條件和重要資訊 [!DNL Analytics for Advertising Cloud]](prerequisites.md)

