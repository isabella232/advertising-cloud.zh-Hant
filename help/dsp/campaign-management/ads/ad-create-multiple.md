---
title: 建立多個第三方廣告
description: 瞭解如何一次建立多個第三方廣告。
feature: DSP Ads
exl-id: 83d35d27-1ab6-4fcf-877f-650a2dc6975a
source-git-commit: bcece4bfec6f8a765cced3ee230fd8cbf3055b7b
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# 建立多個第三方廣告

通過上傳標籤，您一次可以建立多達500個第三方廣告，這些標籤指向第三方廣告伺服器上承載的創意資產。 可以包括廣告的跟蹤像素。<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

您可以上載 [!DNL DoubleClick] 和 [!DNL Flashtalking] 標籤頁或使用提供的模板手動填充的檔案。

>[!TIP]
>
> 最佳做法是使用使用HTTPS安全提供的第三方廣告。 使用HTTPS服務的URL以「https」開頭。

1. 在主菜單中，按一下 **[!UICONTROL Campaigns]**。

1. 按一下將包含廣告的市場活動的名稱。

1. 在資料表上方，按一下 **[!UICONTROL Create]**。 在菜單的「廣告類型」部分，按一下 **[!UICONTROL Bulk upload ads]**。

1. 選擇廣告承載的廣告伺服器： *[!UICONTROL DoubleClick]*。 *[!UICONTROL Flashtalking]*&#x200B;或 *[!UICONTROL Other]*。

1. ([!DNL DoubleClick] 和 [!DNL Flashtalking] ads)選擇要用於每個視頻資產和每個顯示資產的標籤類型。 可用選項因廣告伺服器而異。

1. (所有廣告伺服器上的廣告，除 [!DNL DoubleClick] 和 [!DNL Flashtalking])按一下 **[!UICONTROL Download this template]** 下載模板 [!DNL Microsoft Excel] 電子錶格(XLSX)格式，您可以用廣告資料填充並在本地保存。 所需列包括 [!UICONTROL Ad Name]。 [!UICONTROL VAST/VPAID URL or Ad Tag], [!UICONTROL Ad Types]。

1. 按一下 **[!UICONTROL Upload]** 並從設備或網路中選擇.xlsx或.xls格式的檔案。

   對於 [!DNL DoubleClick] 和 [!DNL Flashtalking] 廣告，從廣告伺服器上載未編輯的標籤頁。 對於其他廣告伺服器，請使用您在步驟3中下載的模板。

1. 上載完成後，按一下 **[!UICONTROL Start Building Ads]**。

1. 查看每個廣告的詳細資訊和狀態：

   1. 查看每個廣告的狀態，該狀態基於對上載標籤的驗證檢查。
   1. （可選）對每個廣告執行下列任一操作：
      * 要預覽廣告，請按一下 ![玩](/help/dsp/assets/play.png) 的下界。
      * 要編輯廣告詳細資訊，請按一下 ![編輯](/help/dsp/assets/edit.png)，編輯詳細資訊，然後按一下 **保存**。
      * 要刪除廣告，請按一下 **[!UICONTROL X]** 的下界。

1. 按一下 **[!UICONTROL Create *N *廣告]**。

1. 執行下列操作之一：

   * 按一下 **[!UICONTROL Done]**.

   * (廣告被拒絕的；（可選）要編輯廣告記錄並重新提交廣告以供審閱：
      1. 按一下廣告名稱。
      1. 編輯廣告設定。
      1. 按一下 **[!UICONTROL Save & submit for review]**.

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [廣告規格](ad-specs.md)
>* [建立單個廣告](ad-create.md)
>* [視頻：如何批量上載第三方廣告標籤](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)

