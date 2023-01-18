---
title: '[!UICONTROL Simple Ad Serving] 交易設定'
description: 了解 [!UICONTROL Simple Ad Serving] 交易。
feature: DSP Simple Ad Serving
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 1%

---

# [!UICONTROL Simple Ad Serving] 交易設定

## 新增 [!UICONTROL Simple Ad Serving] 交易

### [!UICONTROL Select Ad Source]

| 參數 | 說明 |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | 此交易的媒體類型： *[!UICONTROL Video],* *[!UICONTROL Display],* 或 *[!UICONTROL Audio].* |
| **[!UICONTROL Publisher Site Served On]** | 銷售此庫存的發佈商的名稱。 在名稱中至少輸入前兩個字元，以搜尋發佈者。 若要新增未列出的發佈者，請連絡您的 [!DNL Adobe] 客戶團隊。 |
| **[!UICONTROL Advertiser]** | 帳戶中可存取此交易的單一廣告商。 也選擇交易可用的促銷活動和（可選）包。 |
| **[!UICONTROL Media Quality Assessment?]** | （部分使用者）讓廣告可在其他DSP上執行，以進行協力廠商驗證。 <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | 唯一的選項是 *[!UICONTROL Site Serve (Event Pixels)]*. |
| **[!UICONTROL Ad Creation]** | （僅限新交易）是否：<ul><li>*[!UICONTROL Create New]:* 為此交易建立廣告。</li><li>*[!UICONTROL Select Ads]:* 為此交易使用現有廣告。</li></ul> |
| **[!UICONTROL Ad Type]** | 此交易的廣告類型。 如果您要為交易建立廣告，請根據要求包含廣告大小或持續時間。 可用的選項因介質類型而異。 |

{style=&quot;table-layout:auto&quot;}

### [!UICONTROL Select Ad(s)]

（當您使用現有廣告時）要包含在交易中的廣告。 選取每個要包含的廣告旁的核取方塊。

### [!UICONTROL Select & Upload [Media Type]]

（僅限新廣告）建立新廣告的畫面 [第三方廣告](/help/dsp/campaign-management/ads/ad-create-multiple.md).

### [!UICONTROL Feed Details]

| 參數 | 說明 |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | 每1000次曝光(CPM)的成本，反映在合約的費率卡上。 請連絡您的 [!DNL Adobe] 帳戶團隊取得此值。 <br><br>也指定交易的貨幣。 所有使用者都可以選取美元，或者，如果SSP支援其他貨幣，則可以選取DSP帳戶的貨幣。 |
| **[!UICONTROL Third Party Billed Fees]** | （可選）要以不計費成本和交易貨幣來跟蹤的靜態第三方費用。<br><br>所有使用者都可以選取美元，或者，如果SSP支援其他貨幣，則可以選取DSP帳戶的貨幣。 **注意：** 可結算費用反映於 [!UICONTROL Net CPM] 量度。 |
| **[!UICONTROL Third Party Fee Description]** | （選用）協力廠商費用的說明。 |
| **[!UICONTROL Flight Dates]** | 使用此交易的流量的開始和結束日期。 投放日期必須包含在促銷活動投放日期中。 廣告標籤只會在指定的投放期間傳回回應。<br><br> 最佳實務是建立持續一年的個別簡單廣告服務促銷活動，並在其中建立追蹤像素。 |
| **[!UICONTROL Impressions]** | （可選）使用此交易預計要執行的曝光次數。 此值僅用於追蹤目的，以及在達到傳送目標時加以標幟；發佈者會控制實際的廣告傳送。 最佳作法是輸入大量曝光數，讓標籤在DSP內保持作用中，以便視需要更新或延長標籤。 |
| **[!UICONTROL Deal Name]** | 交易名稱。 輸入名稱，或選擇 *[!UICONTROL Auto Generate Deal Name]* 讓DSP根據交易詳細資訊產生名稱。<br><br>自動產生的名稱範例： `Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | （唯讀）屬於交易一部分的廣告。 若要編輯廣告，請按一下廣告名稱。 若要從交易中移除廣告，請按一下 **[!UICONTROL X]** 廣告名稱旁邊。 |

{style=&quot;table-layout:auto&quot;}

<!-- 
## Existing Simple Ad Serving Deals

Changes aren't applied retroactively.
-->

<!-- completely different settings layout, so need a separate section for them -->

<!-- From Abhinav: Editable fields are Name, Start & End date, Impressions & CPM. Changes are not applied retroactively.

But I see:

| Parameter | Description |
|-----------|-------------|

| **[!UICONTROL Are you using Deal ID?] | (Read-only) Whether the deal was set up as a [!UICONTROL Deal ID] (*[!DNL Yes]*)  or a [!UICONTROL Simple Ad Serving] deal (*[!DNL No]*). |
| **[!UICONTROL Inventory Type] | (Read-only) The inventory type for the deal. |
| **[!UICONTROL Feed Name] | The name of the [!UICONTROL Simple Ad Serving] deal. |
| **[!UICONTROL Publisher Ad Server] | (Read-only)  |
| **[!UICONTROL Publisher maximum ad length] | The maximum length of the ad, per the publisher. |
| **[!UICONTROL Publisher minimum ad length] | The minimum length of the ad, per the publisher. |
| **[!UICONTROL Fill Type] | (Read-only)  |
| **[!UICONTROL Contracted CPM] | This field is required if billing through TubeMogul, but enter your CPM in this field to track your actual spend. |
| **[!UICONTROL 3rd party technology CPM] | (Optional)  |
| **[!UICONTROL Planned Flight Dates] | The beginning and end dates for the deal flight. These dates don't control ad delivery but are used to track delivery pacing. **THIS IS CONTRARY TO WHAT THE NEW DEAL SETTINGS ABOVE, FROM ABHINAV, SAY**> |
| **[!UICONTROL Target Impressions] | (Optional) The estimated number of impressions you expect to run using this deal. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
 -->

>[!MORELIKETHIS]
>
>* [關於 [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [建立 [!UICONTROL Simple Ad Serving] 交易](simple-deal-create.md)
>* [編輯 [!UICONTROL Simple Ad Serving] 交易設定](simple-deal-edit.md)
>* [查看交易的詳細報表](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
