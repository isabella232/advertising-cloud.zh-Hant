---
title: 自訂報表設定
description: 請參閱自訂報表設定的說明。
feature: DSP Custom Reports
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 0%

---

# 自訂報表設定

**[!UICONTROL Name]** 報表名稱。 長度上限為180個字元。

**[!UICONTROL Report Type]** 報表類型： *[!UICONTROL Custom]* （包括最多可用選項）, *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*,  *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*,  *[!UICONTROL Segment]*，或 *[!UICONTROL Site]*.

## [!UICONTROL Apply Filters] 區段

**[!UICONTROL Timezone]:** 報告時區。

**[!UICONTROL Observe Daylight Savings Time]:** 考量日光節約時間（以報告時間計）。

**\[日期範圍\]:** 要產生資料的日期範圍。 可用天數依報表和選取的維度而異。 選擇一個：

* **[!UICONTROL Previous N days]:** 包含今天之前特定天數的資料。

* **[!UICONTROL Custom]:** 包括特定開始和結束日期之間的資料。 要報告前一天的資料，請選擇 **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]:** 包括前一個日曆月的資料。

**[!UICONTROL Add Filters]:** （選用）要篩選資料的其他維度，無論維度是否列在報表中： *[!UICONTROL Account]*,\* *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Placement]*, *[!UICONTROL Ad]*, *[!UICONTROL Ad Type]*, *[!UICONTROL Video]*, *[!UICONTROL Video Duration]*, *[!UICONTROL Country]*，和 *[!UICONTROL Package]*.

\* *[!UICONTROL Account]* 只有在貴組織已設定為 [跨帳戶報告](report-about.md#cross-account-reporting):  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)]，和 [!UICONTROL Conversion]. 請連絡您的 [!DNL Adobe] 帳戶團隊，以取得跨帳戶報告的詳細資訊。

若要套用一或多個篩選器，請執行下列動作：

* 選取維度，選取運算子(*等於* 或 *不等於*)，然後選取適用的值。 例如，若要僅傳回前段廣告的資料，請指定「[!UICONTROL Ad Type equals Preroll].&quot;
* （選用）新增其他條件至篩選器。
* （選用）新增其他篩選器，每個都包含一或多個條件。

## [!UICONTROL Build Your Report] 區段

**[!UICONTROL Select To Add As Report Headers]:**  要包含在報表中的資料欄或標題。 若要新增欄，請展開類別並選取欄名稱旁的核取方塊。 所有無法使用的量度皆會停用。 可用的資料類別包括：

* [!UICONTROL  Dimensions]
* [!UICONTROL Metrics]
* [!UICONTROL Conversion Metrics] （依廣告商排序）
* [!UICONTROL Custom Goals] （依廣告商排序）

**[!UICONTROL Drag to Re-Order Report Headers Below]:** 欄標題的順序。 您可以拖放任何欄來自訂順序。

## [!UICONTROL Multi-Touch Conversion Options] 區段

**[!UICONTROL Format]:** 是否要在中產生報表 *[!UICONTROL CSV]* （逗號分隔值）或 *[!UICONTROL Tab]* （以Tab分隔的值）格式。

**[!UICONTROL Report Headers]:** 是否 *[!UICONTROL Include]* 或 *[!UICONTROL Do Not Include]* 欄標題。

**[!UICONTROL Attribution Rule Settings]:** (全部 [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]，和 [!UICONTROL Site] 報表 [!UICONTROL Conversion Metrics] 或 [!UICONTROL Custom Goals] 欄；廣告商(僅限Adobe廣告轉換追蹤)在報表內，如何歸因導致轉換的一系列事件中的轉換資料。 如果要比較規則之間的差異，可以選擇多個規則。

>[!NOTE]
>
>轉換路徑包含廣告商曝光數和點按次數，或點按回顧期間(在 [!DNL Adobe Advertising Search]. 點按次數會在轉換歸因期間受到曝光數的偏好。 轉換路徑中的任何點按都會根據歸因規則獲得滿分。 只有在轉換路徑中未追蹤任何點按時，曝光數才會獲得評分。

* *[!UICONTROL Last Event]:* 將轉換歸因於轉換路徑中的上次點按或曝光。

* *[!UICONTROL Weight Last More]:* 將轉換歸因於轉換路徑中的所有事件，但為最後一個事件賦予了最大的權重，而為前一個事件賦予了更少的權重。

* *[!UICONTROL Even Distribution]:* 將轉換平均歸因至轉換路徑中的每個事件。

* *[!UICONTROL Weight First More]:* 將轉換歸因於轉換路徑中的所有事件，但會賦予第一個事件最大的權重，而後為下列事件提供較少的權重。

* *[!UICONTROL First Event]:* 將轉換歸因於轉換路徑中的第一次點按或曝光。

* *[!UICONTROL U-shaped]:* 將轉換歸因於轉換路徑中的所有事件，但賦予第一個和最後一個事件最大的權重，並連續減少對轉換路徑中間事件的權重。

* *[!UICONTROL Display Only]:*  將轉換歸因於轉換路徑中的上次DSP點按或曝光。 這包括視訊和連線電視廣告，並排除點按次數 [!DNL Adobe Advertising Search] 廣告。

* *[!UICONTROL Social Only]:* 過時

<!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

**[!UICONTROL Paths as Columns]:**  (全部 [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]，和 [!UICONTROL Site] 報表 [!UICONTROL Conversion Metrics] 或 [!UICONTROL Custom Goals] 欄)在相同裝置上發生先前事件時要報告的轉換類型。 您最多可以包含三種類型。 對於每個選取的類型，每個轉換量度會包含個別的欄，並附加指定的尾碼([!UICONTROL (tl)], [!UICONTROL (ct)]，或 [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* 包括歸因於點按（點進為CT）和曝光（閱覽為VT）的轉換。 曝光次數的轉換數乘以指定的檢視權數。 預設的檢視權數為100%，這表示歸因於曝光的轉換會計為點按的轉換值的100%。

* *[!UICONTROL With Clicks (CT)]:* 僅包含歸因於點按的轉換。

* *[!UICONTROL Impressions Only (VT)]:* 僅包含歸因於曝光次數的轉換，因為轉換路徑中未追蹤任何點按。

**[!UICONTROL Conversion Reporting Based On]:**  如何報告轉換資料：

* *[!UICONTROL Conversion Timestamp]:* （預設）轉換會與轉換日期相關聯。

* *[!UICONTROL Event Timestamp]:* 系統會根據造成轉換的曝光或點按日期來報告轉換，由指定 [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Report Destinations] 區段

**[!UICONTROL Destination Type]:** 選擇以下目標類型之一：

* *[!UICONTROL S3]:* 將完成的報告發送到一個或多個 [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3])位置，您將在 **[!UICONTROL Destination Name]** 欄位。
* *[!UICONTROL sFTP]:* 若要將完成的報表傳送至一或多個SFTP位置，請在 **[!UICONTROL Destination Name]** 欄位。
* *[!UICONTROL FTP]:* 若要將完成的報表傳送至一或多個FTP位置，請在 **[!UICONTROL Destination Name]** 欄位。
* *[!UICONTROL FTP SSL]（目前為測試版）:* 若要將完成的報表傳送至一或多個FTP SSL位置，請在 **[!UICONTROL Destination Name]** 欄位。
* *[!UICONTROL Email]:* 指定在因錯誤而取消報表時，要將已完成報表或通知傳送至其的電子郵件地址。 若要指定多個地址，請以逗號或空格分隔。

>[!NOTE]
>
> 儲存報表後，就無法變更目的地類型。

**[!UICONTROL Destination Name]:** （僅限S3、FTP、sFTP和FTP SSL目的地類型）將要傳送自訂報表的報表目的地名稱。

* 要指定現有目標，請從清單中選擇目標名稱。 您可以個別選取多個目的地名稱。

* 要建立新目標：

   1. 按一下 **新增目的地**.

   1. 輸入 [報表目的地設定](/help/dsp/reports/report-destinations/report-destination-settings.md)，然後按一下 **儲存**.

   1. 返回報表設定，按一下 **刷新目標名稱。**

      現在可從現有目的地清單中取得新目的地，您也可以選擇將其新增至報表。

**[!UICONTROL Frequency]:** (針對 [!UICONTROL Destination Name] 將報表傳送至目的地的頻率： *[!UICONTROL Once]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*，或 *[!UICONTROL Monthly]*.

## [!UICONTROL Save Report] 區段

**[!UICONTROL Send & Save]:** 何時傳送報表： *[!UICONTROL On Schedule]* 或 *[!UICONTROL Run Now]*. 排程報表將在帳戶時區的09:00前傳送。

>[!NOTE]
>
>您可以 [隨時執行自訂報表](report-run-now.md) 從 [!UICONTROL Reports] 檢視。

>[!MORELIKETHIS]
>
>* [關於自訂報表](/help/dsp/reports/report-about.md)
>* [建立自訂報表](/help/dsp/reports/report-create.md)
>* [複製自訂報表](/help/dsp/reports/report-copy.md)
>* [編輯自訂報表](/help/dsp/reports/report-edit.md)
>* [執行自訂報表](/help/dsp/reports/report-run-now.md)
>* [自訂報表設定](/help/dsp/reports/report-settings.md)
>* [關於報表目的地](/help/dsp/reports/report-destinations/report-destination-about.md)

* [可用報表欄](/help/dsp/reports/report-columns.md)
