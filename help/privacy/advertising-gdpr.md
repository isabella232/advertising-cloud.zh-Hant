---
title: Adobe廣告支援一般資料保護規範
description: 了解支援的資料請求類型、必要的設定和欄位值，以及使用舊版產品ID和傳回資料欄位的API存取請求範例
feature: GDPR
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 0%

---

# Adobe廣告支援一般資料保護規範

*針對 [!DNL Adobe Advertising Search];Adobe廣告DSP;Adobe廣告創意；和Adobe廣告DCO*

>[!IMPORTANT]
>
>本檔案的內容不是法律建議，且用意並非要取代法律建議。 如需一般資料保護規範的相關建議，請諮詢法律顧問。

2018年5月25日生效的一般資料保護規範(GDPR)賦予歐盟(EU)境內的所有個人（資料主體）控制其個人資料，並簡化國際業務的法規環境。 本法適用於向歐盟境內之個人提供商品或服務、監控其行為或收集其個人資料的所有企業（資料控管單位），無論資料控管單位的營業位置為何，其個人資料都會受到處理。

Adobe Experience Cloud代表客戶擔任資料處理者，負責處理其收到和儲存的任何個人資料。 身為資料控管單位，您可以決定要由Adobe Experience Cloud代表您處理和儲存哪些個人資料。

本檔案說明如何 [!DNL Advertising Search];廣告創意；廣告DSP(Demand Side Platform);和 [!DNL Advertising DCO] 使用Adobe Experience Platform Privacy Service API和Privacy ServiceUI，支援您的資料主體存取GDPR資料和刪除權限。

如需GDPR對您業務所代表之意義的詳細資訊，請參閱 [GDPR與您的業務](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## 支援的Adobe廣告資料請求類型

Adobe Experience Platform可讓企業完成下列工作：

* 在中存取資料主體的Cookie層級資料或裝置ID層級資料（適用於行動應用程式中的廣告） [!DNL Search], [!DNL Creative], [!DNL DSP]，或 [!DNL DCO].
* 刪除儲存在中的Cookie層級資料 [!DNL Search], [!DNL Creative], [!DNL DSP]，或 [!DNL DCO] 適用於使用瀏覽器的資料主體；或刪除儲存在 [!DNL DSP] 適用於在行動裝置上使用應用程式的資料主體。
* 檢查一或所有現有請求的狀態。

## 傳送Adobe廣告請求的必要設定

若要請求存取和刪除Adobe廣告的資料，您需要：

1. 部署JavaScript程式庫以擷取和移除您的資料主體Cookie。 同一個圖書館， `AdobePrivacy.js`，會用於所有Adobe Experience Cloud解決方案。

   >[!IMPORTANT]
   >
   >對某些Adobe Experience Cloud解決方案的請求不需要JavaScript程式庫，但請求AdobeAdvertising則需要它。

   您應將程式庫部署在網頁上，資料主體可從此頁面提交存取和刪除請求，例如您公司的隱私權入口網站。 程式庫可協助您擷取AdobeCookie(命名空間ID: `gsurferID`)，以便您能透過Adobe Experience Platform Privacy Service API提交這些身分資料，以納入存取和刪除請求。

   當資料主體要求刪除個人資料時，資料庫也會從資料主體的瀏覽器中刪除資料主體的Cookie。

   >[!NOTE]
   >
   >刪除個人資料與選擇退出不同，退出會停止使用受眾區段來鎖定目標使用者。 不過，當資料主體要求從 [!DNL Creative], [!DNL DSP]，或 [!DNL DCO]，資料庫也會傳送請求給「Adobe廣告」，以選擇退出資料主體的區段鎖定目標。 適用於廣告商 [!DNL Search]，建議您提供資料主體的連結 [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html)，說明如何選擇退出對象區段鎖定目標。

1. 識別您的Experience Cloud組織ID，並確認已連結至您的AdobeAdvertising帳戶。

   Experience Cloud組織ID是24個字元的英數字串，後面附加了「@AdobeOrg」。 大部分Experience Cloud客戶都獲派組織ID。 如果您的行銷團隊或內部Adobe系統管理員不知道您的組織ID，或不確定是否已布建，請透過gdprsupport@adobe.com聯絡Adobe客戶服務。 您需要組織ID，才能使用 `imsOrgID` 命名空間。

   >[!IMPORTANT]
   >
   >請連絡您公司的Adobe廣告代表，確認您組織的所有Adobe廣告帳戶，包括 [!DNL DSP] 帳戶或廣告商 [!DNL Search] 帳戶，和 [!DNL Creative] 或 [!DNL DCO] 帳戶 — 連結至您的Experience Cloud組織ID。

1. 使用 [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （針對自動請求）或 [Privacy ServiceUI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) （針對臨機請求）代表資料主體向Adobe廣告提交存取和刪除請求，以及檢查現有請求的狀態。

   若廣告商有行動應用程式可與資料主體互動，並透過DSP啟動行銷活動，則您需要下載適合隱私權的行動SDK以供Experience Cloud。 行動SDK可讓資料控管者設定選擇退出狀態旗標、擷取資料主體的裝置ID(命名空間ID:deviceID)，並將請求提交至Privacy ServiceAPI。 您的行動應用程式需要SDK 4.15.0版或更新版本。

   當您提交資料主體的存取請求時，Privacy ServiceAPI會根據指定的Cookie或裝置ID傳回資料主體的資訊，然後您必須傳回資料主體。

   提交資料主體的刪除請求時，Cookie ID或裝置ID以及與Cookie相關聯的所有成本、點按和收入資料都會從伺服器中刪除。

   >[!NOTE]
   如果您的公司有多個Experience Cloud組織ID，則您必須為每個ID傳送個別的API請求。 不過，您可以向多個Adobe廣告子解決方案([!DNL Search], [!DNL Creative], [!DNL DSP]，和 [!DNL DCO])，每個子解決方案各一個帳戶。

所有這些步驟對於Adobe廣告都是必要的。 如需使用Adobe Experience Platform Privacy Service執行這些及其他相關工作的詳細資訊，以及在何處尋找您需要的項目，請參閱 [www.adobe.io/apis/cloudplatform/gdpr.html](https://www.adobe.io/apis/experienceplatform/gdpr.html).

## Adobe廣告JSON請求中的必填欄位值

&quot;&quot;公司上下文&quot;:

* `"namespace": **imsOrgID**`
* `"value":` &lt;*您的IMS組織ID值*>

`"users":`

* `"key":` &lt;*通常是資料主體的名稱*>

* `"action":` heer `**access**` 或 `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (表示 [!DNL adcloud] cookie空間)

   * `"value":` &lt;*實際資料主體的cookie ID值，從`AdobePrivacy.js`*>

* `"include": **adCloud**` (適用於請求的Adobe產品)

* `"regulation": **gdpr**` （適用於請求的隱私權法規）

## 資料主體使用從中擷取的Adobe廣告使用者ID提交的請求範例 `AdobePrivacy.js`

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
    "regulation":"gdpr"
}
}
```

## 針對存取請求傳回的資料欄位

以下是Adobe廣告的存取回應範例。

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
