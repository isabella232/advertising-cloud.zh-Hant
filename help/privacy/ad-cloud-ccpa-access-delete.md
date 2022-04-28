---
title: Adobe Advertising Cloud支援《加利福尼亞消費者隱私法》：使用者資料存取和刪除支援
description: 瞭解支援的資料請求類型、必需的設定和欄位值，以及使用舊產品ID和返回的資料欄位的API訪問請求示例。
feature: CCPA
exl-id: 1330da6c-a944-4bb5-8539-488d97f56175
source-git-commit: ca19836d5918c69161c4d850a65eaff311249225
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---

# Adobe Advertising Cloud支援加州消費者隱私法：使用者資料存取和刪除支援

*Adobe Advertising Cloud Search、Adobe Advertising Cloud Creative、Adobe Advertising Cloud DSP和Adobe[!DNL Media Optimizer DCO]*

>[!IMPORTANT]
>
>本檔案內容不是法律意見，不是代替法律意見。 請咨詢您的法律顧問，以獲取有關《加利福尼亞消費者隱私法》的建議。

《加利福尼亞消費者隱私法》(CCPA)是加利福尼亞新的隱私法，自2020年1月1日起生效。 CCPA為加利福尼亞州居民提供了有關其個人資訊的新權利，並對在加利福尼亞開展業務的某些實體規定了資料保護責任。 CCPA向消費者提供了訪問和刪除其個人資訊的權利，以及選擇不參與某些符合向第三方「銷售」個人資訊資格的活動的權利。

作為企業，您將確定Adobe Experience Cloud代表您處理和儲存的個人資料。

作為您的服務提供商，Adobe Advertising Cloud支援您的企業履行CCPA規定的義務，這些義務適用於Advertising Cloud產品和服務的使用，包括管理訪問和刪除個人資訊的請求以及管理退出個人資訊銷售的請求。

本文檔介紹Advertising Cloud Search、Advertising Cloud Creative、Advertising Cloud DSP(Demand Side Platform)和 [!DNL Media Optimizer DCO]  — 作為服務提供商 — 支援消費者使用Adobe訪問和刪除個人資訊的權利 [!DNL Experience Platform Privacy Service API] 和 [!DNL Privacy Service UI]。

有關Advertising Cloud DSP如何支援消費者選擇退出個人資訊銷售的權利的資訊，請參閱 [Adobe Advertising Cloud支援加州消費者隱私法：消費者選擇退出支援](/help/privacy/ad-cloud-ccpa-opt-out-of-sale.md)。

有關CCPA的Adobe隱私服務的詳細資訊，請參見 [Adobe隱私中心](https://www.adobe.com/privacy/ccpa.html)。

## 支援的Advertising Cloud資料請求類型

Adobe Experience Platform為企業提供了完成以下任務的能力：

* 訪問用戶的Cookie級資料或設備ID級資料（用於移動應用中的廣告） [!DNL Search]。 [!DNL Creative]。 [!DNL DSP]或 [!DNL DCO]。
* 刪除儲存在 [!DNL Search]。 [!DNL Creative]。 [!DNL DSP]或 [!DNL DCO] 消費者使用瀏覽器；或刪除儲存在 [!DNL DSP] 用於在移動設備上使用應用的消費者。
* 檢查一個或所有現有請求的狀態。

## 發送Advertising Cloud請求所需的設定

要請求訪問和刪除Advertising Cloud的消費者個人資訊，您需要：

1. 部署JavaScript庫以檢索和刪除客戶的Cookie。 同一個圖書館， `AdobePrivacy.js`，用於所有Adobe Experience Cloud解決方案。

   >[!IMPORTANT]
   >
   >對某些Experience Cloud解決方案的請求不需要JavaScript庫，但對Advertising Cloud的請求需要它。

   您應在網頁上部署庫，客戶可以從該網頁上提交訪問和刪除請求，如您公司的隱私門戶。 庫可幫助您檢索AdobeCookie(命名空間ID: `gsurferID`)，以便您可以提交這些身份，作為訪問和刪除請求的一部分 [!DNL  Adobe Experience Platform Privacy Service API]。

   當客戶要求刪除個人資料時，庫還會從客戶的瀏覽器中刪除客戶的cookie。

   >[!NOTE]
   >
   >刪除個人資料與選擇退出不同，這會阻止最終用戶針對受眾群體。 但是，當消費者要求從 [!DNL Creative]。 [!DNL DSP]或 [!DNL DCO]，該庫還向Advertising Cloud發出請求，要求其不再選擇客戶作為細分目標。 對於具有 [!DNL Search]，我們建議您向客戶提供一個連結 [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse)，說明如何選擇不以受眾為目標。

1. 確定您組織的Experience CloudID，並確保它連結到您的Advertising Cloud帳戶。

   Experience CloudID是附加有「@AdobeOrg」的24個字元的字母數字字串。 大多數Experience Cloud客戶已分配ID。 如果您的營銷團隊或內部Adobe系統管理員不知道您組織的ID，或者不確定是否已預配，請通過gdprsupport@adobe.com聯繫Adobe客戶服務。 您需要ID才能使用 `imsOrgID` 命名空間。

   >[!IMPORTANT]
   >
   >聯繫您公司的Advertising Cloud代表，確認您公司的所有Advertising Cloud帳戶，包括 [!DNL DSP] 或者廣告商， [!DNL Search] 帳戶和 [!DNL Creative] 或 [!DNL DCO] 帳戶 — 連結到您的Experience CloudID。

1. 使用 [Adobe Experience Platform Privacy ServiceAPI](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （用於自動請求）或 [Privacy ServiceUI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) （特別請求）代表消費者向Advertising Cloud提交訪問和刪除個人資訊的請求，並檢查現有請求的狀態。

   對於擁有移動應用與客戶交互併發起活動的廣告商 [!DNL DSP]，您需要下載Privacy-ready Mobile SDK以進行Experience Cloud。 移動SDK允許企業設定選擇退出狀態標誌，檢索使用者的設備ID(命名空間ID: `deviceID`)，並將請求提交到Privacy ServiceAPI。 您的移動應用需要SDK 4.15.0版或更高版本。

   當您提交使用者訪問請求時，Privacy ServiceAPI將根據指定的cookie或設備ID返回使用者資訊，然後您必須將其返回給使用者。

   在您提交使用者刪除請求時，Cookie ID或設備ID以及所有成本，按一下並從伺服器中刪除與Cookie關聯的收入資料。

   >[!NOTE]
   如果您的企業具有多個Experience CloudID，則必須為每個API請求發送單獨的API請求。 但是，您可以向多個Advertising Cloud子解決方案發出一個API請求([!DNL Search]。 [!DNL Creative]。 [!DNL DSP], [!DNL DCO])，每個子解決方案有一個帳戶。

所有這些步驟都是獲得Advertising Cloud支援所必需的。 有關使用Adobe Experience Platform Privacy Service執行這些任務和其他相關任務的詳細資訊，以及在何處查找需要的項目，請參閱 [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)。

## Advertising CloudJSON請求中的必需欄位值

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*您組織的Experience CloudID值*>

&quot;用戶&quot;:

* `"key":` &lt;*通常客戶的姓名*>

* `"action":` 或 `**access**` 或 `**delete**`

* `"user IDs":`

   * `"namespace": **411**` （表示adcloud cookie空間）

   * `"value":` &lt;*從中檢索的實際客戶的cookie ID值`AdobePrivacy.js`*>

* `"include": **adCloud**` (即適用於請求的Adobe產品)

* `"regulation": **ccpa**` （即適用於請求的隱私法規）

## 使用從AdobePrivacy.js檢索到的Advertising Cloud用戶ID由使用者提交的請求示例

```
{
"companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
  "userIDs":[
      {
         "namespace":"411",
         "value":"Wqersioejr-wdg",
         "type":"namespaceId",
         "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"ccpa"
}
}
```

## 為訪問請求返回的資料欄位

以下是Advertising Cloud個人資訊訪問響應示例。

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
