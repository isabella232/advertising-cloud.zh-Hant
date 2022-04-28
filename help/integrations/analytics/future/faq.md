---
title: 常見問題
description: xx
source-git-commit: 2e0395dc1e5aa52adc83c1aaea49793fd5555390
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# 常見問題解答xxx

## 標題

https://adobeadcloud.zendesk.com/agent/tickets/14214預設情況下，Adobe Analytics會報告每個報告中捕獲的所有事件。 &quot;[!UICONTROL Unspecified]&quot;事件代表未與Advertising Cloud聯繫的表格完成事件。 例如，在廣告平台報告中，由電子郵件活動驅動的有機轉換或轉換將歸為「未指定」。

通過「包括未指定（無）」選項刪除複選標籤，可以使用篩選器從報告中刪除未指定的事件。 <!-- Not sure if this is in DSP or in Analytics Workspace -->

## 標題

https://adobeadcloud.zendesk.com/agent/tickets/24323將Analytics事件標籤置於與Ad Cloud像素相同的位置，以確保XXX匹配。

## 標題

https://adobeadcloud.zendesk.com/agent/tickets/24323

問：在內部安全審計過程中，某些功能被標籤為安全問題，當我們將Ad Cloud整合到現有Adobe Analytics安裝中時，就啟用了這些功能。

所討論的整合是AdCloud和Adobe Audience Manager之間。 此功能可提高AdCloud和Adobe Audience Manager之間訪問者ID的匹配率。 它通過將網路請求發送到pagead.l.doubleclick.net、star-mini.c10r.facebook.com和pug88000nf.pubmatic.com來確定這些服務是否具有可用於訪問者的現有ID。 這些網路請求已被標籤為安全風險，並且發生於所有站點訪問者。

我們的審計員要求我們禁用此功能。 如果我們阻止這些網路請求會發生什麼？

答：我們查閱了我們的產品，他們提到，所涉像素的目的是提高Ad Cloud、特定庫存/SSP合作夥伴(在DSP這方面)和之間的Cookie匹配率AAM。  如果刪除它們，客戶可能會看到AAC/AAM和庫存合作夥伴之間的匹配率有所降低，但他們不會認為匹配率會很大。

對於Ad Cloud搜索，我們確實看到廣告商的Experience Cloud組織ID已設定為Mathworks，但我們的產品團隊看不到Mathworks設定以激活Ad Cloud觀眾。 是否使用Adobe受眾經理將受眾發送到Ad Cloud搜索？ 否則，刪除這些內容不會影響當前工作流。 如AAM果您不希望解雇這些像素，「客戶保護」可以幫助刪除這些像素。

