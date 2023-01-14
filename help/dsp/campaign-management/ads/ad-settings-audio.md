---
title: 音訊廣告設定
description: 請參閱音訊廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# 音訊廣告設定

## [!UICONTROL Insert Ad Tag]

*僅限新廣告*

**[!UICONTROL URL]**:VAST標籤URL。

**[!UICONTROL Title]**:檔案的名稱，將用於 [!UICONTROL Ads] 檢視和報表。

>[!TIP]
>
> 若要檢查VAST標籤的有效性，請將其貼到瀏覽器中，然後點擊 **[!UICONTROL Enter]** 鍵。 如果標籤有效，您會看到包含 `<VAST>` 靠近頂端。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （唯讀）您要建立的廣告類型，與廣告可附加的版位類型相對應。 預設為 *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** 廣告名稱。 預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 在 [!UICONTROL Ads] 檢視和報表。 例如，說明裝置類型和某些關鍵屬性(例如「假日產品預覽」：30秒音頻」)。

**[!UICONTROL Ad Duration]:** 音訊檔案的長度。 會自動設定為 [!UICONTROL 15] 或 [!UICONTROL 30]，視選取的廣告單位而定。

視帳戶權限而定，此欄位可能會顯示，也可能不顯示。

**[!UICONTROL VAST Tag]:** （僅限使用VAST標籤的廣告）協力廠商廣告來源的URL。 請確定VAST標籤僅包含音訊媒體檔案。

**[!UICONTROL Final VAST Tag]:** （僅限使用VAST標籤的廣告）具有必要之協力廠商廣告來源的URL [Advertising DSP追蹤巨集](/help/dsp/campaign-management/macros.md) 插入（如果適用）。

**[!UICONTROL Select Rate]:** （僅具有權限的用戶）通過Adobe計費的預議費率，或您已協商的費率之一，並將通過供應商計費。 若要新增費率，請連絡您的 [!DNL Adobe] 客戶團隊。

### 像素

版位的所有現有事件追蹤像素會自動附加。 您可以根據個別廣告的追蹤需求，分離現有像素並視需要建立新像素。

下列設定會套用至您建立或編輯的每個像素。

**[!UICONTROL Integration Event]:** 觸發像素的事件。 對於此廣告類型，請使用 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** 像素是否為 *[!UICONTROL IMG UR]L* （1x1像素影像檔案）, *[!UICONTROL HTML]*，或 *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** 像素影像的URL，以指定像素類型的適當格式。

**[!UICONTROL Pixel Name]:** 像素名稱。 使用可協助您輕鬆識別像素的名稱。

**[!UICONTROL Pixel Provider]:** 像素提供者： *[!UICONTROL None]*, *[!UICONTROL Nielsen]*，或 *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立單一廣告](ad-create.md)
>* [列出與廣告相關聯的版位](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [廣告規格](ad-specs.md)
>* [DSP巨集](/help/dsp/campaign-management/macros.md)

