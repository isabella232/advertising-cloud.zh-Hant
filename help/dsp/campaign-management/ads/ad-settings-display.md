---
title: 顯示廣告設定
description: 請參閱顯示廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: bcece4bfec6f8a765cced3ee230fd8cbf3055b7b
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---

# 顯示廣告設定

以下設定用於標準顯示廣告。

## [!UICONTROL Ad Options]

### 基本

**[!UICONTROL Ad Type]:** （只讀）您正在建立的廣告類型，它與廣告可附加到的放置類型相對應。 預設為 *[!UICONTROL Display]*。

**[!UICONTROL Ad Name]:** 廣告名。 預設情況下，資產標題會被使用，但您可以更改名稱。

>[!TIP]
>
> 使用將廣告附加到位置時容易找到的名稱， [!UICONTROL Ads] 視圖和報表中。 例如，描述設備類型和某些關鍵屬性(如「假日產品預覽」：300x250 Gamer」)。

**\[Ad源\]**:（只讀） *[!UICONTROL 3rd party]*。

**[!UICONTROL This is an expandable Banner]:** （僅限第三方廣告）表示廣告是可擴展的橫幅廣告。 相關擴展設定確定要購買的庫存，因此確保它們反映廣告行為。

**[!UICONTROL Expansion Method]:** （僅限第三方可擴展的橫幅廣告） *[!UICONTROL Click]* 或 *[!UICONTROL Rollover]*。

**[!UICONTROL Expansion Directions]:** （僅限第三方可擴展的橫幅廣告）廣告擴展的方向： *[!UICONTROL Up]*。 *[!UICONTROL Down]*。 *[!UICONTROL Left]*&#x200B;或 *[!UICONTROL Right]*。

**[!UICONTROL Certified Vendors]:** （僅限第三方可擴展橫幅廣告）廣告可用的認證供應商： *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]) *[!UICONTROL Flashtalking]*。 *[!UICONTROL Sizmek]*&#x200B;或 *[!UICONTROL Jivox]*。

**[!UICONTROL Display Code]:** （僅限第三方廣告）第三方創意資產的URL。 任意 [時間戳] 和[[時間戳]]參數將替換為實際值。

**[!UICONTROL Final Display Code]:** （僅限第三方廣告）第三方創意資產的URL，並且 [Advertising Cloud DSP跟蹤宏](/help/dsp/campaign-management/macros.md) 插入（如果適用）。

**[!UICONTROL Ad Size]:** 廣告的寬度和高度。 一定是 [支援的標準顯示和大小](ad-specs.md)。 您可以在上載廣告或輸入廣告之前手動輸入廣告大小 [!UICONTROL Display Code]。 如果未輸入廣告大小，則上載的廣告或廣告標籤的尺寸將自動以只讀方式輸入。 請注意，如果尺寸不在「標準顯示」中，則「顯示」廣告不會保存為大小 — 例如301x250而不是300x250廣告大小。

>[!IMPORTANT]
>
> 在寬度和高度欄位中聲明的廣告大小將與傳入的投標請求匹配。 如果廣告的尺寸與聲明的廣告尺寸不匹配，您可能會遇到交付問題。

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
>* [列出與廣告關聯的放置](ad-list-placements.md)
>* [廣告規格](ad-specs.md)
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)

