---
title: 新增功能Advertising Cloud DSP
description: 本頁說明Advertising Cloud DSP中最近變更的新功能。
cloud: Experience Cloud
product: advertising cloud
index: true
exl-id: d4b67393-e8c5-4170-92eb-bcf643ba3ec3
source-git-commit: 8721411c1cd9905d362dff6ea5da39767dcb2c9b
workflow-type: tm+mt
source-wordcount: '1411'
ht-degree: 0%

---

# 新增功能

下列是新功能或最近變更的功能。

<!--  -->

| 日期 | 功能 | 說明 | 如需詳細資訊 |
| ---- | ------- | ----------- | -------------------- |
| 2021年11月12日 | [!UICONTROL Deal IDs] | 在 [!UICONTROL Deal ID] 設定， &quot;[!DNL Rubicon]&quot;已更改為&quot;[!DNL Magnite DV+],&quot;其中 [!DNL DV+] 代表顯示、視訊和其他格式，例如音訊。 這反映了 [!DNL Magnite] SSP。 **注意：** [!DNL Magnite DV+] 仍列為「[!DNL Rubicon]」 [!UICONTROL Deal ID Inbox]. | 請參閱「[SSP合作夥伴](/help/dsp/inventory/ssp-partners.md).&quot; |
| 2021年10月27日 | 自訂報表 | 您現在可以建立和管理 [!DNL Amazon S3] 和不同類型的FTP傳送位置，稱為 *[!DNL report destinations]*，用於自訂報表。 設定報表目的地後，您可以設定每個新的自訂報表，以傳送至單一目的地類型的一或多個位置，或傳送至電子郵件收件者。 更新至 [!DNL Amazon S3] 和FTP憑證不會中斷報表傳送。<br><br>您的現有報表仍會傳送給指定的電子郵件收件者。 若要設定傳送至不同報表目的地，請使用新目的地建立新報表。 | 請參閱「[關於 [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md), &quot;[建立 [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md), &quot;[[!UICONTROL Report Destination] 設定](/help/dsp/reports/report-destinations/report-destination-settings.md),&quot;和&quot;[自訂報表設定](/help/dsp/reports/report-settings.md).&quot; |
|  | [!UICONTROL Packages], [!UICONTROL Placements]，和 [!UICONTROL Ads] 檢視 | 當您檢視單一天的資料時，趨勢圖現在會包含每小時資料。 將游標停留在任一點上，即可查看該小時的資料。 | 請參閱「[單一促銷活動報告](/help/dsp/campaign-management/reports/campaign-reports-about.md#single-campaign-reporting).&quot; |
|  | [!UICONTROL Placements] | 版位 [!UICONTROL Inspector] 現在包含 [!UICONTROL Inventory] 標籤中，此標籤會顯示所有交易及其投放位置的相關量度。 使用資訊進行快速調整或疑難排解問題，而不產生自訂報表。 | 請參閱「[版位 [!UICONTROL Inspector]](/help/dsp/campaign-management/reports/campaign-reports-about.md#placement-inspector).&quot; |
|  | [!UICONTROL Ads] | (具有包含 [!DNL Clearcast] 廣告中的時鐘數)如果您使用附加至其他廣告的時鐘數，DSP不再顯示錯誤。 **注意：**  最佳實務是為每個視訊廣告使用唯一的時鐘號碼。 否則，發佈者不會核准所有廣告。 | — |
|  | [!UICONTROL Deal IDs] | 此 [!UICONTROL Deal ID] 設定和使用者介面中的其他位置會反映 [!DNL Magnite] SSP:<br><ul><li>SSP &quot;[!DNL Tremor]&quot;([!DNL Telaria])現在為「[!DNL Magnite CTV].&quot;</li><li>在接下來的幾週裡， [!DNL Rubicon]&quot;將更改為&quot;[!DNL Magnite DV+],&quot;其中 [!DNL DV+] 代表顯示、視訊和其他格式，例如音訊。</li></ul> | 請參閱「[SSP合作夥伴](/help/dsp/inventory/ssp-partners.md).&quot; |
|  | [!DNL Freewheel] 程式保證的交易 | 您現在可以提交廣告，並檢查廣告的狀態 [!DNL Freewheel] 程式保證的交易 [!UICONTROL Ads] 檢視。 以前，您只能透過 [!UICONTROL Deals] 檢視。 | 請參閱「[提交程式化保證交易的廣告以 [!DNL Freewheel]](/help/dsp/inventory/freewheel-submit.md)&quot;和&quot;[檢查廣告的狀態 [!DNL Freewheel] 程式化保證交易](/help/dsp/inventory/freewheel-check-status.md).&quot; |
| 2021年10月7日 | 說明 | 全部 [DSP和其他Advertising Cloud檔案](https://experienceleague.adobe.com/docs/advertising-cloud.html) on [!DNL Experience League] 現在，機器已翻譯成所有可用語言。 若要變更顯示的語言，請使用任何頁面左下角的「變更語言」功能表。<br>![變更語言](/help/dsp/assets/change-language.png) |
| 2021年9月30日 | 品牌安全 | （9月22日發行） [!DNL DoubleVerify] 品牌安全預先出價產品更新至 [!DNL Brand Suitability Tiers]，廣告商可針對特定區段在三個風險等級（低、中、高）之間進行選擇，而不會避免特定主題的所有例項。 在過去，段不包含任何容差級別。<br><br>與新 [!DNL DoubleVerify] 區段結構，DSP會將您現有的品牌安全區段移轉至新的建議 *媒體*-level段。 您可以選擇將區段層調整為 *low* 或 *高*.<br><br>**注意：** 一小組區段沒有層級，但有新名稱，例如「滋擾/間諜軟體/惡意軟體、Warez」>「激勵/惡意軟體/凌亂」。 | — |
|  | 最佳化 | 已棄用下列最佳化目標和出價前篩選器：<ul><li>最佳化目標：<ul><li>[!UICONTROL Always Max Bid & Highest Viewability Rate (Moat – GroupM)]</li><li>[!UICONTROL Always Max Bid & Highest Viewability Rate (Moat – MRC)]</li></ul><li>預先出價篩選目標：<ul><li>[!UICONTROL Viewability IAS]</li><li>[!UICONTROL Viewability Moat]</li></ul></ul> | 請參閱「[最佳化目標及其使用方式](/help/dsp/optimization/optimization-goals.md)&quot;和&quot;[版位層級出價前篩選器及其使用方法](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot; |
| 2021年9月28日 | 行銷活動管理檢視 | A &quot;[!UICONTROL Creation date]「 」欄現在可用於 [!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements]，和 [!UICONTROL Ads] 檢視。 您也可以篩選 [!UICONTROL Placements] 和 [!UICONTROL Ads] 檢視次數 [!UICONTROL Creation date]. | 請參閱「[建立自訂欄檢視](/help/dsp/campaign-management/reports/column-view-create.md)&quot;和&quot;[篩選促銷活動資料](/help/dsp/campaign-management/reports/campaign-data-filter.md).&quot; |
|  | 程式擔保交易 | （9月8日發行）您現在可以編輯 [!UICONTROL Max Bid] 程式化保證(PG)交易的預設位置。 不過，由於PG交易一律有固定CPM，因此只有國際客戶才應編輯 [!UICONTROL Max Bid] 將貨幣兌換費納入考慮。 | — |
|  |  | （9月8日發行）具有[!DNL FreeWheel Programmatic Guaranteed]「權限現在可以將廣告提交至 [!DNL FreeWheel Programmatic Creative API] 從 [!UICONTROL Ads] 檢視或 [!UICONTROL Placements] 檢視。 您仍可從 [!UICONTROL Deals] 檢視。 | —<!-- Add link to page on submitting ads to Freewheel once it's edited. --> |
| 2021年8月11日 | 預先出價的可檢視性 | 競標前可檢視性篩選來自 [!DNL Oracle Advertising (Moat)] 現在可供您的版位使用。 | 查看更多關於 [協力廠商整合以提供出價前的可檢視性](/help/dsp/introduction/features/brand-safety-media-quality.md#pre-bid-viewability) 和[版位層級出價前篩選器及其使用方法](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot; |
| 7月15日 | 說明 | 新增了有關Advertising Cloud DSP如何為客戶帳戶購買媒體和服務的詳細資訊。 | 請參閱「[帳戶資金](/help/dsp/introduction/billing/account-funding.md).&quot; |
| 2021年6月12日 | 說明 | 已更新廣告原則。 | 請參閱「[Adobe Advertising Cloud廣告需求政策](/help/policies/ad-requirements-policy.md).&quot; |
| 2021年6月7日 | 說明 | 使用程式化保證交易與發佈商在 [!DNL FreeWheel]. | 請參閱「[在中設定程式化保證交易概覽 [!DNL FreeWheel]](/help/dsp/inventory/freewheel-overview.md), &quot;[提交程式化保證交易的廣告以 [!DNL FreeWheel]](/help/dsp/inventory/freewheel-submit.md), &quot;[檢查廣告的狀態 [!DNL Freewheel] 程式化保證交易](/help/dsp/inventory/freewheel-check-status.md),&quot;和&quot;[的錯誤代碼 [!DNL FreeWheel] 廣告提交](/help/dsp/inventory/freewheel-error-codes.md).&quot; |
| 2021年5月27日 | 說明 | 可接受的健康相關受眾區段和策略提供准則，以作為鎖定健康相關受眾區段的替代方案。 | 請參閱「[可接受的健康區段指南](/help/policies/health-segment-guidelines.md).&quot; |
| 2021年5月26日 | 說明 | 「與Adobe Experience Cloud整合」章節現在是個別指南，可從 [Advertising Cloud檔案首頁](https://experienceleague.adobe.com/docs/advertising-cloud.html). 新指南包含新的子章節「在 [!DNL Analytics Marketing Channels].&quot;<br>本DSP指南的目錄包含新指南的連結。 | 請參閱「[與Adobe Experience Cloud整合](/help/integrations/home.md).&quot; |
| 2021年5月24日 | 說明 | 在「促銷活動管理」章節中，提供新主題，說明如何使用Excel QA試算表，檢閱及編輯促銷活動的關鍵位置設定。 | 請參閱「[關於使用試算表更正促銷活動的位置設定](/help/dsp/campaign-management/qa/qa-about.md), &quot;[下載行銷活動的版位設定](/help/dsp/campaign-management/qa/qa-sheet-download.md), &quot;[行銷活動的上傳位置設定](/help/dsp/campaign-management/qa/qa-sheet-upload.md)，和[已下載/已上載電子錶格中的列](/help/dsp/campaign-management/qa/qa-sheet-columns.md). |
| 2021年5月5日 | 套件設定 | 提供新的步調填滿策略選項「稍微提前」，這是新包的預設選項。 此策略可加快傳送速度，使其在飛行期間完成55-65%。 | 請參閱「[套件設定](/help/dsp/campaign-management/packages/package-settings.md).&quot; |
| 2021年3月17日 | 說明 | 「促銷活動管理」章節已擴充，加入更多程式和參考。 | 在目錄中，開啟「促銷活動管理」章節和子區段。 |
| 2021年3月10日 | 庫存 | 您無法再建立 [!UICONTROL Smart Ad Serving] 使用VAST標籤的交易。 相反地，請詢問您的發行者是否可透過交易ID執行您的私人交易。 您可以使用 [!UICONTROL Deal ID inbox] 或手動輸入交易詳細資訊。<br><br>您現有的智慧廣告服務交易仍可供使用，但今年晚些時候將停止。 | 請參閱「[關於 [!UICONTROL Deal ID inbox]](/help/dsp/inventory/deal-id-inbox-about.md)&quot;和&quot;[手動建立 [!UICONTROL Deal ID] 詳細資料](/help/dsp/inventory/deal-id-create.md)&quot; |
| 2021年2月25日 | 說明 | 關於 [!DNL Analytics for Advertising Cloud]，已整合Adobe Analytics和Adobe Advertising Cloud，現已推出。 | 如需整合的概觀，請參閱[概觀 [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md).&quot; 如需完整檔案，請參閱「與Adobe Experience Cloud整合」>「[!DNL Analytics for Advertising Cloud].&quot; |
| 2020年10月28日 | 新增說明 | 舊版說明已更換為更新頁面，您可以透過 [!DNL DSP] 主功能表，也可隨時從 [https://experienceleague.adobe.com/docs/advertising-cloud/dsp/home.html](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/home.html). | — |
|  | 行銷活動 | 上一個 [!UICONTROL Campaigns Beta] 檢視現在為預設 [!UICONTROL Campaigns] 檢視，提供更快速的深入分析、簡化的工作流程和自訂檢視。<br><br>新 [!UICONTROL Campaigns] 檢視包括：<ul><li>新導覽。 您可以檢視帳戶內所有促銷活動的清單。 在促銷活動中，您可以根據促銷活動實體篩選資料： [!UICONTROL Packages], [!UICONTROL Placements]，和 [!UICONTROL Ads].<br><br>![促銷活動實體索引標籤](/help/dsp/assets/campaign-subtabs.png)</li><li>最多可比較三個量度的資料視覺效果。<br><br>![三個度量的獨立趨勢圖](/help/dsp/assets/trend-chart-separate.png)</li><li>使用預先定義的功能，建立和管理自訂欄檢視 [!UICONTROL Pacing] 和 [!UICONTROL Performance] 檢視。<br><br>![欄檢視選取器](/help/dsp/assets/column-view-selector.png)</li><li>升級搜尋和篩選。</li></ul><br>舊版 [!UICONTROL Campaigns Classic] 檢視仍可從右上方的「設定檔」功能表使用。 若要開啟 [!UICONTROL Campaigns Classic] 檢視，按一下 **[!UICONTROL Switch to Campaigns Classic]**.<br><br>![連結至 [!UICONTROL Campaigns Classic]](/help/dsp/assets/switch-campaigns-classic.png)<br><br>若要返回 [!UICONTROL Campaigns] 首頁，按一下 **[!UICONTROL Exit Classic]**. | 請參閱「[關於平台內報表](/help/dsp/campaign-management/reports/campaign-reports-about.md).&quot;<br><br>另請參閱「[關於促銷活動資料檢視](/help/dsp/campaign-management/reports/campaign-data-views-about.md).&quot; |
|  | 版位 | 包含手動競標規則的選項已移除，讓DSP最佳化可為您執行工作。 現在會自動最佳化以最近一次為基礎的所有現有「最大出價」。 | — |
|  |  | 為了改善整體效能，您無法再以檢視器的時區為基礎進行日時分段。 現在，所有時段劃分都是根據促銷活動的時區&#x200B;。 | 請參閱「[版位設定](/help/dsp/campaign-management/placements/placement-settings.md).&quot; |
| 2020年10月15日 | 私人詳細目錄 | 所有使用者現在都可以使用新交易ID表單來設定及編輯交易ID詳細資訊，此表單是舊版的簡化版本 [!UICONTROL Smart Ad Serving] 表單。 若要設定新交易ID詳細資訊，請前往 [!UICONTROL Inventory] > [!UICONTROL Deals]，按一下 [!UICONTROL Create]，然後按一下 [!UICONTROL Deal ID Beta]. | 請參閱「[手動建立交易ID詳細資訊](/help/dsp/inventory/deal-id-create.md)&quot;和&quot;[手動交易ID設定](/help/dsp/inventory/deal-id-settings.md).&quot; |
|  | 版位預測 | 若刊登版位具有刊登版位層級步調， [!UICONTROL Forecast] 版位設定的區段包含新 [!UICONTROL Estimated Maximums] 區段，指出目前定位設定有多少容量可用。 | — |
| 2020年9月2日 | 報表 | 任何具有多個DSP帳戶的組織均可根據組織的需求，選擇在自訂報表中啟用跨帳戶資料。 | 請參閱「[關於自訂報表](/help/dsp/reports/report-about.md#cross-account-reporting).&quot; |

{style=&quot;table-layout:auto&quot;}
