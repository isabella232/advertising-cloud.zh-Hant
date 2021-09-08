---
title: 自訂報表設定
description: 請參閱自訂報表設定的說明。
feature: Custom Reports
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---


# 自訂報表設定

**[!UICONTROL Name]** 報表名稱。長度上限為180個字元。

**[!UICONTROL Report Type]** 報表類型： *[!UICONTROL Custom]* （包含最多可用選項）、  *[!UICONTROL Billing]*、  *[!UICONTROL Conversion]*、  *[!UICONTROL Device]*、  *[!UICONTROL Frequency (by Impression)]*、   *[!UICONTROL Frequency (by App/Site)]*、  *[!UICONTROL Geo]*、  *[!UICONTROL Margin]*、  *[!UICONTROL Media Performance]*、   *[!UICONTROL Segment]*&#x200B;或 *[!UICONTROL Site]*。

## [!UICONTROL Apply Filters] 區段

**[!UICONTROL Timezone]:** 報表的時區。

**[!UICONTROL Observe Daylight Savings Time]:** 考量日光節約時間在報告的時間內。

**\[日期範圍\]:** 要產生資料的日期範圍。可用天數依報表和選取的維度而異。 選擇一個：

* **[!UICONTROL Previous N days]:** 包含今天之前特定天數的資料。

* **[!UICONTROL Custom]:** 包括特定開始和結束日期之間的資料。要報告前一天的資料，請選擇&#x200B;**[!UICONTROL Present]**。

* **[!UICONTROL Last Calendar Month]:** 包含上個日曆月的資料。

**[!UICONTROL Add Filters]:** （選用）要篩選資料的其他維度，無論維度是否要納入報表中列為欄： *[!UICONTROL Account]*、\*  *[!UICONTROL Advertiser]*、  *[!UICONTROL Campaign]*、  *[!UICONTROL Placement]*、  *[!UICONTROL Ad]*、  *[!UICONTROL Ad Type]*、  *[!UICONTROL Video]*、  *[!UICONTROL Video Duration]*、  *[!UICONTROL Country]*&#x200B;和 *[!UICONTROL Package]*。

\* *[!UICONTROL Account]*&#x200B;只有當您的組織設定為[跨帳戶報表](report-about.md#cross-account-reporting)時，才適用於下列報表類型： [!UICONTROL Custom]、[!UICONTROL Site]、[!UICONTROL Segment]、[!UICONTROL Geo]、[!UICONTROL Device]、[!UICONTROL Frequency (by Impression)]和[!UICONTROL Conversion]。 如需跨帳戶報告的詳細資訊，請連絡您的Adobe客戶經理。

若要套用一或多個篩選器，請執行下列動作：

* 選取維度，選取運算子（*等於*&#x200B;或&#x200B;*不等於*），然後選取適用的值。 例如，若要僅傳回前段廣告的資料，請指定&quot;[!UICONTROL Ad Type equals Preroll]&quot;。
* （選用）新增其他條件至篩選器。
* （選用）新增其他篩選器，每個都包含一或多個條件。

## [!UICONTROL Build Your Report] 區段

**[!UICONTROL Select To Add As Report Headers]:**  要包含在報表中的資料欄或標題。若要新增欄，請展開類別並選取欄名稱旁的核取方塊。 所有無法使用的量度皆會停用。 可用的資料類別包括：

* [!UICONTROL  Dimensions]
* [!UICONTROL Metrics]
* [!UICONTROL Conversion Metrics] （依廣告商排序）
* [!UICONTROL Custom Goals] （依廣告商排序）

**[!UICONTROL Drag to Re-Order Report Headers Below]:** 欄標題的順序。您可以拖放任何欄來自訂順序。

## [!UICONTROL Multi-Touch Conversion Options] 區段

**[!UICONTROL Format]:** 是以(逗號分 *[!UICONTROL CSV]* 隔值)或( *[!UICONTROL Tab]* 定位點分隔值)格式產生報表。

**[!UICONTROL Report Headers]:** 是否 *[!UICONTROL Include]* 或 *[!UICONTROL Do Not Include]* 欄標題。

**[!UICONTROL Attribution Rule Settings]:** (所有 [!UICONTROL Custom]包含 [!UICONTROL Conversion]、 [!UICONTROL Device]、 [!UICONTROL Geo]、 [!UICONTROL Segment]和 [!UICONTROL Site]  [!UICONTROL Conversion Metrics]  [!UICONTROL Custom Goals] 欄的報表；僅限具有Advertising Cloud轉換追蹤的廣告商)在報表內，如何歸因一系列導致轉換的事件中的轉換資料。如果要比較規則之間的差異，可以選擇多個規則。

>[!NOTE]
>
>轉換路徑包含廣告商曝光數和點按次數，或點按回顧期間(在Advertising Cloud Search中設定)。 點按次數會在轉換歸因期間受到曝光數的偏好。 轉換路徑中的任何點按都會根據歸因規則獲得滿分。 只有在轉換路徑中未追蹤任何點按時，曝光數才會獲得評分。

* *[!UICONTROL Last Event]:* 將轉換歸因於轉換路徑中的上次點按或曝光。

* *[!UICONTROL Weight Last More]:* 將轉換歸因於轉換路徑中的所有事件，但為最後一個事件賦予了最大的權重，而為前一個事件賦予的權重依次較低。

* *[!UICONTROL Even Distribution]:* 對轉換路徑中的每個事件歸因轉換的平等。

* *[!UICONTROL Weight First More]:* 將轉換歸因於轉換路徑中的所有事件，但會賦予第一個事件最大的權重，而後為下列事件提供較少的權重。

* *[!UICONTROL First Event]:* 將轉換歸因於轉換路徑中的第一次點按或曝光。

* *[!UICONTROL U-shaped]:* 將轉換歸因於轉換路徑中的所有事件，但為第一個和最後一個事件賦予了最大的權重，並連續減少了轉換路徑中間事件的權重。

* *[!UICONTROL Display Only]:*  將轉換歸因於轉換路徑中的上次DSP點按或曝光數。這包括視訊和連線電視廣告，並排除對Advertising Cloud Search廣告的點按。

* *[!UICONTROL Social Only]:* 過時

<!-- See also [How Attribution Rules Are Calculated for Adobe Advertising Cloud](). -->

**[!UICONTROL Paths as Columns]:**  (所有 [!UICONTROL Custom]、 [!UICONTROL Conversion]、 [!UICONTROL Device]、 [!UICONTROL Geo]、 [!UICONTROL Segment]以及 [!UICONTROL Site] 含 [!UICONTROL Conversion Metrics] 或 [!UICONTROL Custom Goals] 欄的報表)在相同裝置上發生先前事件時要報告的轉換類型。您最多可以包含三種類型。 對於每個選取的類型，每個轉換量度都會包含一個單獨的欄，並附加指定的尾碼（[!UICONTROL (tl)]、[!UICONTROL (ct)]或[!UICONTROL (vt)]）:

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* 包括歸因於點按（點進為CT）和曝光（閱覽為VT）的轉換。曝光次數的轉換數乘以指定的檢視權數。 預設的檢視權數為100%，這表示歸因於曝光的轉換會計為點按的轉換值的100%。

* *[!UICONTROL With Clicks (CT)]:* 僅包含歸因於點按的轉換。

* *[!UICONTROL Impressions Only (VT)]:* 僅包含歸因於曝光次數的轉換，因為轉換路徑中未追蹤任何點按。

**[!UICONTROL Cross Device Level]:**  (所有 [!UICONTROL Custom]包含 [!UICONTROL Conversion]、 [!UICONTROL Device]、 [!UICONTROL Geo]、 [!UICONTROL Segment]和 [!UICONTROL Site]  [!UICONTROL Conversion Metrics]  [!UICONTROL Custom Goals] 欄的報表；僅適用於具有跨裝置歸因的廣告商)追蹤轉換的層級： *[!UICONTROL People]* 或 *[!UICONTROL Household]*。

深入了解[跨裝置解決方案](/help/dsp/introduction/features/cross-device-solutions.md)。

**[!UICONTROL Cross-Device Breakout]:** (所有 [!UICONTROL Custom]包含 [!UICONTROL Conversion]、 [!UICONTROL Device]、 [!UICONTROL Geo]、 [!UICONTROL Segment]和 [!UICONTROL Site]  [!UICONTROL Conversion Metrics]  [!UICONTROL Custom Goals] 欄的報表；僅適用於具有跨裝置歸因的廣告商)要納入報表的跨裝置轉換詳細程度。如果您想要詳細的劃分，可以選擇最多三個級別，每個級別都將包含在單獨的列中。

* *[!UICONTROL Total People (TP)]:* 包含轉換總數，包括相同裝置轉換和跨裝置轉換（若適用）。在報表中，「[!UICONTROL (tp)]」會附加至轉換量度名稱和規則類型。

* *[!UICONTROL Same Device (SD)]:* 僅包含轉換路徑中僅追蹤單一裝置的轉換。在報表中，「[!UICONTROL (sd)]」會附加至轉換量度名稱和規則類型。

* *[!UICONTROL Cross Device (XD)]:* 僅包含在轉換路徑中追蹤超過一個裝置的轉換。在報表中，「[!UICONTROL (xd)]」會附加至轉換量度名稱和規則類型。

**[!UICONTROL Conversion Reporting Based On]:**  如何報告轉換資料：

* *[!UICONTROL Conversion Timestamp]:* （預設）轉換會與轉換日期相關聯。

* *[!UICONTROL Event Timestamp]:* 系統會根據造成轉換的曝光或點按日期來報告轉換，由指定的決定 [!UICONTROL Attribution Rule Settings]。

## [!UICONTROL Add Email Recipients] 區段

**[!UICONTROL Email]:** 如果報表因錯誤而取消，則要傳送已完成報表或通知的電子郵件地址。若要指定多個地址，請以逗號或空格分隔。

**[!UICONTROL Frequency]:** 報表的傳送頻率： *[!UICONTROL Once]*、  *[!UICONTROL Daily]*、  *[!UICONTROL Weekly]*&#x200B;或 *[!UICONTROL Monthly]*。

## [!UICONTROL Save Report] 區段

**[!UICONTROL Send & Save]:** 報表的傳送時間： *[!UICONTROL On Schedule]* 或 *[!UICONTROL Run Now]*。排程報表將在帳戶時區的09:00前傳送。

>[!NOTE]
>
>您可以從[!UICONTROL Reports]檢視隨時](report-run-now.md)執行自訂報表。[

>[!MORELIKETHIS]
>
>* [關於自訂報表](/help/dsp/reports/report-about.md)
>* [建立自訂報表](/help/dsp/reports/report-create.md)
>* [複製自訂報表](/help/dsp/reports/report-copy.md)
>* [編輯自訂報表](/help/dsp/reports/report-edit.md)
>* [執行自訂報表](/help/dsp/reports/report-run-now.md)
>* [自訂報表設定](/help/dsp/reports/report-settings.md)

* [可用報表欄](/help/dsp/reports/report-columns.md)
