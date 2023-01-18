---
title: 原生顯示廣告設定
description: 請參閱原生顯示廣告可用廣告設定的說明。
feature: DSP Ads
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# 原生顯示廣告設定

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （唯讀）您要建立的廣告類型，與廣告可附加的版位類型相對應。

**[!UICONTROL Ad Name]:** 廣告名稱。 預設會使用廣告類型，但您可以變更名稱。

>[!TIP]
>
> 在 [!UICONTROL Ads] 檢視和報表。 例如，說明裝置類型和某些關鍵屬性(例如「假日產品預覽」：15秒本機」)。

**[!UICONTROL Native Creative]:** 1200x627影像，可在行動裝置詳細目錄上將傳送作業最大化。 按一下 **[!UICONTROL Browse]** 並在您的裝置或網路上找到檔案，然後按一下 **[!UICONTROL Upload]**.

**[!UICONTROL Title]:** 吸引觀眾眼球的標題。

**[!UICONTROL Description]:** 廣告的正文。 長度上限為100個字元。

**[!UICONTROL Landing Page]:** 檢視器點按廣告時著陸的URL。

**[!UICONTROL Final Landing Page]:** 此 [!UICONTROL Landing Page] 具有必要的URL [Advertising DSP追蹤巨集](/help/dsp/campaign-management/macros.md) 插入（如果適用）。

**[!UICONTROL Sponsored By (Advertiser Name)]:** 廣告的廣告商。

**[!UICONTROL Call to Action]:** （選用）檢視者看到此廣告後，所要採取的步驟。

**[!UICONTROL Advertiser Logo]:** （選用）1:1比例的標誌，可加入廣告以獲得更多品牌認可。 按一下 **[!UICONTROL Browse]** 並在您的裝置或網路上找到檔案，然後按一下 **[!UICONTROL Upload]**.

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

