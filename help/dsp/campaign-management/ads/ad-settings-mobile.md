---
title: 移動廣告設定
description: 請參閱移動廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: f67c4ba0-1011-4ad6-bd36-98c312b81b67
source-git-commit: bcece4bfec6f8a765cced3ee230fd8cbf3055b7b
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---

# Mobile廣告設定

## [!UICONTROL Insert Ad Tag]

*新移動視頻廣告格式*

**[!UICONTROL URL]** 或 **[!UICONTROL Ad Tag]**:包含創意資產和跟蹤像素的第三方VAST廣告標籤或廣告標籤

**[!UICONTROL Ad Title]** 或 **[!UICONTROL Title]**:中使用的廣告的名稱 [!UICONTROL Ads] 查看和報告。

>[!TIP]
>
> 要檢查VAST標籤的有效性，請將其貼上到瀏覽器中，然後點擊 **[!UICONTROL Enter]** 按鈕 如果標籤有效，您將看到包含 `<VAST>` 靠近頂端。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]:移動顯示廣告

**[!UICONTROL Ad Type]:** （只讀）您正在建立的廣告類型，它與廣告可附加到的放置類型相對應。

**[!UICONTROL Ad Name]:** 廣告名。 預設情況下，資產標題會被使用，但您可以更改名稱。

>[!TIP]
>
> 在將廣告附加到位置、「廣告」視圖和報告時，使用易於查找的名稱。 例如，描述設備類型和某些關鍵屬性(如「假日產品預覽」：300x250 Gamer」)。

**\[Ad源\]**:（只讀） *[!UICONTROL 3rd party]*。

**[!UICONTROL Display Code]:** 第三方創意資產的URL。 任意 [時間戳] 和[[時間戳]]參數將替換為實際值。

**[!UICONTROL Final Display Code]:** 第三方創意資產的URL，並且必要 [Advertising Cloud DSP跟蹤宏](/help/dsp/campaign-management/macros.md) 插入（如果適用）。

### [!UICONTROL Basic]:視頻廣告

**[!UICONTROL Ad Type]:** （只讀）您正在建立的廣告類型，它與廣告可附加到的放置類型相對應。

**[!UICONTROL Ad Name]:** 廣告名。 預設情況下，資產標題會被使用，但您可以更改名稱。

>[!TIP]
>
> 在將廣告附加到位置、「廣告」視圖和報告時，使用易於查找的名稱。 例如，描述設備類型和某些關鍵屬性(如「假日產品預覽」：30秒電話預轉」)。

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** 整個廣告單元的寬度。 此選項可能會根據您選擇的廣告單元類型鎖定。

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** 整個廣告單元的高度。 此選項可能會根據您選擇的廣告單元類型鎖定。

**[!UICONTROL Player X]:** 廣告單元的X坐標。 保留預設設定。

**[!UICONTROL Player Y]:** 廣告單位的Y坐標。 保留預設設定。

**[!UICONTROL Player Width]:** 整個廣告單元的寬度。 此選項可能會根據您選擇的廣告單元類型鎖定。

這和 **[!UICONTROL Width]** 的子菜單。

**[!UICONTROL Player Height]:** 整個廣告單元的高度。 此選項可能會根據您選擇的廣告單元類型鎖定。

這和 **[!UICONTROL Height]** 的子菜單。

**[!UICONTROL Show Controls]:** 廣告的視頻控制項包括的位置： *[!UICONTROL Under]*。 *[!UICONTROL Over]*。 *[!UICONTROL Bottom]*&#x200B;或 *[!UICONTROL None]* （預設）。

**[!UICONTROL Preserve Aspect Ratio]:** 是否保留視頻的寬度和高度比例(*[!UICONTROL Yes]*)或拉伸視頻以填充可用空間(*[!UICONTROL No]*)。

**[!UICONTROL Close Button Delay]:** （某些廣告類型）延遲關閉按鈕外觀的秒數。

**[!UICONTROL VAST Tag]:** (僅使用VAST標籤的廣告；只讀)作為創意資產輸入的第三方VAST標籤。

**[!UICONTROL Final VAST Tag]:** (僅使用VAST標籤的廣告；只讀)您作為創意資產輸入的第三方VAST標籤，並且 [Advertising Cloud DSP跟蹤宏](/help/dsp/campaign-management/macros.md) 插入（如果適用）。

**[!UICONTROL Wmode]:** （某些廣告類型）窗口模式： *[!UICONTROL window]*。 *[!UICONTROL transparent]*&#x200B;或 *[!UICONTROL opaque]*。

### [!UICONTROL Pixel]

位置的所有現有事件跟蹤像素都會自動附加。 您可以根據對單個廣告的跟蹤需求分離現有像素並根據需要建立新像素。

以下設定適用於您建立或編輯的每個像素。

**[!UICONTROL Integration Event]:** 觸發像素觸發的事件。 對於此廣告類型，使用 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*。

**[!UICONTROL Pixel Type]:** 像素是否為 *[!UICONTROL IMG URL]* （1x1像素影像檔案）, *[!UICONTROL HTML]*&#x200B;或 *[!UICONTROL JavaScript URL]*。

**[!UICONTROL Pixel URL or Code]:** 像素影像的URL，格式與指定的 [!UICONTROL Pixel Type]。

**[!UICONTROL Pixel Name]:** 像素名稱。 使用有助於輕鬆識別像素的名稱。

**[!UICONTROL Pixel Provider]:** 像素提供器： *[!UICONTROL None]*。 *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*。

### [!UICONTROL Sharing]

已棄用

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立單個廣告](ad-create.md)
>* [列出與廣告關聯的放置](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [廣告規格](ad-specs.md)
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)

