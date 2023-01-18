---
title: 建立並實作CCPA選擇退出銷售區段
description: 了解如何建立和實作區段，以追蹤使用者ID，使其免受消費者選擇退出銷售的請求影響。
feature: CCPA, DSP Segments
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# 建立並實作CCPA選擇退出銷售區段

您可以根據加州消費者隱私法(CCPA)，建立區段來追蹤使用者ID，使其不受您網站上的消費者選擇退出銷售請求影響。 使用者無限期保留在CCPA選擇退出銷售的區段中。

實作區段像素標籤後，Adobe廣告將開始代表廣告商收集一組ID。

>[!NOTE]
>
>* 如需如何使用Adobe Experience Platform Privacy Service API向Adobe廣告傳達CCPA選擇退出銷售請求的相關資訊，請參閱 [https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ccpa-opt-out-of-sale.html).
>* 若要追蹤出於與追蹤CCPA選擇退出銷售事件無關的目的而造訪網頁的使用者，以及透過桌上型電腦、行動裝置和CTV裝置公開廣告的使用者，請建立 [自訂區段](/help/dsp/audiences/custom-segment-create.md).


1. 建立區段：

   1. 在主功能表中，按一下 **受眾>區段**.

   1. 在資料表格上方，按一下 **[!UICONTROL Create]**.

   1. 輸入唯一 **[!UICONTROL Segment Name]**.

      建議的區段名稱：&quot;&lt;*您的廣告商名稱*> - CCPA選擇退出銷售」（例如「Acme - CCPA選擇退出銷售」）

   1. 若 [!UICONTROL Segment Type]，選取 **[!UICONTROL CCPA Opt-out of sale]**.

   1. 按一下 **[!UICONTROL Save]**.

1. 複製並實作像素標籤以追蹤區段：

   1. 返回 **[!UICONTROL Audiences]>[!UICONTROL Segments]**.

   1. 在區段列中，將游標停留在新區段上，然後按一下 **[!UICONTROL Get pixel]**.

   1. 複製影像像素(從 `<img src="https://rtd-tm.everesttech.net"`)，收集網頁案頭和行動訪客的使用者ID。

   1. 將標籤提供給廣告商或網站連絡人，以便使用公司用來追蹤CCPA選擇退出銷售請求的機制（例如使用同意管理平台）進行部署。

      廣告商的IT部門或其他群組可能需要排程標籤部署，或接收相關通知。

      實作像素後，Adobe廣告將開始代表廣告商收集一組ID。

      雖然實作選擇和邏輯取決於廣告商，但以下範例說明廣告商如何引發像素：

      1. 消費者登陸廣告商的首頁。
      1. 消費者找到並點按廣告商的「CCPA選擇退出銷售」按鈕。
      1. 消費者會收到廣告商所使用的服務提供者清單。
      1. 消費者會核取方塊，選擇退出向Adobe廣告銷售資料。

         此動作會觸發像素，並在指定的「[!UICONTROL CCPA Opt-out of sale]」區段。

>[!MORELIKETHIS]
>
>* [加州消費者隱私法的Adobe廣告支援：消費者選擇退出支援](/help/privacy/ccpa-opt-out-of-sale.md)
>* [關於 [!UICONTROL CCPA Opt-out-of-Sale] 區段與報表](ccpa-opt-out-about.md)
>* [擷取消費者選擇退出銷售報表](ccpa-opt-out-segment-report-retrieve.md)
>* [建立和實作自訂區段](custom-segment-create.md)
>* [關於Audience Management](audience-about.md)

