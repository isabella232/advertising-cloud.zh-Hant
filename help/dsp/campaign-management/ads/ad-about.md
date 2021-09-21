---
title: 關於Advertising Cloud DSP中的廣告管理
description: 了解廣告管理。
feature: DSP Ads
exl-id: 72c8bbef-d09c-4cf4-994d-99578d043d39
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# 關於Advertising Cloud DSP中的廣告管理

<!-- add "The Ads View (Dashboard?)" section -->

Advertising Cloud DSP提供兩種提供廣告的方式：

* 當您將自己的資產（例如顯示橫幅、視訊資產、音訊檔案或URL）直接上傳至DSP時，Advertising Cloud DSP會免費提供您的廣告。 若為DSP提供的資產，您可以存取其他功能，例如覆蓋。

* 如果您使用協力廠商廣告伺服器（例如Google、Flashtalking或Sizmek），則可將您的協力廠商廣告服務標籤個別或大量上傳至DSP。 大量上傳功能需要您a)上傳DoubleClick和Flashtalking標籤表，或b)下載範本，將標籤輸入範本，然後重新上傳範本。<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

設定廣告後，您需要將每個廣告附加至版位，其中包括將控制促銷活動傳送方式的定位參數（例如地理、對象、裝置和庫存目標）。 您可以將單一廣告附加至一或多個版位。

## 可用廣告類型

* 音訊
* 連接電視
* 顯示
* 行動
* 原生
* 前段

如需這些廣告類型的詳細資訊，請參閱[可用廣告類型](ad-types.md)和完整的[廣告規格](/help/dsp/assets/ad-specs.pdf)。

## 特殊廣告功能

下列功能僅適用於DSP提供的廣告。

### 隨附橫幅

隨附橫幅會與[前段廣告](ad-settings-pre-roll.md)或（與部分發佈者）[音訊廣告](ad-settings-audio.md)搭配提供，並有助於加強品牌與訊息的關聯。

>[!NOTE]
>
>* 並非所有發佈商都允許隨附橫幅廣告。 允許隨附橫幅的發行者無法保證隨附橫幅曝光次數。
>* 來自協力廠商廣告標籤的隨附橫幅可能不一定會可供預覽。


您可以上傳自己的隨附橫幅資產，或從經認證的第三方廣告服務合作夥伴上傳第三方iFrame或指令碼橫幅標籤。

### 覆蓋

覆蓋可協助您在整個視訊中持續建立品牌，並可帶來額外的點按次數。 覆蓋功能適用於[互動式前段廣告](ad-settings-pre-roll.md)和[互動式和點播播放格式的行動廣告](ad-settings-mobile.md)。

請參閱[設計覆蓋的最佳作法](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)

### 茶匙

預告是吸引觀眾播放廣告的引人注目的影像。 預告器僅適用於行動點選播放廣告格式。

## Advertising Cloud DSP廣告核准

建立廣告時，Advertising Cloud DSP會檢視其是否有敏感類別、按一下URL功能，以及預覽呈現。

一開始，您會在[!UICONTROL Status]欄中看到紅點。 審查過程通常需要24到48小時。 但是，中斷的廣告的擱置狀態可能超過48小時，因此您有時間在廣告遭拒絕前修正錯誤。 拒絕的廣告包含拒絕的原因。

DSP核准廣告時，「狀態」欄中會出現綠色圓點。

![欄中的核准 [!UICONTROL Status] 指標](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>只有DSP和SSP都核准創作內容時，才會提供您的廣告。 每個SSP都有自己的核准要求和程式。

>[!MORELIKETHIS]
>
>* [建立廣告](ad-create.md)
>* [建立多個第三方廣告](ad-create-third-party.md)
>* [可用廣告類型](ad-types.md)
>* [廣告規格](/help/dsp/assets/ad-specs.pdf)

