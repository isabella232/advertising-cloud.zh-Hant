---
title: Advertising Cloud [!DNL Analytics]使用的ID
description: Advertising Cloud [!DNL Analytics]使用的ID
feature: Integration with Adobe Analytics
exl-id: ed1aab7b-9bd0-4d42-9bfb-9c6fa6db76bc
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---

# Advertising Cloud [!DNL Analytics]使用的ID

*僅具有Advertising Cloud-Adobe Analytics整合的廣告商*

*適用於Advertising Cloud DSP和Advertising Cloud Search*

Advertising Cloud使用兩個ID進行站上效能追蹤： EF ID和AMO ID。

發生廣告曝光時，Advertising Cloud會建立AMO ID和EF ID值並加以儲存。 當看過廣告的訪客未點按廣告就進入網站時，[!DNL Analytics]會透過[!DNL Analytics for Advertising Cloud] JavaScript程式碼從Advertising Cloud呼叫這些值。 對於閱覽流量，[!DNL Analytics]會產生補充ID(`SDID`)，以便將EF ID和AMO ID匯整至[!DNL Analytics]。 對於點進流量，這些ID會使用`s_kwcid`和`ef_id`查詢字串參數包含在登陸頁面URL中。

Advertising Cloud使用下列條件來區分網站的點進或閱覽項目：

* 當使用者檢視廣告但未點按廣告後造訪網站時，會擷取閱覽項目。 [!DNL Analytics] 如果符合兩個條件，則記錄閱覽：
   * 在[點擊回顧期間，訪客沒有[!DNL DSP]或[!DNL Search]廣告的點進次數](#lookback-a4adc)。
   * 訪客在[曝光回顧期間](#lookback-a4adc)至少看到一個[!DNL DSP]廣告。 最後一次曝光會以閱覽傳遞。
* 當網站訪客進入網站前點按廣告時，會擷取點進項目。 [!DNL Analytics] 在下列任一情況發生時擷取點進：
   * 此URL包含EF ID和AMO ID，如Advertising Cloud所新增至登陸頁面URL。
   * URL不包含追蹤程式碼，但Advertising Cloud JavaScript程式碼會在過去兩分鐘內偵測到點按。

![Advertising Cloud檢視型整 [!DNL Analytics] 合](/help/integrations/assets/a4adc-view-through-process.png)

*圖1:Advertising Cloud檢視型整 [!DNL Analytics] 合*

![Advertising Cloud點按URL型整 [!DNL Analytics] 合](/help/integrations/assets/a4adc-click-through-process.png)

*圖2:Advertising Cloud點按URL型整 [!DNL Analytics] 合*

## Advertising Cloud EF ID

EF ID是唯一代號，Advertising Cloud用來將活動與線上點按或廣告曝光建立關聯。 EF ID儲存在[!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)或rVar(保留eVar)維度(Advertising Cloud EF ID)中，並在個別瀏覽器或裝置層級追蹤每個廣告點按或曝光次數。 EF ID主要作為傳送[!DNL Analytics]資料至Advertising Cloud，以便在Advertising Cloud內報告及最佳化出價的金鑰。

### EF ID格式

```<Advertising Cloud visitor ID>:<timestamp>:<channel type>```

<!-- <*Advertising Cloud visitor ID*>:<*timestamp*>:<*channel type*> -->

其中：

* &lt;>Advertising Cloud訪客ID *>是每位訪客的唯一ID（例如UhKVaAABCkJ0mDt）。*&#x200B;也稱為&#x200B;*瀏覽者ID*。

* &lt;>timestamp *>是格式為YYYYMMDDHMMSS的時間(例如2019年20190821192533、月08、第21天、時間19:25: 33)。*

* &lt;>管道類型&#x200B;*>是負責點按或曝光的管道類型：*

   * `d` （顯示點進）
   * `i` （顯示檢視）以顯示DSP顯示廣告的曝光次數
   * `s` ，以按一下搜尋廣告（搜尋點進）。

範例`EF `ID:WcmibgAAAHJK1RyY:1551968087687:d

>[!NOTE]
>
>EF ID區分大小寫。 如果[!DNL Analytics]實作強制URL追蹤為小寫，則Advertising Cloud將無法辨識EF ID。 這會影響Advertising Cloud的競標和報告，但對[!DNL Analytics]內的Advertising Cloud報告沒有影響。

### [!DNL Analytics]中的EF IDDimension

在[!DNL Analytics]報表中，您可以搜尋[!UICONTROL EF ID]維度並使用[!UICONTROL EF ID Instance]量度來尋找EF ID資料。

`EF IDs` 須受Analysis Workspace中50萬個唯一識別碼的限制。達到500k值後，所有新追蹤代碼都會在單行項目標題&quot;[!UICONTROL Low Traffic]&quot;下報告。 由於報表保真度可能會遺失，因此未分類`EF IDs`，且您不應將它們用於[!DNL Analytics]中的區段或報表。

## Advertising Cloud AMO ID

AMO ID可在較不精細的層級追蹤每個不重複廣告組合，並用於[!DNL Analytics]資料分類和從Advertising Cloud擷取廣告量度（例如曝光數、點按和成本）。 AMO ID會儲存在[!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)或rVar維度(AMO ID)中，並專用於[!DNL Analytics]中的報表。

AMO ID也稱為`s_kwcid`，有時稱為「squid」。

### [!DNL DSP]的AMO ID格式

```<Channel ID>!<Ad ID>!<Placement ID>```

其中：

* &lt;>管道ID *>可能是：*

   * `AC` = Advertising Cloud DSP
   * `AL` 針對Advertising Cloud Search

* &lt;>廣告ID *>是Advertising Cloud產生的廣告唯一識別碼。*&#x200B;這可做為將Advertising Cloud實體中繼資料轉譯為可讀[!DNL Analytics]維度的索引鍵。

* &lt;>版位ID *>是Advertising Cloud產生的版位唯一識別碼。*&#x200B;這可做為將Advertising Cloud實體中繼資料轉譯為可讀[!DNL Analytics]維度的索引鍵。

<!-- <*Channel ID*>!<*Ad ID*>!<*Placement ID*>

where:

* <*Channel ID*> may be:

    * `AC` = Advertising Cloud DSP
    * `AL` for Advertising Cloud Search

* <*Ad ID*> is used an Advertising Cloud-generated unique identifier for an ad. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.

* <*Placement ID*> is an Advertising Cloud-generated unique identifier for an placement. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.
 -->

範例AMO ID:AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### [!DNL Search]的AMO ID格式

[!DNL Search]的AMO ID會依照每個搜尋引擎的不同格式執行。 所有搜尋引擎的格式開頭為：

```AL!{ef_userid}!{ef_sid}```

其中：

* `AL` 是搜尋管道的管道ID。
* `{ef_userid}` 是Advertising Cloud指派給廣告商的不重複數值使用者ID。
* `{ef_sid}` 是Advertising Cloud用於指定搜尋引擎的數值ID，例如 `3` for [!DNL Google Ads] 或 `10` for [!DNL Microsoft Advertising]。

以下為數個搜尋引擎的完整AMO ID格式。 如需其他搜尋引擎的AMO ID格式，請連絡您的Adobe帳戶管理員。

[!DNL Google Ads]的AMO ID格式：

```AL!{ef_userid}!{ef_sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

其中：

* `{creative}` 是創 [!DNL Google Ads] 作的唯一數值ID。
* `{matchtype}` 是觸發廣告之關鍵字的符合類型： `e` 例如， `p` 片語或 `b` 廣泛。
* `{placement}` 是點按廣告的網站的網域名稱。位置定位促銷活動中的廣告，以及內容網站上顯示之關鍵字定位促銷活動中的廣告，都可使用值。
* `{network}` 指示發生點擊的網路：  `g` 搜 [!DNL Google] 尋（僅限關鍵字定位廣告）、 `s` 搜尋合作夥伴（僅限關鍵字定位廣告）或 `d` 顯示網路（針對關鍵字定位或位置定位廣告）。
* `{keyword}` 是觸發廣告的特定關鍵字（在搜尋網站上），或最符合的關鍵字（在內容網站上）。

[!DNL Microsoft Advertising]的AMO ID格式：

```AL!{ef_userid}!{ef_sid}!{AdId}!{OrderItemId}```

其中：

* `{AdId}` 是創 [!DNL Microsoft Advertising] 作的唯一數值ID。
* `{OrderItemId}` 是關 [!DNL Microsoft Advertising] 鍵字的數值ID。

### [!DNL Analytics]中的AMO IDDimension

在Analytics報表中，您可以搜尋[!UICONTROL AMO ID]維度並使用[!UICONTROL AMO ID Instance]量度來尋找AMO ID資料。 [!UICONTROL AMO ID]維度會儲存所有擷取的AMO ID值，而[!UICONTROL AMO ID Instance]量度則會指出網站擷取AMO ID值的頻率。 例如，如果同一個搜尋廣告被點按了四次，但Analytics追蹤了七個網站項目，則[!UICONTROL AMO ID Instance]會是七(7)，而[!UICONTROL Clicks]會是四(4)。

對於[!DNL Analytics]內的任何報表或稽核，最佳實務是使用AMO ID及其對應的例項。 如需詳細資訊，請參閱[!DNL Analytics]與Advertising Cloud之間預期資料差異中的「[ [!DNL Analytics for Advertising Cloud]](data-variances.md#data-validation)的資料驗證」。

## 關於Analytics分類

在[!DNL Analytics]中，[classification](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html)是指定追蹤代碼（如帳戶、促銷活動或廣告）的中繼資料片段。 Advertising Cloud使用分類來分類原始Advertising Cloud資料，以便您在產生報表時能以不同方式（例如依「廣告類型」或「促銷活動」）顯示資料。 分類是[!DNL Analytics]中Advertising Cloud報表的基礎，可與AMO量度（例如[!UICONTROL AMO Cost]、[!UICONTROL AMO Impressions]和[!UICONTROL AMO Clicks]）搭配使用，也可與自訂和標準站上事件（例如[!UICONTROL Visits]、[!UICONTROL Leads]、[!UICONTROL Orders]和[!UICONTROL Revenue]）搭配使用。

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [和之間的預期 [!DNL Analytics] 資料差異Advertising Cloud](data-variances.md)

