---
title: 適用於 [!DNL Analytics for Advertising]
description: 適用於 [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 0%

---

# 適用於 [!DNL Analytics for Advertising]

*廣告商與Adobe廣告 — 僅Adobe Analytics整合*

*僅具有Advertising DSP的廣告商*

若為Advertising DSP, [!DNL Analytics for Advertising] 整合會追蹤閱覽和點進網站的互動。 您的網頁上的標準Adobe Analytics程式碼會追蹤點進造訪；the [!DNL Analytics] 程式碼會擷取登陸頁面URL中的AMO ID和EF ID參數，並在各自保留的eVar中追蹤這些參數。 您可以在網頁中部署JavaScript程式碼片段，以追蹤閱覽造訪。

在造訪網站的第一個頁面檢視中，AdobeAdvertising JavaScript程式碼會檢查訪客之前是否看過或點擊過廣告。 如果使用者先前透過點進方式進入網站，或未看到廣告，則會忽略訪客。 如果訪客看過廣告，且未在 [點按回顧期間](/help/integrations/analytics/prerequisites.md#lookback-a4adc) 在Adobe廣告中設定，則Adobe廣告JavaScript程式碼a)會使用 [Experience CloudID服務](https://experienceleague.adobe.com/docs/id-service/using/home.html) 產生補充ID(`SDID`)或b)使用Adobe Experience Platform [!DNL Web SDK] `generateRandomID` 生成方法 `[!DNL StitchID]`. 其中一個ID可用來將資料從Adobe廣告連結至訪客的Adobe Analytics點擊。 Adobe Analytics接著會查詢AdobeAdvertising，以取得與廣告曝光度相關聯的AMO ID和EF ID。 AMO ID和EF ID接著會填入各自的eVar中。 這些值會持續指定的期間（預設為60天）。

[!DNL Analytics] 傳送網站流量量度（例如頁面檢視、造訪和逗留時間）和 [!DNL Analytics] 自訂或標準事件，以EF ID為索引鍵，每小時AdobeAdvertising 。 這些 [!DNL Analytics] 然後，透過「Adobe廣告」歸因系統執行量度，將轉換連結至點按和曝光記錄。

>[!NOTE]
>
>Adobe廣告JavaScript追蹤邏輯發生在Adobe端，因此對頁面載入時間幾乎沒有影響。
>
>相反地， [!DNL DCM] 資料連接器 [!DNL Analytics] (使用 [!DNL Google Campaign Manager 360])(針對DSP)，會發生在用戶端。 用戶端連結會降低頁面載入速度，並增加資料遺失的風險。 這是因為 [!DNL Analytics] JavaScript必須Ping [!DNL DoubleClick] 等待 [!DNL DoubleClick] 若要傳回上次點按/曝光資料至 [!DNL Analytics]. 當 [!DNL DSP] 團隊設定 [!DNL DCM] data connector，您必須指定您願意延遲頁面的時間。

## 部署JavaScript程式碼

JavaScript程式庫包含兩行，允許 [!DNL Analytics] 和Adobe廣告，以相互溝通。 若 [!DNL Analytics for Advertising] 整合已在「Adobe廣告」實作期間完成，則您應已收到此程式碼，其中包含如何部署的指示。

### 程式碼

#### 使用Experience CloudIdentity Service的實作 `visitorAPI.js` 代碼

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

#### 使用Experience Platform的實作 [!DNL Web SDK] `alloy.js`代碼

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

### 程式碼的放置位置

此 [!DNL Analytics for Advertising] JavaScript函式必須位於Experience CloudID服務之後，而位於Analytics應用程式測量程式碼之前，以便提供補充ID(`SDID`)或 `[!DNL StitchID]` 可包含在Analytics呼叫中。

![程式碼放置](/help/integrations/assets/a4adc-code-placement.png)

### 驗證程式碼部署

您可以使用任何封包嗅探器類型的工具(例如 [!DNL Charles], [!DNL Fiddler]，或 [!DNL Chrome Developer Tools])，比較前往「Adobe廣告」的請求與前往 [!DNL Analytics]，如下所述。

#### 如何確認程式碼 [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. 開啟 [!DNL Chrome Developer Tools] 並按一下 **網路** 標籤。

1. 載入包含 [!DNL Analytics for Advertising] JavaScript。

1. 篩選 [!UICONTROL Network] 標籤 `last` 並檢閱兩列：

   ![上次篩選](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * 第一列是對JavaScript程式庫的呼叫，並且會加上標題 `last-event-tag-latest.min.js`.
   * 第二列是傳送要求至Adobe廣告的呼叫。 開頭如下： `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      如果您沒有看見對Adobe廣告的呼叫，則可能不是您造訪的第一個頁面檢視。 為了測試之用，您可以移除Cookie，這樣下次呼叫就會是對應造訪的第一個頁面檢視：

      1. 在「應用程式」標籤上，找到 `adcloud` cookie，並確認cookie包含 `_les_v` （上次造訪），其值為 `y` 以及30分鐘後到期的UTC紀元時間戳記。
      1. 刪除 `ad cloud` cookie並重新整理頁面。

1. (使用Experience CloudIdentity Service的實作 `visitorAPI.js` 代碼)篩選 `/b/ss` 來查看Analytics點擊。

   ![篩選 `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (使用Experience Platform的實作 [!DNL Web SDK] `alloy.js`代碼)篩選 `/interact` 驗證傳送至邊緣網路的要求裝載包含 `advertisingStitchID`.

   ![篩選 `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. 比較兩次點擊之間的ID值。 除了Analytics點擊中的報表套裝ID（緊接在後的URL路徑）之外，所有值都會位於查詢字串參數中 `/b/ss/`.

   | ID | Analytics參數 | 邊緣網路 | Adobe廣告參數 |
   | --- | --- | --- | --- |
   | Experience CloudIMS組織 | `mcorgid` |  | `_les_imsOrgid` |
   | 補充資料ID | sdid |  | `_les_sdid` |
   | Stitch ID | stitchId | `advertisingStitchID` 在 `_adcloud` 屬性 |  |
   | Analytics報表套裝 | 之後的值 `/b/ss/` |  | `_les_rsid` |
   | Experience Cloud訪客ID | mid |  | `_les_mid` |

   如果ID值相符，則確認JavaScript實施。 Adobe廣告會將 [!DNL Analytics] 伺服器任何點進或閱覽追蹤詳細資料（如果存在）。

#### 如何確認程式碼 [!DNL Adobe Experience Cloud Debugger]

1. 開啟 [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) 在首頁上。
1. 前往 [!UICONTROL Network] 標籤。
1. 在 [!UICONTROL Solutions Filter] 按一下 [!UICONTROL Adobe Advertising] 和 [!UICONTROL Analytics].
1. 在 [!UICONTROL Request URL – Hostname] 參數行，查找 `lasteventf-tm.everesttech.net`.
1. 在 [!UICONTROL Request – Parameters] 列，稽核產生的訊號，類似於「[如何確認程式碼 [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * (使用Experience CloudIdentity Service的實作 `visitorAPI.js` 程式碼)請確定 `Sdid` 參數符合 `Supplemental Data ID` 在Adobe Analytics篩選器中。
   * (使用Experience Platform的實作 [!DNL Web SDK] `alloy.js`程式碼)請確定 `advertisingStitchID` 參數符合 `Sdid` 傳送至Experience Platform邊緣網路。
   * 如果程式碼未產生，請檢查以確定Adobe廣告Cookie已移除，位於 [!UICONTROL Application] 標籤。 移除後，重新整理頁面並重複此程式。

   ![稽核 [!DNL Analytics for Advertising] 中的JavaScript程式碼 [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising]](overview.md)
>* [實作的必要條件和重要資訊 [!DNL Analytics for Advertising]](prerequisites.md)

