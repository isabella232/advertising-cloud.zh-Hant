---
title: 建立並實作CCPA選擇退出銷售區段
description: 了解如何建立和實作區段，以追蹤使用者ID，使其免受消費者選擇退出銷售的請求影響。
feature: CCPA, DSP Segments
exl-id: aebe0c5b-382f-4e4a-b145-c32f32d216ca
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# 建立並實作CCPA選擇退出銷售區段

您可以根據加州消費者隱私法(CCPA)，建立區段來追蹤使用者ID，使其不受您網站上的消費者選擇退出銷售請求影響。 使用者無限期保留在CCPA選擇退出銷售的區段中。

實作區段像素標籤後，Advertising Cloud將開始代表廣告商收集一組ID。

>[!NOTE]
>
>* 如需如何使用Adobe Experience Platform Privacy Service API將CCPA選擇退出銷售的請求與Advertising Cloud通訊的詳細資訊，請參閱[https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)。
>* 若要追蹤出於與追蹤CCPA選擇退出銷售事件無關的目的而造訪網頁的使用者，以及從案頭、行動裝置和CTV裝置公開至廣告的使用者，請建立[自訂區段](/help/dsp/audiences/custom-segment-create.md)。


1. 建立區段：

   1. 在主功能表中，按一下「**對象>區段**」。

   1. 在資料表上方，按一下&#x200B;**[!UICONTROL Create]**。

   1. 輸入唯一&#x200B;**[!UICONTROL Segment Name]**。

      建議的區段名稱：&quot;&lt;*您的廣告商名稱*> - CCPA選擇退出銷售&quot;（例如&quot;Acme - CCPA選擇退出銷售&quot;）

   1. 對於[!UICONTROL Segment Type]，選擇&#x200B;**[!UICONTROL CCPA Opt-out of sale]**。

   1. 按一下 **[!UICONTROL Save]**.

1. 複製並實作像素標籤以追蹤區段：

   1. 返回&#x200B;**[!UICONTROL Audiences]>[!UICONTROL Segments]**。

   1. 在段行中，將游標停留在新段上，然後按一下&#x200B;**[!UICONTROL Get pixel]**。

   1. 複製影像像素（從`<img src="https://rtd-tm.everesttech.net"`開始），以收集案頭和行動訪客的使用者ID至網頁。

   1. 將標籤提供給廣告商或網站連絡人，以便使用公司用來追蹤CCPA選擇退出銷售請求的機制（例如使用同意管理平台）進行部署。

      廣告商的IT部門或其他群組可能需要排程標籤部署，或接收相關通知。

      實作像素後，Advertising Cloud將開始代表廣告商收集一組ID。

      雖然實作選擇和邏輯取決於廣告商，但以下範例說明廣告商如何引發像素：

      1. 消費者登陸廣告商的首頁。
      1. 消費者找到並點按廣告商的「CCPA選擇退出銷售」按鈕。
      1. 消費者會收到廣告商所使用的服務提供者清單。
      1. 消費者會核取方塊，選擇退出將資料銷售給Adobe Advertising Cloud。

         此動作會觸發像素引發，並在指定的「[!UICONTROL CCPA Opt-out of sale]」區段內收集消費者的Cookie ID。

>[!MORELIKETHIS]
>
>* [Adobe Advertising Cloud支援加州消費者隱私法：消費者選擇退出支援](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)
>* [關於 [!UICONTROL CCPA Opt-out-of-Sale] 區段和報表](ccpa-opt-out-about.md)
>* [擷取消費者選擇退出銷售報表](ccpa-opt-out-segment-report-retrieve.md)
>* [建立和實作自訂區段](custom-segment-create.md)
>* [關於Audience Management](audience-about.md)

