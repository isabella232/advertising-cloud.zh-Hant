---
title: 從Advertising Cloud DSP促銷活動收集點按和曝光資料
description: 了解如何使用Audience Manager像素，從Advertising Cloud DSP廣告擷取Cookie型曝光次數和點擊事件
feature: Integration with Adobe Audience Manager
exl-id: eb717148-00ab-428a-97b9-e8396a5c47b0
source-git-commit: 8de057df8bf2b67f20a915e6e711902f11176747
workflow-type: tm+mt
source-wordcount: '1062'
ht-degree: 0%

---

# 從Advertising Cloud DSP促銷活動收集媒體曝光資料

*僅包含Advertising Cloud DSP的廣告商*

*僅具有Advertising Cloud-Adobe Audience Manager整合的廣告商*

本檔案說明如何標籤Advertising Cloud DSP廣告，以使用Audience Manager像素擷取Cookie型曝光和點按事件，以及使用資料所需的其他工作。

事件像素不會擷取在無Cookie環境(例如行動應用程式和已連線電視(CTV))中發生的事件。

## 步驟1:在Audience Manager中設定資料來源 {#set-up-data-source}

在Audience Manager中，建立 [資料來源](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) 針對DSP曝光次數，然後按一下資料。 包含資料來源ID [每個事件標籤](#implement-dsp-pixels) 以便將所有追蹤的事件歸因於資料來源。

>[!NOTE]
> 您可以針對在單一資料來源中多個DSP上執行的廣告促銷活動，收集所有曝光次數和點按資料。

## 步驟2:在網頁上實作曝光數和點擊事件像素 {#implement-dsp-pixels}

廣告商可以建立並實作其自有品牌的事件標籤。 如有必要，請連絡您的Adobe Audience Manager顧問或您的 [!DNL Adobe] 客戶經理以尋求支援。

>[!NOTE]
>
>如果貴組織使用 [!DNL Analytics] 追蹤，則您可能不需要Audience Manager點擊追蹤。 Adobe Analytics會擷取點擊訊號，並可將其傳送至Audience Manager [伺服器端轉送](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

### 像素語法

事件像素必須包含下列參數。

**曝光追蹤像素：**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

with [其他可選參數](#parameters) 前置詞為 `&`

**點擊追蹤像素：**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

with [其他可選參數](#parameters) 前置詞為 `&`

其中：

* `[Audience Manager customer domain]` 是會將曝光或點按事件傳送至的網域名稱 [!DNL Adobe].

* `[source id]` 是 [資料來源](#set-up-data-source) 在其中追蹤DSP曝光次數並按一下資料。

* `[redirect URL]` 是雙重編碼的重新導向URL。 如果您使用線上編碼工具(例如www.urlencoder.org)，則通過編碼器運行字串並重新編碼結果。

* `${TM_CAMPAIGN_ID_NUM}` 是DSP中的數值促銷活動ID。 如果您想以硬式編碼撰寫個別促銷活動ID，而不是使用DSP巨集，請在促銷活動設定中找出該ID。

* 每個 [參數](#key-value-pairs) 前置詞為 `&` 和格式 `d_parameter=parameter_id`，其中 `parameter` 會由新欄位的鍵值組取代。 範例： `&d_placement=${TM_PLACEMENT_ID_NUM}`

### 作為索引鍵值配對的參數 {#parameters}

**格式：**  `d_parameter=parameter_id`

    其中：
    
    *參數的前置詞為「&amp;」
    
    *新欄位的鍵值值組會取代「parameter」
    
    範例：&#39;&amp;d_placement=${TM_PLACEMENT_ID_NUM}&#39;

這兩種像素都可包含其他參數，如 *索引鍵值配對* 收集特徵，或為其他報表提供行銷活動中繼資料（例如版位名稱或行銷活動名稱）。 機碼 — 值組包含兩個相關元素：a *key*，此為定義資料集的常數，以及 *value*，此為屬於集的變數。

在機碼值組中，值變數可以是硬式編碼ID或 *宏*，這是自包含的程式碼的一小部分，當廣告標籤載入以進行促銷活動和使用者追蹤時，會以對應的值動態取代。 對於促銷活動相關參數，您可以使用 [DSP巨集](/help/dsp/campaign-management/macros.md) 不使用Audience Manager巨集，而是使用所有廣告中的單一像素，將促銷活動屬性與對應的曝光次數或點按資料一起傳送至Audience Manager。 您插入事件像素中的DSP巨集必須是像素中包含的索引鍵值組的適當值。 例如，對於 `d_placement` 鍵，您會使用DSP巨集 `${TM_PLACEMENT_ID_NUM}` 作為擷取Advertising Cloud巨集產生之放置ID的值。

如需Audience Manager支援曝光事件像素的巨集清單，請參閱「[透過像素呼叫擷取促銷活動的曝光資料](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs).&quot;

如需Audience Manager支援點擊事件像素的宏清單，請參閱「[透過像素呼叫擷取促銷活動的點按資料](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html).&quot;

>[!TIP]
>
>* 最佳實務是納入促銷活動、版位、創意（廣告）和網站ID，讓您能使用促銷活動屬性來建立Audience Manager特徵。
>* 若要建立Audience Optimization報表，需要其他參數。
>* 在機碼值組中，將值取代為相關 [DSP巨集](/help/dsp/campaign-management/macros.md) 因此，您可以在所有行銷活動中使用所有廣告的單一像素。 例如，變更 `d_campaign=[%campaignID%]`to `d_campaign=${TM_CAMPAIGN_ID_NUM}` 擷取Advertising Cloud巨集產生的促銷活動ID。
>* 如有需要，您可以使用硬式編碼值建立自己的參數。 範例： `d_DSP=AdCloud`


曝光事件像素範例：

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### 像素的新增位置

#### 曝光追蹤像素

在您的 [!DNL DSP] 行銷活動。 您可以在下列任一位置執行此操作：

* 在放置層級，預設情況下，像素會套用至放置中的所有廣告。 在位置設定的「追蹤」區段中，將像素新增至 [[!UICONTROL Event pixels] 欄位](/help/dsp/campaign-management/placements/placement-settings.md).

* 在廣告層級，會覆寫任何版位層級的事件像素。 在廣告設定中， [在 [!UICONTROL Pixel] 標籤](/help/dsp/campaign-management/ads/ad-edit.md).

* （適用於第三方廣告伺服器上的廣告）在廣告伺服器內的廣告層級。

#### 點擊追蹤像素

在廣告伺服器內，只要您一般插入廣告的點進URL，請插入點按事件像素（並附加編碼URL）。

## 步驟3:實施後任務

實施事件標籤後，資料會流入Audience Manager資料收集伺服器。 請先完成下列工作，才能在報表中使用資料。

### 建立 [!DNL Amazon S3] 貯體和資料來源

在您的資料上Audience Manager伺服器後，您必須建立 [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3])貯體，然後是資料來源，所有像素資料都將傳送至該來源。 請聯絡您的Audience Manager顧問，或 [客戶服務](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) 需要支援。

### 建立Audience Manager特徵和區段

您的事件資料會以 [未使用的訊號](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html). 手動建立 [規則型特徵](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) 從擷取的資料，然後建立 [區段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) 使用這些特徵，您才能在報表中使用資料。

為在DSP中公開特定創意內容的使用者填入使用者層級資料的範例特徵：

1. 將事件識別為 `d_event = imp`.
1. 識別DSP促銷活動中的創作ID，然後將其對應至特徵，如下 `d_creative=[Creative ID]`.

![特徵建立畫面](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [Advertising Cloud DSP巨集](/help/dsp/campaign-management/macros.md)
>* [傳送DSP媒體曝光資料至Adobe Audience Manager概述](overview.md)
>* [使用案例](use-cases.md)

