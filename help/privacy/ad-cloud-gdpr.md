---
title: Adobe Advertising Cloud支援一般資料保護規範
description: 了解支援的資料請求類型、必要的設定和欄位值，以及使用舊版產品ID和傳回資料欄位的API存取請求範例
feature: GDPR
exl-id: 304d88d0-d63d-4b32-8d4d-c61ba2409adc
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 0%

---

# Adobe Advertising Cloud支援一般資料保護規範

*針對Adobe Advertising Cloud Search、Adobe Advertising Cloud Creative、Adobe Advertising Cloud DSP和Adobe Media Optimizer DCO*

>[!IMPORTANT]
>
>本檔案的內容不是法律建議，且用意並非要取代法律建議。 如需一般資料保護規範的相關建議，請諮詢法律顧問。

2018年5月25日生效的一般資料保護規範(GDPR)賦予歐盟(EU)境內的所有個人（資料主體）控制其個人資料，並簡化國際業務的法規環境。 本法適用於向歐盟境內之個人提供商品或服務、監控其行為或收集其個人資料的所有企業（資料控管單位），無論資料控管單位的營業位置為何，其個人資料都會受到處理。

Adobe Experience Cloud代表客戶擔任資料處理者，負責處理其收到和儲存的任何個人資料。 身為資料控管單位，您可以決定要由Adobe Experience Cloud代表您處理和儲存哪些個人資料。

本檔案說明Advertising Cloud Search、Advertising Cloud Creative、Advertising Cloud DSP(Demand Side Platform)和Media Optimizer DCO如何使用Adobe Experience Platform Privacy Service API和Privacy ServiceUI，支援您的資料主體存取GDPR資料和刪除權限。

如需有關GDPR對您業務所代表之意義的詳細資訊，請參閱[GDPR和您的業務](https://www.adobe.com/privacy/general-data-protection-regulation.html)。

## Advertising Cloud支援的資料請求類型

Adobe Experience Platform可讓企業完成下列工作：

* 在[!DNL Search]、[!DNL Creative]、[!DNL DSP]或[!DNL DCO]記憶體取資料主體的Cookie層級資料或裝置ID層級資料（適用於行動應用程式中的廣告）。
* 使用瀏覽器，刪除資料主體在[!DNL Search]、[!DNL Creative]、[!DNL DSP]或[!DNL DCO]中儲存的Cookie層級資料；或使用行動裝置上的應用程式，刪除資料主體在[!DNL DSP]中儲存的ID層級資料。
* 檢查一或所有現有請求的狀態。

## 傳送Advertising Cloud請求的必要設定

若要請求存取和刪除Advertising Cloud的資料，您必須：

1. 部署JavaScript程式庫以擷取和移除您的資料主體Cookie。 所有Adobe Experience Cloud解決方案都會使用相同的程式庫`AdobePrivacy.js`。

   >[!IMPORTANT]
   >
   >對某些Adobe Experience Cloud解決方案的請求不需要JavaScript程式庫，但對Advertising Cloud的請求則需要它。

   您應將程式庫部署在網頁上，資料主體可從此頁面提交存取和刪除請求，例如您公司的隱私權入口網站。 程式庫可協助您擷取AdobeCookie(命名空間ID:`gsurferID`)，以便透過Adobe Experience Platform Privacy Service API在存取和刪除請求時提交這些身分。

   當資料主體要求刪除個人資料時，資料庫也會從資料主體的瀏覽器中刪除資料主體的Cookie。

   >[!NOTE]
   >
   >刪除個人資料與選擇退出不同，退出會停止使用受眾區段來鎖定目標使用者。 不過，當資料主體要求從[!DNL Creative]、[!DNL DSP]或[!DNL DCO]刪除個人資料時，資料庫也會傳送請求給Advertising Cloud，要求退出資料主體的區段鎖定目標。 若為具有[!DNL Search]的廣告商，建議您為資料主體提供[https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html)的連結，說明如何選擇退出對象區段鎖定目標。

1. 識別您的IMS組織ID，並確認已連結至您的Advertising Cloud帳戶。

   IMS組織ID是24個字元的英數字串，並附加@AdobeOrg。 大部分的Adobe Experience Cloud客戶都已獲派IMS組織ID。 如果您的行銷團隊或內部Adobe系統管理員不知道貴組織的IMS組織ID，或不確定是否已布建，請透過gdprsupport@adobe.com聯絡Adobe客戶服務。 您需要IMS組織ID才能將請求提交至隱私權API。

   >[!IMPORTANT]
   >
   >請連絡您公司的Advertising Cloud代表，確認您組織的所有Advertising Cloud帳戶（包括[!DNL DSP]帳戶或廣告商、[!DNL Search]帳戶及[!DNL Creative]或[!DNL DCO]帳戶）皆已連結至您的IMS組織ID。

1. 使用[Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html)（適用於自動請求）或[Privacy ServiceUI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html)（適用於臨機請求），代表資料主體向Advertising Cloud提交存取和刪除請求，並檢查現有請求的狀態。

   若廣告商有行動應用程式可與資料主體互動，並透過DSP啟動行銷活動，則您需要下載適合隱私權的行動SDK以供Experience Cloud。 行動SDK可讓資料控管者設定選擇退出狀態旗標、擷取資料主體的裝置ID(命名空間ID:deviceID)，並將請求提交至Privacy ServiceAPI。 您的行動應用程式需要SDK 4.15.0版或更新版本。

   當您提交資料主體的存取請求時，Privacy ServiceAPI會根據指定的Cookie或裝置ID傳回資料主體的資訊，然後您必須傳回資料主體。

   提交資料主體的刪除請求時，Cookie ID或裝置ID以及與Cookie相關聯的所有成本、點按和收入資料都會從伺服器中刪除。

   >[!NOTE]
   如果您的公司有多個Adobe Experience Cloud Identity Management服務組織ID（IMS組織ID），則您必須分別傳送各個API請求。 不過，您可以對多個Advertising Cloud子解決方案（[!DNL Search]、[!DNL Creative]、[!DNL DSP]及[!DNL DCO]）發出一個API請求，每個子解決方案各一個帳戶。

所有這些步驟對Advertising Cloud都是必要的。 有關使用Adobe Experience Platform Privacy Service執行這些任務和其他相關任務的詳細資訊，以及在何處查找需要的項目，請參閱[www.adobe.io/apis/cloudplatform/gdpr.html](https://www.adobe.io/apis/experienceplatform/gdpr.html)。

## Advertising Cloud JSON請求中的必填欄位值

&quot;&quot;公司上下文&quot;:

* `"namespace": **imsOrgID**`
* `"value":` &lt;>您的IMS組織ID值&#x200B;*>*

`"users":`

* `"key":` &lt;>通常是資料主體的名稱&#x200B;*>*

* `"action":`  `**access**` 或  `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (表示cookie [!DNL adcloud] 空間)

   * `"value":` &lt;>從>擷取的實際資料主體的cookie ID值 `AdobePrivacy.js`**

* `"include": **adCloud**` (適用於請求的Adobe產品)

* `"regulation": **gdpr**` （適用於請求的隱私權法規）

## 資料主體使用從`AdobePrivacy.js`擷取的Advertising Cloud使用者ID提交的請求範例

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

以下是Advertising Cloud的存取回應範例。

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
