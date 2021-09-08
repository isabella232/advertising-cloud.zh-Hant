---
title: 已連接的電視廣告設定
description: 請參閱連線電視廣告可用廣告設定的說明。
feature: Ads
exl-id: 4daae9e4-27eb-4496-9186-f33aebd8daae
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# 已連接的電視廣告設定

## [!UICONTROL Upload or Select Creative]

*僅限新廣告*

**[!UICONTROL Upload Audio]:** 將原始資產上傳至DSP。選取此選項時，請執行下列動作：

1. 按一下&#x200B;**[!UICONTROL Choose File]**&#x200B;並在您的設備或網路上找到該檔案。
1. 輸入檔案的標題，該標題將用於[!UICONTROL Ads]視圖和報告中。
1. 按一下 **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** 在帳戶內以正確格式選取任何先前上傳的創意內容。

**[!UICONTROL Advanced: VAST Tag URL]:** （某些廣告類型）若要輸入包含創意資產和追蹤像素的協力廠商VAST標籤：

1. 按一下![](/help/dsp/assets/compressed.png)旁邊的&#x200B;**[!UICONTROL Advanced: VAST Tag URL]**。
1. 在&#x200B;**[!UICONTROL URL]**&#x200B;欄位中，輸入VAST標籤URL。
1. 輸入檔案的&#x200B;**[!UICONTROL Title]**，該檔案將用於廣告檢視和報表。

>[!TIP]
>
> 若要檢查VAST標籤的有效性，請將其貼到瀏覽器中，然後按一下&#x200B;**[!UICONTROL Enter]**&#x200B;鍵。 如果標籤有效，您會在頂端附近看到包含`<VAST>`的XML檔案。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （唯讀）您要建立的廣告類型，與廣告可附加的版位類型相對應。

**[!UICONTROL Ad Name]:** 廣告名稱。預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 在[!UICONTROL Ads]檢視和報表中，使用將廣告附加至版位時容易找到的名稱。 例如，說明裝置類型和某些關鍵屬性(例如「假日產品預覽」：30秒CTV」)。

**[!UICONTROL Width | Ad Unit Width]:** 整個廣告單位的寬度。此選項可能會根據您選取的廣告單位類型而鎖定。

**[!UICONTROL Height | Ad Unit Height]:** 整個廣告單位的高度。此選項可能會根據您選取的廣告單位類型而鎖定。

**[!UICONTROL Player X]:** 廣告單位的X座標。保留預設設定。

**[!UICONTROL Player Y]:** 廣告單位的Y座標。保留預設設定。

**[!UICONTROL Player Width]:** 整個廣告單位的寬度。此選項可能會根據您選取的廣告單位類型而鎖定。

這與&#x200B;**[!UICONTROL Width]**&#x200B;欄位相同。

**[!UICONTROL Player Height]:** 整個廣告單位的高度。此選項可能會根據您選取的廣告單位類型而鎖定。

這與&#x200B;**[!UICONTROL Height]**&#x200B;欄位相同。

**[!UICONTROL Show Controls]:** 要在何處納入廣告的視訊控制： *[!UICONTROL Under]*、  *[!UICONTROL Over]*、  *[!UICONTROL Bottom]*&#x200B;或( *[!UICONTROL None]* 預設)。

**[!UICONTROL Preserve Aspect Ratio]:** 是要保留視訊的寬度和高度比例(*[!UICONTROL Yes]*)，還是要延伸視訊以填滿可用空間(*[!UICONTROL No]*)。

**[!UICONTROL Click URL]:** (僅限Adobe提供的廣告)檢視者點按廣告時將登陸的URL。

**[!UICONTROL Final Click URL]:** (僅限Adobe提供的廣告；唯讀)具有必 [!UICONTROL Click URL] 要Advertising Cloud DSP [追蹤](/help/dsp/campaign-management/macros.md) 宏集（若適用）。

**[!UICONTROL VAST Tag]:** (僅使用VAST標籤的廣告；唯讀)您輸入做為廣告來源的第三方VAST標籤。

**[!UICONTROL Final VAST Tag]:** (僅使用VAST標籤的廣告；唯讀)您輸入做為廣告來源的第三方VAST標籤，且會納入必要的 [Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) 追蹤宏集（若適用）。

**[!UICONTROL Clock Number]**:(僅在聯合王國使用；僅限具有權限的使用者使用)用來確保廣告廣播的唯一識別碼。如果此設定不適用，請將其留空。

### [!UICONTROL Pixel]

版位的所有現有事件追蹤像素會自動附加。 您可以根據追蹤需求分離現有像素並視需要建立新像素。

下列設定會套用至您建立或編輯的每個像素。

**[!UICONTROL Integration Event]:** 觸發像素的事件。對於此廣告類型，請使用在&#x200B;*[!UICONTROL Impression]*&#x200B;或&#x200B;*[!UICONTROL Click-through]*&#x200B;上引發的像素。

**[!UICONTROL Pixel Type]:** 像素是(1x1 *[!UICONTROL IMG URL]* 像素影像檔案)、 *[!UICONTROL HTML]*&#x200B;還是 *[!UICONTROL JavaScript URL]*。

**[!UICONTROL Pixel URL or Code]:** 像素影像的URL，為指定的「像素類型」的適當格式。

**[!UICONTROL Pixel Name]:** 像素名稱。使用有助於輕鬆識別像素的名稱。

**[!UICONTROL Pixel Provider]:** 像素提供者： *[!UICONTROL None]*、  *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*。

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立廣告](ad-create.md)
>* [列出與廣告相關聯的版位](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [可用廣告類型](ad-types.md)
>* [廣告規格](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP巨集](/help/dsp/campaign-management/macros.md)

