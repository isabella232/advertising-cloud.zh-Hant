---
title: 關於Advertising Cloud DSP的廣告管理
description: 瞭解廣告管理。
feature: DSP Ads
exl-id: 72c8bbef-d09c-4cf4-994d-99578d043d39
source-git-commit: ff0e153344f8245ff217cc8b2b276184dd7422b5
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 0%

---

# 關於Advertising Cloud DSP的廣告管理

<!-- add "The Ads View (Dashboard?)" section -->

Advertising Cloud DSP支援通過第三方廣告服務標籤(如Google、Flashtalk或Sizmek)為各種廣告類型提供廣告交付，並支援直接資產上傳為本地顯示廣告。 您可以單獨或批量上載第三方標籤。 批量上載使用夥伴標籤工作表或批量標籤模板。

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

設定廣告後，您需要將每個廣告附加到廣告位置，其中包括目標參數（如地域、受眾、設備和庫存目標），這些參數將控制您的活動將如何進行。 可以將單個廣告附加到一個或多個放置位置。

## 可用廣告類型 {#ad-types}

以下所有廣告類型均可在Advertising Cloud DSP提供。 有關每種廣告類型的完整規範，請參見 [廣告規格](/help/dsp/assets/ad-specs.pdf)。

* **音頻廣告（僅限第三方）**:音頻廣告在數字發行商網站上的內容之間播放，可以單獨作為音頻檔案或隨伴橫幅運行。 音頻最適合用於提升品牌知名度，並與移動觀眾互動。 音頻的主要效能指標包括 [!UICONTROL Completion Rate] 和 [!UICONTROL Cost per Completion]。

* **顯示廣告（僅限第三方）**:顯示廣告是在Web瀏覽器或應用中顯示的動畫或靜態影像。 按一下廣告單元將用戶帶到品牌網站或微網站。 Display最適合用於推動高效的CPM、增加消息關聯、添加附加品牌或產品觸點，以及推動用戶沿著購買渠道前進。 用於顯示的關鍵績效指標包括 [!UICONTROL Clicks]。 [!UICONTROL Cost per Click]。 [!UICONTROL Conversions], [!UICONTROL Cost per Conversion]。 支DSP持多種顯示橫幅廣告大小。

* **Mobile廣告（僅限第三方）**:Mobile廣告可以採用預卷視頻(VAST, MRAID)或標準顯示格式。 Mobile預卷視頻可以自動播放或點擊播放，最適合在螢幕上接觸觀眾。 Mobile標準顯示器是在移動網路瀏覽器或應用中顯示的靜態影像，最適合用於補充數字視頻購買、推動消息關聯，以及添加附加品牌或產品觸點。 Mobile的廣告還可以充當全屏收購或移動間隙，它們是全屏、高影響力的移動廣告，最適合用於培養移動受眾的品牌知名度和驅動器轉換。

* **本機顯示廣告（僅限第一方）**:標準顯示格式支援本機廣告。 本地廣告包括標題和/或標題、說明、徽標和影像。 廣告元素被組合和渲染以匹配發佈者的頁面樣式，以便廣告與發佈者的有機內容融合，並推動更高的參與。 Native最適合用於品牌知名度以及通過方便觀眾的廣告來推動觀眾觀看和參與率。 主要業績指標包括 [!UICONTROL Clicks]。 [!UICONTROL Cost Per Click]。 [!UICONTROL Conversions], [!UICONTROL Cost Per Conversion]。

* **預卷廣告（僅限第三方）**:預卷廣告（VAST和VPAID）在高級視頻內容之前顯示，並提供身臨其境、引人入勝的觀眾體驗。 預卷視頻可以是互動式的，包含富媒體功能，包括疊加、滾轉和動作呼叫。 預卷視頻廣告的關鍵效能指標包括 [!UICONTROL Video Completion Rate] 和 [!UICONTROL Viewability Rate]。

* **已連接電視廣告（僅限第三方）**:在高級電視視頻內容之前和期間顯示連接的電視廣告。 所有連接的電視清單都運行在電視設備上，這意味著視頻在觀看者無法跳過的瘦後全屏環境中自動播放。 連接電視是最接近電視廣告的數字視頻格式。 連接電視的主要效能指標包括 [!UICONTROL Completion Rate]。

## Advertising Cloud DSP廣告批准

建立廣告時，Advertising Cloud DSP會查看其敏感類別，按一下URL功能，然後預覽呈現。

最初，你會看到 [!UICONTROL Status] 的雙曲餘切值。 審查過程通常需要24-48小時。 但是，中斷的廣告可能具有超過48小時的掛起狀態，因此您有時間在廣告被拒絕之前修復錯誤。 被拒絕的廣告包括拒絕的理由。

批DSP準廣告後，「狀態」(Status)列中將顯示一個綠點。

![批准指示符 [!UICONTROL Status] 列](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>只有雙方和SSP都批准DSP了創意，您的廣告才會送達。 每個SSP都有自己的批准要求和流程。

>[!MORELIKETHIS]
>
>* [建立單個廣告](ad-create.md)
>* [建立多個第三方廣告](ad-create-multiple.md)
>* [廣告規格](/help/dsp/assets/ad-specs.pdf)

