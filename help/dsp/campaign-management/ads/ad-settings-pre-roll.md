---
title: 前段廣告設定
description: 請參閱前段廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: 638d5a3d-3dff-40b6-a3ba-7ab3f08282b9
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 0%

---

# 前段廣告設定

## [!UICONTROL Insert Ad Tag]

*僅限新廣告*

**[!UICONTROL URL]:** VAST標籤URL。

**[!UICONTROL Title]:** 檔案的標題，位於 [!UICONTROL Ads] 檢視和報表。

>[!TIP]
>
> 若要檢查VAST標籤的有效性，請將其貼到瀏覽器中，然後點擊 **[!UICONTROL Enter]** 鍵。 如果標籤有效，您會看到包含 `<VAST>` 靠近頂端。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （唯讀）您要建立的廣告類型，與廣告可附加的版位類型相對應。

**[!UICONTROL Ad Name]:** 廣告名稱。 預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 在 [!UICONTROL Ads] 檢視和報表。 例如，說明裝置類型和某些關鍵屬性(例如「假日產品預覽」：30秒前段」)。

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** （僅限標準和可略過的前段廣告）整個廣告單位的寬度。 此選項可能會根據您選取的廣告單位類型而鎖定。

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** （僅限標準和可略過的前段廣告）整個廣告單位的高度。 此選項可能會根據您選取的廣告單位類型而鎖定。

**[!UICONTROL Player X]:** 廣告單位的X座標。 保留預設設定。

**[!UICONTROL Player Y]:** 廣告單位的Y座標。 保留預設設定。

**[!UICONTROL Player Width]:** 整個廣告單位的寬度。 此選項可能會根據您選取的廣告單位類型而鎖定。

此欄位與 **[!UICONTROL Width]** 欄位。

**[!UICONTROL Player Height]:** 整個廣告單位的高度。 此選項可能會根據您選取的廣告單位類型而鎖定。

這與 **[!UICONTROL Height]** 欄位。

**[!UICONTROL Show Controls]:** 廣告的視訊控制項的加入位置： *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*，或 *[!UICONTROL None]* （預設）。

**[!UICONTROL Preserve Aspect Ratio]:** 是否保留視訊的寬度和高度比例(*[!UICONTROL Yes]*)或拉伸視訊以填滿可用空間(*[!UICONTROL No]*)。

**[!UICONTROL VAST Tag]:** (僅使用VAST標籤的廣告；唯讀)您輸入做為廣告來源的第三方VAST標籤。

**[!UICONTROL Final VAST Tag]:** (僅使用VAST標籤的廣告；唯讀)您輸入做為廣告來源的第三方VAST標籤，且必須 [Advertising DSP追蹤巨集](/help/dsp/campaign-management/macros.md) 插入（如果適用）。

**[!UICONTROL Wmode]:** （僅限互動式前段）視窗模式： *[!UICONTROL window]*, *[!UICONTROL transparent]*，或 *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:** （僅限互動式前段）潛在詳細目錄的廣告播放器格式： *[!UICONTROL VPAID]* 或 *[!UICONTROL VPAID & VAST]*. 可視度一律會針對VPAID進行測量，但VPAID &amp; VAST包含不允許可視度測量的庫存。 如果可檢視性量度對您的促銷活動很重要，請考量此區別。

**[!UICONTROL Clock Number]**:(僅限互動式前段；僅用於英國；僅限具有權限的使用者使用)用來確保廣告廣播的唯一識別碼。 如果此設定不適用，請將其留空。

### [!UICONTROL Pixel]

版位的所有現有事件追蹤像素會自動附加。 您可以根據個別廣告的追蹤需求，分離現有像素並視需要建立新像素。

下列設定會套用至您建立或編輯的每個像素。

**[!UICONTROL Integration Event]:** 觸發像素的事件。 對於此廣告類型，請使用 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** 像素是否為 *[!UICONTROL IMG URL]* （1x1像素影像檔案）, *[!UICONTROL HTML]*，或 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** 像素影像的URL，為指定的 [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** 像素名稱。 使用可協助您輕鬆識別像素的名稱。

**[!UICONTROL Pixel Provider]:** 像素提供者： *[!UICONTROL None]*, *[!UICONTROL Nielsen]*，或 *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立單一廣告](ad-create.md)
>* [列出與廣告相關聯的版位](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [廣告規格](ad-specs.md)
>* [DSP巨集](/help/dsp/campaign-management/macros.md)

