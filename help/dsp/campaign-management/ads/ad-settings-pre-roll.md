---
title: 預滾動廣告設定
description: 請參閱預卷廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: 638d5a3d-3dff-40b6-a3ba-7ab3f08282b9
source-git-commit: bcece4bfec6f8a765cced3ee230fd8cbf3055b7b
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 0%

---

# 預滾動廣告設定

## [!UICONTROL Insert Ad Tag]

*僅新廣告*

**[!UICONTROL URL]:** VAST標籤URL。

**[!UICONTROL Title]:** 檔案的標題，位於 [!UICONTROL Ads] 查看和報告。

>[!TIP]
>
> 要檢查VAST標籤的有效性，請將其貼上到瀏覽器中，然後點擊 **[!UICONTROL Enter]** 按鈕 如果標籤有效，您將看到包含 `<VAST>` 靠近頂端。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （只讀）您正在建立的廣告類型，它與廣告可附加到的放置類型相對應。

**[!UICONTROL Ad Name]:** 廣告名。 預設情況下，資產標題會被使用，但您可以更改名稱。

>[!TIP]
>
> 使用將廣告附加到位置時容易找到的名稱， [!UICONTROL Ads] 視圖和報表中。 例如，描述設備類型和某些關鍵屬性(如「假日產品預覽」：30秒前滾」)。

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** （僅限標準和可滑動的預卷廣告）整個廣告單元的寬度。 此選項可能會根據您選擇的廣告單元類型鎖定。

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** （僅限標準和可滑動的預卷廣告）整個廣告單元的高度。 此選項可能會根據您選擇的廣告單元類型鎖定。

**[!UICONTROL Player X]:** 廣告單元的X坐標。 保留預設設定。

**[!UICONTROL Player Y]:** 廣告單位的Y坐標。 保留預設設定。

**[!UICONTROL Player Width]:** 整個廣告單元的寬度。 此選項可能會根據您選擇的廣告單元類型鎖定。

此欄位與 **[!UICONTROL Width]** 的子菜單。

**[!UICONTROL Player Height]:** 整個廣告單元的高度。 此選項可能會根據您選擇的廣告單元類型鎖定。

這和 **[!UICONTROL Height]** 的子菜單。

**[!UICONTROL Show Controls]:** 廣告的視頻控制項包括的位置： *[!UICONTROL Under]*。 *[!UICONTROL Over]*。 *[!UICONTROL Bottom]*&#x200B;或 *[!UICONTROL None]* （預設）。

**[!UICONTROL Preserve Aspect Ratio]:** 是否保留視頻的寬度和高度比例(*[!UICONTROL Yes]*)或拉伸視頻以填充可用空間(*[!UICONTROL No]*)。

**[!UICONTROL VAST Tag]:** (僅使用VAST標籤的廣告；只讀)作為廣告源輸入的第三方VAST標籤。

**[!UICONTROL Final VAST Tag]:** (僅使用VAST標籤的廣告；只讀)作為廣告源輸入的第三方VAST標籤 [Advertising Cloud DSP跟蹤宏](/help/dsp/campaign-management/macros.md) 插入（如果適用）。

**[!UICONTROL Wmode]:** （僅互動式預滾動）窗口模式： *[!UICONTROL window]*。 *[!UICONTROL transparent]*&#x200B;或 *[!UICONTROL opaque]*。

**[!UICONTROL Video Format]:** （僅互動式預滾動）潛在清單的廣告播放器的格式： *[!UICONTROL VPAID]* 或 *[!UICONTROL VPAID & VAST]*。 可視性始終為VPAID測量，但VPAID &amp; VAST包括不允許可視性測量的庫存。 如果可視性指標對您的市場活動很重要，請考慮這一區別。

**[!UICONTROL Clock Number]**:(僅互動式預卷；僅在英國使用；僅對具有權限的用戶可用)用於確保廣播正確廣告的唯一標識符。 如果此設定不適用，則將其留空。

### [!UICONTROL Pixel]

位置的所有現有事件跟蹤像素都會自動附加。 您可以根據對單個廣告的跟蹤需求分離現有像素並根據需要建立新像素。

以下設定適用於您建立或編輯的每個像素。

**[!UICONTROL Integration Event]:** 觸發像素觸發的事件。 對於此廣告類型，使用 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*。

**[!UICONTROL Pixel Type]:** 像素是否為 *[!UICONTROL IMG URL]* （1x1像素影像檔案）, *[!UICONTROL HTML]*&#x200B;或 *[!UICONTROL JavaScript URL]*。

**[!UICONTROL Pixel URL or Code]:** 像素影像的URL，格式與指定的 [!UICONTROL Pixel Type]。

**[!UICONTROL Pixel Name]:** 像素名稱。 使用有助於輕鬆識別像素的名稱。

**[!UICONTROL Pixel Provider]:** 像素提供器： *[!UICONTROL None]*。 *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*。

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立單個廣告](ad-create.md)
>* [列出與廣告關聯的放置](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [廣告規格](ad-specs.md)
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)

