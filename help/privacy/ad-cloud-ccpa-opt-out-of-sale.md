---
title: Adobe Advertising Cloud支援加州消費者隱私法(&#58;消費者選擇退出銷售支援
description: 了解擷取消費者選擇退出銷售請求的支援。
feature: CCPA
exl-id: 2c0cd4f5-798f-479a-99cd-f555cd676766
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '1036'
ht-degree: 0%

---

# Adobe Advertising Cloud支援加州消費者隱私法：消費者選擇退出銷售支援

*針對Adobe Advertising CloudDemand Side Platform*

>[!IMPORTANT]
>
>本檔案的內容不是法律建議，且用意並非要取代法律建議。 如需加州消費者隱私法的相關建議，請諮詢法律顧問。

加州消費者隱私法(CCPA)是加州新的隱私權法，自2020年1月1日起生效。 CCPA為加州居民提供新的個人資訊權利，並對在加州經營業務的特定實體賦予資料保護責任。 CCPA讓消費者有權存取和刪除其資料，也有權選擇退出某些符合「銷售」第三方個人資訊資格的活動。

身為企業，您將決定要由Adobe Experience Cloud代表您處理和儲存的個人資料。

Adobe Advertising Cloud身為您的服務提供者，可支援您的企業履行CCPA所規定的義務，這些義務適用於使用Advertising Cloud產品和服務，包括管理消費者存取和刪除個人資訊的請求，以及管理消費者選擇退出個人資訊銷售的請求。

本檔案說明Adobe Advertising CloudDemand Side Platform(DSP)身為服務提供者，如何支援消費者選擇退出「個人資訊銷售」的權利，因為CCPA已定義每個詞語。 其中包含如何將退出銷售請求傳達給Advertising Cloud，以及如何擷取組織退出銷售請求報表的資訊。

有關Advertising Cloud Search、Advertising Cloud Creative、Advertising Cloud DSP(Demand Side Platform)和Media Optimizer DCO如何支援消費者的個人資訊存取和刪除權限的資訊，請參閱[Adobe Advertising Cloud加州消費者隱私法支援：消費者資料存取和刪除支援](/help/privacy/ad-cloud-ccpa-access-delete.md)。

如需CCPAAdobe隱私權服務的詳細資訊，請參閱[Adobe隱私權中心](https://www.adobe.com/privacy/ccpa.html)。

## 將消費者選擇退出銷售的請求傳達至Advertising Cloud

您可以使用下列任一項，傳達消費者選擇退出銷售的請求：

* 在Advertising Cloud DSP中建立的CCPA選擇退出銷售區段
* Adobe Experience Platform Privacy Service API

### 方法1:在Advertising Cloud DSP中使用[!UICONTROL CCPA Opt-Out-of-Sale]區段傳達CCPA選擇退出銷售的請求

>[!NOTE]
>
>使用者無限期保留在CCPA選擇退出銷售的區段中。

1. 前往[https://advertising.adobe.com/](https://advertising.adobe.com/)登入Advertising Cloud DSP中的廣告商帳戶。
1. [建立CCPA選擇退出銷售區段，並實作區段像素以擷取選擇退出請求](/help/dsp/audiences/ccpa-opt-out-segment-create.md)。

### 方法2:使用Adobe Experience Platform Privacy Service API傳達CCPA選擇退出銷售的要求

*廣告商僅指派Experience Cloud組織ID（IMS組織ID）*

1. 部署JavaScript程式庫以擷取客戶的Cookie。 所有Adobe Experience Cloud解決方案都會使用相同的程式庫`AdobePrivacy.js`。

   >[!IMPORTANT]
   >
   >對某些Adobe Experience Cloud解決方案的請求不需要JavaScript程式庫，但對Advertising Cloud的請求則需要它。

   您應將程式庫部署在網頁上，客戶可從該網頁提交選擇退出銷售的請求，例如您公司的隱私權入口網站。 程式庫可協助您擷取AdobeCookie(命名空間ID:`gsurferID`)，方便您透過Adobe Experience Platform Privacy Service API在選擇退出銷售請求中提交這些身分。

1. 識別您的IMS組織ID，並確認已連結至您的Advertising Cloud帳戶。

   IMS組織ID是24個字元的英數字串，並附加@AdobeOrg。 大部分的Adobe Experience Cloud客戶都已獲派IMS組織ID。 如果您的行銷團隊或內部Adobe系統管理員不知道貴組織的IMS組織ID，或不確定是否已布建，請透過gdprsupport@adobe.com聯絡Adobe客戶服務。 您需要IMS組織ID才能將請求提交至隱私權API。

   >[!IMPORTANT]
   >
   >請連絡您公司的Advertising Cloud代表，確認您組織的所有Advertising Cloud帳戶（包括[!DNL DSP]帳戶或廣告商、[!DNL Search]帳戶及[!DNL Creative]或[!DNL DCO]帳戶）皆已連結至您的IMS組織ID。

1. 使用Adobe Experience Platform Privacy Service API代表消費者將[選擇退出銷售請求](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html)提交至Advertising Cloud，並檢查現有請求的狀態。

   如需選擇退出銷售請求的範例，請參閱下方的附錄。

   >[!NOTE]
   如果貴公司有多個Adobe Experience Cloud Identity Management服務組織ID（IMS組織ID），則您必須分別傳送各個API請求。 不過，您可以對多個Advertising Cloud子解決方案（[!DNL Search]、[!DNL Creative]、[!DNL DSP]及[!DNL DCO]）發出一個API請求，每個子解決方案各一個帳戶。

若要獲得Advertising Cloud的支援，所有這些步驟都是必要的。 有關使用Adobe Experience Platform Privacy Service執行這些任務和其他相關任務的詳細資訊，以及在何處查找需要的項目，請參閱[https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)。

## 擷取已提交選擇退出銷售請求的消費者的報表

Advertising Cloud會產生客戶針對帳戶選擇退出銷售請求所提交的ID每月報告。 每個報表都以Tab分隔的文字檔壓縮為GZIP格式。 資料整合了使用在Advertising Cloud DSP中建立的CCPA選擇退出銷售區段所擷取的請求，以及透過Privacy ServiceAPI提交的任何請求。 在CCPA選擇退出銷售區段中擷取的使用者ID是由區段和廣告商識別。 報表是在前一個月的每月第一日產生。 例如，6月的每月使用者清單可在7月1日提供。

您可以從Advertising Cloud DSP內或使用Advertising Cloud [!DNL Trafficking API]擷取前三個月內建立之每月報表的連結。 每個連結的有效期為7天，但每次客戶嘗試擷取時都會重新整理。

### 方法1:在Advertising Cloud DSP中擷取消費者選擇退出銷售報表

1. 前往[https://advertising.adobe.com/](https://advertising.adobe.com/)登入Advertising Cloud DSP中的廣告商帳戶。
1. [擷取報表](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md)。

### 方法2:使用Advertising Cloud [!DNL Trafficking API]擷取消費者選擇退出銷售報表

此功能適用於使用[!DNL Trafficking API]的組織。 如需詳細資訊，請參閱[!DNL Trafficking API]的檔案。

如果您的組織未使用[!DNL Trafficking API]但有興趣了解詳細資訊，請連絡您的Adobe客戶經理。

## 附錄：[!UICONTROL CCPA Opt-Out-of-Sale]請求Privacy ServiceAPI使用者範例

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

* `"namespace": "AdCloud"` 指出 `AdCloud` Cookie空間，而對應的值為從擷取的客戶Cookie ID  `AdobePrivacy.js`
* `"include": ["AdCloud"]` 指出要求適用於Advertising Cloud
