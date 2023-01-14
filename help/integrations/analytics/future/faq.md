---
title: 常見問題集
description: xx
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# 常見問題集xxx

## 標題

https://adobeadcloud.zendesk.com/agent/tickets/14214依預設，Adobe Analytics會報告每個報表中所有擷取的事件。 &quot;[!UICONTROL Unspecified]「事件代表未連線至Adobe廣告的表單完成事件。 例如，在「廣告平台」報表中，電子郵件促銷活動所驅動的自然轉換或轉換會歸入「未指定」。

您可以透過「包含未指定（無）」選項移除勾號，使用篩選器來從報表中移除未指定事件。 <!-- Not sure if this is in DSP or in Analytics Workspace -->

## 標題

https://adobeadcloud.zendesk.com/agent/tickets/24323將Analytics事件標籤放置在與Ad Cloud像素相同的位置，以確保XXX相符。

## 標題

https://adobeadcloud.zendesk.com/agent/tickets/24323

問：在內部安全性稽核期間，我們將Ad Cloud整合至現有Adobe Analytics安裝時，會將某些功能標示為安全性疑慮。

相關整合位於AdCloud和Adobe Audience Manager之間。 此功能可提高AdCloud和Adobe Audience Manager之間訪客ID的匹配率。 它會將網路要求傳送至pagead.l.doubleclick.net、star-mini.c10r.facebook.com和pug88000nf.pubmatic.com，以判斷這些服務是否有可供運用的訪客現有ID。 這些網路請求已標示為安全風險，且會發生於所有網站訪客。

我們的稽核員要求我們停用此功能。 如果我們封鎖這些網路請求，會發生什麼事？

答：我們已與產品核對，他們提到相關像素的用途是提高Ad Cloud、特定詳細目錄/SSP合作夥伴(針對DSP)和AAM之間的Cookie匹配率。  如果移除這些像素，客戶可能會看到AAC/AAM與庫存合作夥伴（各自像素用於）之間的匹配率有所降低，但他們不認為會大幅降低。

針對Ad Cloud搜尋，我們確實會看到廣告商的Experience Cloud組織ID已針對Mathworks設定，但我們的產品團隊沒有看見Mathworks設定以在Ad Cloud中啟用對象。 您是否使用AdobeAudience Manager將受眾傳送至Ad Cloud搜尋？ 如果沒有，移除這些項目將不會影響目前的工作流程。 AAM若您不想引發這些像素，客戶服務可協助您移除這些像素。

