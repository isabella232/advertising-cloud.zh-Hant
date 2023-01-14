---
title: Adobe加州消費者隱私法的廣告支援：消費者選擇退出銷售支援
description: 了解擷取消費者選擇退出銷售請求的支援。
feature: CCPA
exl-id: 2c0cd4f5-798f-479a-99cd-f555cd676766
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 0%

---

# 加州消費者隱私法的Adobe廣告支援：消費者選擇退出銷售支援

*針對Adobe廣告Demand Side Platform(DSP)*

>[!IMPORTANT]
>
>本檔案的內容不是法律建議，且用意並非要取代法律建議。 如需加州消費者隱私法的相關建議，請諮詢法律顧問。

加州消費者隱私法(CCPA)是加州新的隱私權法，自2020年1月1日起生效。 CCPA為加州居民提供新的個人資訊權利，並對在加州經營業務的特定實體賦予資料保護責任。 CCPA讓消費者有權存取和刪除其資料，也有權選擇退出某些符合「銷售」第三方個人資訊資格的活動。

身為企業，您將決定要由Adobe Experience Cloud代表您處理和儲存的個人資料。

身為您的服務提供者，Adobe廣告可支援您的企業履行CCPA所規定的義務，這些義務適用於Adobe廣告產品和服務的使用，包括管理消費者存取和刪除個人資訊的請求，以及管理消費者選擇退出個人資訊銷售的請求。

本檔案說明Adobe廣告Demand Side Platform(DSP)身為服務提供者，如何支援消費者選擇退出「個人資訊」的「銷售」權限，因為CCPA已定義每個詞語。 其中包含如何向Advertising傳達退出銷售請求，以及如何擷取貴組織退出銷售請求報表的資訊。

如需如何 [!DNL Advertising Search];廣告創意；和 [!DNL Advertising DCO] 支援消費者的個人資訊存取和刪除權限，請參閱 [加州消費者隱私法的Adobe廣告支援：消費者資料存取和刪除支援](/help/privacy/ad-cloud-ccpa-access-delete.md).

如需CCPAAdobe隱私權服務的詳細資訊，請參閱 [Adobe隱私中心](https://www.adobe.com/privacy/ccpa.html).

## 將消費者選擇退出銷售的請求傳達給Adobe廣告

您可以使用下列任一項，傳達消費者選擇退出銷售的請求：

* 在Advertising DSP中建立的CCPA選擇退出銷售區段
* Adobe Experience Platform Privacy Service API

### 方法1:使用傳達CCPA選擇退出銷售的請求 [!UICONTROL CCPA Opt-Out-of-Sale] Advertising DSP中的區段

>[!NOTE]
>
>使用者無限期保留在CCPA選擇退出銷售的區段中。

1. 登入廣告商的帳戶(位於 [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [建立CCPA選擇退出銷售區段，並實作區段像素以擷取選擇退出請求](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### 方法2:使用Adobe Experience Platform Privacy Service API傳達CCPA選擇退出銷售的要求

*廣告商僅指派Adobe Experience Cloud組織ID*

1. 部署JavaScript程式庫以擷取客戶的Cookie。 同一個圖書館， `AdobePrivacy.js`，會用於所有Adobe Experience Cloud解決方案。

   >[!IMPORTANT]
   >
   >對某些Adobe Experience Cloud解決方案的請求不需要JavaScript程式庫，但請求AdobeAdvertising則需要它。

   您應將程式庫部署在網頁上，客戶可從該網頁提交選擇退出銷售的請求，例如您公司的隱私權入口網站。 程式庫可協助您擷取AdobeCookie(命名空間ID: `gsurferID`)，以便您能透過Adobe Experience Platform Privacy Service API，在選擇退出銷售請求中提交這些身分。

1. 識別您的Experience Cloud組織ID，並確認已連結至您的AdobeAdvertising帳戶。

   Experience Cloud組織ID是24個字元的英數字串，後面附加了「@AdobeOrg」。 大部分Experience Cloud客戶都獲派組織ID。 如果您的行銷團隊或內部Adobe系統管理員不知道您的組織ID，或不確定是否已布建，請透過gdprsupport@adobe.com聯絡Adobe客戶服務。 您需要組織ID，才能使用 `imsOrgID` 命名空間。

   >[!IMPORTANT]
   >
   >請連絡您公司的Adobe廣告代表，確認您組織的所有Adobe廣告帳戶，包括 [!DNL DSP] 帳戶或廣告商 [!DNL Search] 帳戶，和 [!DNL Creative] 或 [!DNL DCO] 帳戶 — 連結至您的Experience Cloud組織ID。

1. 使用Adobe Experience Platform Privacy Service API [提交退出銷售請求](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) 代表消費者Adobe廣告，並檢查現有請求的狀態。

   如需選擇退出銷售請求的範例，請參閱下方的附錄。

   >[!NOTE]
   如果您的企業有多個Experience Cloud組織ID，則您必須為每個ID傳送個別的API請求。 不過，您可以向多個Adobe廣告子解決方案([!DNL Search], [!DNL Creative], [!DNL DSP]，和 [!DNL DCO])，每個子解決方案各一個帳戶。

若要獲得Adobe廣告的支援，必須執行上述所有步驟。 如需使用Adobe Experience Platform Privacy Service執行這些及其他相關工作的詳細資訊，以及在何處尋找您需要的項目，請參閱 [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## 擷取已提交選擇退出銷售請求的消費者的報表

Adobe廣告會產生客戶針對帳戶選擇退出銷售請求所提交的ID每月報表。 每個報表都以Tab分隔的文字檔壓縮為GZIP格式。 這些資料整合了使用在Advertising DSP中建立的CCPA選擇退出銷售區段所擷取的請求，以及透過Privacy ServiceAPI提交的任何請求。 在CCPA選擇退出銷售區段中擷取的使用者ID是由區段和廣告商識別。 報表是在前一個月的每月第一日產生。 例如，6月的每月使用者清單可在7月1日提供。

您可以從Advertising DSP內或使用Advertising DSP，擷取前三個月內建立之每月報表的連結 [!DNL Trafficking API]. 每個連結的有效期為7天，但每次客戶嘗試擷取時都會重新整理。

### 方法1:在Advertising DSP中擷取消費者選擇退出銷售報表

1. 登入廣告商的帳戶(位於 [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [擷取報表](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### 方法2:使用Advertising DSP擷取消費者選擇退出銷售報表 [!DNL Trafficking API]

此功能適用於使用 [!DNL Trafficking API]. 請參閱 [!DNL Trafficking API] 以取得更多資訊。

如果您的組織未使用 [!DNL Trafficking API] 但對更多資訊感興趣，請 [!DNL Adobe] 客戶團隊。

## 附錄：範例 [!UICONTROL CCPA Opt-Out-of-Sale] 請求Privacy ServiceAPI使用者

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "AdCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["AdCloud"],
    "regulation": "ccpa"
}'
```

其中：

* `"namespace": "AdCloud"` 指出 `AdCloud` cookie空間，而對應的值為從 `AdobePrivacy.js`
* `"include": ["AdCloud"]` 指出請求適用於Adobe廣告
