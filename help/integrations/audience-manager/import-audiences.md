---
title: 導入Adobe Audience Manager段以進行廣告定位
description: 瞭解如何導入 [!DNL Adobe] 觀眾進入Advertising Cloud DSP，利用Adobe Audience Manager搜索
feature: Integration with Adobe Audience Manager
source-git-commit: 9593400e48f5918850447daacfbdaaa9015e94cd
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# 導入Adobe Audience Manager段以進行廣告定位

Advertising Cloud DSP和Advertising Cloud Search可以分別獲取所有廣告商或廣告公司的元資料、層次結構資料和唯一的受眾資料 [!DNL Adobe] 觀眾<!-- segments or audiences? Standardize terms per AAM's docs -->。 這包括以下資料：

* Adobe Audience Manager段

* Adobe Analytics出版給Adobe Experience Cloud

* 在Adobe Experience Cloud使用 [!DNL People core service]

* 在Adobe Experience Platform建立並通過Audience Manager發送到Advertising Cloud的段

訪問 [!DNL Adobe] 觀DSP眾 [!DNL Creative]，必須將觀眾導入DSP。 訪問 [!DNL Adobe] 觀眾 [!DNL Search]，必須將觀眾導入 [!DNL Search]。

## 先決條件

* 廣告商必須實施 [這樣 [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) 版本2.0或更高版本。 的 [!DNL Identity Service] 提供通用、持久的ID，用於識別Experience Cloud中所有解決方案中的訪問者。

   實施包括添加 [!DNL Identity service] 廣告商網站上每個網頁的代碼。

* 組織必須 [為Experience Cloud服務啟用](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html) 然後Experience Cloud [!DNL Organization ID] (以前稱 [!DNL IMS org ID])。

   的 [!UICONTROL Organization ID] 允許具有多個Adobe Experience Cloud產品的組織在某些產品之間共用資料。

* (具有 [!DNL Analytics])廣告商必須 [實施 [!DNL Analytics] 使用 `appMeasurement.js`](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) 1.6.4版或更高版本。

* 廣告商的網站訪問者不包括大量 [!DNL Apple Safari] 。

* (建議廣告商同時使用Audience Manager和 [!DNL Analytics])要減少對每個網頁的調用，請刪除現有Audience Manager [!DNL Data Integration Library] 用於資料收集的代碼，並為每個代碼啟用伺服器端轉發 [!DNL Analytics] 報告套件。 有關詳細資訊，請參閱「」[伺服器端轉發概述](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html)。

* （推薦）要獲得更高的匹配率，請僅將第一方網站資料發送到Advertising Cloud。 如果廣告商捆綁了來自客戶關係管理系統的第三方資料或離線資料，則資料洩漏可能降低匹配率。

## 將Audience Manager訪問群DSP體

### 將受眾導入到的步DSP驟

的 [!DNL Adobe] 客戶和資料操作團隊將執行以下步驟。

1. 的 [!DNL Adobe] 客戶團隊應配置廣告商級別設定「」[!UICONTROL Adobe Analytics Cloud]&quot;

1. 的 [!DNL Adobe] 客戶小組應提交請求<!-- Submit a request as a JIRA task? --> 到資料操作團隊<!-- implementation team? --> 使用Advertising Cloud DSP本機API整合導入組織的Audience Manager段。

### 什麼變化導致Audience Manager?

API自動：

* 在Audience ManagerDSP中建立兩個目標：

   * **[!UICONTROL Adobe Ad Cloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)])**

* 將兩個目標映射到所有Audience Manager段，使Audience Manager能夠與與同一Experience CloudDSP關聯的廣告商帳戶共用這些段 [!DNL Organization ID] 用於Audience Manager。 <!-- Verify -->

   組織可以根據需要從Audience Manager中的目標中刪除不需要的段。

* 將以下exchange cookie-sync像素添加到組織的Audience Manager容器，以提高客戶活動的覆蓋面：

   * AdobeAdCloud:411 [!DNL Identity Service] 2.0版。具有 [!DNL Identity Service] 2.0以下版本應將此像素添加到其Audience Manager容器中。

## 將Audience Manager受眾導入到 [!DNL Search]

### 將受眾導入到 [!DNL Search]

[!DNL Adobe] 人員將執行以下大部分或全部步驟。

1. 的 [!DNL Adobe] 帳戶團隊應向資料操作團隊提交請求，以設定資料操作團隊之間的整合 [!DNL Search] 和Audience Manager。 包括要導出到的Audience Manager段的名稱 [!DNL Search]。

1. 在Audience Manager中，配置目標 [!DNL Search]:

   1. 建立新目標： `[!UICONTROL Adobe Media Optimizer (HTTP)]` 和 `[!UICONTROL Adobe Media Optimizer Batch Destination]`。

      [!DNL Media Optimizer] 以前是 [!DNL Search]。

   1. 指定每個目標的段。

      使用 [!UICONTROL Automatically map all current and future segments] 選項，每天映射並同步所有段。

      的 [!UICONTROL Manually map segments] 選項允許您手動映射要與批處理目標同步的段(`[!UICONTROL Adobe Media Optimizer Batch Destination]`)。 不需要手動將任何段映射到HTTP目標。

1. 在 [!DNL Search]，或 [!DNL Search] 實施團隊或具有直接訪問客戶端管理員角色的用戶應從 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup]。

   您需要輸入組織的Experience Cloud [!DNL Organization ID] ([!DNL IMS org ID])。 ID必須與用於組織Audience Manager帳戶的ID相同。

### 什麼變化導致Audience Manager?

該組織將看到兩個 [!DNL Search] Audience Manager中的目標：

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination])**

## 資料同步

初始導入大約需要24小時。 初始導入後，資料將即時同步，延遲為1到2秒。

<!--
### How DSP Syncs the Data

DSP syncs the data automatically using the [!DNL Adobe Experience Cloud Identity (ECID) Service]. During synchronization, the [!DNL ECID Service] calls Advertising Cloud at [!DNL cm.eversttech.net]. Because Advertising Cloud is a trusted domain, ID syncs take place from parent pages rather than within the destination publishing iframes, as they do with most third-party activation partners. Audience Manager identifies unique users by device IDs, using the [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html#global-device-ids), also called the [!DNL Device ID].
 
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)

### How Search Syncs the Data
-->

<!-- 
Segment membership data is sent only after one of the following events occurs:

* (Advertisers with DSP):

  * The segment is targeted in an Advertising Cloud display ad.

  * The segment is added to the [!DNL Adobe AdCloud Cross-Channel] batch and real-time destinations within the Audience Manager user interface.

* (Advertisers with [!DNL Search]):

  * The segment is targeted in an Advertising Cloud search ad.

  * The segment is added to the [!DNL Adobe Media Optimizer] batch and HTTP destinations within the Audience Manager user interface.
 -->
<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

## 查找同步段的位置

### 在DSP

在中DSP，段名稱按Audience Manager分類組織，並可與以下中的相應段成員資格計數一起使用：

* [放置設定](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/campaign-management/placements/placement-settings.html?#audience-targeting):在 [!UICONTROL Adobe Segments] 頁籤 [!UICONTROL Audience Targeting] 的子菜單。

* 在 [觀眾設定](/help/dsp/audiences/audience-settings.md):在 [!UICONTROL Adobe Segments] 頁籤。

### 在Advertising Cloud Creative

在 [!DNL Creative]，這些段在目標節點的體驗設定中可用。

### 在 [!DNL Search]

在 [!DNL Search]，在建立 [!DNL Google] 使用 [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]從 [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library]。

每個 [!DNL Google] 你創造的觀眾， [!DNL Google] 為受眾提供大小。

>[!MORELIKETHIS]
>
>* [Advertising Cloud與Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

