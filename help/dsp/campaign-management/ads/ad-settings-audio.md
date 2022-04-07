---
title: 音頻廣告設定
description: 請參閱音頻廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: 68af6b1846a37689dce0ca13a05cc1611b1f35a9
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# 音頻廣告設定

## [!UICONTROL Insert Ad Tag]

*僅新廣告*

**[!UICONTROL URL]**:VAST標籤URL。

**[!UICONTROL Title]**:檔案的名稱，將在 [!UICONTROL Ads] 查看和報告。

>[!TIP]
>
> 要檢查VAST標籤的有效性，請將其貼上到瀏覽器中，然後點擊 **[!UICONTROL Enter]** 按鈕 如果標籤有效，您將看到包含 `<VAST>` 靠近頂端。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （只讀）您正在建立的廣告類型，它與廣告可附加到的放置類型相對應。 預設為 *[!UICONTROL Audio]*。

**[!UICONTROL Ad Name]:** 廣告名。 預設情況下，資產標題會被使用，但您可以更改名稱。

>[!TIP]
>
> 使用將廣告附加到位置時容易找到的名稱， [!UICONTROL Ads] 視圖和報表中。 例如，描述設備類型和某些關鍵屬性(如「假日產品預覽」：30秒音頻」)。

**[!UICONTROL Ad Duration]:** 音頻檔案的長度。 自動設定為 [!UICONTROL 15] 或 [!UICONTROL 30]，具體取決於所選廣告單位。

根據帳戶權限，可能顯示或不顯示此欄位。

**[!UICONTROL VAST Tag]:** （僅使用VAST標籤的廣告）第三方廣告源的URL。 確保VAST標籤只包含音頻媒體檔案。

**[!UICONTROL Final VAST Tag]:** （僅使用VAST標籤的廣告）具有必要條件的第三方廣告源的URL [Advertising Cloud DSP跟蹤宏](/help/dsp/campaign-management/macros.md) 插入（如果適用）。

**[!UICONTROL Select Rate]:** （僅具有權限的用戶）通過Adobe計費的預協商費率，或您已協商並將通過供應商計費的費率之一。 要添加費率，請與 [!DNL Adobe] 客戶團隊。

### 像素

位置的所有現有事件跟蹤像素都會自動附加。 您可以根據對單個廣告的跟蹤需求分離現有像素並根據需要建立新像素。

以下設定適用於您建立或編輯的每個像素。

**[!UICONTROL Integration Event]:** 觸發像素觸發的事件。 對於此廣告類型，使用 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*。

**[!UICONTROL Pixel Type]:** 像素是否為 *[!UICONTROL IMG UR]L* （1x1像素影像檔案）, *[!UICONTROL HTML]*&#x200B;或 *[!UICONTROL JavaScript URL]*。

**[!UICONTROL Pixel URL or Code]:** 像素影像的URL，格式與指定的「像素類型」相同。

**[!UICONTROL Pixel Name]:** 像素名稱。 使用有助於輕鬆識別像素的名稱。

**[!UICONTROL Pixel Provider]:** 像素提供器： *[!UICONTROL None]*。 *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*。

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立單個廣告](ad-create.md)
>* [列出與廣告關聯的放置](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [廣告規格](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)

