---
title: '[!UICONTROL Simple Ad Serving] 交易設定'
description: 瞭解的可用設定 [!UICONTROL Simple Ad Serving] 交易。
feature: DSP Simple Ad Serving
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] 交易設定

## 新建 [!UICONTROL Simple Ad Serving] 交易

### [!UICONTROL Select Ad Source]

| 參數 | 說明 |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | 此交易的媒體類型： *[!UICONTROL Video]。* *[!UICONTROL Display]。* 或 *[!UICONTROL Audio]。* |
| **[!UICONTROL Publisher Site Served On]** | 銷售此庫存的發佈者的名稱。 通過在名稱中至少輸入前兩個字元來搜索發佈者。 要添加未列出的發佈者，請與 [!DNL Adobe] 客戶團隊。 |
| **[!UICONTROL Advertiser]** | 可以訪問此交易的客戶中的單個廣告商。 另選市場活動和（可選）交易可用的包。 |
| **[!UICONTROL Media Quality Assessment?]** | （某些用戶）允許廣告在另一個上運DSP行以進行第三方驗證。 <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | 唯一的選擇是 *[!UICONTROL Site Serve (Event Pixels)]*。 |
| **[!UICONTROL Ad Creation]** | （僅限新交易）是否：<ul><li>*[!UICONTROL Create New]:* 為此交易建立廣告。</li><li>*[!UICONTROL Select Ads]:* 將現有廣告用於此交易。</li></ul> |
| **[!UICONTROL Ad Type]** | 此交易的廣告類型。 如果要為交易建立新廣告，請根據要求包括廣告大小或持續時間。 可用選項因介質類型而異。 |

{style=&quot;table-layout:auto&quot;&quot;

### [!UICONTROL Select Ad(s)]

（當您使用現有廣告時）要包含在交易中的廣告。 選中要包括的每個廣告旁邊的複選框。

### [!UICONTROL Select & Upload [Media Type]]

（僅限新廣告）用於建立新廣告的螢幕 [第一方廣告](/help/dsp/campaign-management/ads/ad-create.md) 或 [第三方廣告](/help/dsp/campaign-management/ads/ad-create-third-party.md)。

### [!UICONTROL Feed Details]

| 參數 | 說明 |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | 每千次印數(CPM)的成本，如合同的費率卡中所反映。 聯繫您 [!DNL Adobe] 此值的帳戶團隊。 <br><br>另指定交易的幣種。 所有用戶都可以選擇USD，或者，如果SSP支援其他貨幣，則選擇帳戶的DSP貨幣。 |
| **[!UICONTROL Third Party Billed Fees]** | （可選）要作為不可開單成本跟蹤的靜態第三方費用和交易幣種。<br><br>所有用戶都可以選擇USD，或者，如果SSP支援其他貨幣，則選擇帳戶的DSP貨幣。 **注：** 計費費用反映於 [!UICONTROL Net CPM] 度量。 |
| **[!UICONTROL Third Party Fee Description]** | （可選）第三方費用的說明。 |
| **[!UICONTROL Flight Dates]** | 使用此交易的流量的開始和結束日期。 航班日期必須包括在促銷航班日期中。 廣告標籤將僅在指定飛行期間返迴響應。<br><br> 最好的做法是建立一個單獨的簡單廣告服務市場活動，持續時間為一年，並在其中構建跟蹤像素。 |
| **[!UICONTROL Impressions]** | （可選）您預計使用此交易運行的印數估計數。 此值僅用於跟蹤目的，用於在達到交付目標時標籤；發佈者控制實際廣告遞送。 最佳做法是輸入大量印數，使標籤保持活動狀態，DSP以便在需要時可以更新或擴展標籤。 |
| **[!UICONTROL Deal Name]** | 交易名稱。 輸入名稱或選擇 *[!UICONTROL Auto Generate Deal Name]* 以便根DSP據交易詳細資訊生成名稱。<br><br>自動生成的名稱示例： `Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | （只讀）交易中的廣告。 要編輯廣告，請按一下廣告名稱。 要從交易中刪除廣告，請按一下 **[!UICONTROL X]** 地址欄。 |

{style=&quot;table-layout:auto&quot;&quot;

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
>* [查看事件跟蹤像素 [!UICONTROL Simple Ad Serving] 交易](simple-deal-show-pixels.md)

