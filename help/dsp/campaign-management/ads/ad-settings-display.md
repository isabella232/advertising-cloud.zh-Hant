---
title: 顯示廣告設定
description: 請參閱顯示廣告可用廣告設定的說明。
feature: Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# 顯示廣告設定

以下是標準顯示廣告的設定。 您也可以針對顯示廣告提供點按播放視訊廣告，但我們不建議這麼做，因為沒有多少發佈商支援。

## [!UICONTROL Ad Options]

### 基本

**[!UICONTROL Ad Type]:** （唯讀）您要建立的廣告類型，與廣告可附加的版位類型相對應。預設為&#x200B;*[!UICONTROL Display]*。

**[!UICONTROL Ad Name]:** 廣告名稱。預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 在[!UICONTROL Ads]檢視和報表中，使用將廣告附加至版位時容易找到的名稱。 例如，說明裝置類型和某些關鍵屬性(例如「假日產品預覽」：300x250玩家」)。

**\[廣告來源\]**:無論Advertising Cloud DSP是提供廣告(*[!UICONTROL Adobe served]*)，還是您使用第三方廣告伺服器(*[!UICONTROL 3rd party]*)。

**[!UICONTROL This is an expandable Banner]:** （僅限第三方廣告）指出廣告為可展開的橫幅廣告。相關的擴增設定會決定要購買的庫存，因此請確定它們反映廣告行為。

**[!UICONTROL Expansion Method]:** （僅限第三方可展開橫幅廣告）橫幅會展開 *[!UICONTROL Click]* 還是 *[!UICONTROL Rollover]*。

**[!UICONTROL Expansion Directions]:** （僅限第三方可展開橫幅廣告）廣告展開的方向： *[!UICONTROL Up]*、  *[!UICONTROL Down]*、  *[!UICONTROL Left]*&#x200B;或 *[!UICONTROL Right]*。

**[!UICONTROL Certified Vendors]:** （僅限第三方可展開橫幅廣告）廣告可用的認證供應商： *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers])、  *[!UICONTROL Flashtalking]*、  *[!UICONTROL Sizmek]*&#x200B;或 *[!UICONTROL Jivox]*。

**[!UICONTROL Display Code]:** （僅限第三方廣告）第三方創意資產的URL。任何[timestamp]和[[timestamp]]參數都將替換為實際值。

**[!UICONTROL Final Display Code]:** （僅限第三方廣告）第三方創意資產的URL，並納入必要的Advertising Cloud DSP [追蹤](/help/dsp/campaign-management/macros.md) 巨集指令（若適用）。

**[!UICONTROL Creative type]:** (僅限Adobe提供的廣告)資產是 *[!UICONTROL Image]* 或資 *[!UICONTROL HTML5]* 產。

**[!UICONTROL Asset]|  [!UICONTROL HTML5 Asset]:** (僅限Adobe提供的廣告)要上傳的影像檔案或壓縮HTML5資產，視創作類型而定。按一下&#x200B;**[!UICONTROL Browse]**&#x200B;並在您的設備或網路上找到該檔案，然後按一下&#x200B;**[!UICONTROL Upload]**&#x200B;或&#x200B;**[!UICONTROL Upload Image]**。

**[!UICONTROL Ad Size]:** 廣告的寬度和高度。必須是[支援的標準顯示廣告大小](/help/dsp/assets/ad-specs.pdf)。 您可以在上傳廣告之前手動輸入廣告大小，或輸入[!UICONTROL Display Code]。 如果您未輸入廣告大小，上傳的廣告或廣告標籤的維度會自動輸入為唯讀。 請注意，如果維度不在「標準顯示」內，則顯示廣告不會儲存為大小，例如301x250而非300x250廣告大小。

>[!IMPORTANT]
>
> 在寬度和高度欄位中宣告的廣告大小將與傳入的競標請求相符。 如果廣告的維度與宣告的廣告大小不符，您可能會遇到傳送問題。

**[!UICONTROL Click URL]:** (僅限Adobe提供的廣告)檢視者點按廣告時將登陸的URL。

**[!UICONTROL Final Click URL]:** (僅限Adobe提供的廣告；唯讀)具有必 [!UICONTROL Click URL] 要Advertising Cloud DSP [追蹤](/help/dsp/campaign-management/macros.md) 宏集（若適用）。

### [!UICONTROL Pixel]

版位的所有現有事件追蹤像素會自動附加。 您可以根據追蹤需求分離現有像素並視需要建立新像素。

下列設定會套用至您建立或編輯的每個像素。

**[!UICONTROL Integration Event]:** 觸發像素的事件。對於此廣告類型，請使用在&#x200B;*[!UICONTROL Impression]*&#x200B;或&#x200B;*[!UICONTROL Click-through]*&#x200B;上引發的像素。

**[!UICONTROL Pixel Type]:** 像素是(1x1 *[!UICONTROL IMG URL]* 像素影像檔案)、 *[!UICONTROL HTML]*&#x200B;還是 *[!UICONTROL JavaScript URL]*。

**[!UICONTROL Pixel URL or Code]:** 像素影像的URL，為指定的適當格 [!UICONTROL Pixel Type]式。

**[!UICONTROL Pixel Name]:** 像素名稱。使用有助於輕鬆識別像素的名稱。

**[!UICONTROL Pixel Provider]:** 像素提供者： *[!UICONTROL None]*、  *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*。

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立廣告](ad-create.md)
>* [列出與廣告相關聯的版位](ad-list-placements.md)
>* [可用廣告類型](ad-types.md)
>* [廣告規格](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP巨集](/help/dsp/campaign-management/macros.md)

