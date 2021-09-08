---
title: 前段廣告設定
description: 請參閱前段廣告可用廣告設定的說明。
feature: Ads
exl-id: 638d5a3d-3dff-40b6-a3ba-7ab3f08282b9
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 0%

---

# 前段廣告設定

## [!UICONTROL Upload or Select Creative]

*僅限新廣告*

**[!UICONTROL Transcode to]:** (部分使用者取決於權限；（可選）當發佈者有特定的創意檔案需求時，您要納入VAST標籤的格式。預設會選取大多數發佈者接受的格式。

**[!UICONTROL Custom Transcode]:** (僅限測試版使用者；選取「垂直視訊」時無法使用))指出視訊使用自訂轉碼。如果您選取此選項，請指定檔案格式、視訊位元速率、縮放和維度，最多可達三個自訂轉碼版本。

**[!UICONTROL XTrader]:** （部分使用者，視權限而定）指出視訊使用一或多個動 [!DNL X_TRADER] 態消息。

**[!UICONTROL Upload Video]:** 將原始資產上傳至DSP。選取此選項時，請執行下列動作：

1. 按一下&#x200B;**[!UICONTROL Choose File]**&#x200B;並在您的設備或網路上找到該檔案。
1. 輸入檔案的標題，該標題將用於[!UICONTROL Ads]視圖和報告中。
1. 按一下 **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Video]:** 在帳戶內以正確格式選取任何先前上傳的創意內容。

**[!UICONTROL Advanced: VAST Tag URL]:** （某些廣告類型）若要輸入包含創意資產和追蹤像素的協力廠商VAST標籤：

1. 按一下![](/help/dsp/assets/compressed.png)旁邊的&#x200B;**[!UICONTROL Advanced: VAST Tag URL]**。
1. 在&#x200B;**[!UICONTROL URL]**&#x200B;欄位中，輸入VAST標籤URL。
1. 輸入檔案的&#x200B;**[!UICONTROL Title]**，該檔案將用於[!UICONTROL Ads]視圖和報告。

>[!TIP]
>
> 若要檢查VAST標籤的有效性，請將其貼到瀏覽器中，然後按一下&#x200B;**[!UICONTROL Enter]**&#x200B;鍵。 如果標籤有效，您會在頂端附近看到包含`<VAST>`的XML檔案。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （唯讀）您要建立的廣告類型，與廣告可附加的版位類型相對應。

**[!UICONTROL Ad Name]:** 廣告名稱。預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 在[!UICONTROL Ads]檢視和報表中，使用將廣告附加至版位時容易找到的名稱。 例如，說明裝置類型和某些關鍵屬性(例如「假日產品預覽」：30秒前段」)。

**[!UICONTROL Width]|  [!UICONTROL Ad Unit Width]:** （僅限標準和可略過的前段廣告）整個廣告單位的寬度。此選項可能會根據您選取的廣告單位類型而鎖定。

**[!UICONTROL Height]|  [!UICONTROL Ad Unit Height]:** （僅限標準和可略過的前段廣告）整個廣告單位的高度。此選項可能會根據您選取的廣告單位類型而鎖定。

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

**[!UICONTROL Wmode]:** （僅限互動式前段）視窗模式： *[!UICONTROL window]*、  *[!UICONTROL transparent]*&#x200B;或 *[!UICONTROL opaque]*。

**[!UICONTROL Video Format]:** （僅限互動式前段）潛在詳細目錄的廣告播放器格式： *[!UICONTROL VPAID]* 或 *[!UICONTROL VPAID & VAST]*。可視度一律會針對VPAID進行測量，但VPAID &amp; VAST包含不允許可視度測量的庫存。 如果可檢視性量度對促銷活動很重要，請記住這一點。

**[!UICONTROL Clock Number]**:(僅限互動式前段；僅用於英國；僅限具有權限的使用者使用)用來確保廣告廣播的唯一識別碼。如果此設定不適用，請將其留空。

### [!UICONTROL Companion]

*僅DSP提供廣告*

您可以選擇在廣告中附加最多三個伴隨橫幅。 最佳作法是盡可能附加隨附橫幅。

>[!NOTE]
>
> 並非所有發佈商都允許隨附橫幅廣告。 允許隨附橫幅的發行者無法保證隨附橫幅曝光次數。
> 來自協力廠商廣告標籤的隨附橫幅可能不一定會可供預覽。

**\[核取方塊\]:** 包含廣告中指定的隨附橫幅。核取方塊停用時，不會包含隨附橫幅。

**\[橫幅大小\]:** 隨附橫幅大小： *[!UICONTROL 300x600 (Skyscraper)]*; *[!UICONTROL 300x250 (Medium Rectangle)]*，這是最常見的廣告大小，且建議用於所有廣告； *[!UICONTROL 300x60 (Small Banner)]*;或 *[!UICONTROL 728x90 (Leaderboard)]*，這是較不常見的廣告大小。

**\[來源\]:** 您是要上傳自己的隨附橫幅資產，還是使用協力廠商標籤。

**資產：** （僅限原始資產）隨附橫幅資產。按一下&#x200B;**[!UICONTROL Browse]**，在您的設備或網路上找到該檔案，然後按一下&#x200B;**[!UICONTROL Upload]**。

**廣告標籤]:[!UICONTROL **（僅限使用VAST標籤的廣告）指向第三方隨附橫幅來源的URL。

**[!UICONTROL Final Ad Tag]:** （僅限使用VAST標籤的廣告）具有必要Advertising Cloud DSP追蹤macrosinserted（若適用）的協力廠商 [隨附橫幅](/help/dsp/campaign-management/macros.md) 來源URL。

### [!UICONTROL Overlays]

*DSP服務廣告的互動式前段和行動互動式及點播播放格式*

下列設定會套用至您建立或編輯的每個覆蓋。

**[!UICONTROL Asset]:** （僅限原始資產）覆蓋的影像資產。檔案必須為單幀GIF、JPG或PNG格式，且影像大小最大小小於2MB。 若要上傳資產，請按一下&#x200B;**[!UICONTROL Browse]**&#x200B;並在您的裝置或網路上找到檔案，然後按一下&#x200B;**[!UICONTROL Upload]**。

>[!TIP]
>
>請參閱[設計覆蓋的最佳作法](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)

**[!UICONTROL Click URL]:**  檢視器按一下廣告的覆蓋圖時將著陸的URL。

**[!UICONTROL X]:** 覆蓋的X座標。選取覆蓋起始位置，然後輸入起始位置的像素數（例如從中間10像素）。 最佳實務是使用&#x200B;*From Center*，以防止覆蓋在發佈者網站上以不同播放器大小移動。

**[!UICONTROL Y]:** 覆蓋的Y座標。選取覆蓋圖的起始位置，然後輸入起始位置的像素數（例如從上方10像素）。 最佳作法是根據您希望覆蓋圖在廣告上顯示的位置，指定座標&#x200B;*[!UICONTROL From Bottom]*&#x200B;或&#x200B;*[!UICONTROL From Top]、*。

**[!UICONTROL Layer]:** 將顯示覆蓋圖的圖層。視訊和每個覆蓋圖將位於不同的圖層中。

* *[!UICONTROL 2 through 5]:* 在視訊前面，但在其他覆蓋後面。

* *[!UICONTROL 1]:* 在影片前面。

* *[!UICONTROL 0]:* 與視訊位於相同層。視頻將縮小以填充剩餘空間。 不建議使用互動式前置檔案。

* *[!UICONTROL -1]:* 影片後面。

* *[!UICONTROL -2 through -5]:* 在影片後面，但在其他覆蓋前面。

* *[!UICONTROL Background]:* 影片和其他覆蓋的後面。覆蓋會縮放至視訊的全部寬度和高度，且外觀比例不會保留。

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
>* [列出與廣告相關聯的版位](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [可用廣告類型](ad-types.md)
>* [廣告規格](/help/dsp/assets/ad-specs.pdf)
>* [設計覆蓋圖的最佳作法](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)
>* [Advertising Cloud DSP巨集](/help/dsp/campaign-management/macros.md)

