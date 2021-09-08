---
title: 關於自訂報表
description: 了解手動建立自訂報表或使用預先設定之報表範本的選項。
feature: Custom Reports
exl-id: 59fc1894-1c9d-451d-b644-5640dd311547
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 0%

---

# 關於自訂報表

自訂報表可讓您使用促銷活動維度（例如廣告商、版位、網站或地標）和對您最重要的量度，來自訂報表資料的內容和傳送。 您可以：

* 在精細層級完整設定促銷活動績效報表。
* 從預先設定的報表範本中選擇，並可選擇進一步自訂。

您只需產生一次報表，或排程在指定時區的03:00每天、每週或每月產生報表。 產生報表後，會傳送通知給每個指定的電子郵件收件者，並附上下載檔案的連結。

>[!NOTE]
>
>您也可以在相關促銷活動管理檢視](/help/dsp/campaign-management/reports/campaign-reports-about.md)中檢視促銷活動（促銷活動、套件、版位或廣告）[的所有層級的隨選資料。

## 可用的報表類型

* **[!UICONTROL Custom]:** 此報表是空白範本，可用來使用大部分的維度和量度建立自己的自訂報表。[!UICONTROL Conversion]、 、  [!UICONTROL Device]、  [!UICONTROL Geo] [!UICONTROL Site] 和報表是此範本的變體，其各自使用案例已預先選取欄和維度。

* 預先設定的報表範本

   * **[!UICONTROL Billing]:** 使用此報表可了解關鍵計費量度，例如依促銷活動進行媒體計費的支出量度。

      >[!NOTE]
      >
      >此報表包含有關帳單區段的資料。 如果提供屬於多個區段的使用者或裝置曝光數，則只有一個計費區段會計入曝光數。

   * **[!UICONTROL Conversion]:** 根據使用Advertising Cloud轉換追蹤擷取的轉換量度，使用此報表來了解促銷活動的成效。此報表包含多點接觸歸因。

   * **[!UICONTROL Device]:** 使用此預先填入的範本，可依裝置相關維度查看關鍵量度。

   * **[!UICONTROL Frequency (by Impression)]:** 使用此報表可了解向不重複檢視者顯示的曝光數分佈（例如，有多少個不重複檢視者看過一次曝光、兩次曝光、三次曝光等）。資料可依版位或行銷活動提供。

      >[!NOTE]
      >
      >* 資料可在2019年3月1日之後使用。
      >* 根據資料的採樣來估計頻率。
      >* 對於某些詳細目錄，發佈者不會傳遞裝置識別碼，這會防止頻率追蹤。 此報表僅包含有裝置識別碼可用的曝光數。


   * **[!UICONTROL Frequency (by App/Site)]:** 使用此報表可了解依應用程式或網站觸及的不重複使用者人數。您也可以查看僅透過特定應用程式或網站（「不重複使用者」）觸及的不重複使用者數量。

      >[!NOTE]
      >
      >* 2018年11月15日之後可使用資料。
      >* 對於某些私人詳細目錄，發佈者不會傳遞裝置識別碼，這會防止頻率追蹤。


   * **[!UICONTROL Geo]**:使用此預先填入的範本，可依地理維度查看關鍵量度。

   * **[!UICONTROL Margin]:** 使用此報表，可依促銷活動或位置查看關鍵量度，例如利潤、利潤和其他支出量度。

   * **[!UICONTROL Segment]:** 使用此預先填入的範本，即可依區段查看關鍵量度。

      >[!NOTE]
      >
      >* 此報表旨在顯示不同目標區段的執行方式。 會使用區段成員資格資料。 對屬於兩個或多個目標區段的人員或裝置顯示曝光時，此報表會為每個區段包含一列。 因此，此報表中的總計可能不符合實際傳送。
      >* 區段的轉換量度和自訂目標資料可在2019年8月2日之後使用。 自2018年6月1日起，可使用區段的所有其他資料。


   * **[!UICONTROL Site]:** 依預設，包括標準量度、媒體淨支出總計，以及依網站的可計費淨支出總計。

## 跨帳戶報告 {#cross-account-reporting}

任何具有多個DSP帳戶的組織均可根據組織的需求，選擇在自訂報表中啟用跨帳戶資料。 例如，您可以授予帳戶A存取帳戶B的資料，並授予帳戶B存取帳戶C（但不授予帳戶A）的資料。 若要啟用並設定此功能，請連絡您的帳戶管理員。

為貴組織啟用功能後，您就可以依帳戶篩選[下列任何報表類型： [!UICONTROL Custom]、[!UICONTROL Site]、[!UICONTROL Segment]、[!UICONTROL Geo]、[!UICONTROL Device]、[!UICONTROL Frequency (by Impression)]和[!UICONTROL Conversion]。](report-settings.md)

您在[!UICONTROL Settings] > [!UICONTROL Account]的帳戶設定表示a)其資料可供您帳戶使用的其他帳戶，以及b)可存取您帳戶資料的其他帳戶。

>[!MORELIKETHIS]
>
>* [建立自訂報表](/help/dsp/reports/report-create.md)
>* [自訂報表設定](/help/dsp/reports/report-settings.md)
>* [關於平台內報表](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [可用報表欄](/help/dsp/reports/report-columns.md)

