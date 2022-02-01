---
title: 關於Advertising Cloud DSP的受眾管理
description: 瞭解受眾管理功能。
feature: DSP Audiences, DSP Segments
exl-id: 624d2211-59a2-4791-b8f1-a9a5cecd0b8e
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 0%

---

# 關於Advertising Cloud DSP的受眾管理

在Advertising Cloud DSP，您可以建立和管理受眾段和受眾集，並將它們用作您的廣告投放的目標：

* 您可以通過建立和實施段來收集自己的第一方受眾資料。 您以後可以將廣告重新定位到網段中的用戶，或阻止網段中的用戶接收廣告。 可以建立以下類型的段：

   * [自定義段](/help/dsp/audiences/custom-segment-create.md) 跟蹤a)從案頭、移動和CTV設備上接觸廣告的用戶和b)訪問特定網頁的用戶。

   * [CCPA選擇不銷售分部](/help/dsp/audiences/ccpa-opt-out-segment-create.md) 根據《加利福尼亞消費者隱私法》(CCPA)，跟蹤您網站上消費者選擇不可銷售請求的用戶ID。 您可以從選擇退出銷售請求中檢索用戶ID的月度報告。

      有關Advertising Cloud支援CCPA選擇不出售請求的詳細資訊，請參見 [Adobe Advertising Cloud支援加州消費者隱私法：消費者選擇退出支援](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)。

* 您可以建立的 [可重用的受眾](/help/dsp/audiences/reusable-audience-create.md)。 已保存的觀眾由任何可用的觀眾段和任何其他已保存的觀眾組成。 您對已保存受眾所做的任何更改將自動應用於所有目標放置或排除受眾的放置，以及包括已保存受眾的所有其他受眾。

   通過使用複雜布爾邏輯包括和排除多個段，保存的觀眾允許媒體規劃者根據需要對觀眾進行分組。 在構建受眾時，會指示每個段的大小和總受眾大小。 然後，市場活動執行者可以簡單地選擇一個或多個保存的受眾作為投放目標，而不是為每個投放手動配置受眾目標。

此外，還可提供其他受眾類型以進行定位。

## 導入第一方和第三方資料段

Advertising Cloud DSP可以從您的資料管理平台(DMP)中導入您自己的第一方資料段，並根據需要將它們提供給任何一組廣告商。

Advertising Cloud DSP還可以進口定製的第三方分部，包括第三方分部的複雜組合。 您可以根據需要向任何一組廣告商提供這些片段。

聯繫您 [!DNL Adobe] 帳戶團隊以獲取詳細資訊。

## 受眾可用作放置目標

您可以將放置目標定位到以下所有類型的受眾。

* 保存在Advertising Cloud DSP的所有用戶建立的受眾集。

* 在Advertising Cloud DSP建立的所有用戶建立的受眾段：

   * 針對訪問特定網頁的用戶和接觸特定廣告印象的用戶的自定義段。

   * 根據《加利福尼亞消費者隱私法》(CCPA),CCPA針對在您的網站上提交選擇退出銷售請求的用戶選擇退出銷售受眾群。

* 導入的所有第一方資料段。

* 所有導入的自定義第三方資料段。

* （僅針對美國的配售） [從30多家供應商向Advertising Cloud DSP客戶提供的所有第三方資料段](/help/dsp/audiences/third-party-data-providers.md)，包括 [!DNL Acxiom]。 [!DNL Datalogix]。 [!DNL eXelate] ([!DNL Nielsen]) [!DNL Lotame]。 [!DNL Oracle]。 [!DNL Quantcast]，以及更多。

   您可以針對特定的網段，這些網段基於受眾資料（例如，具有特定人口結構、興趣或意圖和/或行為配置檔案的用戶）來針對用戶。 您可以按資料提供程式和類別瀏覽、按名稱或段ID搜索段，或按資料提供程式、總段大小、Web瀏覽器計數或設備計數篩選結果。

   第三方分部產生額外費用，這些費用在每個分部名稱旁邊注明。

* (只使用Advertising CloudJavaScript轉換標籤的Adobe Experience Cloud、Adobe Audience Manager或Adobe Analytics的廣告主)您所有可用的第一、第二或第三方受眾群在Adobe Experience Cloud建立、以Audience Manager建立或通過Audience Manager或發佈到Adobe Experience Cloud [!DNL Analytics]。

   使用分部的定價是預先商定的，在Advertising Cloud不可見。  <!-- Verify -->

   在Adobe Experience Cloud建立或發佈Adobe Experience Cloud的網段大約一小時後即可找到。 直接從Audience Manager獲取的段在建立後24小時左右可用。 <!-- Verify all -->

   >[!NOTE]
   >
   >請參閱文檔 [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html)。 [分析](https://experienceleague.adobe.com/docs/analytics.html), [Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) 有關為這些解決方案中的段設定和收集資料的資訊。

## 受眾大小資料

在已保存的受眾設定和放置設定中，您可以查看詳細的受眾大小資料：

* 將顯示所有選定段和已保存觀眾的總和和活動的消除重複的觀眾大小，您可以按設備類型（瀏覽器、移動或連接的電視）查看詳細資訊。

   ![合計觀眾規模](/help/dsp/assets/audience-size.png)

* 對於單個節和已保存的觀眾，總觀眾大小和CPM（如果適用）顯示在節名旁邊。 您可以查看有關該段的更多詳細資訊，包括按設備類型（瀏覽器、移動或連接的電視）的大小。 對於已保存的受眾，總大小是消除重複的總大小。

   ![單個段大小](/help/dsp/assets/audience-size-segment.png)

## 觀眾觀

### 所有受眾視圖

在 [!UICONTROL All Audiences] 查看或訪問群體庫，您可以保存和管理可重用的訪問群體，這些訪問群體包括一組訪問群體，甚至包括其他已保存的訪問群體。 您可以將受眾用作多個放置的目標。 每個受眾使用的放映次數在放置名稱旁邊指示。

您可以編輯、克隆、刪除、導出或共用任何受眾。

### 段視圖

在 [!UICONTROL Segments] 視圖，所有用戶都可以建立其他自定義段。

的 [!UICONTROL Segments] 視圖還列出了以下段類型：

* 用戶可用的所有用戶建立的自定義段。

   您可以查看您建立的任何自定義段的跟蹤標籤，並與其他用戶共用這些段。 也可以編輯或刪除您建立的自定義段。

   您無法編輯或共用其他用戶已與您共用的自定義段。

* 用戶可用的所有導入的第一方段。

   不能編輯或共用與您共用的第一方段。 聯繫您 [!DNL Adobe] 帳戶團隊（如果您需要與其他用戶共用第一方段）。

* 用戶可用的所有自定義第三方段。

   您無法編輯或共用與您共用的第三方段。 聯繫您 [!DNL Adobe] 客戶團隊（如果您需要與其他用戶共用第三方網段）。

>[!MORELIKETHIS]
>
>* [建立可重用的受眾](reusable-audience-create.md)
>* [受眾設定](audience-settings.md)
>* [受眾段邏輯的語法](audience-segment-logic-syntax.md)
>* [建立和實施自定義段](custom-segment-create.md)
>* [建立和實施 [!UICONTROL CCPA Opt-Out-of-Sale] 段](ccpa-opt-out-segment-create.md)
>* [可用的第三方資料提供程式](third-party-data-providers.md)
>* [放置設定](/help/dsp/campaign-management/placements/placement-settings.md)

