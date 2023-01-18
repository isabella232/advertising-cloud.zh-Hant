---
title: 廣告規格
description: 參考一般和發佈商專屬的廣告規格。
feature: DSP Ads
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# 支援廣告類型的規格

## 視訊廣告（前段、CTV和通用視訊）

### 支援的畫面

廣告預設會在桌上型電腦、行動裝置和連線電視裝置上傳送。 裝置鎖定目標可用於調整傳送。

### 支援的第三方廣告伺服器

您可以使用 [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]，和 [!DNL Sizmek]. 如需支援廠商的完整清單，請參閱[認證廣告服務合作夥伴](certified-ad-servers.md).&quot;

### 高清視訊資產需求（必要）

**視訊標籤類型：** VPAID 2.0 JavaScript或VAST(CTV)。 所有VPAID廣告單位都必須遵循 [VPAID 2.0規範](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf) 由互動廣告局(IAB)所定義。

**視頻編解碼器：** MP4/H.264

**解決方法：** 720p為1280x720,1080p為1920x1080

**位元速率：** 720p為1500-2500 kbps,1080p為2500-3500 kbps

**H.264配置檔案/級別：** 高調，720便士的3.1級；高調，1080p的4.0級

**視訊影格速率：** NTSC國家/地區為29.970 fps（通常稱為30 fps）,PAL國家/地區為25 fps，膠片外觀內容為23.976 fps（通常稱為24 fps）

**視訊色域：** 4:2:0 YUV色度子採樣

**視頻交錯：** 逐行掃描，即非隔行掃描。 無場內運動（混合幀）或交錯。

**領導人(Slate):** 不允許

**音頻編解碼器：** AAC-LC或HE-AACv1

**音訊位元速率：** AAC-LC為128-192 kbps,HE-AACv1為64-128 kbps

**音頻通道：** 2聲道立體混音

**音頻採樣率：** 44.1 kHz或48 kHz，作為每個源材料

**音頻級別：** 根據ATSC A/85，美國的24個LKFS(+/- 2.0 dB);根據EBU R128，歐盟內23個LUF(+/- 1.0)

#### 連線電視廣告的其他發佈者需求

* **A+E網路：** 請參閱A+E網路的 [廣告規格](/help/dsp/assets/a-e-networks-tve-video-ad-specs.pdf)

* **發現：** 請參閱Discovery的 [廣告規格](/help/dsp/assets/discovery-networks-ad-specs.pdf).

* **迪士尼(包括 斛律):** 請參閱Disney&#39;s [廣告規格](https://hulu.disneyadsales.com/ad-products/video-commercial/).

* **HBO Max:** 觀看HBO Max的 [廣告規格](/help/dsp/assets/hbo-max-ad-specs-2022.xlsx).

* **NBCUniversal:**

   * [數位視訊](https://together.nbcuni.com/nbcu-creative-guidelines/digital-video/)

   * [Livestream](https://together.nbcuni.com/nbcu-creative-guidelines/livestream/)

   * [孔雀](https://together.nbcuni.com/nbcu-creative-guidelines/peacock/)

* **派拉蒙：** 請參閱Paramoun的 [廣告規格](https://www.paramount.com/digital-ads).

## 顯示廣告

### 支援的畫面

廣告預設會在桌上型電腦和行動裝置上傳送。 裝置鎖定目標可用於調整傳送。

### 支援的檔案類型

**影像：** GIF、JPG/JPEG、PNG

**HTML5:** 影像檔案類型：GIF,JPG/JPEG, PNG,SVG

### 影像資產需求（必要）

支援通用顯示。

**建議的廣告大小：** 120x60、160x600、180x150、300x50、300x100、300x1050、300x250、300x600、320x50、320x480、480x60、400x40888x31、728x90、970x250、970x90

**支援的第三方廣告伺服器：** 您可以使用 [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]，和 [!DNL Sizmek]. 如需支援廠商的完整清單，請參閱[認證廣告服務合作夥伴](certified-ad-servers.md).&quot;

## 音訊廣告

### 支援的畫面

台式機、移動設備、平板電腦、智慧揚聲器和連接電視

### 支援的第三方廣告伺服器

您可以使用 [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]，和 [!DNL Sizmek]. 如需支援廠商的完整清單，請參閱[認證廣告服務合作夥伴](certified-ad-servers.md).&quot;

### 音訊資產需求（必要）

**檔案類型：** MP3、OGG、AAC

**領導人（石板）:**  不允許

**最大檔案大小：** 2MB

**位元速率：** 128

**檔案長度：** 0-60年代

#### 其他發佈者需求

* **[!DNL iHeartRadio]**
   * 長度：5、15、30或60秒
   * 檔案類型：MP3
   * 最大檔案大小：320 kbps
   * 卷：44.1千赫

* **[!DNL Pandora]**
   * 長度：15或30秒
   * 檔案類型：MP4（應用程式內）、MP3（案頭）
   * 最大檔案大小：2.2 MB

* **[!DNL SoundCloud]**
   * 長度：6、15或30秒
   * 檔案類型：MP3
   * 最大檔案大小：5 MB

* **[!DNL Spotify]**
   * 長度：最多30秒
   * 檔案類型：OGG
   * 最大檔案大小：500MB
   * 卷：RMS歸一化為–14;dBFS峰歸一化為–0.2 dBFS

* **[!DNL TargetSpot]**
   * 長度：15、30或60秒
   * 檔案類型：MP3

* **[!DNL TuneIn]**
   * 長度：10、15或30秒
   * 檔案類型：MP3, OGG
   * 卷：44.1千赫

### 隨附橫幅廣告的需求（選用）

**支援的大小：** 300x250、500x500、640x640、1024x1024

#### 其他發佈者需求

* **[!DNL iHeartRadio]:**
   * 檔案類型：JPEG,JPG, PNG,GIF,SWF,HTML
   * 最大檔案大小：2.2 MB
   * Dimension:300x250

* **[!DNL Pandora]:**
   * 檔案類型：JPEG,GIF
   * 最大檔案大小：大小：100 KB
   * Dimension:300x250（行動或案頭）或500x500（案頭）

* **[!DNL SoundCloud]:**
   * 檔案類型：靜態JPG, PNG
   * 最大檔案大小：400 KB以下
   * Dimension:1024x1024

* **[!DNL Spotify]:**
   * 檔案類型：靜態JPG, PNG
   * 最大檔案大小：200 KB
   * Dimension:300x250

* **[!DNL TuneIn]:**
   * 檔案類型：JPEG,JPG, PNG,GIF,HTML
   * 最大檔案大小：2 MB
   * Dimension:300x250
 

## 原生顯示廣告

每個廣告可以包括靜止影像或移動GIF（電影）。

### 支援的畫面

廣告預設會在桌上型電腦和行動裝置上傳送。 裝置鎖定目標可用於調整傳送。

### 所有原生In-Feed格式的必要資產

#### 影像資產

**解決方法：** 至少600x600px;建議最小為1200x627px

**檔案類型：** JPEG（影像廣告或視訊廣告封面影像）、GIF（電影）

**檔案大小：** 小於1 MB（影像應不含文字）。

#### 廣告商標誌

**解決方法：** 至少80x80px;建議的最小值為300x300px

**檔案類型：** JPEG或PNG。

**外觀比例：**  1x1比率

>[!NOTE]
>
>視重疊的影像而定，可在淺或深標誌資產之間進行選擇。

#### 文字/複製

**標題：** 最多200個字元；建議使用25個字元

**註解：** 最多200個字元；建議使用100個字元

**贊助者：** 最多200個字元；建議使用30個字元

**動作呼叫（僅限MoPub）:** 最多15個字元

>[!NOTE]
>
>最終版面由發佈者在執行階段定義。 如果廣告超過建議的字元數，某些詳細目錄提供者可能不會傳送廣告，否則發佈者或SSP可能會截斷文字。

#### 登陸頁面URL

具有選用點按追蹤的點進URL。

點按追蹤的需求：

* 第三方曝光追蹤像素：僅1x1影像URL格式

* 可檢視性JavaScript追蹤器：僅支援IAS;僅限JS.append格式的1x1影像

* 第三方點擊追蹤像素：必須重新導向至內嵌於URL中的登錄頁面（HTTP 302重新導向）

* 不支援具有200個或更多回應的點按追蹤平台(DMP)。

>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立單一廣告](ad-create.md)
>* [建立多個第三方廣告](ad-create-multiple.md)
>* [編輯廣告](ad-edit.md)

