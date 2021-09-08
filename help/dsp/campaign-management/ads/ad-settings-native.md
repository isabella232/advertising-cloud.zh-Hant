---
title: 原生廣告設定
description: 請參閱原生廣告可用廣告設定的說明。
feature: Ads
exl-id: 3ae59e63-ae64-41b2-8734-3df2da020c7c
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# 原生廣告設定

## [!UICONTROL Upload or Select Creative]

*僅限新視訊（但不顯示）廣告*

**[!UICONTROL Upload Audio]:** 將原始資產上傳至DSP。選取此選項時，請執行下列動作：

1. 按一下&#x200B;**[!UICONTROL Choose File]**&#x200B;並在您的設備或網路上找到該檔案。
1. 輸入檔案的標題，該標題將用於[!UICONTROL Ads]視圖和報告中。
1. 按一下 **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** 在帳戶內以正確格式選取任何先前上傳的創意內容。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （唯讀）您要建立的廣告類型，與廣告可附加的版位類型相對應。

**[!UICONTROL Ad Name]:** 廣告名稱。預設會使用廣告類型（顯示原生）或視訊標題（視訊格式），但您可以變更名稱。

>[!TIP]
>
> 在[!UICONTROL Ads]檢視和報表中，使用將廣告附加至版位時容易找到的名稱。 例如，說明裝置類型和某些關鍵屬性(例如「假日產品預覽」：15秒本機」)。

**[!UICONTROL Native Creative]:** 1200x627影像，可將行動詳細目錄上的傳送作業最大化。對於視訊廣告，這會是原生視訊播放前所顯示的影像。 按一下&#x200B;**[!UICONTROL Browse]**，在您的設備或網路上找到該檔案，然後按一下&#x200B;**[!UICONTROL Upload]**。

**[!UICONTROL Title]:** 吸引觀眾目光的標題。

**[!UICONTROL Description]:** 對於視訊廣告，此為廣告的簡短摘要。對於顯示廣告，這是廣告的內文。 長度上限為100個字元。

**[!UICONTROL Landing Page]:** 檢視器點按廣告時將著陸的URL。

**[!UICONTROL Final Landing Page]:** 具有必 [!UICONTROL Landing Page] 要Advertising Cloud DSP追蹤 [的](/help/dsp/campaign-management/macros.md) URL（如果適用）。

**[!UICONTROL Sponsored By (Advertiser Name)]:** 廣告的廣告商。

**[!UICONTROL Call to Action]:** （選用）檢視者看到此廣告後，所要採取的步驟。

**[!UICONTROL Advertiser Logo]:** （選用）要加入廣告的1:1比例標誌，以獲得更多品牌認可。按一下&#x200B;**[!UICONTROL Browse]**，在您的設備或網路上找到該檔案，然後按一下&#x200B;**[!UICONTROL Upload]**。

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
>* [Advertising Cloud DSP巨集](/help/dsp/campaign-management/macros.md)

