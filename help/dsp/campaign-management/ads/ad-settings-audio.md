---
title: 音訊廣告設定
description: 請參閱音訊廣告可用廣告設定的說明。
feature: DSP Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 0%

---

# 音訊廣告設定

## [!UICONTROL Upload or Select Creative]

*僅限新廣告*

**[!UICONTROL Upload Audio]:** 將原始資產上傳至DSP。選取此選項時，請執行下列動作：

1. 按一下&#x200B;**[!UICONTROL Choose File]**&#x200B;並在您的設備或網路上找到該檔案。
1. 輸入檔案的標題，該標題將用於[!UICONTROL Ads]視圖和報告中。
1. 按一下 **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** 在帳戶內以正確格式選取任何先前上傳的創意內容。

**[!UICONTROL Advanced: VAST Tag URL]:** 若要輸入包含創意資產和追蹤像素的協力廠商VAST標籤：

1. 按一下![](/help/dsp/assets/compressed.png)旁邊的&#x200B;**[!UICONTROL Advanced: VAST Tag URL]**。
1. 在&#x200B;**[!UICONTROL URL]**&#x200B;欄位中，輸入VAST標籤URL。
1. 輸入檔案的&#x200B;**[!UICONTROL Title]**，該檔案將用於[!UICONTROL Ads]視圖和報告。

>[!TIP]
>
> 若要檢查VAST標籤的有效性，請將其貼到瀏覽器中，然後按一下&#x200B;**[!UICONTROL Enter]**&#x200B;鍵。 如果標籤有效，您會在頂端附近看到包含`<VAST>`的XML檔案。

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** （唯讀）您要建立的廣告類型，與廣告可附加的版位類型相對應。預設為&#x200B;*[!UICONTROL Audio]*。

**[!UICONTROL Ad Name]:** 廣告名稱。預設會使用資產標題，但您可以變更名稱。

>[!TIP]
>
> 在[!UICONTROL Ads]檢視和報表中，使用將廣告附加至版位時容易找到的名稱。 例如，說明裝置類型和某些關鍵屬性(例如「假日產品預覽」：30秒音頻」)。

**[!UICONTROL Ad Duration]:** 音訊檔案的長度。視選取的廣告單位而定，會自動設為[!UICONTROL 15]或[!UICONTROL 30]。

視帳戶權限而定，此欄位可能會顯示，也可能不顯示。

**[!UICONTROL Click URL]:** (僅使用原始資產且具有顯示橫幅的廣告；選用)檢視器按一下廣告隨附的顯示橫幅時將著陸的URL。

**[!UICONTROL Final Click URL]:** (僅使用原始資產且具有顯示橫幅的廣告；唯讀)具有必 [!UICONTROL Click URL] 要Advertising Cloud DSP [追蹤](/help/dsp/campaign-management/macros.md) 宏集（若適用）。

**[!UICONTROL VAST Tag]:** （僅限使用VAST標籤的廣告）協力廠商廣告來源的URL。請確定VAST標籤僅包含音訊媒體檔案。

**[!UICONTROL Final VAST Tag]:** （僅限使用VAST標籤的廣告）具有必要Advertising Cloud DSP追蹤macroserted之協力廠商廣 [告](/help/dsp/campaign-management/macros.md) 來源的URL（若適用）。

**[!UICONTROL Select Rate]:** （僅限擁有權限的使用者）透過Adobe計費的預先協商費率，或您已洽談且將透過供應商計費的其中一種費率。若要新增費率，請連絡您的Adobe帳戶管理員。

### [!UICONTROL Companion]

*僅DSP提供廣告*

您可以選擇在廣告中附加最多三個伴隨橫幅。 最佳作法是盡可能附加隨附橫幅。

>[!NOTE]
>
>* 並非所有發佈商都允許隨附橫幅廣告。 允許隨附橫幅的發行者無法保證隨附橫幅曝光次數。
>* 來自協力廠商廣告標籤的隨附橫幅可能不一定會可供預覽。


**\[核取方塊\]:** 包含廣告中指定的隨附橫幅。核取方塊停用時，不會包含隨附橫幅。

**\[橫幅大小\]:** 隨附橫幅大小： *[!UICONTROL 300x250]* (用 [!DNL iHeartRadio]於、  [!DNL Spotify]、  [!DNL SoundCloud]和 [!DNL TuneIn])、( *[!UICONTROL 640x640]* 用於 [!DNL Spotify), or *1024x1024]*(用於 [!DNL SoundCloud])。

**\[來源\]:** 隨附橫幅資產的來源：

* *[!UICONTROL Upload My Own Asset]:* 上傳您自己的資產。
* *[!UICONTROL Use a Third Party Tag]:* 從經認證的第三方廣告服務合作夥伴輸入iFrame或指令碼標籤。

當您想要追蹤協力廠商隨附橫幅曝光次數時，請使用協力廠商標籤。

**[!UICONTROL Asset]:** （僅限原始資產）隨附的橫幅資產，格式為GIF、JPG或PNG格式。按一下&#x200B;**[!UICONTROL Browse]**，在您的設備或網路上找到該檔案，然後按一下&#x200B;**[!UICONTROL Upload]**。

**[!UICONTROL Click URL]:** （僅限原始資產）檢視器按一下廣告的隨附橫幅時將著陸的URL。其中可包含使用協力廠商點擊追蹤像素的點擊重新導向。

**[!UICONTROL Final Click URL]:** (僅限原始資產；唯讀)點按URL並加上必要的Advertising Cloud DSP [追蹤](/help/dsp/campaign-management/macros.md) 宏集（若適用）。

**[!UICONTROL Ad Tag]:** （僅限使用協力廠商廣告標籤的廣告）第三方隨附橫幅來源的iFrame或指令碼橫幅標籤。必須來自經認證的第三方廣告服務合作夥伴。

**[!UICONTROL Final Ad Tag]:** （僅限使用協力廠商廣告標籤的廣告）具有必要Advertising Cloud DSP追 [蹤](/help/dsp/campaign-management/macros.md) 宏集的廣告標籤（若適用）。

### 像素

版位的所有現有事件追蹤像素會自動附加。 您可以根據追蹤需求分離現有像素並視需要建立新像素。

下列設定會套用至您建立或編輯的每個像素。

**[!UICONTROL Integration Event]:** 觸發像素的事件。對於此廣告類型，請使用在&#x200B;*[!UICONTROL Impression]*&#x200B;或&#x200B;*[!UICONTROL Click-through]*&#x200B;上引發的像素。

**[!UICONTROL Pixel Type]:** 像素是 *[!UICONTROL IMG UR]L* （1x1像素影像檔案）、 *[!UICONTROL HTML]*&#x200B;還是 *[!UICONTROL JavaScript URL]*。

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

