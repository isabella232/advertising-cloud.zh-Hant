---
title: 顯示廣告設定
description: 請參閱顯示廣告可用廣告設定的說明。
feature: DSP Ads
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# 顯示廣告設定

以下是標準顯示廣告的設定。

## [!UICONTROL Ad Options]

### 基本

**[!UICONTROL Ad Type]:** （唯讀）您要建立的廣告類型，與廣告可附加的版位類型相對應。 預設為 *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** 廣告名稱。 預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 在 [!UICONTROL Ads] 檢視和報表。 例如，說明裝置類型和某些關鍵屬性(例如「假日產品預覽」：300x250玩家」)。

**\[廣告來源\]**:（唯讀） *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** （僅限第三方廣告）指出廣告為可展開的橫幅廣告。 相關的擴增設定會決定要購買的庫存，因此請確定它們反映廣告行為。

**[!UICONTROL Expansion Method]:** （僅限第三方可展開橫幅廣告）橫幅是否展開 *[!UICONTROL Click]* 或 *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** （僅限第三方可展開橫幅廣告）廣告展開的方向： *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]*，或 *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** （僅限第三方可擴展橫幅廣告）廣告可用的認證供應商： *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]*，或 *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** （僅限第三方廣告）第三方創意資產的URL。 任何 [timestamp] 和[[timestamp]]參數將替換為實際值。

**[!UICONTROL Final Display Code]:** （僅限第三方廣告）第三方創意資產的URL，必要 [Advertising DSP追蹤巨集](/help/dsp/campaign-management/macros.md) 插入（如果適用）。

**[!UICONTROL Ad Size]:** 廣告的寬度和高度。 一定是 [支援的標準顯示廣告大小](ad-specs.md). 您可以在上傳廣告或輸入 [!UICONTROL Display Code]. 如果您未輸入廣告大小，上傳的廣告或廣告標籤的維度會自動輸入為唯讀。 請注意，如果維度不在「標準顯示」內，則顯示廣告不會儲存為大小 — 例如301x250而非300x250廣告大小。

>[!IMPORTANT]
>
> 在寬度和高度欄位中宣告的廣告大小將與傳入的競標請求相符。 如果廣告的維度與宣告的廣告大小不符，您可能會遇到傳送問題。

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
>* [列出與廣告相關聯的版位](ad-list-placements.md)
>* [廣告規格](ad-specs.md)
>* [DSP巨集](/help/dsp/campaign-management/macros.md)

