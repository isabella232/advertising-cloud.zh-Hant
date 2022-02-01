---
title: 自定義報表設定
description: 請參閱自定義報告設定的說明。
feature: DSP Custom Reports
exl-id: 1d37fc96-0f9b-4eb2-ba8d-9534f627adaf
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 0%

---

# 自定義報表設定

**[!UICONTROL Name]** 報告名稱。 最大長度為180個字元。

**[!UICONTROL Report Type]** 報告類型： *[!UICONTROL Custom]* （其中包括大多數可用選項）, *[!UICONTROL Billing]*。 *[!UICONTROL Conversion]*。 *[!UICONTROL Device]*。 *[!UICONTROL Frequency (by Impression)]*。  *[!UICONTROL Frequency (by App/Site)]*。 *[!UICONTROL Geo]*。 *[!UICONTROL Margin]*。 *[!UICONTROL Media Performance]*。  *[!UICONTROL Segment]*&#x200B;或 *[!UICONTROL Site]*。

## [!UICONTROL Apply Filters] 節

**[!UICONTROL Timezone]:** 報告的時區。

**[!UICONTROL Observe Daylight Savings Time]:** 在報告的時間內考慮夏令時。

**\[日期範圍\]:** 要生成資料的日期範圍。 可用天數因報告和所選維而異。 選擇一個：

* **[!UICONTROL Previous N days]:** 包括今天之前特定天數的資料。

* **[!UICONTROL Custom]:** 包括特定開始日期和結束日期之間的資料。 要報告上一天的資料，請選擇 **[!UICONTROL Present]**。

* **[!UICONTROL Last Calendar Month]:** 包括上一個日曆月的資料。

**[!UICONTROL Add Filters]:** （可選）用於篩選資料的附加維，無論這些維是否作為列包含在報表中： *[!UICONTROL Account]*,\* *[!UICONTROL Advertiser]*。 *[!UICONTROL Campaign]*。 *[!UICONTROL Placement]*。 *[!UICONTROL Ad]*。 *[!UICONTROL Ad Type]*。 *[!UICONTROL Video]*。 *[!UICONTROL Video Duration]*。 *[!UICONTROL Country]*, *[!UICONTROL Package]*。

\* *[!UICONTROL Account]* 僅當您的組織配置為 [跨帳戶報告](report-about.md#cross-account-reporting):  [!UICONTROL Custom]。 [!UICONTROL Site]。 [!UICONTROL Segment]。 [!UICONTROL Geo]。 [!UICONTROL Device]。 [!UICONTROL Frequency (by Impression)], [!UICONTROL Conversion]。 聯繫您 [!DNL Adobe] 帳戶團隊，瞭解有關跨帳戶報告的詳細資訊。

要應用一個或多個篩選器，請執行以下操作：

* 選擇維，選擇運算子(*等於* 或 *不等於*)，然後選擇適用的值。 例如，要僅返回前置廣告的資料，請指定「[!UICONTROL Ad Type equals Preroll]&quot;
* （可選）向篩選器添加附加條件。
* （可選）添加附加篩選器，每個篩選器都包含一個或多個條件。

## [!UICONTROL Build Your Report] 節

**[!UICONTROL Select To Add As Report Headers]:**  要包括在報表中的資料列或標題。 要添加列，請展開類別並選中列名稱旁邊的複選框。 禁用所有不可用度量。 可用的資料類別包括：

* [!UICONTROL  Dimensions]
* [!UICONTROL Metrics]
* [!UICONTROL Conversion Metrics] （按廣告商排序）
* [!UICONTROL Custom Goals] （按廣告商排序）

**[!UICONTROL Drag to Re-Order Report Headers Below]:** 列標題的順序。 可以拖放任意列以自定義順序。

## [!UICONTROL Multi-Touch Conversion Options] 節

**[!UICONTROL Format]:** 是否在中生成報告 *[!UICONTROL CSV]* （逗號分隔值）或 *[!UICONTROL Tab]* （以制表符分隔的值）格式。

**[!UICONTROL Report Headers]:** 是否 *[!UICONTROL Include]* 或 *[!UICONTROL Do Not Include]* 列標題。

**[!UICONTROL Attribution Rule Settings]:** （全部） [!UICONTROL Custom]。 [!UICONTROL Conversion]。 [!UICONTROL Device]。 [!UICONTROL Geo]。 [!UICONTROL Segment], [!UICONTROL Site] 報告 [!UICONTROL Conversion Metrics] 或 [!UICONTROL Custom Goals] 欄；在報告中，如何將轉換資料屬性化為導致轉換的一系列事件。 如果要比較規則之間的差異，可以選擇多個規則。

>[!NOTE]
>
>轉換路徑包括廣告商印象中的任何印象和點擊量，或按一下在Advertising Cloud Search配置的回望窗口。 在轉換屬性期間，點擊優先於印象。 轉換路徑中的任何點擊都會基於屬性規則獲得完全信用。 只有在轉換路徑中未跟蹤任何點擊時，印象才會獲得積分。

* *[!UICONTROL Last Event]:* 屬性轉換為轉換路徑中的上次按一下或印象。

* *[!UICONTROL Weight Last More]:* 屬性轉換到轉換路徑中的所有事件，但為最後一個事件賦予了最大權重，而為前一個事件賦予了相繼較少的權重。

* *[!UICONTROL Even Distribution]:* 屬性轉換與轉換路徑中的每個事件相同。

* *[!UICONTROL Weight First More]:* 屬性轉換到轉換路徑中的所有事件，但賦予第一個事件最大權重，而賦予以下事件的權重依次減小。

* *[!UICONTROL First Event]:* 屬性轉換為轉換路徑中的第一次按一下或印象。

* *[!UICONTROL U-shaped]:* 對轉換路徑中的所有事件進行轉換的屬性，但對第一個事件和最後一個事件賦予的權重最大，對轉換路徑中間的事件的權重連續較小。

* *[!UICONTROL Display Only]:*  屬性轉換為轉換路DSP徑中的最後一次按一下或印象。 這包括視頻和連接電視廣告，不包括Advertising Cloud Search廣告的點擊量。

* *[!UICONTROL Social Only]:* 過時

<!-- See also [How Attribution Rules Are Calculated for Adobe Advertising Cloud](). -->

**[!UICONTROL Paths as Columns]:**  （全部） [!UICONTROL Custom]。 [!UICONTROL Conversion]。 [!UICONTROL Device]。 [!UICONTROL Geo]。 [!UICONTROL Segment], [!UICONTROL Site] 報告 [!UICONTROL Conversion Metrics] 或 [!UICONTROL Custom Goals] 列)在同一設備上發生先前事件時要報告的轉換類型。 最多可包括三種類型。 對於每個選定類型，每個轉換度量都包括一個單獨的列，並附加指定的尾碼([!UICONTROL (tl)]。 [!UICONTROL (ct)]或 [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* 包括由點擊（CT用於點擊）和印象（VT用於查看）引起的轉換。 由印數引起的轉換乘以指定的透視權重。 預設的查看權重為100%，這意味著由印象引起的轉換被計算為由點擊引起的轉換值的100%。

* *[!UICONTROL With Clicks (CT)]:* 僅包括由按一下引起的轉換。

* *[!UICONTROL Impressions Only (VT)]:* 僅包括由於轉換路徑中未跟蹤任何點擊而導致的轉換。

**[!UICONTROL Cross Device Level]:**  （全部） [!UICONTROL Custom]。 [!UICONTROL Conversion]。 [!UICONTROL Device]。 [!UICONTROL Geo]。 [!UICONTROL Segment], [!UICONTROL Site] 報告 [!UICONTROL Conversion Metrics] 或 [!UICONTROL Custom Goals] 欄；僅適用於具有跨設備屬性的廣告主)跟蹤轉換的級別： *[!UICONTROL People]* 或 *[!UICONTROL Household]*。

瞭解有關 [跨設備解決方案](/help/dsp/introduction/features/cross-device-solutions.md)。

**[!UICONTROL Cross-Device Breakout]:** （全部） [!UICONTROL Custom]。 [!UICONTROL Conversion]。 [!UICONTROL Device]。 [!UICONTROL Geo]。 [!UICONTROL Segment], [!UICONTROL Site] 報告 [!UICONTROL Conversion Metrics] 或 [!UICONTROL Custom Goals] 欄；僅適用於具有跨設備屬性的廣告主)要包含在報告中的跨設備轉換的詳細資訊級別。 如果您想要詳細的分段，您最多可以選擇三個級別，每個級別都將包含在單獨的列中。

* *[!UICONTROL Total People (TP)]:* 包括總轉換，包括相同設備轉換和跨設備轉換（如果適用）。 在報告中， &quot;[!UICONTROL (tp)]「 」附加到轉換度量名稱和規則類型。

* *[!UICONTROL Same Device (SD)]:* 僅包括轉換路徑中僅跟蹤單個設備的轉換。 在報告中， &quot;[!UICONTROL (sd)]「 」附加到轉換度量名稱和規則類型。

* *[!UICONTROL Cross Device (XD)]:* 僅包括在轉換路徑中跟蹤多個設備的轉換。 在報告中， &quot;[!UICONTROL (xd)]「 」附加到轉換度量名稱和規則類型。

**[!UICONTROL Conversion Reporting Based On]:**  如何報告轉換資料：

* *[!UICONTROL Conversion Timestamp]:* （預設）轉換將與轉換日期關聯。

* *[!UICONTROL Event Timestamp]:* 將根據印象日期或按一下導致轉換的日期報告轉換，具體取決於指定的 [!UICONTROL Attribution Rule Settings]。

## [!UICONTROL Add Report Destinations] 節

**[!UICONTROL Destination Type]:** 選擇以下目標類型之一：

* *[!UICONTROL S3]:* 將已完成的報告發送到一個或多個 [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3])位置，您將在 **[!UICONTROL Destination Name]** 的子菜單。
* *[!UICONTROL sFTP]:* 將完成的報告發送到一個或多個SFTP位置，您將在 **[!UICONTROL Destination Name]** 的子菜單。
* *[!UICONTROL FTP]:* 將完成的報告發送到一個或多個FTP位置，您將在 **[!UICONTROL Destination Name]** 的子菜單。
* *[!UICONTROL FTP SSL]（當前為Beta版）:* 將完成的報告發送到一個或多個FTP SSL位置，您將在 **[!UICONTROL Destination Name]** 的子菜單。
* *[!UICONTROL Email]:* 指定在由於錯誤而取消報告時向其發送已完成報告或通知的電子郵件地址。 要指定多個地址，請用逗號或空格分隔。

>[!NOTE]
>
> 保存報告後，無法更改目標類型。

**[!UICONTROL Destination Name]:** （僅限S3、FTP、sFTP和FTP SSL目標類型）將自定義報告發送到的報告目標的名稱。

* 要指定現有目標，請從清單中選擇目標名稱。 可以單獨選擇多個目標名稱。

* 要建立新目標：

   1. 按一下 **添加新目標**。

   1. 輸入 [報告目標設定](/help/dsp/reports/report-destinations/report-destination-settings.md)，然後按一下 **保存**。

   1. 返回報告設定中，按一下 **刷新目標名稱。**

      現在，新目標可以從現有目標清單中找到，您可以選擇將其添加到報表中。

**[!UICONTROL Frequency]:** (每個 [!UICONTROL Destination Name] 將報告發送到目標的頻率： *[!UICONTROL Once]*。 *[!UICONTROL Daily]*。 *[!UICONTROL Weekly]*&#x200B;或 *[!UICONTROL Monthly]*。

## [!UICONTROL Save Report] 節

**[!UICONTROL Send & Save]:** 何時發送報告： *[!UICONTROL On Schedule]* 或 *[!UICONTROL Run Now]*。 定時報告將在帳戶的時區中09:00之前交付。

>[!NOTE]
>
>你可以 [隨時運行自定義報告](report-run-now.md) 從 [!UICONTROL Reports] 的子菜單。

>[!MORELIKETHIS]
>
>* [關於自定義報告](/help/dsp/reports/report-about.md)
>* [建立自定義報告](/help/dsp/reports/report-create.md)
>* [複製自定義報告](/help/dsp/reports/report-copy.md)
>* [編輯自定義報告](/help/dsp/reports/report-edit.md)
>* [運行自定義報告](/help/dsp/reports/report-run-now.md)
>* [自定義報表設定](/help/dsp/reports/report-settings.md)
>* [關於報告目標](/help/dsp/reports/report-destinations/report-destination-about.md)

* [可用報表列](/help/dsp/reports/report-columns.md)
