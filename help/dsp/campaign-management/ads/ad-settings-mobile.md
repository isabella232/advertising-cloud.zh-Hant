---
title: 行動廣告設定
description: 請參閱行動廣告可用廣告設定的說明。
feature: Ads
exl-id: f67c4ba0-1011-4ad6-bd36-98c312b81b67
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '1335'
ht-degree: 0%

---

# 行動廣告設定

## [!UICONTROL Upload or Select Creative]

*僅限全新行動視訊廣告格式*

**[!UICONTROL Vertical video]:** (選取時無 [!UICONTROL Custom Transcode] 法使用)指出視訊為垂直（縱向模式）。

**[!UICONTROL Transcode to]:** (部分使用者取決於權限；（可選）當發佈者有特定的創意檔案需求時，您要納入VAST標籤的格式。預設會選取大多數發佈者接受的格式。

**[!UICONTROL Custom Transcode]:** (僅限測試版使用者；選取「垂直視訊」時無法使用))指出視訊使用自訂轉碼。如果您選取此選項，請指定檔案格式、視訊位元速率、縮放和維度，最多可達三個自訂轉碼版本。

**[!UICONTROL XTrader]:** （部分使用者，視權限而定）指出視訊使用一或多個 [!DNL X_TRADER] 摘要。

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

**[!UICONTROL Advanced: 3rd party Ad Tag]:** （某些廣告類型）若要輸入包含創意資產和追蹤像素的第三方廣告標籤：

1. 按一下![](/help/dsp/assets/compressed.png)旁邊的&#x200B;**[!UICONTROL Advanced: #3rd party Ad Tag]**。
1. 輸入檔案的&#x200B;**[!UICONTROL Ad Title]**，該檔案將用於[!UICONTROL Ads]視圖和報告。
1. 在&#x200B;**[!UICONTROL Ad Tag]**&#x200B;欄位中，輸入廣告標籤。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]:行動顯示廣告

**[!UICONTROL Ad Type]:** （唯讀）您要建立的廣告類型，與廣告可附加的版位類型相對應。

**[!UICONTROL Ad Name]:** 廣告名稱。預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 在廣告檢視和報表中將廣告附加至版位時，請使用易於找到的名稱。 例如，說明裝置類型和某些關鍵屬性(例如「假日產品預覽」：300x250玩家」)。

**\[廣告來源\]**:無論Advertising Cloud DSP是提供廣告(*[!UICONTROL Adobe served]*)，還是您使用第三方廣告伺服器(*[!UICONTROL 3rd party]*)。

**[!UICONTROL Creative type]:** (僅限Adobe提供的廣告)資產是 *[!UICONTROL Image]* 或資 *[!UICONTROL HTML5]* 產。

**[!UICONTROL Asset]|  [!UICONTROL HTML5 Asset]:** (僅限Adobe提供的廣告)要上傳的影像檔案或壓縮HTML5資產，視創作類型而定。按一下&#x200B;**[!UICONTROL Browse]**，在您的設備或網路上找到該檔案，然後按一下&#x200B;**[!UICONTROL Upload]**。

**[!UICONTROL Click URL]:** (僅限Adobe提供的廣告)檢視者點按廣告時將登陸的URL。

**[!UICONTROL Final Click URL]:** (僅限Adobe提供的廣告；唯讀)點按URL並加上必要的Advertising Cloud DSP [追蹤](/help/dsp/campaign-management/macros.md) 宏集（若適用）。

**[!UICONTROL Display Code]:** （僅限第三方廣告）第三方創意資產的URL。任何[timestamp]和[[timestamp]]參數都將替換為實際值。

**[!UICONTROL Final Display Code]:** （僅限第三方廣告）第三方創意資產的URL，並納入必要的Advertising Cloud DSP [追蹤](/help/dsp/campaign-management/macros.md) 巨集指令（若適用）。

### [!UICONTROL Basic]:視訊廣告

**[!UICONTROL Ad Type]:** （唯讀）您要建立的廣告類型，與廣告可附加的版位類型相對應。

**[!UICONTROL Ad Name]:** 廣告名稱。預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 在廣告檢視和報表中將廣告附加至版位時，請使用易於找到的名稱。 例如，說明裝置類型和某些關鍵屬性(例如「假日產品預覽」：30秒Phone Preroll」)。

**[!UICONTROL Width]|  [!UICONTROL Ad Unit Width]:** 整個廣告單元的寬度。此選項可能會根據您選取的廣告單位類型而鎖定。

**[!UICONTROL Height]|  [!UICONTROL Ad Unit Height]:** 整個廣告單元的高度。此選項可能會根據您選取的廣告單位類型而鎖定。

**[!UICONTROL Player X]:** 廣告單位的X座標。保留預設設定。

**[!UICONTROL Player Y]:** 廣告單位的Y座標。保留預設設定。

**[!UICONTROL Player Width]:** 整個廣告單位的寬度。此選項可能會根據您選取的廣告單位類型而鎖定。

這與&#x200B;**[!UICONTROL Width]**&#x200B;欄位相同。

**[!UICONTROL Player Height]:** 整個廣告單位的高度。此選項可能會根據您選取的廣告單位類型而鎖定。

這與&#x200B;**[!UICONTROL Height]**&#x200B;欄位相同。

**[!UICONTROL Show Controls]:** 要在何處納入廣告的視訊控制： *[!UICONTROL Under]*、  *[!UICONTROL Over]*、  *[!UICONTROL Bottom]*&#x200B;或( *[!UICONTROL None]* 預設)。

**[!UICONTROL Preserve Aspect Ratio]:** 是要保留視訊的寬度和高度比例(*[!UICONTROL Yes]*)，還是要延伸視訊以填滿可用空間(*[!UICONTROL No]*)。

**[!UICONTROL Close Button Delay]:** （某些廣告類型）延遲關閉按鈕外觀的秒數。

**[!UICONTROL Click URL]:** (僅限Adobe提供的廣告)檢視者點按廣告時將登陸的URL。

**[!UICONTROL Final Click URL]:** (僅限Adobe提供的廣告；唯讀)具有必 [!UICONTROL Click URL] 要Advertising Cloud DSP [追蹤](/help/dsp/campaign-management/macros.md) 宏集（若適用）。

**[!UICONTROL VAST Tag]:** (僅使用VAST標籤的廣告；唯讀)您作為創意資產輸入的第三方VAST標籤。

**[!UICONTROL Final VAST Tag]:** (僅使用VAST標籤的廣告；唯讀)您輸入做為創意資產的第三方VAST標籤，且會納入必要的 [Advertising Cloud DSP](/help/dsp/campaign-management/macros.md) 追蹤宏集（若適用）。

**[!UICONTROL Wmode]:** （部分廣告類型）視窗模式： *[!UICONTROL window]*、  *[!UICONTROL transparent]*&#x200B;或 *[!UICONTROL opaque]*。

### [!UICONTROL Teaser]

*DSP服務廣告的行動點播格式*

**[!UICONTROL Asset]:** 預告影像或影片資產：

* 要選擇您自己的映像，請按一下&#x200B;**[!UICONTROL Choose File],**&#x200B;在您的設備或網路上找到該檔案，然後按一下&#x200B;**[!UICONTROL Upload Image]**。

   最佳實務是使用與廣告單位維度相同的影像。

* 若要從創作中選取影像，請按一下&#x200B;**[!UICONTROL Choose Thumbnail]**。

靜態影像預告器的需求：

* 格式：GIF、JPEG、PNG
* 影像大小：300x250
* 檔案大小：50KB或更短
* 建議：行動呼籲，可識別的影像，品牌標誌

視訊預告器需求：

* 檔案類型：MOV, MP4
* 檔案大小：小於2MB
* 持續時間：7-10秒
* 建議：可識別的影像、面孔、快速剪切

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

### [!UICONTROL Endcap]

已棄用

### [!UICONTROL Pixel]

版位的所有現有事件追蹤像素會自動附加。 您可以根據追蹤需求分離現有像素並視需要建立新像素。

下列設定會套用至您建立或編輯的每個像素。

**[!UICONTROL Integration Event]:** 觸發像素的事件。對於此廣告類型，請使用在&#x200B;*[!UICONTROL Impression]*&#x200B;或&#x200B;*[!UICONTROL Click-through]*&#x200B;上引發的像素。

**[!UICONTROL Pixel Type]:** 像素是(1x1 *[!UICONTROL IMG URL]* 像素影像檔案)、 *[!UICONTROL HTML]*&#x200B;還是 *[!UICONTROL JavaScript URL]*。

**[!UICONTROL Pixel URL or Code]:** 像素影像的URL，為指定的適當格 [!UICONTROL Pixel Type]式。

**[!UICONTROL Pixel Name]:** 像素名稱。使用有助於輕鬆識別像素的名稱。

**[!UICONTROL Pixel Provider]:** 像素提供者： *[!UICONTROL None]*、  *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*。

### [!UICONTROL Sharing]

已棄用

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立廣告](ad-create.md)
>* [列出與廣告相關聯的版位](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [可用廣告類型](ad-types.md)
>* [廣告規格](/help/dsp/assets/ad-specs.pdf)
>* [設計覆蓋圖的最佳作法](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)
>* [Advertising Cloud DSP巨集](/help/dsp/campaign-management/macros.md)

