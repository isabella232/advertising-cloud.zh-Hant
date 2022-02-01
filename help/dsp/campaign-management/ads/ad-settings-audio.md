---
title: 音頻廣告設定
description: 請參閱音頻廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 0%

---

# 音頻廣告設定

## [!UICONTROL Upload or Select Creative]

*僅新廣告*

**[!UICONTROL Upload Audio]:** 將原始資產上載到DSP。 選擇此選項時，請執行以下操作：

1. 按一下 **[!UICONTROL Choose File]** 並在設備或網路上找到該檔案。
1. 輸入檔案的標題，該標題將在 [!UICONTROL Ads] 查看和報告。
1. 按一下 **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** 以帳戶中正確的格式選擇任何先前上載的創作內容。

**[!UICONTROL Advanced: VAST Tag URL]:** 要輸入包含創意資產和跟蹤像素的第三方VAST標籤：

1. 按一下 ![箭頭](/help/dsp/assets/compressed.png) 下 **[!UICONTROL Advanced: VAST Tag URL]**。
1. 在 **[!UICONTROL URL]** 欄位，輸入VAST標籤URL。
1. 輸入 **[!UICONTROL Title]** 檔案，將在 [!UICONTROL Ads] 查看和報告。

>[!TIP]
>
> 要檢查VAST標籤的有效性，請將其貼上到瀏覽器中，然後點擊 **[!UICONTROL Enter]** 按鈕 如果標籤有效，您將看到包含 `<VAST>` 靠近頂端。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （只讀）您正在建立的廣告類型，它與廣告可附加到的放置類型相對應。 預設為 *[!UICONTROL Audio]*。

**[!UICONTROL Ad Name]:** 廣告名。 預設情況下，資產標題會被使用，但您可以更改名稱。

>[!TIP]
>
> 使用將廣告附加到位置時容易找到的名稱， [!UICONTROL Ads] 視圖和報表中。 例如，描述設備類型和某些關鍵屬性(如「假日產品預覽」：30秒音頻」)。

**[!UICONTROL Ad Duration]:** 音頻檔案的長度。 自動設定為 [!UICONTROL 15] 或 [!UICONTROL 30]，具體取決於所選廣告單位。

根據帳戶權限，可能顯示或不顯示此欄位。

**[!UICONTROL Click URL]:** (僅使用原始資產和展示橫幅的廣告；（可選）當查看者按一下廣告附帶的顯示標語時，將登錄到的URL。

**[!UICONTROL Final Click URL]:** (僅使用原始資產和展示橫幅的廣告；只讀) [!UICONTROL Click URL] 必要時 [Advertising Cloud DSP跟蹤宏](/help/dsp/campaign-management/macros.md) 插入（如果適用）。

**[!UICONTROL VAST Tag]:** （僅使用VAST標籤的廣告）第三方廣告源的URL。 確保VAST標籤只包含音頻媒體檔案。

**[!UICONTROL Final VAST Tag]:** （僅使用VAST標籤的廣告）具有必要條件的第三方廣告源的URL [Advertising Cloud DSP跟蹤宏](/help/dsp/campaign-management/macros.md) 插入（如果適用）。

**[!UICONTROL Select Rate]:** （僅具有權限的用戶）通過Adobe計費的預協商費率，或您已協商並將通過供應商計費的費率之一。 要添加費率，請與 [!DNL Adobe] 客戶團隊。

### [!UICONTROL Companion]

*僅DSP提供廣告*

您可以選擇在廣告中附加最多三個伴隨橫幅。 最佳做法是盡可能附上伴隨橫幅。

>[!NOTE]
>
>* 並非所有發佈者都允許附帶條幅。 允許附帶條幅的出版商不能保證附帶條幅的印象。
>* 來自第三方廣告標籤的伴隨橫幅可能並不總是可用於預覽。


**\[複選框\]:** 在廣告中包括指定的伴隨標題。 禁用複選框後，不會包括伴隨橫幅。

**\[橫幅大小\]:** 夥伴橫幅大小： *[!UICONTROL 300x250]* (用於 [!DNL iHeartRadio]。 [!DNL Spotify]。 [!DNL SoundCloud], [!DNL TuneIn]) *[!UICONTROL 640x640]* (用於 [!DNL Spotify), or *1024x1024]*(用於 [!DNL SoundCloud])。

**\[源\]:** 伴隨橫幅資產的來源：

* *[!UICONTROL Upload My Own Asset]:* 上載您自己的資產。
* *[!UICONTROL Use a Third Party Tag]:* 從經認證的第三方廣告服務合作夥伴輸入iFrame或指令碼標籤。

當要跟蹤第三方伴隨橫幅印象時，請使用第三方標籤。

**[!UICONTROL Asset]:** （僅限原始資產）GIF、JPG或PNG格式的伴隨橫幅資產。 按一下 **[!UICONTROL Browse]** 並在設備或網路上找到檔案，然後按一下 **[!UICONTROL Upload]**。

**[!UICONTROL Click URL]:** （僅限原始資產）當查看者按一下廣告的伴隨標題時將登錄的URL。 它可以包括使用第三方點擊跟蹤像素的點擊重定向。

**[!UICONTROL Final Click URL]:** (僅限原始資產；只讀)Click URL(包含必需的 [Advertising Cloud DSP跟蹤宏](/help/dsp/campaign-management/macros.md) 插入（如果適用）。

**[!UICONTROL Ad Tag]:** （僅使用第三方廣告標籤的廣告）用於第三方夥伴橫幅源的iFrame或指令碼橫幅標籤。 它必須來自經認證的第三方廣告服務合作夥伴。

**[!UICONTROL Final Ad Tag]:** （僅使用第三方廣告標籤的廣告）具有必要的廣告標籤 [Advertising Cloud DSP跟蹤宏](/help/dsp/campaign-management/macros.md) 插入（如果適用）。

### 像素

位置的所有現有事件跟蹤像素都會自動附加。 您可以根據跟蹤需要分離現有像素並根據需要建立新像素。

以下設定適用於您建立或編輯的每個像素。

**[!UICONTROL Integration Event]:** 觸發像素觸發的事件。 對於此廣告類型，使用 *[!UICONTROL Impression]* 或 *[!UICONTROL Click-through]*。

**[!UICONTROL Pixel Type]:** 像素是否為 *[!UICONTROL IMG UR]L* （1x1像素影像檔案）, *[!UICONTROL HTML]*&#x200B;或 *[!UICONTROL JavaScript URL]*。

**[!UICONTROL Pixel URL or Code]:** 像素影像的URL，格式與指定的「像素類型」相同。

**[!UICONTROL Pixel Name]:** 像素名稱。 使用有助於輕鬆識別像素的名稱。

**[!UICONTROL Pixel Provider]:** 像素提供器： *[!UICONTROL None]*。 *[!UICONTROL Nielsen]*&#x200B;或 *[!UICONTROL Comscore]*。

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立廣告](ad-create.md)
>* [列出與廣告關聯的放置](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [可用廣告類型](ad-types.md)
>* [廣告規格](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP宏](/help/dsp/campaign-management/macros.md)

