---
title: Adobe廣告ID：使用者 [!DNL Analytics]
description: Adobe廣告ID：使用者 [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ed1aab7b-9bd0-4d42-9bfb-9c6fa6db76bc
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '1186'
ht-degree: 0%

---

# Adobe廣告ID：使用者 [!DNL Analytics]

*廣告商與Adobe廣告 — 僅Adobe Analytics整合*

*適用於Advertising DSP和[!DNL Advertising Search]*

Adobe廣告使用兩個ID進行站上效能追蹤：the *EF ID* 和 *AMO ID*.

當出現廣告曝光時，Adobe廣告會建立AMO ID和EF ID值並加以儲存。 看過廣告的訪客未點按廣告就進入網站時， [!DNL Analytics] 從Adobe廣告呼叫這些值，透過 [!DNL Analytics for Advertising] JavaScript程式碼。 若為閱覽流量， [!DNL Analytics] 產生補充ID(`SDID`)，此ID可用來將EF ID和AMO ID匯整至 [!DNL Analytics]. 若為點進流量，這些ID會包含在使用 `s_kwcid` 和 `ef_id` 查詢字串參數。

Adobe廣告使用下列條件，來區分網站的點進或閱覽項目：

* 當使用者檢視廣告但未點按廣告後造訪網站時，會擷取閱覽項目。 [!DNL Analytics] 如果符合兩個條件，則記錄閱覽：
   * 訪客沒有 [!DNL DSP] 或 [!DNL Search] 廣告期間 [點按回顧期間](#lookback-a4adc).
   * 訪客至少看到一個 [!DNL DSP] 廣告期間 [印象回顧期間](#lookback-a4adc). 最後一次曝光會以閱覽傳遞。
* 當網站訪客進入網站前點按廣告時，會擷取點進項目。 [!DNL Analytics] 在下列任一情況發生時擷取點進：
   * 此URL包含EF ID和AMO ID，如Adobe廣告所新增至登陸頁面URL。
   * URL不包含追蹤代碼，但Adobe廣告JavaScript程式碼會在過去兩分鐘內偵測到點按。

![Adobe廣告檢視型 [!DNL Analytics] 整合](/help/integrations/assets/a4adc-view-through-process.png)

*圖1:Adobe廣告檢視型 [!DNL Analytics] 整合*

![Adobe廣告點按URL型 [!DNL Analytics] 整合](/help/integrations/assets/a4adc-click-through-process.png)

*圖2:Adobe廣告點按URL型 [!DNL Analytics] 整合*

## Adobe廣告EF ID

EF ID是唯一代號，Adobe廣告會使用它來將活動與線上點按或廣告曝光建立關聯。 EF ID儲存在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar(保留eVar)維度(Adobe廣告EF ID)，並在個別瀏覽器或裝置層級追蹤每個廣告點按或曝光次數。 EF ID主要作為傳送金鑰 [!DNL Analytics] 資料Adobe廣告，以便在Adobe廣告內報告和出價最佳化。

### EF ID格式

>[!NOTE]
>
>EF ID區分大小寫。 若 [!DNL Analytics] 實作會強制URL追蹤變為小寫，則Adobe廣告將無法辨識EF ID。 這將影響Adobe廣告競標和報告，但不會影響內的Adobe廣告報告 [!DNL Analytics].

#### [!DNL Google Ads] 搜尋廣告

```{gclid}:G:s```

其中：

* `gclid` 是 [!DNL Google Click ID] (GCLID)。
* `s` 是網路類型（「s」用於搜尋）。

#### Microsoft Advertising搜尋廣告

```{msclkid}:G:s```

其中：

* `msclkid` 是 [!DNL Microsoft Click ID] (MSCLKID)。
* `s` 是網路類型（「s」用於搜尋）。

#### 在其他搜尋引擎上顯示廣告和搜尋廣告

```<Adobe Advertising visitor ID>:<timestamp>:<channel type>```

其中：

* &lt;*AdobeAdvertising訪客ID*>是每位訪客的唯一ID（例如UhKVaAABCkJ0mDt）。 也稱為 *瀏覽者ID*.

* &lt;*timestamp*>是格式為YYYYMMDDHHMMSS的時間(例如2019年20190821192533，月08，第21天，時間19:25:33)。

* &lt;*通道類型*>是負責點按或曝光的管道類型：

   * `d` （顯示點進）
   * `i` （顯示檢視）以顯示DSP顯示廣告的曝光次數
   * `s` ，以按一下搜尋廣告（搜尋點進）。

範例 `EF `ID:WcmibgAAAHJK1RyY:1551968087687:d

### 中的EF IDDimension [!DNL Analytics]

在 [!DNL Analytics] 報表，您可以搜尋 [!UICONTROL EF ID] 維度和使用 [!UICONTROL EF ID Instance] 量度。

EF ID在Analysis Workspace中有50萬個唯一識別碼限制。 達到50萬個值後，所有新的追蹤代碼都會報告在單行項目標題「[!UICONTROL Low Traffic].&quot; 由於報表保真度可能會遺失，因此系統不會分類EF ID，且您不應將EF ID用於區段或 [!DNL Analytics].

## Adobe廣告AMO ID

AMO ID會在較不精細的層級追蹤每個唯一廣告組合，並用於 [!DNL Analytics] 從Adobe廣告擷取廣告量度（例如曝光數、點按次數和成本）的資料分類。 AMO ID儲存在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar維度(AMO ID)，且僅用於 [!DNL Analytics].

AMO ID也稱為 `s_kwcid`，有時會朗讀為「[!DNL the squid].&quot;

### 適用於的AMO ID格式 [!DNL DSP]

```<Channel ID>!<Ad ID>!<Placement ID>```

其中：

* &lt;*管道ID*>可能是：

   * `AC` = Advertising DSP
   * `AL` for [!DNL Advertising Search]

* &lt;*廣告ID*>是Adobe廣告產生的廣告唯一識別碼。 它可做為將Adobe廣告實體中繼資料轉譯為可讀的索引鍵 [!DNL Analytics] 維度。

* &lt;*版位ID*>是Adobe廣告產生的版位唯一識別碼。 它可做為將Adobe廣告實體中繼資料轉譯為可讀的索引鍵 [!DNL Analytics] 維度。

範例AMO ID:AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### 適用於的AMO ID格式 [!DNL Search]

適用於 [!DNL Search] 對每個搜尋引擎遵循不同格式。 所有搜尋引擎的格式開頭為：

```AL!{userid}!{sid}```

其中：

* `AL` 是廣告網路的頻道ID。
* `{userid}` 是Adobe廣告指派給廣告商的唯一數值使用者ID。
* `{sid}` 是Adobe廣告用於指定廣告網路的數值ID，例如 `3` for [!DNL Google Ads] 或 `10` for [!DNL Microsoft Advertising].

以下為幾個廣告網路的完整AMO ID格式。 如需其他廣告網路的AMO ID格式，請連絡您的 [!DNL Adobe] 客戶團隊。

適用於的AMO ID格式 [!DNL Google Ads]:

```AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

其中：

* `{creative}` 是 [!DNL Google Ads] 創意素材的唯一數值ID。
* `{matchtype}` 是觸發廣告之關鍵字的符合類型： `e` 確切地說， `p` 對於短語，或 `b` 廣大的。
* `{placement}` 是點按廣告的網站的網域名稱。 位置定位促銷活動中的廣告，以及內容網站上顯示之關鍵字定位促銷活動中的廣告，都可使用值。
* `{network}` 指示發生點擊的網路：  `g` for [!DNL Google] 搜尋（僅限關鍵字定位廣告）, `s` 搜尋合作夥伴（僅限關鍵字定位廣告），或 `d` 顯示網路（針對關鍵字定位或位置定位廣告）。
* `{keyword}` 是觸發廣告的特定關鍵字（在搜尋網站上），或最符合的關鍵字（在內容網站上）。

適用於的AMO ID格式 [!DNL Microsoft Advertising]:

```AL!{userid}!{sid}!{AdId}!{OrderItemId}```

其中：

* `{AdId}` 是 [!DNL Microsoft Advertising] 創意素材的唯一數值ID。
* `{OrderItemId}` 是 [!DNL Microsoft Advertising] 關鍵字的數值ID。

### AMO IDDimension於 [!DNL Analytics]

在Analytics報表中，您可以搜尋 [!UICONTROL AMO ID] 維度和使用 [!UICONTROL AMO ID Instance] 量度。 此 [!UICONTROL AMO ID] 維度會儲存所有擷取的AMO ID值，而 [!UICONTROL AMO ID Instance] 量度會指出網站擷取AMO ID值的頻率。 例如，如果同一個搜尋廣告被點按了4次，但Analytics追蹤了7個網站項目，則 [!UICONTROL AMO ID Instance] 會是七(7) [!UICONTROL Clicks] 會是四(4)。

針對內的任何報告或審核 [!DNL Analytics]，最佳實務是使用AMO ID及其對應的例項。 如需詳細資訊，請參閱[資料驗證 [!DNL Analytics for Advertising]](data-variances.md#data-validation)」中， [!DNL Analytics] 和Adobe廣告。」

## 關於Analytics分類

在 [!DNL Analytics], [分類](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) 是指定追蹤代碼（例如帳戶、促銷活動或廣告）的中繼資料。 Adobe廣告使用分類來分類原始Adobe廣告資料，以便您在產生報表時能以不同方式（例如依廣告類型或促銷活動）顯示資料。 分類構成Adobe廣告報告的基礎，於 [!DNL Analytics] 和可與AMO量度搭配使用，例如 [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions]，和 [!UICONTROL AMO Clicks]，以及自訂和標準網站上事件(例如 [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders]，和 [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising]](overview.md)
>* [之間的預期資料差異 [!DNL Analytics] 和Adobe廣告](data-variances.md)

