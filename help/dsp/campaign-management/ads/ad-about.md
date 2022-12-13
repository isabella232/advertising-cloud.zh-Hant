---
title: 關於Advertising Cloud DSP中的廣告管理
description: 了解廣告管理。
feature: DSP Ads
exl-id: 72c8bbef-d09c-4cf4-994d-99578d043d39
source-git-commit: 1499d9d86d8c2bafb03b41687c50dbf708c715da
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 0%

---

# 關於Advertising Cloud DSP中的廣告管理

<!-- add "The Ads View (Dashboard?)" section -->

Advertising Cloud DSP支援透過協力廠商廣告服務標籤(例如Google、Flashtalking或Sizmek)，針對各種廣告類型支援廣告傳送，並可針對原生顯示廣告直接上傳資產。 您可以個別或大量上傳協力廠商標籤。 大量上傳使用合作夥伴標籤表或大量標籤範本。

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

設定廣告後，您需要將每個廣告附加至版位，其中包括將控制促銷活動傳送方式的定位參數（例如地理、對象、裝置和庫存目標）。 您可以將單一廣告附加至一或多個版位。

## 可用廣告類型 {#ad-types}

下列所有廣告類型皆可在Advertising Cloud DSP中使用。 如需每種廣告類型的完整規格，請參閱 [廣告規格](ad-specs.md).

* **音訊廣告（僅限第三方）**:音訊廣告可在數位發行者網站上的內容之間播放，且可以獨立以音訊檔案或隨附橫幅執行。 音訊最適合用來提升品牌知名度，並與隨選受眾互動。 音頻的關鍵效能指標包括 [!UICONTROL Completion Rate] 和 [!UICONTROL Cost per Completion].

* **顯示廣告（僅限第三方）**:顯示廣告是顯示在網頁瀏覽器或應用程式中的動畫或靜態影像。 按一下廣告單元會將使用者帶往品牌網站或微網站。 「顯示」最適合用來促進有效的CPM、增加訊息關聯、新增其他品牌或產品接觸點，以及將使用者帶往購買漏斗。 顯示的關鍵績效指標包括 [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions]，和 [!UICONTROL Cost per Conversion]. DSP支援多種顯示橫幅廣告大小。

* **行動廣告（僅限第三方）**:行動廣告可採用前段視訊(VAST、MRAID)或標準顯示格式。 行動前段視訊可以自動播放或點按播放，最適合用來觸及各螢幕的檢視者。 行動標準顯示是顯示在行動網頁瀏覽器或應用程式中的靜態影像，最適合用來補充數位視訊購買、促進訊息關聯，以及新增其他品牌或產品接觸點。 行動廣告也可以作為全螢幕收購或行動插入式廣告運作，這些為全螢幕、高影響力的行動廣告，最適合用來開發行動受眾的品牌認知度並促進轉換。

* **原生顯示廣告（僅限第一方）**:標準顯示格式支援原生廣告。 原生廣告包括標題和/或標題、說明、標誌和影像。 廣告元素會結合併轉譯，以符合發佈商的頁面樣式，讓廣告與發佈商的自然內容混合，並促進更高的參與度。 Native最適合用於品牌認知度，以及透過適合檢視者的廣告來提升受眾檢視和參與率。 關鍵業績指標包括 [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions]，和 [!UICONTROL Cost Per Conversion].

* **前段廣告（僅限第三方）**:前段廣告（VAST和VPAID）會在優質視訊內容之前顯示，提供身臨其境、吸引觀眾的體驗。 前段視訊可以是互動式視訊，包含多媒體功能，並包含覆蓋、變換和動作呼叫。 前段視訊廣告的關鍵績效指標包括 [!UICONTROL Video Completion Rate] 和 [!UICONTROL Viewability Rate].

* **連線電視廣告（僅限第三方）**:連接的電視廣告在付費電視視頻內容之前和期間顯示。 所有連接的電視清單都運行在電視設備上，這意味著視頻在觀看者無法跳過的向後全屏環境中自動播放。 連線電視是最接近電視廣告的數位視訊格式。 連接電視的關鍵效能指標包括 [!UICONTROL Completion Rate].

* **通用視訊廣告（僅限第三方）**:通用視訊廣告將連線電視、前段和行動前段廣告（VAST和VPAID）的所有功能結合為一，並在視訊內容之前和期間顯示。 從案頭、行動裝置及連線電視環境定位視訊詳細目錄時，可使用通用視訊廣告，因此可避免建立多個視訊廣告的需求。 通用視訊的關鍵績效指標包括 [!UICONTROL Completion Rate] 和 [!UICONTROL Viewability Rate].

## Advertising Cloud DSP廣告核准

建立廣告時，Advertising Cloud DSP會檢視其是否有敏感類別、按一下URL功能，以及預覽呈現。

一開始，您會在 [!UICONTROL Status] 欄。 審查過程通常需要24到48小時。 但是，中斷的廣告的擱置狀態可能超過48小時，因此您有時間在廣告遭拒絕前修正錯誤。 拒絕的廣告包含拒絕的原因。

DSP核准廣告時，「狀態」欄中會出現綠色圓點。

![核准指標 [!UICONTROL Status] 欄](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>只有DSP和SSP都核准創作內容時，才會提供您的廣告。 每個SSP都有自己的核准要求和程式。

>[!MORELIKETHIS]
>
>* [建立單一廣告](ad-create.md)
>* [建立多個第三方廣告](ad-create-multiple.md)
>* [廣告規格](ad-specs.md)

