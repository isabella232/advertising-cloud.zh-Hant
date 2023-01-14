---
title: Adobe加州消費者隱私法的廣告支援：消費者資料存取和刪除支援
description: 了解支援的資料請求類型、必要的設定和欄位值，以及使用舊版產品ID和傳回資料欄位的API存取請求範例。
feature: CCPA
exl-id: 1330da6c-a944-4bb5-8539-488d97f56175
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 0%

---

# 加州消費者隱私法的Adobe廣告支援：消費者資料存取和刪除支援

*針對 [!DNL Adobe Advertising Search];Adobe廣告DSP;Adobe廣告創意；和Adobe廣告DCO*

>[!IMPORTANT]
>
>本檔案的內容不是法律建議，且用意並非要取代法律建議。 如需加州消費者隱私法的相關建議，請諮詢法律顧問。

加州消費者隱私法(CCPA)是加州新的隱私權法，自2020年1月1日起生效。 CCPA為加州居民提供新的個人資訊權利，並對在加州經營業務的特定實體賦予資料保護責任。 CCPA為消費者提供存取和刪除其個人資訊的權利，以及選擇退出符合「銷售」第三方個人資訊資格的特定活動的權利。

身為企業，您將決定要由Adobe Experience Cloud代表您處理和儲存的個人資料。

身為您的服務提供者，Adobe廣告可支援您的企業履行CCPA所規定的義務，這些義務適用於Adobe廣告產品和服務的使用，包括管理存取和刪除個人資訊的請求，以及管理選擇退出個人資訊銷售的請求。

本檔案說明如何 [!DNL Advertising Search];廣告創意；廣告DSP(Demand Side Platform);和 [!DNL Advertising DCO]  — 作為服務提供商 — 支援消費者使用Adobe訪問和刪除個人資訊的權利 [!DNL Experience Platform Privacy Service API] 和 [!DNL Privacy Service UI].

如需Advertising DSP如何支援消費者選擇退出個人資訊銷售權限的相關資訊，請參閱 [加州消費者隱私法的Adobe廣告支援：消費者選擇退出支援](/help/privacy/ad-cloud-ccpa-opt-out-of-sale.md).

如需CCPAAdobe隱私權服務的詳細資訊，請參閱 [Adobe隱私中心](https://www.adobe.com/privacy/ccpa.html).

## 支援的Adobe廣告資料請求類型

Adobe Experience Platform可讓企業完成下列工作：

* 在中存取消費者的Cookie層級資料或裝置ID層級資料（適用於行動應用程式中的廣告） [!DNL Search], [!DNL Creative], [!DNL DSP]，或 [!DNL DCO].
* 刪除儲存在中的Cookie層級資料 [!DNL Search], [!DNL Creative], [!DNL DSP]，或 [!DNL DCO] 使用瀏覽器的消費者；或刪除儲存在 [!DNL DSP] 適用於在行動裝置上使用應用程式的消費者。
* 檢查一或所有現有請求的狀態。

## 傳送Adobe廣告請求的必要設定

若要從Adobe廣告提出存取和刪除消費者個人資訊的請求，您必須：

1. 部署JavaScript程式庫以擷取和移除客戶的Cookie。 同一個圖書館， `AdobePrivacy.js`，會用於所有Adobe Experience Cloud解決方案。

   >[!IMPORTANT]
   >
   >對某些Experience Cloud解決方案的請求不需要JavaScript程式庫，但請求AdobeAdvertising則需要它。

   您應將程式庫部署在網頁上，客戶可從此頁面提交存取和刪除請求，例如您公司的隱私權入口網站。 程式庫可協助您擷取AdobeCookie(命名空間ID: `gsurferID`)，這樣您就可以透過 [!DNL Adobe Experience Platform Privacy Service API].

   當客戶要求刪除個人資料時，程式庫也會從客戶的瀏覽器中刪除客戶的Cookie。

   >[!NOTE]
   >
   >刪除個人資料與選擇退出不同，這會停止使用受眾區段來鎖定目標的使用者。 不過，當消費者要求從 [!DNL Creative], [!DNL DSP]，或 [!DNL DCO]，程式庫也會傳送請求給「Adobe廣告」，以選擇讓客戶退出區段鎖定目標。 適用於廣告商 [!DNL Search]，建議您提供客戶的連結 [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse)，說明如何選擇退出對象區段鎖定目標。

1. 識別您的Experience Cloud組織ID，並確認已連結至您的AdobeAdvertising帳戶。

   Experience Cloud組織ID是24個字元的英數字串，後面附加了「@AdobeOrg」。 大部分Experience Cloud客戶都獲派組織ID。 如果您的行銷團隊或內部Adobe系統管理員不知道您的組織ID，或不確定是否已布建，請透過gdprsupport@adobe.com聯絡Adobe客戶服務。 您需要組織ID，才能使用 `imsOrgID` 命名空間。

   >[!IMPORTANT]
   >
   >請連絡您公司的Adobe廣告代表，確認您組織的所有Adobe廣告帳戶，包括 [!DNL DSP] 帳戶或廣告商 [!DNL Search] 帳戶，和 [!DNL Creative] 或 [!DNL DCO] 帳戶 — 連結至您的Experience Cloud組織ID。

1. 使用 [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （針對自動請求）或 [Privacy ServiceUI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) （針對臨機請求）代表消費者向Adobe廣告提交存取和刪除個人資訊的請求，以及檢查現有請求的狀態。

   廣告商若有行動應用程式可與客戶互動，並透過 [!DNL DSP]，您將需要下載適用於隱私權的行動SDK以進行Experience Cloud。 行動SDK可讓企業設定選擇退出狀態旗標、擷取消費者的裝置ID(命名空間ID: `deviceID`)，並將請求提交至Privacy ServiceAPI。 您的行動應用程式需要SDK 4.15.0版或更新版本。

   當您提交消費者存取請求時，Privacy ServiceAPI會根據指定的Cookie或裝置ID傳回消費者的資訊，然後您必須傳回給消費者。

   當您提交消費者刪除請求時，Cookie ID或裝置ID以及所有與Cookie相關聯的成本、點按和收入資料都會從伺服器中刪除。

   >[!NOTE]
   如果您的企業有多個Experience Cloud組織ID，則您必須為每個ID傳送個別的API請求。 不過，您可以向多個Adobe廣告子解決方案([!DNL Search], [!DNL Creative], [!DNL DSP]，和 [!DNL DCO])，每個子解決方案各一個帳戶。

若要獲得Adobe廣告的支援，必須執行上述所有步驟。 如需使用Adobe Experience Platform Privacy Service執行這些及其他相關工作的詳細資訊，以及在何處尋找您需要的項目，請參閱 [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Adobe廣告JSON請求中的必填欄位值

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*您的Experience Cloud組織ID*>

&quot;users&quot;:

* `"key":` &lt;*通常是客戶的名稱*>

* `"action":` heer `**access**` 或 `**delete**`

* `"user IDs":`

   * `"namespace": **411**` （表示adcloud cookie空間）

   * `"value":` &lt;*實際客戶的cookie ID值，從`AdobePrivacy.js`*>

* `"include": **adCloud**` (適用於請求的Adobe產品)

* `"regulation": **ccpa**` （適用於請求的隱私權法規）

## 消費者使用從AdobePrivacy.js擷取的Adobe廣告使用者ID提交請求的範例

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

以下是Adobe廣告的個人資訊存取回應範例。

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
