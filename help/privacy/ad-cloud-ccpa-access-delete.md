---
title: Adobe Advertising Cloud支援加州消費者隱私法(&#58;消費者資料存取和刪除支援
description: 了解支援的資料請求類型、必要的設定和欄位值，以及使用舊版產品ID和傳回資料欄位的API存取請求範例。
feature: CCPA
exl-id: 1330da6c-a944-4bb5-8539-488d97f56175
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# Adobe Advertising Cloud支援加州消費者隱私法：消費者資料存取和刪除支援

*針對Adobe Advertising Cloud Search、Adobe Advertising Cloud Creative、Adobe Advertising Cloud DSP和Adobe[!DNL Media Optimizer DCO]*

>[!IMPORTANT]
>
>本檔案的內容不是法律建議，且用意並非要取代法律建議。 如需加州消費者隱私法的相關建議，請諮詢法律顧問。

加州消費者隱私法(CCPA)是加州新的隱私權法，自2020年1月1日起生效。 CCPA為加州居民提供新的個人資訊權利，並對在加州經營業務的特定實體賦予資料保護責任。 CCPA為消費者提供存取和刪除其個人資訊的權利，以及選擇退出符合「銷售」第三方個人資訊資格的特定活動的權利。

身為企業，您將決定要由Adobe Experience Cloud代表您處理和儲存的個人資料。

Adobe Advertising Cloud身為您的服務提供者，可支援您的企業履行CCPA所規定的義務，這些義務適用於使用Advertising Cloud產品和服務，包括管理存取和刪除個人資訊的請求，以及管理選擇退出個人資訊銷售的請求。

本檔案說明Advertising Cloud Search、Advertising Cloud Creative、Advertising Cloud DSP(Demand Side Platform)和[!DNL Media Optimizer DCO]作為服務提供者如何支援消費者使用Adobe[!DNL Experience Platform Privacy Service API]和[!DNL Privacy Service UI]存取和刪除個人資訊的權利。

如需Advertising Cloud DSP如何支援消費者選擇退出個人資訊銷售權利的詳細資訊，請參閱[加州消費者隱私法的Adobe Advertising Cloud支援：消費者選擇退出支援](/help/privacy/ad-cloud-ccpa-opt-out-of-sale.md)。

如需CCPAAdobe隱私權服務的詳細資訊，請參閱[Adobe隱私權中心](https://www.adobe.com/privacy/ccpa.html)。

## Advertising Cloud支援的資料請求類型

Adobe Experience Platform可讓企業完成下列工作：

* 在[!DNL Search]、[!DNL Creative]、[!DNL DSP]或[!DNL DCO]記憶體取消費者的Cookie層級資料或裝置ID層級資料（適用於行動應用程式中的廣告）。
* 為使用瀏覽器的消費者，刪除儲存在[!DNL Search]、[!DNL Creative]、[!DNL DSP]或[!DNL DCO]中的Cookie層級資料；或刪除儲存在[!DNL DSP]中的ID層級資料，供在行動裝置上使用應用程式的消費者使用。
* 檢查一或所有現有請求的狀態。

## 傳送Advertising Cloud請求的必要設定

若要從Advertising Cloud提出存取和刪除消費者個人資訊的請求，您必須：

1. 部署JavaScript程式庫以擷取和移除客戶的Cookie。 所有Adobe Experience Cloud解決方案都會使用相同的程式庫`AdobePrivacy.js`。

   >[!IMPORTANT]
   >
   >對某些Adobe Experience Cloud解決方案的請求不需要JavaScript程式庫，但對Advertising Cloud的請求則需要它。

   您應將程式庫部署在網頁上，客戶可從此頁面提交存取和刪除請求，例如您公司的隱私權入口網站。 程式庫可協助您擷取AdobeCookie(命名空間ID:`gsurferID`)，以便您能透過[!DNL  Adobe Experience Platform Privacy Service API]在存取和刪除請求中提交這些身分。

   當客戶要求刪除個人資料時，程式庫也會從客戶的瀏覽器中刪除客戶的Cookie。

   >[!NOTE]
   >
   >刪除個人資料與選擇退出不同，這會停止使用受眾區段來鎖定目標的使用者。 不過，當消費者要求從[!DNL Creative]、[!DNL DSP]或[!DNL DCO]刪除個人資料時，程式庫也會傳送請求給Advertising Cloud，讓客戶退出區段鎖定目標。 若為具有[!DNL Search]的廣告商，建議您為客戶提供[https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse)的連結，說明如何選擇退出對象區段鎖定目標。

1. 識別您的IMS組織ID，並確定已連結至您的Advertising Cloud帳戶。

   IMS組織ID是24個字元的英數字串，並附加「@AdobeOrg」。 大部分的Adobe Experience Cloud客戶都已獲派IMS組織ID。 如果您的行銷團隊或內部Adobe系統管理員不知道貴組織的IMS組織ID，或不確定是否已布建，請透過gdprsupport@adobe.com聯絡Adobe客戶服務。 您需要IMS組織ID才能將請求提交至隱私權API。

   >[!IMPORTANT]
   >
   >請連絡您公司的Advertising Cloud代表，確認您組織的所有Advertising Cloud帳戶（包括[!DNL DSP]帳戶或廣告商、[!DNL Search]帳戶及[!DNL Creative]或[!DNL DCO]帳戶）皆已連結至您的IMS組織ID。

1. 使用[Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html)（適用於自動請求）或[Privacy ServiceUI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html)（適用於臨機請求），代表消費者向Advertising Cloud提交存取和刪除個人資訊的請求，並檢查現有請求的狀態。

   若廣告商有行動應用程式可與客戶互動，並透過[!DNL DSP]啟動行銷活動，則您需要下載適用於隱私權的行動SDK以供Experience Cloud。 行動SDK可讓企業設定選擇退出狀態旗標、擷取消費者的裝置ID(命名空間ID:`deviceID`)，並將請求提交至Privacy ServiceAPI。 您的行動應用程式需要SDK 4.15.0版或更新版本。

   當您提交消費者存取請求時，Privacy ServiceAPI會根據指定的Cookie或裝置ID傳回消費者的資訊，然後您必須傳回給消費者。

   當您提交消費者刪除請求時，Cookie ID或裝置ID以及所有與Cookie相關聯的成本、點按和收入資料都會從伺服器中刪除。

   >[!NOTE]
   如果貴公司有多個Adobe Experience Cloud Identity Management服務組織ID（IMS組織ID），則您必須分別傳送各個API請求。 不過，您可以對多個Advertising Cloud子解決方案（[!DNL Search]、[!DNL Creative]、[!DNL DSP]及[!DNL DCO]）發出一個API請求，每個子解決方案各一個帳戶。

若要獲得Advertising Cloud的支援，所有這些步驟都是必要的。 有關使用Adobe Experience Platform Privacy Service執行這些任務和其他相關任務的詳細資訊，以及在何處查找需要的項目，請參閱[https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)。

## Advertising Cloud JSON請求中的必填欄位值

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;>您的IMS組織ID值&#x200B;*>*

&quot;users&quot;:

* `"key":` &lt;>通常是客戶的名稱&#x200B;*>*

* `"action":`  `**access**` 或  `**delete**`

* `"user IDs":`

   * `"namespace": **411**` （表示adcloud cookie空間）

   * `"value":` &lt;>從>擷取的實際客戶cookie ID值 `AdobePrivacy.js`**

* `"include": **adCloud**` (適用於請求的Adobe產品)

* `"regulation": **ccpa**` （適用於請求的隱私權法規）

## 消費者使用從AdobePrivacy.js擷取的Advertising Cloud使用者ID提交請求的範例

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

## 針對存取請求傳回的資料欄位

以下是Advertising Cloud個人資訊存取回應的範例。

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
