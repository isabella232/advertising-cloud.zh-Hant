---
title: 傳送DSP媒體曝光資料至Adobe Audience Manager概述
description: 了解如何使用Audience Manager事件像素，擷取Advertising DSP行銷活動的曝光層級和點擊層級資料
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# 傳送DSP媒體曝光資料至Adobe Audience Manager概述

*僅具有Advertising DSP的廣告商*

*廣告商與Adobe廣告 — 僅Adobe Audience Manager整合*

擁有Adobe Audience Manager的Advertising DSP客戶可使用Audience Manager事件像素，擷取DSP促銷活動的曝光層級資料和點按層級資料。 事件像素會將資料當作可操作的訊號傳送至Audience Manager。 這些訊號會啟用各種DSP使用案例，例如更進階的細分、頻率管理、行銷分析和報表深入分析。

DSP不會向您收費，將這些訊號傳送至Audience Manager。 不過，您需根據您的Audience Manager合約，根據伺服器呼叫支付標準Audience Manager擷取成本。 Audience Manager會移除以兩種不同方式追蹤的重複事件，因此每個事件只需計費一次。

>[!NOTE]
>
> Audience Manager也支援從廣告伺服器記錄檔擷取資料，因此提供的彈性較低。 本檔案未涵蓋該程式。

## 主要優點

* DSP促銷活動資料會即時流入Audience Manager，而您可以用它來建立用於定義群體的規則型特徵。

* 區段可在使用者特徵和區段資格後立即用於鎖定目標，進而支援即時鎖定目標工作。

* 您可以針對創意素材的頻率限定、重新鎖定前次公開促銷活動的使用者，以及分析下游網站行為和登入點等使用案例，運用促銷活動資料。

* 匯總的資料可提供促銷活動績效的統一檢視，有助於識別自訂轉換路徑，且可用來改善透過Audience Manager導致轉換的事件順序 [!DNL Audience Optimization Reports] 或透過 [[!DNL Audience Analytics] 整合Adobe Analytics](/help/integrations/audience-manager/audience-analytics.md).

## 資料的追蹤方式

Audience Manager曝光次數和點按事件像素是以Cookie為基礎。 像素不會擷取在無Cookie環境(例如行動應用程式和連線電視(CTV))中發生的事件。

### 曝光追蹤像素

Audience Manager會在您附加1xl像素透明事件追蹤像素至廣告時追蹤廣告的曝光資料。 每次向使用者提供廣告並由網頁瀏覽器載入時，都會載入事件像素。 像素是從用戶端專屬的子網域載入 [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html)，此為舊版的Audience Manager網域，包含作為機碼值組的參數。 事件呼叫會收集曝光數和轉換資料，並傳送至Audience Manager資料收集伺服器。

### 點擊追蹤像素

Audience Manager追蹤點按的方式與曝光數類似，只是每次提供廣告時不會載入透明事件像素。 而是會在廣告的點進URL中追蹤點按資料。 廣告指向的用戶端專屬子網域 [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html)，此為舊版的Audience Manager網域，供Audience Manager資料收集伺服器處理。 然後，伺服器會將使用者重新導向至預期的登陸頁面。 URL包含作為機碼值組的參數。

>[!NOTE]
>
>如果貴組織使用 [!DNL Analytics] 追蹤，則您可能不需要Audience Manager點擊追蹤。 Adobe Analytics會擷取點擊訊號，並可將其傳送至Audience Manager [伺服器端轉送](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

>[!MORELIKETHIS]
>
>* [從Advertising DSP促銷活動收集點按和曝光資料](collect.md)
>* [使用案例](use-cases.md)

