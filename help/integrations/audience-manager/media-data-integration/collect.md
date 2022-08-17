---
title: 收集Advertising Cloud DSP市場活動的點擊和印象資料
description: 瞭解如何使用Audience Manager像素從Advertising Cloud DSP廣告中捕獲基於cookie的印象並點擊事件
feature: Integration with Adobe Audience Manager
source-git-commit: b4dae983d390aaa5476951aa0c4c39648f07975c
workflow-type: tm+mt
source-wordcount: '1062'
ht-degree: 0%

---

# 從Advertising Cloud DSP活動收集媒體曝光資料

*僅包含Advertising Cloud DSP的廣告商*

*只有Advertising Cloud-Adobe Audience Manager整合的廣告商*

本文檔介紹如何為Advertising Cloud DSP廣告添加標籤以捕獲基於cookie的印象並使用Audience Manager像素按一下事件，以及使用資料所需的其他任務。

事件像素不會捕獲在無cookie環境（如移動應用和連接的電視）中發生的事件。

## 步驟1:在Audience Manager中設定資料源 {#set-up-data-source}

在Audience Manager中，建立 [資料源](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) ，然DSP後按一下資料。 包括資料源ID [在每個事件標籤中](#implement-dsp-pixels) 以便所有跟蹤事件都歸屬於資料源。

>[!NOTE]
> 可以收集所有印象並按一下資料，以便在單個資料源內的多個資料源上DSP運行廣告活動。

## 步驟2:在網頁上實現印象並按一下事件像素 {#implement-dsp-pixels}

廣告商可以為自己的品牌建立和實施事件標籤。 如有必要，請聯繫您的Adobe Audience Manager顧問或 [!DNL Adobe] 客戶經理。

>[!NOTE]
>
>如果您的組織使用 [!DNL Analytics] 跟蹤，則可能不需要Audience Manager按一下跟蹤。 Adobe Analytics捕獲點擊信號，並將其發送給Audience Manager [伺服器端轉發](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html)。

### 像素語法

事件像素必須包括以下參數。

**印象跟蹤像素：**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}` 與 [可選附加參數](#parameters) 前置詞 `&`

**按一下跟蹤像素：**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}` 與 [可選附加參數](#parameters) 前置詞 `&`

位置：

* `[Audience Manager customer domain]` 是要發送印象或按一下事件的域名 [!DNL Adobe]。

* `[source id]` 是 [資料源](#set-up-data-source) 在中，您將跟蹤DSP印象並按一下資料。

* `[redirect URL]` 是雙編碼重定向URL。 如果您使用線上編碼工具(如www.urlencoder.org)，則通過編碼器運行字串並重新編碼結果。

* `${TM_CAMPAIGN_ID_NUM}` 是中的數字市場活動IDDSP。 如果要硬編碼單個市場活動ID而不是使用宏DSP，請在市場活動設定中找到該ID。

* 每個 [參數](#key-value-pairs) 前置詞為 `&` 格式 `d_parameter=parameter_id`，也請參見Wiki頁。 `parameter` 替換為新欄位的key-value對。 示例： `&d_placement=${TM_PLACEMENT_ID_NUM}`

### 參數作為鍵值對 {#parameters}

**格式：**  `d_parameter=parameter_id`

    其中：
    
    *參數的前置詞為「&amp;」
    
    *新欄位的鍵值對替換為「parameter」
    
    示例：「&amp;d_placement=${TM_PLACEMENT_ID_NUM}」

這兩種類型的像素都可以包含附加參數，如 *鍵值對* 收集特徵或為其他報表提供市場活動元資料（如職位名稱或市場活動名稱）。 鍵值對由兩個相關元素組成：a *鍵*，是定義資料集的常數，以及 *值*，是屬於集的變數。

在鍵值對中，值變數可以是硬編碼ID或 *宏*&#x200B;它是一個自包含代碼的小單元，當廣告標籤載入用於市場活動和用戶跟蹤時，它被動態地替換為相應的值。 對於與市場活動相關的參數，您可以使用 [DSP宏](/help/dsp/campaign-management/macros.md) 而不是Audience Manager宏以將促銷活動屬性與相應印象一起發送，或者按一下資料以Audience Manager所有廣告中的單個像素。 插入DSP到事件像素中的宏必須是包含在像素中的鍵值對的適當值。 例如， `d_placement` 鍵，您使用宏DSP `${TM_PLACEMENT_ID_NUM}` 作為捕獲由Advertising Cloud宏生成的放置ID的值。

有關Audience Manager支援的印象事件像素的宏清單，請參閱[通過像素呼叫捕獲市場活動印象資料](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs)&quot;

有關Audience Manager支援按一下事件像素的宏清單，請參閱[通過像素呼叫捕獲市場活動按一下資料](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html)&quot;

>[!TIP]
>
>* 最佳做法是包括促銷活動、廣告投放、創意（廣告）和網站ID，以便您可以使用促銷活動屬性建立Audience Manager特徵。
>* 要建立Audience Optimization報告，需要其他參數。
>* 在鍵值對中，將值替換為 [DSP宏](/help/dsp/campaign-management/macros.md) 這樣，您就可以在所有市場活動中在所有廣告中使用單個像素。 例如，更改 `d_campaign=[%campaignID%]`至 `d_campaign=${TM_CAMPAIGN_ID_NUM}` 捕獲由Advertising Cloud宏生成的市場活動ID。
>* 如果需要，可以使用硬編碼值建立自己的參數。 示例： `d_DSP=AdCloud`


印象事件像素示例：

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### 添加像素的位置

#### 印象跟蹤像素

將印象事件跟蹤像素附加到您的所有廣告 [!DNL DSP] 活動。 您可以在以下任何位置執行此操作：

* 在放置級別，預設情況下，該級別將像素應用於放置中的所有廣告。 在放置設定的「跟蹤」部分中，將像素添加到 [[!UICONTROL Event pixels] 場](/help/dsp/campaign-management/placements/placement-settings.md)。

* 在廣告級別，它覆蓋任何放置級別的事件像素。 在廣告設定中， [在 [!UICONTROL Pixel] 頁籤](/help/dsp/campaign-management/ads/ad-edit.md)。

* （用於第三方廣告伺服器上的廣告）在廣告伺服器中的廣告級別。

#### 按一下跟蹤像素

在廣告伺服器中，無論您通常插入廣告的點擊式URL，都可插入點擊事件像素（附加編碼URL）。

## 第3步：實施後任務

一旦實現事件標籤，資料將流入Audience Manager資料收集伺服器。 在報告中使用資料之前，請完成以下任務。

### 建立 [!DNL Amazon S3] 儲存桶和資料源

資料在Audience Manager伺服器上後，必須建立 [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3])儲存桶，然後是資料源，所有像素資料都將發送到該資料源。 與Audience Manager顧問聯繫或 [客戶服務](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) 如果你需要支援。

### 建立Audience Manager特徵和段

您的事件資料將作為 [未用信號](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html)。 手動建立 [基於規則的特徵](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) 從攝取的資料中，然後建立 [段](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) 使用這些特徵，然後才能在報告中使用資料。

填充用戶級資料的示例特性，該用戶級資料暴露於特定創DSP作：

1. 將事件標識為 `d_event = imp`。
1. 確定活動中的創DSP意ID，然後將其與特徵映射為 `d_creative=[Creative ID]`。

![特徵建立螢幕](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)
>* [向Adobe Audience Manager發送DSP媒體曝光資料概述](overview.md)
>* [使用案例](use-cases.md)

