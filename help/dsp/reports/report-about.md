---
title: 關於自定義報告
description: 瞭解手動建立自定義報告或使用預配置的報告模板的選項。
feature: DSP Custom Reports
exl-id: 59fc1894-1c9d-451d-b644-5640dd311547
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# 關於自定義報告

自定義報告允許您使用市場活動維度（如廣告商、位置、站點或geo）和對您最重要的指標自定義報告資料的內容和傳遞。 您可以：

* 在細粒度級別完全配置市場活動績效報告。
* 從預配置的報告模板中進行選擇，並根據需要進一步自定義這些模板。

您可以生成一次報告，或安排在指定時區的03:00每天、每週或每月生成報告。 生成報表後，它將發送給每個指定的電子郵件收件人或連結 [報告目標](/help/dsp/reports/report-destinations/report-destination-about.md) 類型：

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SFTP
* FTP SSL（測試版）

>[!NOTE]
>
>您還可以查看市場活動所有級別（市場活動、包、職位安排或廣告）的按需資料 [在相關市場活動管理視圖內](/help/dsp/campaign-management/reports/campaign-reports-about.md)。

## 可用報告類型

* **[!UICONTROL Custom]:** 此報表是一個空白模板，您可以使用大多數維和度量建立自己的自定義報表。 [!UICONTROL Conversion]。 [!UICONTROL Device]。 [!UICONTROL Geo], [!UICONTROL Site] 報告是此模板的變體，其中預選的列和維用於各自的使用情形。

* 預配置的報告模板

   * **[!UICONTROL Billing]:** 使用此報告可以瞭解關鍵計費指標，如按市場活動開單的媒體計費支出指標。

      >[!NOTE]
      >
      >此報表包括有關開單段的資料。 如果向用戶或設備提供屬於多個段的印象，則只有一個可計費的段被計入該印象。

   * **[!UICONTROL Conversion]:** 使用此報表可瞭解您的市場活動如何根據使用Advertising Cloud轉換跟蹤獲取的轉換指標執行。 本報告包括多點觸控屬性。

   * **[!UICONTROL Device]:** 使用此預填充的模板按與設備相關的維查看關鍵度量。

   * **[!UICONTROL Frequency (by Impression)]:** 使用此報告可瞭解給獨特觀眾的印象的分發情況（例如，有多少獨特觀眾看到了一個印象、兩個印象、三個印象等）。 資料可通過職位安排或市場活動獲得。

      >[!NOTE]
      >
      >* 2019年3月1日以後提供資料。
      >* 基於資料的採樣來估計頻率。
      >* 對於某些清單，發佈者不會傳遞設備標識符，這會阻止頻率跟蹤。 此報告僅包括設備標識符可用的印象。


   * **[!UICONTROL Frequency (by App/Site)]:** 使用此報告可瞭解應用程式或站點訪問的唯一用戶數。 您還可以看到僅通過特定應用或站點（「不同的唯一用戶」）訪問了多少個獨特用戶。

      >[!NOTE]
      >
      >* 2018年11月15日之後提供資料。
      >* 對於某些專用清單，發佈者不會傳遞設備標識符，這會阻止頻率跟蹤。


   * **[!UICONTROL Geo]**:使用此預填充的模板按地理維查看關鍵度量。

   * **[!UICONTROL Margin]:** 使用此報表可以按市場活動或職位安排查看關鍵指標，如利潤、利潤和其他支出指標。

   * **[!UICONTROL Segment]:** 使用此預填充的模板按段查看關鍵度量。

      >[!NOTE]
      >
      >* 此報告旨在顯示不同目標段的執行情況。 它使用段成員資料。 當向屬於兩個或多個目標段的人員或設備提供印象時，此報表包括每個段的一行。 因此，此報表中的合計可能與實際交貨不匹配。
      >* 2019年8月2日以後，可獲得段的轉換指標和自定義目標資料。 從2018年6月1日以後開始，所有其他資料都可供使用。


   * **[!UICONTROL Site]:** 預設情況下，包括標準指標、介質淨支出總額和按站點列出的可計費淨支出總額。

## 跨帳戶報告 {#cross-account-reporting}

具有多個帳戶DSP的任何組織都可以根據組織的需要，在自定義報告中選擇啟用交叉帳戶資料。 例如，您可以授予帳戶A對帳戶B資料的訪問權限，並授予帳戶B對帳戶C（但不授予帳戶A）資料的訪問權限。 要啟用和配置此功能，請與 [!DNL Adobe] 客戶團隊。

為您的組織啟用該功能後，您可以 [濾波器](report-settings.md) 以下任何報表類型（按帳戶）:  [!UICONTROL Custom]。 [!UICONTROL Site]。 [!UICONTROL Segment]。 [!UICONTROL Geo]。 [!UICONTROL Device]。 [!UICONTROL Frequency (by Impression)], [!UICONTROL Conversion]。

您的帳戶設定位於 [!UICONTROL Settings] > [!UICONTROL Account] 指示a)其資料可用於您的帳戶的其他帳戶，以及b)可訪問您帳戶資料的其他帳戶。

>[!MORELIKETHIS]
>
>* [建立自定義報告](/help/dsp/reports/report-create.md)
>* [自定義報表設定](/help/dsp/reports/report-settings.md)
>* [關於平台內報告](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [可用報表列](/help/dsp/reports/report-columns.md)
>* [關於 [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)

