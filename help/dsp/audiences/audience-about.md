---
title: 關於Advertising DSP中的受眾管理
description: 了解受眾管理功能。
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: e9d9d51302d32b06af805917db2f46e5f6daee62
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 關於Advertising DSP中的受眾管理

在DSP中，您可以建立和管理受眾區段和受眾集，以用作版位的目標：

* 您可以建立和實作區段，以收集您自己的第一方對象資料。 您之後可以透過廣告重新定位區段中的使用者，或防止區段中的使用者收到廣告。 您可以建立下列類型的區段：

   * [自訂區段](/help/dsp/audiences/custom-segment-create.md) 追蹤a)從案頭、行動裝置和CTV裝置公開廣告的使用者，以及b)造訪特定網頁的使用者。

   * [CCPA選擇退出銷售區段](/help/dsp/audiences/ccpa-opt-out-segment-create.md) 若要根據加州消費者隱私法(CCPA)，在您的網站上追蹤來自消費者選擇退出銷售請求的使用者ID。 您可以從選擇退出銷售的請求中擷取使用者ID的每月報表。

      如需CCPA選擇退出銷售請求的Adobe廣告支援詳細資訊，請參閱 [加州消費者隱私法的Adobe廣告支援：消費者選擇退出支援](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* 您可以建立對象庫 [可重複使用的對象](/help/dsp/audiences/reusable-audience-create.md). 已儲存的對象會由任何可用的對象區段和任何其他已儲存的對象組成。 您對儲存的對象所做的任何變更都會自動套用至鎖定或排除對象的所有版位，以及包含儲存對象的所有其他對象。

   儲存的對象可讓媒體規劃人員視需要將對象分組，方法是使用複雜的布林邏輯包含和排除多個區段。 在您建立受眾時，會指出每個個別區段的大小和總受眾大小。 然後，行銷活動行政人員只需選取一或多個儲存的對象作為版位目標，而非手動設定每個版位的對象目標。

版位鎖定目標也提供其他對象類型。

## 匯入第一方和第三方資料區段

DSP可以從您的資料管理平台(DMP)匯入您自己的第一方資料區段，並視需要提供給任何廣告商集合。

DSP是 [the [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html)，可讓您與核准的廣告商和使用者共用已驗證的第一方區段，以便進行促銷活動啟用。 若要深入了解Real-Time CDP整合，請參閱 [來源區段](/help/dsp/audiences/sources/source-about.md).

DSP也可匯入自訂第三方區段，包括複雜的第三方區段組合。 您可以視需要將區段提供給任何廣告商集合。

請連絡您的 [!DNL Adobe] 客戶團隊，以了解詳細資訊。

## 可用作版位目標的對象

您可以將版位鎖定在下列所有類型的對象。

* 儲存在DSP中的所有使用者建立的對象集。

* 在DSP中建立的所有使用者建立的受眾區段：

   * 造訪特定網頁的使用者和曝光特定廣告的使用者的自訂區段。

   * 根據加州消費者隱私保護法(CCPA)，針對在您的網站上提交選擇退出銷售請求的使用者，提供CCPA選擇退出銷售對象區段。

* 所有匯入的第一方資料區段。

* 所有匯入的自訂第三方資料區段。

* （僅限美國版位） [來自超過30個提供者的DSP客戶可使用的所有協力廠商資料區段](/help/dsp/audiences/third-party-data-providers.md)，包括 [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast]等。

   您可以根據受眾資料來鎖定特定區段，例如具有特定人口統計、興趣或意圖及/或行為設定檔的使用者，來鎖定使用者。 您可以依資料提供者和類別瀏覽、依名稱或區段ID搜尋區段，或依資料提供者、總區段大小、網頁瀏覽器計數或裝置計數來篩選結果。

   第三方區段會產生額外費用，會在每個區段名稱旁顯示。

* (廣告商，包含Adobe Experience Platform和 [!DNL Real-Time CDP]、僅使用Adobe廣告JavaScript轉換標籤的Adobe Audience Manager或Adobe Analytics)所有在 [!DNL Real-Time CDP]，在Audience Manager中建立，或從Audience Manager發佈至Adobe Experience Cloud [!DNL Analytics].

   使用區段的定價是預先商定的，不會顯示在DSP中。

   區段來自 [!DNL Analytics] 在您建立或發佈為Experience Cloud對象後大約一小時內可用。 區段直接來自Audience Manager或 [!DNL Real-Time CDP] 可在您共用後24小時內取得。

   >[!NOTE]
   >
   >請參閱 [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics.html)，和 [the [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) 以取得在這些解決方案中設定和收集區段資料的相關資訊。

## 對象大小資料

在儲存的受眾設定和版位設定中，您可以看到詳細的受眾大小資料：

* 系統會顯示所有選取區段和儲存之對象的已刪除重複的受眾總數和作用中的大小，而您可以依裝置類型（瀏覽器、行動裝置或連線電視）檢視詳細資訊。

   ![合併的受眾規模](/help/dsp/assets/audience-size.png)

* 對於個別區段和儲存的對象，總對象大小和CPM（若適用）會顯示在區段名稱旁。 您可以檢視區段的更多詳細資訊，包括依裝置類型（瀏覽器、行動裝置或連線電視）的大小。 對於儲存的對象，總大小為去重複化總計。

   ![個別區段大小](/help/dsp/assets/audience-size-segment.png)

## 受眾檢視

### 「所有對象」檢視

在 [!UICONTROL All Audiences] 檢視或受眾程式庫，您可以儲存和管理可重複使用的受眾，其中包括受眾群組區段，甚至其他已儲存的受眾。 您可以使用對象作為多個版位的目標。 版位名稱旁會顯示每個對象的使用版位數。

您可以編輯、原地複製、刪除、匯出或共用任何對象。

### 區段檢視

在 [!UICONTROL Segments] 檢視，所有使用者都可以建立其他自訂區段。

此 [!UICONTROL Segments] 檢視也列出下列區段類型：

* 使用者可使用所有使用者建立的自訂區段。

   您可以檢視您建立之任何自訂區段的追蹤標籤，並與其他使用者共用這些區段。 您也可以編輯或刪除您建立的自訂區段。

   您無法編輯或共用其他使用者已與您共用的自訂區段。

* 使用者可使用的所有匯入第一方區段。

   您無法編輯或共用已與您共用的第一方區段。 請連絡您的 [!DNL Adobe] 帳戶團隊。

* 使用者可使用的所有自訂第三方區段。

   您無法編輯或共用已與您共用的第三方區段。 請連絡您的 [!DNL Adobe] 客戶團隊。

>[!MORELIKETHIS]
>
>* [建立可重複使用的受眾](reusable-audience-create.md)
>* [對象設定](audience-settings.md)
>* [對象區段邏輯語法](audience-segment-logic-syntax.md)
>* [建立和實作自訂區段](custom-segment-create.md)
>* [建立和實作 [!UICONTROL CCPA Opt-Out-of-Sale] 區段](ccpa-opt-out-segment-create.md)
>* [可用的第三方資料提供者](third-party-data-providers.md)
>* [版位設定](/help/dsp/campaign-management/placements/placement-settings.md)

