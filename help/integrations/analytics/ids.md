---
title: Advertising CloudID使用者 [!DNL Analytics]
description: Advertising CloudID使用者 [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ed1aab7b-9bd0-4d42-9bfb-9c6fa6db76bc
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---

# Advertising CloudID使用者 [!DNL Analytics]

*只有Advertising Cloud-Adobe Analytics整合的廣告商*

*適用於Advertising Cloud DSP和Advertising Cloud Search*

Advertising Cloud使用兩個ID進行現場效能跟蹤：這樣 *EF ID* 和 *AMO ID*。

當出現廣告印象時，Advertising Cloud會建立AMO ID和EF ID值並儲存它們。 看到廣告的訪客不點擊廣告就進入網站， [!DNL Analytics] 從Advertising Cloud到 [!DNL Analytics for Advertising Cloud] JavaScript代碼。 對於直通通信， [!DNL Analytics] 生成補充ID(`SDID`)，用於將EF ID和AMO ID縫合到 [!DNL Analytics]。 對於點擊式通信，這些ID將使用 `s_kwcid` 和 `ef_id` 查詢字串參數。

Advertising Cloud使用以下標準來區分網站的點擊或查看條目：

* 當用戶在查看廣告但不按一下廣告後訪問該站點時，將捕獲直覽項。 [!DNL Analytics] 如果滿足以下兩個條件，則記錄查看：
   * 訪問者沒有 [!DNL DSP] 或 [!DNL Search] 在 [按一下「回望」窗口](#lookback-a4adc)。
   * 訪客至少見過一次 [!DNL DSP] 在 [印象回望窗口](#lookback-a4adc)。 最後的印象作為透視傳遞。
* 當站點訪問者在進入站點之前按一下廣告時，將捕獲一個點擊式條目。 [!DNL Analytics] 在出現以下任一情況時捕獲按一下穿透：
   * 該URL包括由Advertising Cloud添加到登錄頁URL的EF ID和AMO ID。
   * 該URL不包含跟蹤代碼，但Advertising CloudJavaScript代碼在過去兩分鐘內檢測到按一下。

![Advertising Cloud視圖 [!DNL Analytics] 整合](/help/integrations/assets/a4adc-view-through-process.png)

*圖1:Advertising Cloud視圖 [!DNL Analytics] 整合*

![Advertising Cloud按一下基於URL [!DNL Analytics] 整合](/help/integrations/assets/a4adc-click-through-process.png)

*圖2:Advertising Cloud按一下基於URL [!DNL Analytics] 整合*

## Advertising CloudEF ID

EF ID是Advertising Cloud用於將活動與線上點擊或廣告暴露關聯的唯一令牌。 EF ID儲存在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar(保留eVar)維(Advertising CloudEF ID)，並在單個瀏覽器或設備級別跟蹤每個廣告點擊或曝光。 EF ID主要用作發送密鑰 [!DNL Analytics] 資料，以供Advertising CloudAdvertising Cloud內彙報及投標優化。

### EF ID格式

```<Advertising Cloud visitor ID>:<timestamp>:<channel type>```

<!-- <*Advertising Cloud visitor ID*>:<*timestamp*>:<*channel type*> -->

其中：

* &lt;*Advertising Cloud遊客ID*>是每個訪問者的唯一ID（如UhKVaAABCkJ0mDt）。 也稱為 *衝浪ID*。

* &lt;*時間戳*>是格式為YYYYMMDDHHMMSS的時間(例如2019082192533，適用於2019年，月08，第21天，時間19:25:33)。

* &lt;*通道類型*>是負責按一下或曝光的通道類型：

   * `d` 顯示廣告(DSP顯示按一下)
   * `i` 顯示廣告DSP的印象（顯示視圖）
   * `s` 的上界。

示例 `EF `ID:WcmibgAAAHJK1RyY:1551968087687:d

>[!NOTE]
>
>EF ID區分大小寫。 如果 [!DNL Analytics] 實現強制URL跟蹤為小寫，Advertising Cloud將無法識別EF ID。 這將影響Advertising Cloud的投標和報告，但對Advertising Cloud內的報告沒有影響 [!DNL Analytics]。

### 中的EF IDDimension [!DNL Analytics]

在 [!DNL Analytics] 報告，您可以通過搜索 [!UICONTROL EF ID] 維和使用 [!UICONTROL EF ID Instance] 度量。

EF ID受Analysis Workspace500k唯一標識符限制的限制。 達到500k值後，將在單行項標題&quot;下報告所有新跟蹤代碼[!UICONTROL Low Traffic]&quot; 由於可能丟失報告保真度，因此EF ID不會被分類，您不應將它們用於段或報告 [!DNL Analytics]。

## Advertising CloudAMO ID

AMO ID以較小粒度級別跟蹤每個唯一廣告組合，並用於 [!DNL Analytics] 對Advertising Cloud的廣告指標（如印象、點擊量和成本）進行資料分類和接收。 AMO ID儲存在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar維(AMO ID)，僅用於在中報告 [!DNL Analytics]。

AMO ID也稱為 `s_kwcid`，有時讀為&quot;[!DNL the squid]&quot;

### AMO ID格式 [!DNL DSP]

```<Channel ID>!<Ad ID>!<Placement ID>```

其中：

* &lt;*通道ID*>可能是：

   * `AC` =Advertising Cloud DSP
   * `AL` 為Advertising Cloud Search

* &lt;*廣告ID*>是廣告的Advertising Cloud生成的唯一標識符。 它是將Advertising Cloud實體元資料翻譯成可讀的關鍵 [!DNL Analytics] 尺寸。

* &lt;*放置ID*>是位置的Advertising Cloud生成的唯一標識符。 它是將Advertising Cloud實體元資料翻譯成可讀的關鍵 [!DNL Analytics] 尺寸。

<!-- <*Channel ID*>!<*Ad ID*>!<*Placement ID*>

where:

* <*Channel ID*> may be:

    * `AC` = Advertising Cloud DSP
    * `AL` for Advertising Cloud Search

* <*Ad ID*> is used an Advertising Cloud-generated unique identifier for an ad. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.

* <*Placement ID*> is an Advertising Cloud-generated unique identifier for an placement. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.
 -->

示例AMO ID:AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### AMO ID格式 [!DNL Search]

的AMO ID [!DNL Search] 對每個搜索引擎執行不同的格式。 所有搜索引擎的格式以下列內容開頭：

```AL!{ef_userid}!{ef_sid}```

其中：

* `AL` 是搜索頻道的頻道ID。
* `{ef_userid}` 是Advertising Cloud分配給廣告商的唯一數字用戶ID。
* `{ef_sid}` 是Advertising Cloud用於指定搜索引擎的數字ID，如 `3` 為 [!DNL Google Ads] 或 `10` 為 [!DNL Microsoft Advertising]。

以下是幾個搜索引擎的完整AMO ID格式。 有關其他搜索引擎的AMO ID格式，請與 [!DNL Adobe] 客戶團隊。

AMO ID格式 [!DNL Google Ads]:

```AL!{ef_userid}!{ef_sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

其中：

* `{creative}` 是 [!DNL Google Ads] 創作的唯一數字ID。
* `{matchtype}` 是觸發廣告的關鍵字的匹配類型： `e` 準確地說， `p` 片語或 `b` 為廣大人。
* `{placement}` 是按一下廣告的網站的域名。 值可用於定位市場活動中的廣告和顯示在內容站點上的關鍵字定位市場活動中的廣告。
* `{network}` 指示出現按一下的網路：  `g` 為 [!DNL Google] 搜索（僅針對關鍵字廣告）, `s` 搜索合作夥伴（僅針對關鍵字定向廣告），或 `d` 顯示網路（針對關鍵字或定位廣告）。
* `{keyword}` 是觸發廣告的特定關鍵字（在搜索站點上）或最佳匹配關鍵字（在內容站點上）。

AMO ID格式 [!DNL Microsoft Advertising]:

```AL!{ef_userid}!{ef_sid}!{AdId}!{OrderItemId}```

其中：

* `{AdId}` 是 [!DNL Microsoft Advertising] 創作的唯一數字ID。
* `{OrderItemId}` 是 [!DNL Microsoft Advertising] 關鍵字的數字ID。

### AMO IDDimension [!DNL Analytics]

在分析報告中，可通過搜索 [!UICONTROL AMO ID] 維和使用 [!UICONTROL AMO ID Instance] 度量。 的 [!UICONTROL AMO ID] 維包含捕獲的所有AMO ID值，而 [!UICONTROL AMO ID Instance] metric指示站點捕獲AMO ID值的頻率。 例如，如果按一下了4次同一搜索廣告，但Analytics跟蹤了7個網站條目，則 [!UICONTROL AMO ID Instance] 將是七(7) [!UICONTROL Clicks] 將是四(4)。

對於 [!DNL Analytics]最佳做法是使用AMO ID及其相應實例。 有關詳細資訊，請參閱「」[資料驗證 [!DNL Analytics for Advertising Cloud]](data-variances.md#data-validation)」中 [!DNL Analytics] 和Advertising Cloud。」

## 關於分析分類

在 [!DNL Analytics]的 [分類](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) 是給定跟蹤代碼（如帳戶、市場活動或廣告）的元資料。 Advertising Cloud使用分類對原始Advertising Cloud資料進行分類，以便您在生成報表時可以以不同方式（如按廣告類型或市場活動）顯示資料。 分類構成Advertising Cloud報告的基礎 [!DNL Analytics] 可與AMO度量一起使用，如 [!UICONTROL AMO Cost]。 [!UICONTROL AMO Impressions], [!UICONTROL AMO Clicks]以及定制和標準現場活動(如 [!UICONTROL Visits]。 [!UICONTROL Leads]。 [!UICONTROL Orders], [!UICONTROL Revenue]。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [預期資料差異 [!DNL Analytics] 和Advertising Cloud](data-variances.md)

