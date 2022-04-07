---
title: 本機顯示廣告設定
description: 請參閱本機顯示廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: 3ae59e63-ae64-41b2-8734-3df2da020c7c
source-git-commit: 68af6b1846a37689dce0ca13a05cc1611b1f35a9
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# 本機顯示廣告設定

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （只讀）您正在建立的廣告類型，它與廣告可附加到的放置類型相對應。

**[!UICONTROL Ad Name]:** 廣告名。 預設情況下使用廣告類型，但可以更改名稱。

>[!TIP]
>
> 使用在將廣告附加到位置時易於查找的名稱， [!UICONTROL Ads] 視圖和報表中。 例如，描述設備類型和某些關鍵屬性(如「假日產品預覽」：15秒本機」)。

**[!UICONTROL Native Creative]:** 1200x627映像，可最大限度地提高移動庫存交付。 按一下 **[!UICONTROL Browse]** 並在設備或網路上找到檔案，然後按一下 **[!UICONTROL Upload]**。

**[!UICONTROL Title]:** 一個吸引觀眾眼球的標題。

**[!UICONTROL Description]:** 廣告的正文。 最大長度為100個字元。

**[!UICONTROL Landing Page]:** 查看者按一下廣告時登陸的URL。

**[!UICONTROL Final Landing Page]:** 的 [!UICONTROL Landing Page] 具有必要的URL [Advertising Cloud DSP跟蹤宏](/help/dsp/campaign-management/macros.md) 插入（如果適用）。

**[!UICONTROL Sponsored By (Advertiser Name)]:** 廣告的廣告商。

**[!UICONTROL Call to Action]:** （可選）查看者在看到此廣告後要執行的步驟。

**[!UICONTROL Advertiser Logo]:** （可選）1:1比率徽標，用於廣告，以獲得更多品牌認可。 按一下 **[!UICONTROL Browse]** 並在設備或網路上找到檔案，然後按一下 **[!UICONTROL Upload]**。

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
>* [廣告規格](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)

