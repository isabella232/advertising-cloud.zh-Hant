---
title: 行動廣告設定
description: 請參閱行動廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: f67c4ba0-1011-4ad6-bd36-98c312b81b67
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# 行動廣告設定

## [!UICONTROL Insert Ad Tag]

*僅限全新行動視訊廣告格式*

**[!UICONTROL URL]** 或 **[!UICONTROL Ad Tag]**:包含創意資產和追蹤像素的協力廠商VAST廣告標籤或廣告標籤

**[!UICONTROL Ad Title]** 或 **[!UICONTROL Title]**:廣告的名稱，用於 [!UICONTROL Ads] 檢視和報表。

>[!TIP]
>
> 若要檢查VAST標籤的有效性，請將其貼到瀏覽器中，然後點擊 **[!UICONTROL Enter]** 鍵。 如果標籤有效，您會看到包含 `<VAST>` 靠近頂端。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]:行動顯示廣告

**[!UICONTROL Ad Type]:** （唯讀）您要建立的廣告類型，與廣告可附加的版位類型相對應。

**[!UICONTROL Ad Name]:** 廣告名稱。 預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 在廣告檢視和報表中將廣告附加至版位時，請使用易於找到的名稱。 例如，說明裝置類型和某些關鍵屬性(例如「假日產品預覽」：300x250玩家」)。

**\[廣告來源\]**:（唯讀） *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** 協力廠商創意資產的URL。 任何 [timestamp] 和[[timestamp]]參數將替換為實際值。

**[!UICONTROL Final Display Code]:** 協力廠商創意資產的URL，必要 [Advertising DSP追蹤巨集](/help/dsp/campaign-management/macros.md) 插入（如果適用）。

### [!UICONTROL Basic]:視訊廣告

**[!UICONTROL Ad Type]:** （唯讀）您要建立的廣告類型，與廣告可附加的版位類型相對應。

**[!UICONTROL Ad Name]:** 廣告名稱。 預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 在廣告檢視和報表中將廣告附加至版位時，請使用易於找到的名稱。 例如，說明裝置類型和某些關鍵屬性(例如「假日產品預覽」：30秒Phone Preroll」)。

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** 整個廣告單位的寬度。 此選項可能會根據您選取的廣告單位類型而鎖定。

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** 整個廣告單位的高度。 此選項可能會根據您選取的廣告單位類型而鎖定。

**[!UICONTROL Player X]:** 廣告單位的X座標。 保留預設設定。

**[!UICONTROL Player Y]:** 廣告單位的Y座標。 保留預設設定。

**[!UICONTROL Player Width]:** 整個廣告單位的寬度。 此選項可能會根據您選取的廣告單位類型而鎖定。

這與 **[!UICONTROL Width]** 欄位。

**[!UICONTROL Player Height]:** 整個廣告單位的高度。 此選項可能會根據您選取的廣告單位類型而鎖定。

這與 **[!UICONTROL Height]** 欄位。

**[!UICONTROL Show Controls]:** 廣告的視訊控制項的加入位置： *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*，或 *[!UICONTROL None]* （預設）。

**[!UICONTROL Preserve Aspect Ratio]:** 是否保留視訊的寬度和高度比例(*[!UICONTROL Yes]*)或拉伸視訊以填滿可用空間(*[!UICONTROL No]*)。

**[!UICONTROL Close Button Delay]:** （某些廣告類型）延遲關閉按鈕外觀的秒數。

**[!UICONTROL VAST Tag]:** (僅使用VAST標籤的廣告；唯讀)您作為創意資產輸入的第三方VAST標籤。

**[!UICONTROL Final VAST Tag]:** (僅使用VAST標籤的廣告；唯讀)您輸入的協力廠商VAST標籤，是具有必要的創意資產 [Advertising DSP追蹤巨集](/help/dsp/campaign-management/macros.md) 插入（如果適用）。

**[!UICONTROL Wmode]:** （某些廣告類型）視窗模式： *[!UICONTROL window]*, *[!UICONTROL transparent]*，或 *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

版位的所有現有事件追蹤像素會自動附加。 您可以根據個別廣告的追蹤需求，分離現有像素並視需要建立新像素。

下列設定會套用至您建立或編輯的每個像素。

**[!UICONTROL Integration Event]:** 觸發像素的事件。 對於此廣告類型，請使用 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** 像素是否為 *[!UICONTROL IMG URL]* （1x1像素影像檔案）, *[!UICONTROL HTML]*，或 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** 像素影像的URL，為指定的 [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** 像素名稱。 使用可協助您輕鬆識別像素的名稱。

**[!UICONTROL Pixel Provider]:** 像素提供者： *[!UICONTROL None]*, *[!UICONTROL Nielsen]*，或 *[!UICONTROL Comscore]*.

### [!UICONTROL Sharing]

已棄用

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立單一廣告](ad-create.md)
>* [列出與廣告相關聯的版位](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [廣告規格](ad-specs.md)
>* [DSP巨集](/help/dsp/campaign-management/macros.md)

