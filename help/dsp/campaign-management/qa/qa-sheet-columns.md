---
title: 已下載/已上載電子錶格中的列
description: 參考下載和上傳的Excel QA試算表中的欄。
feature: DSP Placements
exl-id: 8a8dceed-f77d-4b6b-a842-f57528125c92
source-git-commit: 6a0e9f1888da7b5fca28f69ef1320910a2a49fa0
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 已下載/已上載電子錶格中的列

<!-- rename -- not specific enough - I think you can download Excel files of other things too -->

<!-- see notes within the table about descriptions that need to be edited -->

>[!TIP]
>
> 在下載的試算表中，所有可編輯的欄都會以藍色強調顯示。

| 區段 | 欄 | 說明 | 可編輯？ |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | 版位的數值ID。 | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | 版位的名稱。 | 是 |
| [!UICONTROL Basic] | [!UICONTROL Labels] | 任何已套用的標籤，用於報告。 | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | 在「編輯」模式中開啟放置的連結。 | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | 版位狀態： *[!UICONTROL active]* 或 *[!UICONTROL inactive]*. | 是 |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | 版位類型。 | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | 父包的名稱（如果適用）。 | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | 版位的開始日期。 | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | 投放的結束日期。 | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | 日時段是否為 *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*.<br><b>注意：</b> 若要檢查實際的日分段排程，請開啟 [!DNL DSP]. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | 版位預算（如果有）。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | 預算間隔： &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*，或 *[!UICONTROL All Time]*.[!UICONTROL >Daily] | 是 |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | 包的目標。 | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | 目標的目標值。 | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | 版位是否正朝 *[!UICONTROL Budget]* 或 *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | 版位的最高出價。 | 是 |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | 投放的飛行步調策略： *[!UICONTROL evenly]*, * *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*，或 *[!UICONTROL aggressive frontload]*. | 是 |
| [!UICONTROL Goals] | [!UICONTROL  Pre-Bid Filters] | 要套用的任何出價前篩選條件。 | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | 競標規則（已廢止）是否 *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | 指定期間放置的主頻率上限 [!UICONTROL Frequency Cap Interval]. | 是 |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | 主頻上限的間隔： *[!UICONTROL Day]*, *[!UICONTROL Week]*，或 *[!UICONTROL Month]*. | 是 |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | 指定期間放置的次頻蓋 [!UICONTROL Secondary Frequency Cap Interval] | 是 |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | 次頻上限的間隔類型： *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*，或 *[!UICONTROL Minute]*. 適用的周數、天數、小時數或分鐘數以 [!UICONTROL Secondary Frequency Cap Interval Value]. | 是 |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | 周數、天數、小時數或分鐘數 [!UICONTROL Secondary Frequency Cap] 的URL。 例如，如果次要次數上限是每六小時三次曝光次數，則此處的值會是 <b>6&lt;/>。 | 是 |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | 目標地理位置的數量， *[!UICONTROL All]*，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | 目標地理位置，以分號分隔，或 *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | 排除的地理位置或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | 排除的地理位置，以分號分隔，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | 已指定目標公共庫存交易的數量（如果有） *[!UICONTROL All]*，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | 已排除的公用庫存交易數（如果有指定），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | 已指定目標私人庫存交易的數量（如果有）, *[!UICONTROL All]*，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | 已排除的私人庫存交易數（如果有指定），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | 目標數量 [!UICONTROL On-Demand Inventory] 交易，如有， *[!UICONTROL All]*，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | 已排除的按需庫存交易（如果有）的數量，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | 流量的目標類型： *[!UICONTROL Website]* 和/或 *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | 排除流出流流量的庫存鎖定目標選項是否為 &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*或 *[!UICONTROL OFF]*.[!UICONTROL >ON]<br>外流廣告通常在內容上顯示為快顯視窗或填入內容（在原生體驗中），而非視訊播放器中的一般視訊廣告。 | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | 要定位的網站品質： *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]*，或 *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | 目標網站類別（如果有指定）的數量，或 *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | 已排除的網站類別（如有指定）的數量，或 *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | 排除的網站（如果有指定），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | 目標網站語言。 | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | （僅限標準顯示版位）是否允許在非稽核的網站上傳送廣告： *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*. 當版位鎖定私人詳細目錄時，此選項可能會在封鎖的網站上傳送廣告。 | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | 已指定的目標網站數，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | 目標對象（若有），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | 已排除的對象（如果有），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | 無論 [!DNL Comscore] 已針對版位（和促銷活動中的其他版位）啟用人口統計區段： *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*. 此功能僅可針對 [!DNL Audience Verification] 功能 [!DNL Nielsen] 和/或 [!DNL Comscore].  這會產生額外的費用。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | 是否要跨裝置延伸廣告鎖定目標： *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*. 跨裝置鎖定目標會根據促銷活動設定中指定的裝置圖表，將您的鎖定目標延伸至人員的所有已知裝置。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting]  — 包含# | 目標主題代碼（如果有指定）的數量，或 *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | 已排除的主題代碼數（如果有指定），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | 已指定的目標設備目標數，或 *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | 已排除的設備目標（如果有）的數量，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | 目標ISP提供商（如果有）的數量，或*[!UICONTROL All]/i>。 | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | 已排除的ISP提供者數量（若有），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | 已套用的品牌安全篩選器（若有指定）的數量，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | 已套用的競標前欺詐封鎖篩選器數量（若有），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | 已套用的競標前可檢視性篩選條件數（若有），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | 是否啟用站點安全塊： *[!UICONTROL ON]* 或 *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | 附加至版位的第三方事件追蹤像素數，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | 附加至版位的轉換追蹤像素數，或 *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | 靜態的第三方費用率，可以作為每1000次曝光的不計費成本（如果適用）進行跟蹤。 | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | 附加至版位的廣告數（如果有的話），或 *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | 附加至版位的廣告名稱（如果有），或 *[!UICONTROL None]*. | — |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [關於使用試算表更正促銷活動的位置設定](qa-about.md)
>* [下載行銷活動的版位設定](qa-sheet-download.md)
>* [行銷活動的上傳位置設定](qa-sheet-upload.md)
>* [版位設定](/help/dsp/campaign-management/placements/placement-settings.md)

