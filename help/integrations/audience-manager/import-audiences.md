---
title: 匯入Adobe Audience Manager區段以用於廣告鎖定目標
description: 了解如何匯入 [!DNL Adobe] Advertising DSP和使用Adobe Audience Manager搜尋對象
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%

---

# 匯入Adobe Audience Manager區段以用於廣告鎖定目標

Advertising DSP和 [!DNL Advertising Search] 每個都能提取所有廣告商或代理商的中繼資料、階層資料和不重複對象資料 [!DNL Adobe] 對象<!-- segments or audiences? Standardize terms per AAM's docs -->. 這包括下列項目的資料：

* Adobe Audience Manager區段

* 發佈至Adobe Analytics的Adobe Experience Cloud區段

* 在Adobe Experience Cloud中建立的區段使用 [!DNL People core service]

* 在Adobe Experience Platform中建立並透過Audience Manager傳送至Adobe廣告的區段

若要存取 [!DNL Adobe] DSP或 [!DNL Creative]，您必須將對象匯入DSP。 若要存取 [!DNL Adobe] [!DNL中的對象 [!DNL Search]]，您必須將對象匯入[!DNL [!DNL Search]]。

## 必要條件

* 廣告商必須實作 [the [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) 2.0版或更新版本。 此 [!DNL Identity Service] 提供永續性的通用ID，可識別Experience Cloud中所有解決方案的訪客。

   實作包括新增 [!DNL Identity service] 廣告商網站上每個網頁的程式碼。

* 組織必須 [啟用Experience Cloud服務](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html) 有Experience Cloud [!DNL Organization ID] (先前稱為 [!DNL IMS org ID])。

   此 [!UICONTROL Organization ID] 可讓擁有多個Adobe Experience Cloud產品的組織在部分產品之間共用資料。

* (廣告商與 [!DNL Analytics])廣告商必須 [實施 [!DNL Analytics] 使用 `appMeasurement.js`](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) 1.6.4版或更新版本。

* 廣告商的網站訪客不包含大量 [!DNL Apple Safari] 使用者。

* (若廣告商同時使用Audience Manager和 [!DNL Analytics])若要減少對每個網頁的呼叫，請移除現有Audience Manager [!DNL Data Integration Library] 資料收集的程式碼，並啟用每個程式的伺服器端轉送 [!DNL Analytics] 報表套裝。 如需詳細資訊，請參閱[伺服器端轉送概觀](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

* （建議）若要提高匹配率，請僅傳送第一方網站資料至Adobe廣告。 如果廣告商捆綁來自客戶關係管理系統的第三方資料或離線資料，則資料洩漏可能會降低匹配率。

## 將Audience Manager對象匯入DSP

### 將受眾匯入至DSP的步驟

此 [!DNL Adobe] 帳戶和資料操作團隊將執行下列步驟。

1. 此 [!DNL Adobe] 帳戶團隊應設定廣告商層級的設定「[!UICONTROL Adobe Analytics Cloud].&quot;

1. 此 [!DNL Adobe] 客戶團隊應提交請求<!-- Submit a request as a JIRA task? --> 資料運營團隊<!-- implementation team? --> 若要使用Advertising DSP原生API整合匯入組織的Audience Manager區段。

### 哪些變更會導致Audience Manager?

API會自動：

* 在Audience Manager中建立兩個DSP目的地：

   * **[!UICONTROL Adobe Ad Cloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)])**

* 將兩個目的地對應至所有Audience Manager區段，讓Audience Manager可與相同Experience Cloud相關聯的DSP廣告商帳戶共用區段 [!DNL Organization ID] 用於Audience Manager。 <!-- Verify -->

   組織可選擇從Audience Manager內的目的地移除不需要的區段。

* 將下列exchange Cookie同步像素新增至組織的Audience Manager容器，以改善客戶促銷活動的觸及範圍：

   * AdobeAdCloud:411(此版本為標準，並自動納入 [!DNL Identity Service] 2.0版。具有 [!DNL Identity Service] 2.0版以下的版本應將此像素新增至其Audience Manager容器。

## 將Audience Manager對象匯入至 [!DNL Search]

### 將對象匯入至的步驟 [!DNL Search]

[!DNL Adobe] 人員將執行以下大部分或全部步驟。

1. 此 [!DNL Adobe] 客戶團隊應向資料營運團隊提交請求，以設定 [!DNL Search] 和Audience Manager。 包含您要匯出至的Audience Manager區段名稱 [!DNL Search].

1. 在Audience Manager中，為 [!DNL Search]:

   1. 建立兩個新目的地： `[!UICONTROL Adobe Media Optimizer (HTTP)]` 和 `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] 是 [!DNL Search].

   1. 指定每個目的地的區段。

      使用 [!UICONTROL Automatically map all current and future segments] 選項，則所有區段會每日對應並同步。

      此 [!UICONTROL Manually map segments] 選項可讓您手動對應區段以與批次目的地同步(`[!UICONTROL Adobe Media Optimizer Batch Destination]`)。 不需要手動將區段對應至HTTP目的地。

1. 內 [!DNL Search]，可以是 [!DNL Search] 實作團隊或具有直接存取用戶端管理員角色的使用者應從 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   您需要輸入組織的Experience Cloud [!DNL Organization ID] ([!DNL IMS org ID])。 ID必須與用於組織Audience Manager帳戶的ID相同。

### 哪些變更會導致Audience Manager?

組織將看到兩個 [!DNL Search] Audience Manager中的目的地：

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination])**

## 資料同步

初始匯入約需24小時。 初始匯入後，資料會即時同步，延遲一至兩秒。

<!--
### How DSP Syncs the Data

DSP syncs the data automatically using the [!DNL Adobe Experience Cloud Identity (ECID) Service]. During synchronization, the [!DNL ECID Service] calls Adobe Advertising at [!DNL cm.eversttech.net]. Because Adobe Advertising is a trusted domain, ID syncs take place from parent pages rather than within the destination publishing iframes, as they do with most third-party activation partners. Audience Manager identifies unique users by device IDs, using the [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html#global-device-ids), also called the [!DNL Device ID].
 
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)

### How Search Syncs the Data
-->

<!-- 
Segment membership data is sent only after one of the following events occurs:

* (Advertisers with DSP):

  * The segment is targeted in an Adobe Advertising display ad.

  * The segment is added to the [!DNL Adobe AdCloud Cross-Channel] batch and real-time destinations within the Audience Manager user interface.

* (Advertisers with [!DNL Search]):

  * The segment is targeted in an Adobe Advertising search ad.

  * The segment is added to the [!DNL Adobe Media Optimizer] batch and HTTP destinations within the Audience Manager user interface.
 -->
<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

## 在何處尋找同步的區段

### 在DSP

在DSP中，區段名稱是依Audience Manager分類法組織，並可搭配下列項目中對應的區段成員資格計數使用：

* [版位設定](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting):在 [!UICONTROL Adobe Segments] 的 [!UICONTROL Audience Targeting] 區段。

* 在 [對象設定](/help/dsp/audiences/audience-settings.md):在 [!UICONTROL Adobe Segments] 標籤。

### 廣告創意

在 [!DNL Creative]，則「體驗」設定中會提供目標節點的區段。

### 在 [!DNL Advertising Search]

在[!DNL [!DNL Search]]，當您建立 [!DNL Google] 對象使用 [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]從 [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

針對每個 [!DNL Google] 您建立的受眾， [!DNL Google] 提供對象大小。

>[!MORELIKETHIS]
>
>* [Adobe廣告整合Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

