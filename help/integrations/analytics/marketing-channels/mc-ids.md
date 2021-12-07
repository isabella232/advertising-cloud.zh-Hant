---
title: 使用Advertising Cloud ID建立 [!DNL Marketing Channels] 規則
description: 了解如何使用Advertising Cloud ID建立 [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
source-git-commit: 1ae45d0ceee2efc4fc52b86fd6737d4c7467a6ca
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# 使用Advertising Cloud ID建立 [!DNL Marketing Channels] 處理規則

*僅具有Advertising Cloud-Adobe Analytics整合的廣告商*

您可以使用Advertising Cloud ID([AMO ID和EF ID](../ids.md))若要設定 [!DNL Marketing Channels] 處理規則。 使用Advertising Cloud ID作為Advertising Cloud促銷活動的特定規則。

## 處理規則中的AMO ID

AMO ID是主要追蹤代碼，用於報告內的Advertising Cloud資料 [!DNL Analytics]. AMO ID是由Adobe管理的動態值串連，以在內提供精細的報表 [!DNL Analytics]. 它儲存在 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 或rVar維度(AMO ID)。 AMO ID可在 [!DNL Analytics] 有兩種方式：

* 點進追蹤：Advertising Cloud設定 `s_kwcid` 連結中的查詢字串參數，以及 [!DNL Analytics] 點進發生時，會從登陸頁面URL中取用參數。
* 閱覽追蹤([!DNL DSP] 僅限):上次事件服務會偵測伺服器端的閱覽，並將AMO ID傳送至 [!DNL Analytics]. 在此情況下，URL不包含 `s_kwcid` 參數。

AMO ID內的動態值會指出已追蹤的行銷管道：

* AMO ID中的首碼可用來識別 [!DNL Marketing Channels].

* AMO ID內文中的字元片語代表更具體的促銷活動類型。

* 的尾碼為「vt」 [!DNL DSP] 閱覽流量，可用來建立個別的點進和閱覽 [!DNL DSP] 管道。

其餘的AMO ID則可以忽略。

| AMO ID | 管道 | 規則邏輯 |
|--------|---------|--------------------|
| 艾爾！ （前置詞） | [!UICONTROL Paid Search] | 開頭為 |
| AC （前置詞） | [!UICONTROL DSP] | 開頭為 |
| !g! （正文） | [!UICONTROL Google Search] | 包含 |
| !s! （正文） | [!UICONTROL Search Partner] | 包含 |
| !d! （正文） | [!UICONTROL Display Network] | 包含 |
| !u! （正文） | [!UICONTROL Smart Shopping Campaign] | 包含 |
| !ytv! （正文） | [!UICONTROL YouTube Video Ad] | 包含 |
| !yts! （正文） | [!UICONTROL YouTube Search Ad] | 包含 |
| !vp! （正文） | [!UICONTROL Google Video Partners] | 包含 |
| !vt（尾碼） | [!UICONTROL DSP View-through] | 結尾為 |

### 使用AMO ID的處理規則範例

此 [!DNL Marketing Channels] 的處理規則 [!UICONTROL Paid Search] 管道可能如下所示：

![範例 [!UICONTROL Paid Search] 規則](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

此 [!DNL Marketing Channels] 的處理規則 [!UICONTROL YouTube Video Ads] 管道可能如下所示：

![範例 [!UICONTROL YouTube Video Ads] 規則](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> 請務必依特定順序執行規則。 如果上述兩個規則依序執行， [!DNL YouTube] 視訊廣告流量將全部計入 [!UICONTROL Paid Search] 管道，因為AMO ID都會以「AL！」開頭 並包含「！ytv！」。

## 處理規則中的EF ID

AMO EF ID(EF ID)是 [!DNL Analytics for Advertising Cloud] 整合。 其主要用途是追蹤及通過 [!DNL Analytics] 事件資料匯入Advertising Cloud。 每次點進或閱覽發生時，都會產生唯一的EF ID，即使這是相同訪客的相同廣告亦然。 EF ID不會用於 [!DNL Analytics] 報告使用者介面，因為該介面通常超過 [!DNL Analytics]，導致無法用於報告。 Advertising Cloud量度和中繼資料不會套用至EF ID;它們只會套用至AMO ID。 在Advertising Cloud中，促銷活動最佳化需要新增的追蹤粒度，因此需要兩個ID。

雖然EF ID維度未直接用於 [!DNL Analytics] 報告時，EF ID在建立行銷管道時相當實用。 EF ID尾碼會指出管道（顯示或搜尋），以及造訪是由點進或閱覽所驅動。 EF ID中的分隔字元是冒號，而非AMO ID中的感嘆號。

| EF ID尾碼 | 管道 |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### 使用EF ID的處理規則範例

#### 顯示點進規則

僅擷取點進次數，以建立顯示點進行銷管道。 由於點進和閱覽的AMO ID都相同，因此此規則會使用EF ID變數，並 `ef_id` 查詢字串參數。

有時點進會透過URL（預設）追蹤。 在其他情況下，點進會透過伺服器端的最後一個事件服務來追蹤，因此URL不會包含 `ef_id` 參數。 因此，規則會檢查EF ID變數或 `ef_id` 查詢字串參數的結尾為「：d」。 使用「`Any`」運算子，因為您想要針對任一條件觸發此規則。

![顯示點進規則的範例](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### 顯示閱覽規則

若要建立「顯示」檢視管道，請建立EF ID結尾為「：i」的規則。 由於訪客未點按廣告，因此閱覽追蹤不包含 `ef_id` 或 `s_kwcid` 中。 因此，只需要一個條件。

![顯示檢視規則的範例](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [基礎 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [為何管道資料可能因Advertising Cloud和 [!DNL Marketing Channels]](mc-data-variances.md)
>* [使用 [!DNL Analytics Marketing Channels] 使用Advertising Cloud資料](mc-ac-data.md)
>* [影片：使用Advertising Cloud製作報表 [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Advertising Cloud使用的ID [!DNL Analytics]](/help/integrations/analytics/ids.md)

