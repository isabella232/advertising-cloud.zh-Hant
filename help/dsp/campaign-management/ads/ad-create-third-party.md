---
title: 建立多個第三方廣告
description: 了解如何一次建立多個第三方廣告。
feature: DSP Ads
exl-id: 83d35d27-1ab6-4fcf-877f-650a2dc6975a
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# 建立多個第三方廣告

您可以上傳標籤，將該標籤指向在第三方廣告伺服器上托管的創意資產，一次最多建立500個第三方廣告。 您可以包含廣告的追蹤像素。<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

您可以上傳[!DNL DoubleClick]和[!DNL Flashtalking]標籤表，或使用提供的範本手動填入檔案。

若要建立單一第三方廣告，請參閱[建立廣告](ad-create.md)。

>[!TIP]
>
> 最佳實務是使用使用HTTPS安全提供的協力廠商廣告。 使用HTTPS提供的URL以「https」開頭。

1. 在主菜單中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 按一下將包含廣告的促銷活動名稱。

1. 在資料表上方，按一下&#x200B;**[!UICONTROL Create]**。 在功能表的「廣告類型」區段中，按一下&#x200B;**[!UICONTROL Bulk upload ads]**。

1. 選取裝載廣告的廣告伺服器：*[!UICONTROL DoubleClick]*、*[!UICONTROL Flashtalking]*&#x200B;或&#x200B;*[!UICONTROL Other]*。

1. （[!DNL DoubleClick]和[!DNL Flashtalking]廣告）選取要用於每個視訊資產和每個顯示資產的標籤類型。 可用選項依廣告伺服器而異。

1. （在[!DNL DoubleClick]和[!DNL Flashtalking]以外的所有廣告伺服器上顯示廣告）按一下&#x200B;**[!UICONTROL Download this template]**&#x200B;下載[!DNL Microsoft Excel]試算表(XLSX)格式的範本，您可以填入廣告資料並在本機儲存。 所需欄包括[!UICONTROL Ad Name]、[!UICONTROL VAST/VPAID URL or Ad Tag]和[!UICONTROL Ad Types]。

1. 按一下&#x200B;**[!UICONTROL Upload]**&#x200B;並從您的裝置或網路中選取.xlsx或.xls格式的檔案。

   對於[!DNL DoubleClick]和[!DNL Flashtalking]廣告，從廣告伺服器上傳未編輯的標籤表。 對於其他廣告伺服器，請使用您在步驟3中下載的範本。

1. 上傳完成後，按一下&#x200B;**[!UICONTROL Start Building Ads]**。

1. 檢閱每個廣告的詳細資訊和狀態：

   1. 檢閱每個廣告的狀態，此狀態以上傳標籤的驗證檢查為基礎。
   1. （選用）對每個廣告執行下列任一操作：
      * 若要預覽廣告，請按一下廣告列中的![play](/help/dsp/assets/play.png)。
      * 若要編輯廣告詳細資訊，請按一下「![edit](/help/dsp/assets/edit.png)」，編輯詳細資訊，然後按一下「**儲存**」。
      * 若要移除廣告，請按一下廣告列中的&#x200B;**[!UICONTROL X]**。

1. 按一下&#x200B;**[!UICONTROL Create *N *廣告]**。

1. 執行下列任一操作：

   * 按一下 **[!UICONTROL Done]**.

   * (如果廣告遭拒；（可選）要編輯廣告記錄並重新提交廣告以供複查：
      1. 按一下廣告名稱。
      1. 編輯廣告設定。
      1. 按一下 **[!UICONTROL Save & submit for review]**.

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立廣告](ad-create.md)
>* [可用廣告類型](ad-types.md)
>* [廣告規格](/help/dsp/assets/ad-specs.pdf)

