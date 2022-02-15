---
title: JavaScript代碼 [!DNL Analytics for Advertising Cloud]
description: JavaScript代碼 [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: 7bf8f3524954b17d9da336a2210a098bf571399e
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 0%

---

# JavaScript代碼 [!DNL Analytics for Advertising Cloud]

*只有Advertising Cloud-Adobe Analytics整合的廣告商*

*僅包含Advertising Cloud DSP的廣告商*

對Advertising Cloud DSP來說 [!DNL Analytics for Advertising Cloud] 整合跟蹤查看和點擊瀏覽站點交互。 點擊訪問按您網頁上的標準Adobe Analytics代碼進行跟蹤；這樣 [!DNL Analytics] 代碼捕獲登錄頁URL中的AMO ID和EF ID參數，並在各自的保留eVar中跟蹤它們。 通過在網頁中部署JavaScript代碼段，可以跟蹤查看訪問。

在訪問站點的首頁視圖上，Advertising CloudJavaScript代碼會檢查訪問者以前是否看過或點擊過廣告。 如果用戶以前通過點擊方式輸入了站點或未看到廣告，則訪問者將被忽略。 如果訪問者在訪問期間看到廣告，並且未通過點擊進入站點 [按一下「回望」窗口](/help/integrations/analytics/prerequisites.md#lookback-a4adc) 在Advertising Cloud內設定，然後Advertising CloudJavaScript代碼a)使用 [Experience CloudID服務](https://experienceleague.adobe.com/docs/id-service/using/home.html) 生成補充ID(`SDID`)或b)使用Adobe Experience Platform [!DNL Web SDK] `generateRandomID` 生成方法 `[!DNL StitchID]`。 任何一個ID都用於將資料從Advertising Cloud縫製到遊客的Adobe Analytics。 Adobe Analytics隨後查詢Advertising Cloud，以查找與廣告曝光相關聯的AMO ID和EF ID。 AMO ID和EF ID隨後被填充到它們各自的eVar中。 這些值在指定期間（預設為60天）內持續。

[!DNL Analytics] 發送站點流量度量（如頁面視圖、訪問和花費的時間）和 [!DNL Analytics] 使用EF ID作為鍵，將自定義或標準事件按小時發送到Advertising Cloud。 這些 [!DNL Analytics] 然後，通過Advertising Cloud歸屬系統來將轉換與點擊和曝光歷史記錄相連。

>[!NOTE]
>
>Advertising CloudJavaScript跟蹤邏輯發生在Adobe側，因此對頁面載入時間幾乎沒有影響。
>
>相反，我們的邏輯 [!DNL DCM] 資料連接器 [!DNL Analytics] (使用 [!DNL Google Campaign Manager 360]),Advertising Cloud DSP在客戶端。 客戶端縫合降低了頁面負載並增加了資料丟失的風險。 這是因為 [!DNL Analytics] JavaScript必須ping [!DNL DoubleClick] 等待 [!DNL DoubleClick] 將上次按一下/印象資料傳回 [!DNL Analytics]。 當 [!DNL DSP] 團隊設定 [!DNL DCM] 資料連接器，必須指定您願意延遲頁面的時間。

## 部署JavaScript代碼

JavaScript庫由兩行組成，它們允許 [!DNL Analytics] 和Advertising Cloud互相溝通。 如果 [!DNL Analytics for Advertising Cloud] 整合在Advertising Cloud實施期間完成，您應該收到此代碼並說明如何部署它。

**(使用Experience Cloud標識服務的實現 `visitorAPI.js` 代碼)**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

**(使用該Experience Platform的實現 [!DNL Web SDK] `alloy.js`代碼)**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

### 代碼放置位置

的 [!DNL Analytics for Advertising Cloud] JavaScript函式必須位於Experience CloudID服務之後，但必須位於分析應用程式測量代碼之前，以便補充ID(`SDID`)或 `[!DNL StitchID]` 可以包含在分析呼叫中。

![代碼放置](/help/integrations/assets/a4adc-code-placement.png)

### 驗證代碼部署

可以使用任何資料包嗅探器類型的工具(如 [!DNL Charles]。 [!DNL Fiddler]或 [!DNL Chrome Developer Tools])，通過比較傳往Advertising Cloud的請求和將傳往 [!DNL Analytics]，如下所述。

#### 如何確認代碼 [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. 開啟 [!DNL Chrome Developer Tools] 並按一下 **網路** 頁籤。

1. 載入包含 [!DNL Analytics for Advertising Cloud] JavaScript。

1. 篩選 [!UICONTROL Network] 頁籤 `last` 並查看兩行：

   ![上次篩選](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * 第一行是對JavaScript庫的調用，標題為 `last-event-tag-latest.min.js`。
   * 第二行是將請求發送到Advertising Cloud的呼叫。 開始如下： `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      如果你沒有看到致Advertising Cloud的電話，那可能不是你訪問的第一頁。 為了測試目的，您可以刪除cookie，以便下次調用將是相應訪問的第一個頁面視圖：

      1. 在「應用程式」頁籤上，查找 `adcloud` cookie ，並驗證cookie是否包含 `_les_v` (上次訪問，其值為 `y` 以及30分鐘後過期的UTC時間戳。
      1. 刪除 `ad cloud` cookie並刷新頁面。

1. (使用Experience Cloud標識服務的實現 `visitorAPI.js` 代碼)篩選 `/b/ss` 查看分析命中。

   ![篩選於 `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (使用該Experience Platform的實現 [!DNL Web SDK] `alloy.js`代碼)篩選 `/interact` 驗證到邊緣網路的請求負載是否包含 `advertisingStitchID`。

   ![篩選於 `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. 比較兩個命中的ID值。 除分析命中的報告套件ID（即緊接在後面的URL路徑）外，所有值都將位於查詢字串參數中 `/b/ss/`。

   | ID | 分析參數 | 邊緣網路 | Advertising Cloud參數 |
   | --- | --- | --- | --- |
   | Experience CloudIMS組織 | `mcorgid` |  | `_les_imsOrgid` |
   | 補充資料ID | 斯 |  | `_les_sdid` |
   | 縫合ID | stitchId | `advertisingStitchID` 下 `_adcloud` 屬性 |  |
   | 分析報告套件 | 之後的值 `/b/ss/` |  | `_les_rsid` |
   | Experience Cloud訪問者ID | 中 |  | `_les_mid` |

   如果ID值匹配，則確認JavaScript實現。 Advertising Cloud會 [!DNL Analytics] 伺服器任何按一下或查看跟蹤詳細資訊（如果存在）。

#### 如何確認代碼 [!DNL Adobe Experience Cloud Debugger]

1. 開啟 [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html) 首頁上。
1. 轉到 [!UICONTROL Network] 頁籤。
1. 在 [!UICONTROL Solutions Filter] 工具欄，按一下 [!UICONTROL Advertising Cloud] 和 [!UICONTROL Analytics]。
1. 在 [!UICONTROL Request URL – Hostname] 參數行，定位 `lasteventf-tm.everesttech.net`。
1. 在 [!UICONTROL Request – Parameters] 行，審核生成的信號，類似於「」中的步驟3[如何確認代碼 [!DNL Chrome Developer Tools]](#validate-js-chrome)&quot;
   * (使用Experience Cloud標識服務的實現 `visitorAPI.js` 代碼)確保 `Sdid` 參數匹配 `Supplemental Data ID` 在Adobe Analytics過濾器上。
   * (使用該Experience Platform的實現 [!DNL Web SDK] `alloy.js`代碼)確保 `advertisingStitchID` 參數匹配 `Sdid` 發送到Experience Platform邊緣網路。
   * 如果未生成代碼，請檢查以確保已在 [!UICONTROL Application] 頁籤。 刪除後，刷新頁面並重複該過程。

   ![審計 [!DNL Analytics for Advertising Cloud] JavaScript代碼 [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [實施的先決條件和關鍵資訊 [!DNL Analytics for Advertising Cloud]](prerequisites.md)

