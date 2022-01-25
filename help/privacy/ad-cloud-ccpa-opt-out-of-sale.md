---
title: Adobe Advertising Cloud支援《加利福尼亞消費者隱私法》：消費者選擇不銷售支援
description: 瞭解對捕獲消費者選擇退出銷售請求的支援。
feature: CCPA
exl-id: 2c0cd4f5-798f-479a-99cd-f555cd676766
source-git-commit: adb3118d291d110e653a62cc1a323410b1a596b2
workflow-type: tm+mt
source-wordcount: '1031'
ht-degree: 0%

---

# Adobe Advertising Cloud支援加州消費者隱私法：消費者選擇退出銷售支援

*為Adobe Advertising CloudDemand Side Platform*

>[!IMPORTANT]
>
>本檔案內容不是法律意見，不是代替法律意見。 請咨詢您的法律顧問，以獲取有關《加利福尼亞消費者隱私法》的建議。

《加利福尼亞消費者隱私法》(CCPA)是加利福尼亞新的隱私法，自2020年1月1日起生效。 CCPA為加利福尼亞州居民提供了有關其個人資訊的新權利，並對在加利福尼亞開展業務的某些實體規定了資料保護責任。 CCPA向消費者提供了訪問和刪除其資料的權利，以及選擇不參與某些符合向第三方「銷售」個人資訊資格的活動的權利。

作為企業，您將確定Adobe Experience Cloud代表您處理和儲存的個人資料。

作為您的服務提供商，Adobe Advertising Cloud支援您的企業履行CCPA規定的義務，這些義務適用於Advertising Cloud產品和服務的使用，包括管理消費者訪問和刪除個人資訊的請求以及管理消費者選擇不銷售個人資訊的請求。

本文檔介紹Adobe Advertising CloudDemand Side Platform(DSP)作為服務提供商，如何支援消費者選擇不&quot;銷售&quot;&quot;個人資訊&quot;的權利，因為CCPA定義了每個術語。 它包括有關如何向Advertising Cloud傳遞選擇不銷售請求以及如何檢索貴組織選擇不銷售請求的報告的資訊。

有關Advertising Cloud Search、Advertising Cloud Creative、Advertising Cloud DSP(Demand Side Platform)和Media Optimizer DCO如何支援消費者的個人資訊訪問和刪除權限的資訊，請參閱 [Adobe Advertising Cloud支援加州消費者隱私法：使用者資料存取和刪除支援](/help/privacy/ad-cloud-ccpa-access-delete.md)。

有關CCPA的Adobe隱私服務的詳細資訊，請參見 [Adobe隱私中心](https://www.adobe.com/privacy/ccpa.html)。

## 向Advertising Cloud傳達消費者選擇不銷售請求

您可以使用以下兩種方法來傳遞消費者選擇退出銷售的請求：

* 在Advertising Cloud DSP建立的CCPA選擇不銷售部門
* Adobe Experience Platform Privacy Service

### 方法1:使用 [!UICONTROL CCPA Opt-Out-of-Sale] 段於Advertising Cloud DSP

>[!NOTE]
>
>用戶無限期地留在CCPA選擇不銷售的部門。

1. 登錄Advertising Cloud DSP的廣告商帳戶 [https://advertising.adobe.com/](https://advertising.adobe.com/)。
1. [建立CCPA選擇退出銷售段，並實施段像素以捕獲選擇退出請求](/help/dsp/audiences/ccpa-opt-out-segment-create.md)。

### 方法2:使用Adobe Experience Platform Privacy ServiceAPI傳遞CCPA選擇不銷售請求

*廣告商給Adobe Experience Cloud [!DNL Organization ID] ([!DNL IMS Org ID]僅*

1. 部署JavaScript庫以檢索客戶的Cookie。 同一個圖書館， `AdobePrivacy.js`，用於所有Adobe Experience Cloud解決方案。

   >[!IMPORTANT]
   >
   >對某些Adobe Experience Cloud解決方案的請求不需要JavaScript庫，但對Advertising Cloud的請求需要它。

   您應在網頁上部署庫，客戶可以從該網頁上提交選擇退出銷售請求，如您公司的隱私門戶。 庫可幫助您檢索AdobeCookie(命名空間ID: `gsurferID`)，以便您可以通過Adobe Experience Platform Privacy ServiceAPI將這些身份作為選擇退出銷售請求的一部分提交。

1. 確定您的IMS組織ID，並確保它與您的Advertising Cloud帳戶連結。

   IMS組織ID是附加有@AdobeOrg的24個字元的字母數字字串。 大多數Adobe Experience Cloud客戶都被分配了IMS組織ID。 如果您的營銷團隊或內部Adobe系統管理員不知道您組織的IMS組織ID，或者不確定是否已預配，請通過gdprsupport@adobe.com聯繫Adobe客戶服務。 您需要IMS組織ID才能向隱私API提交請求。

   >[!IMPORTANT]
   >
   >聯繫您公司的Advertising Cloud代表，確認您公司的所有Advertising Cloud帳戶，包括 [!DNL DSP] 或者廣告商， [!DNL Search] 帳戶和 [!DNL Creative] 或 [!DNL DCO] 帳戶 — 連結到IMS組織ID。

1. 使用Adobe Experience Platform Privacy ServiceAPI [提交選擇退出銷售請求](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) 代表消費者向Advertising Cloud發出，並檢查現有請求的狀態。

   有關選擇退出銷售請求的示例，請參閱下面的附錄。

   >[!NOTE]
   如果您的企業具有多個Adobe Experience CloudIdentity Management服務組織ID（IMS組織ID），則必須為每個API發送單獨的請求。 但是，您可以向多個Advertising Cloud子解決方案發出一個API請求([!DNL Search]。 [!DNL Creative]。 [!DNL DSP], [!DNL DCO])，每個子解決方案有一個帳戶。

所有這些步驟都是獲得Advertising Cloud支援所必需的。 有關使用Adobe Experience Platform Privacy Service執行這些任務和其他相關任務的詳細資訊，以及在何處查找需要的項目，請參閱 [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)。

## 檢索提交選擇退出銷售請求的消費者的報告

Advertising Cloud會生成客戶已提交的ID月度報告，以申請該帳戶的退出銷售。 每個報告都可以作為以制表符分隔的文本檔案壓縮為GZIP格式。 這些資料整合了使用CCPA選擇不可銷售部分捕獲的請求，這些部分是在Advertising Cloud DSP建立的，以及通過Privacy ServiceAPI提交的任何資料。 在CCPA選擇退出銷售分段中捕獲的用戶ID由分段和廣告商標識。 在上個月的每月一日生成報告。 例如，6月的月度用戶清單在7月1日可用。

您可以檢索到前三個月中建立的月度報告的連結，這些連結可以從Advertising Cloud DSP內部或通過使用Advertising Cloud [!DNL Trafficking API]。 每個連結的有效期為七天，但每次客戶嘗試檢索一個連結時都會刷新。

### 方法1:在Advertising Cloud DSP內檢索消費者選擇不可銷售報告

1. 登錄Advertising Cloud DSP的廣告商帳戶 [https://advertising.adobe.com/](https://advertising.adobe.com/)。
1. [檢索報告](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md)。

### 方法2:使用Advertising Cloud檢索消費者選擇不可銷售報告 [!DNL Trafficking API]

此功能可供使用 [!DNL Trafficking API]。 請參閱 [!DNL Trafficking API] 的子菜單。

如果您的組織不使用 [!DNL Trafficking API] 但對更多資訊感興趣，請與 [!DNL Adobe] 客戶經理。

## 附錄：示例 [!UICONTROL CCPA Opt-Out-of-Sale] 請求Privacy ServiceAPI用戶

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

* `"namespace": "AdCloud"` 指示 `AdCloud` cookie空間，相應值是從中檢索到的客戶cookie ID `AdobePrivacy.js`
* `"include": ["AdCloud"]` 表明請求適用於Advertising Cloud
