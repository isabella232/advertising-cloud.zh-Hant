---
title: 附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Google Campaign Manager 360] 廣告標籤
description: 了解新增原因及方式 [!DNL Analytics for Advertising] 巨集 [!DNL Google Campaign Manager 360] 廣告標籤
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# 附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Google Campaign Manager 360] 廣告標籤

*廣告商與Adobe廣告 — 僅Adobe Analytics整合*

*僅適用於Advertising DSP*

如果您使用來自 [!DNL Google Campaign Manager 360] 針對您的Advertising DSP廣告，附加 [!DNL Analytics for Advertising] 參數至您的登錄頁面URL，使用 [`%p` 宏](https://support.google.com/campaignmanager/table/6096962). 參數記錄 `s_kwcid` 和 `ef_id` 登錄頁面URL中的查詢字串參數，讓Adobe廣告可將廣告的點按資料傳送至Adobe Analytics。

使用宏 [!DNL Campaign Manager 360] 顯示廣告和視訊廣告，適用於下列類型 [!DNL Analytics for Advertising] 實作：

* **廣告商與 [!DNL Adobe] [!DNL Analytics for Advertising] 在其網站上實作的JavaScript程式碼**:JavaScript程式碼已記錄 `s_kwcid` 和 `ef_id` 查詢字串參數。 不過，使用巨集會延伸追蹤功能，在不支援第三方Cookie時納入點擊式轉換。 最佳實務是將下列區段中的巨集新增至您的廣告標籤，以擷取未透過JavaScript程式碼擷取的其他點進資料。

>[!NOTE]
>
>JavaScript程式碼是只有在Cookie仍可用時，才能用於點擊追蹤的解決方案。 Cookie停止後，就需要實作下列巨集。

* **網站不使用 [!DNL Analytics for Advertising] JavaScript程式碼，而是依賴 [!DNL Analytics] 僅限點進資料的伺服器端轉送** （不含任何閱覽資料）:若要報告從您透過Adobe廣告購買的廣告所驅動的站上點按活動，需要下列巨集。

## 將巨集附加至 [!DNL Google Campaign Manager 360] 廣告

內 [!DNL Google Campaign Manager 360]，會將下列參數附加至每個顯示與視訊廣告的登陸頁面URL: `%pamo=!;`

您可以透過數種方式指定登錄頁面URL。 下列子節將說明各選項。

以下是尾碼格式化的登錄頁面URL範例。

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>
>* 如果登錄頁面URL包含非常常見的雜湊符號(#)，請放置 `amo` 參數。
>* 若 `amo` 參數，然後在其後新增參數（例如&amp;a=b）。 範例：`https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`


### 設定廣告商層級登錄頁面URL尾碼

1. 請參閱 [開啟廣告商屬性的指示](https://support.google.com/campaignmanager/answer/2829344).
1. 在 [!UICONTROL Landing page URL suffix] 設定，包括 `%pamo!;` 在 [!UICONTROL URL suffix] 欄位。

### 設定促銷活動層級登錄頁面URL尾碼

1. 請參閱 [開啟促銷活動屬性的指示](https://support.google.com/campaignmanager/answer/2838056#set).
1. 在 [!UICONTROL Landing page URL suffix] 設定，包括 `%pamo!;` 在 [!UICONTROL URL suffix] 欄位。

### 設定創作層級登陸頁面URL尾碼

1. 開啟創作屬性。
1. 在 [!UICONTROL Click tags] 設定，包括 `%pamo!;` 在 [!UICONTROL Landing page] 欄。

## 如何 [!DNL Analytics for Advertising] 巨集在DSP中展開

在DSP中，當您建立包含 [!DNL Analytics for Advertising] 參數(`amo`), `ef_id` 和 `s_kwcid` 巨集會自動附加至點按URL。 最佳實務是檢查DSP中的標籤，以確保 `ef_id` 和 `s_kwcid` 宏存在。

以下是 [!DNL Google Campaign Manager 360] [ins標籤](https://support.google.com/campaignmanager/answer/6080468) 如DSP中所示。

```
<ins class='dcmads' style='display:inline-block;width:160px;height:600px'
data-dcm-placement='N6482.2155306TUBEMOGUL/B23486129.261313631'
data-dcm-rendering-mode='iframe'
data-dcm-https-only
data-dcm-resettable-device-id=''
data-dcm-app-id='' data-dcm-click-tracker='${TM_CLICK_URL}'
data-dcm-param-amo='ef_id=${TM_USER_ID}:${TM_DATETIME}:d&s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}'>
<script src='https://www.googletagservices.com/dcm/dcmads.js'></script>
</ins>
```

當使用者點按廣告時， [!DNL Google Campaign Manager 360] sees `%pamo` 並動態插入 `amo` 參數。

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising]](overview.md)
>* [Adobe廣告ID：使用者 [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [附加 [!DNL Analytics for Advertising] 巨集至 [!DNL Flashtalking] 廣告標籤](macros-flashtalking.md)

