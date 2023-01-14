---
title: 建立多個第三方廣告
description: 了解如何一次建立多個第三方廣告。
feature: DSP Ads
exl-id: 83d35d27-1ab6-4fcf-877f-650a2dc6975a
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# 建立多個第三方廣告

您可以上傳標籤，將該標籤指向在第三方廣告伺服器上托管的創意資產，一次最多建立500個第三方廣告。 您可以包含廣告的追蹤像素。<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

您可以上傳 [!DNL DoubleClick] 和 [!DNL Flashtalking] 標籤表或使用提供的範本手動填入的檔案。

>[!TIP]
>
> 最佳實務是使用使用HTTPS安全提供的協力廠商廣告。 使用HTTPS提供的URL以「https」開頭。

1. 在主功能表中，按一下 **[!UICONTROL Campaigns]**.

1. 按一下將包含廣告的促銷活動名稱。

1. 在資料表格上方，按一下 **[!UICONTROL Create]**. 在功能表的「廣告類型」區段中，按一下 **[!UICONTROL Bulk upload ads]**.

1. 選取裝載廣告的廣告伺服器： *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]*，或 *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] 和 [!DNL Flashtalking] 廣告)選取要用於每個視訊資產和每個顯示資產的標籤類型。 可用選項依廣告伺服器而異。

1. (廣告在除 [!DNL DoubleClick] 和 [!DNL Flashtalking])按一下 **[!UICONTROL Download this template]** 若要下載範本，請在 [!DNL Microsoft Excel] 試算表(XLSX)格式，您可填入廣告資料並儲存於本機。 所需欄包括 [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag]，和 [!UICONTROL Ad Types].

1. 按一下 **[!UICONTROL Upload]** 並從您的裝置或網路選取.xlsx或.xls格式的檔案。

   針對 [!DNL DoubleClick] 和 [!DNL Flashtalking] 廣告，從廣告伺服器上傳未編輯的標籤表。 對於其他廣告伺服器，請使用您在步驟3中下載的範本。

1. 上傳完成後，按一下 **[!UICONTROL Start Building Ads]**.

1. 檢閱每個廣告的詳細資訊和狀態：

   1. 檢閱每個廣告的狀態，此狀態以上傳標籤的驗證檢查為基礎。

   1. （選用）對每個廣告執行下列任一操作：

      * 若要預覽廣告，請按一下 ![play](/help/dsp/assets/play.png) 在廣告列中。

      * 若要編輯廣告詳細資訊，請按一下 ![編輯](/help/dsp/assets/edit.png)，編輯詳細資訊，然後按一下 **儲存**.

      * 若要移除廣告，請按一下 **[!UICONTROL X]** 在廣告列中。

1. 按一下 **[!UICONTROL Create *N *廣告]**.

1. 執行下列任一操作：

   * 按一下 **[!UICONTROL Done]**.

   * (如果廣告遭拒；（可選）要編輯廣告記錄並重新提交廣告以供複查：

      1. 按一下廣告名稱。

      1. 編輯廣告設定。

      1. 按一下 **[!UICONTROL Save & submit for review]**.

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [廣告規格](ad-specs.md)
>* [建立單一廣告](ad-create.md)
>* [影片：如何大量上傳協力廠商廣告標籤](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)

