---
title: 連接的電視廣告設定
description: 請參閱連接電視廣告的可用廣告設定說明。
feature: DSP Ads
exl-id: 4daae9e4-27eb-4496-9186-f33aebd8daae
source-git-commit: bcece4bfec6f8a765cced3ee230fd8cbf3055b7b
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# 連接的電視廣告設定

## [!UICONTROL Insert Ad Tag]

*僅新廣告*

**[!UICONTROL URL]**:VAST標籤URL。

**[!UICONTROL Title]**:檔案的名稱，將在「廣告」視圖和報告中使用。

>[!TIP]
>
> 要檢查VAST標籤的有效性，請將其貼上到瀏覽器中，然後點擊 **[!UICONTROL Enter]** 按鈕 如果標籤有效，您將看到包含 `<VAST>` 靠近頂端。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （只讀）您正在建立的廣告類型，它與廣告可附加到的放置類型相對應。

**[!UICONTROL Ad Name]:** 廣告名。 預設情況下，資產標題會被使用，但您可以更改名稱。

>[!TIP]
>
> 使用將廣告附加到位置時容易找到的名稱， [!UICONTROL Ads] 視圖和報表中。 例如，描述設備類型和某些關鍵屬性(如「假日產品預覽」：30秒CTV」)。

**[!UICONTROL Width | Ad Unit Width]:** 整個廣告單元的寬度。 此選項可能會根據您選擇的廣告單元類型鎖定。

**[!UICONTROL Height | Ad Unit Height]:** 整個廣告單元的高度。 此選項可能會根據您選擇的廣告單元類型鎖定。

**[!UICONTROL Player X]:** 廣告單元的X坐標。 保留預設設定。

**[!UICONTROL Player Y]:** 廣告單位的Y坐標。 保留預設設定。

**[!UICONTROL Player Width]:** 整個廣告單元的寬度。 此選項可能會根據您選擇的廣告單元類型鎖定。

這和 **[!UICONTROL Width]** 的子菜單。

**[!UICONTROL Player Height]:** 整個廣告單元的高度。 此選項可能會根據您選擇的廣告單元類型鎖定。

這和 **[!UICONTROL Height]** 的子菜單。

**[!UICONTROL Show Controls]:** 廣告的視頻控制項包括的位置： *[!UICONTROL Under]*。 *[!UICONTROL Over]*。 *[!UICONTROL Bottom]*&#x200B;或 *[!UICONTROL None]* （預設）。

**[!UICONTROL Preserve Aspect Ratio]:** 是否保留視頻的寬度和高度比例(*[!UICONTROL Yes]*)或拉伸視頻以填充可用空間(*[!UICONTROL No]*)。

**[!UICONTROL VAST Tag]:** (僅使用VAST標籤的廣告；只讀)作為廣告源輸入的第三方VAST標籤。

**[!UICONTROL Final VAST Tag]:** (僅使用VAST標籤的廣告；只讀)作為廣告源輸入的第三方VAST標籤 [Advertising Cloud DSP跟蹤宏](/help/dsp/campaign-management/macros.md) 插入（如果適用）。

**[!UICONTROL Clock Number]**:(僅在聯合王國使用；僅對具有權限的用戶可用)用於確保廣播正確廣告的唯一標識符。 如果此設定不適用，則將其留空。

### [!UICONTROL Pixel]

位置的所有現有事件跟蹤像素都會自動附加。 您可以根據對單個廣告的跟蹤需求分離現有像素並根據需要建立新像素。

以下設定適用於您建立或編輯的每個像素。

**[!UICONTROL Integration Event]:** 觸發像素觸發的事件。 對於此廣告類型，使用 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*。

**[!UICONTROL Pixel Type]:** 像素是否為 *[!UICONTROL IMG URL]* （1x1像素影像檔案）, *[!UICONTROL HTML]*&#x200B;或 *[!UICONTROL JavaScript URL]*。

**[!UICONTROL Pixel URL or Code]:** 像素影像的URL，格式與指定的「像素類型」相同。

**[!UICONTROL Pixel Name]:** 像素名稱。 使用有助於輕鬆識別像素的名稱。

**[!UICONTROL Pixel Provider]:** 像素提供器： *[!UICONTROL None]*。 *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*。

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立單個廣告](ad-create.md)
>* [列出與廣告關聯的放置](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [廣告規格](ad-specs.md)
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)

