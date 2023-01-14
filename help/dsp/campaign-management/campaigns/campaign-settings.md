---
title: 促銷活動設定
description: 請參閱可用促銷活動設定的說明。
feature: DSP Campaigns
exl-id: ff2e22ff-8073-4532-884b-36e0c1f22641
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 0%

---

# 促銷活動設定

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** 促銷活動名稱。

**[!UICONTROL Advertiser]:** （現有促銷活動的唯讀）適用的廣告商（品牌）。 選取現有廣告商或建立新廣告商。

**[!UICONTROL Advertiser URL]:** 廣告商的正式頁面。 此欄位可加速您與詳細目錄合作夥伴的廣告核准程式。

**[!UICONTROL Timezone]:** （現有促銷活動的唯讀）報表和競標的時區。

**[!UICONTROL Customer PO]:** （可選）插入訂單/採購訂單的客戶採購訂單。

**[促銷活動日期]:** 促銷活動的開始和結束日期。

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** 是否管理促銷活動的邊距： *[!UICONTROL Yes]* 或 *[!UICONTROL No]* （預設）。

當您選擇 *[!UICONTROL Yes],* 指定邊距類型和金額：

* **[!UICONTROL Margin Type]:** 邊距的類型。 一旦啟用毛利管理並儲存促銷活動，便無法變更毛利類型。

   * *[!UICONTROL Fixed]:* （預設）允許DSP根據 [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* 允許您通過指定單獨的 [!UICONTROL Budget Reserve %] 和 [!UICONTROL Gross Budget] 促銷活動中的每個套件和版位。 DSP會根據每個版位的財務效率來最佳化，不需要保證特定的利潤。 對於由多個行項組成的插入訂單，您同意以固定費率交付固定數量的件數或件數類型，請使用此選項。

* **[!UICONTROL Fixed Margin %]:** （僅具有固定邊距的促銷活動）每個插入順序的預設標籤 <!-- impression? -->，百分比。 此金額會從 [!UICONTROL Gross Budget] 定義淨促銷活動預算。

* **[!UICONTROL Budget Reserve %]:** (僅具有固定利潤的促銷活動；選用)保留指定百分比 [!UICONTROL Gross Budget] 作為保障。 此金額會從 [!UICONTROL Gross Budget] 定義淨促銷活動預算。

**[!UICONTROL Gross Budget]:** （僅限具有毛利管理的促銷活動）在套用指定的邊際調整之前的促銷活動預算總額。

您可以選擇新增額外的每日、每週或每月總預算：

1. 按一下 **[!UICONTROL Add an additional Gross Budget]**.

1. 輸入 **[!UICONTROL Gross Budget]** 並選擇預算間隔： *[!UICONTROL Daily],* *[!UICONTROL Weekly],* 或 *[!UICONTROL Monthly]*.

總淨預算（即促銷活動的支出上限）會根據利潤設定自動計算，並在此值下方指出。

**[!UICONTROL Budget]:** （無利潤管理的促銷活動）整體促銷活動預算。

**[!UICONTROL Estimated Tax Withholding]:** 在國家/地區或地方稅的帳戶層級中，其佔廣告費、廣告服務費和/或資料費總支出的百分比。 稅率是預算和步調的估計，因此開具發票的稅率可能有所不同。

要估計預扣的稅，請執行以下操作：

1. 按一下 **[!UICONTROL Update rates here]**.

1. 指定 **[!UICONTROL Estimated tax rate]**，百分比。

1. 選擇要預扣稅的每個費用類型旁邊的複選框。 費用類型包括：

   * *[!UICONTROL Include estimated tax - ads fee]:* 適用於所有Advertising DSP媒體支出，包括行銷活動管理費稅。

   * *[!UICONTROL Include estimated tax - ad serving fee]:* 套用至除媒體和資料外的所有Advertising DSP支出。 它不包括競選管理費的稅

   * *[!UICONTROL Include estimated tax - data fee]:* 套用至Advertising DSP上的所有資料支出。

1. 按一下 **[!UICONTROL Submit]**.

>[!NOTE]
>
>* 在美國，各州在將稅費納入廣告、廣告服務和資料方面可能會有所不同。 對於其他國家/地區的組織，包括所有三類稅費，以計算增值稅。
>
>* 您也可以在帳戶的費用設定中設定這些值。<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->


**[!UICONTROL Cross Device Level]:** (自2020年6月22日起建立之現有促銷活動的唯讀；不適用於2020年6月22日之前建立的促銷活動)DSP將定位廣告並套用頻率上限的層級： *相同裝置* 定位設備或 *人員* 將目標鎖定在所有已知裝置上。

**[!UICONTROL Device Graph]:** (現有行銷活動的唯讀；僅限使用以人物為基礎的跨裝置鎖定目標的促銷活動)用於跨裝置鎖定目標和頻率管理的裝置圖表：

* *[!UICONTROL LiveRamp - U.S. only]:* 以$0.35 CPM供所有跨裝置目標定位的廣告商使用，以了解透過 [!DNL LiveRamp] 裝置圖表（亦即針對在目標受眾區段內找不到的裝置）。 您可以在放置層級設定跨裝置定位。

   此選項也可供所有廣告商使用，不需支付任何費用，便可用於頻率管理和歸因測量。

**[!UICONTROL Frequency Cap]:** （選用）不重複裝置或人員的次數(取決於指定 [!UICONTROL Cross Device Level])將會從行銷活動中提供廣告。 選項包括 *[!UICONTROL Unlimited]* 或每天、每週或每月的特定數量。

>[!NOTE]
>
> 您可以在促銷活動、封裝和位置層級設定頻率上限。 DSP將遵循促銷活動階層中最嚴格的頻率上限。

**[!UICONTROL Packages]:** 此 [套件](/help/dsp/campaign-management/packages/package-about.md) 以包含在促銷活動中。 選擇現有包和/或建立要包含的包。 如果您建立套件，請參閱 [套件設定](/help/dsp/campaign-management/packages/package-settings.md) 以取得更多資訊。

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>下列設定僅啟用測量和報告功能。 效能最佳化只會在封裝和放置層級執行。

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** （可選）啟用 [!DNL IAS] 使用指定的設定，測量並報告可見度、詐騙、品牌安全和受眾驗證。 需支付額外費用。

* **[!UICONTROL Measure On]:** 要測量的清單： *[!UICONTROL Display and VPAID video inventory]* （預設）或 *[!UICONTROL Display, VPAID & VAST video inventory]*.

   >[!NOTE]
   >
   >視訊可檢視性僅可在VPAID詳細目錄中測量。

* **[!UICONTROL IAS Account ID (AnID)]:** (廣告商擁有自己的 [!DNL IAS] 賬戶；選用)組織的 [!DNL IAS] 帳戶ID, [!DNL IAS] 將直接收費以供使用。

* **[!UICONTROL IAS Team ID]:** (廣告商擁有自己的 [!DNL IAS] 賬戶；選用)組織的團隊ID [!DNL IAS] 帳戶， [!DNL IAS] 將直接收費以供使用。 <!-- verify -->

**[!UICONTROL MOAT]:** （可選）啟用 [!DNL MOAT] 可見度、欺詐、品牌安全和受眾驗證的測量和報告。 需支付額外費用。

#### 受眾驗證

**[!UICONTROL Nielsen]:** （可選）啟用 [!DNL Nielsen] 使用指定設定來測量和報告受眾驗證。 需支付額外費用。

* **[!UICONTROL Target Gender]:** 目標性別： *[!UICONTROL Both]* （預設）、 *[!UICONTROL Male]*，或 *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** 要定位的年齡範圍。 視需要使用左滑桿和右滑桿來縮小範圍。

* **[!UICONTROL Target Country]:** （選用）要定位的國家。 [!DNL Nielsen] 只會測量在受支援國家/地區提供的曝光數。

**[!UICONTROL comScore vCE]:** （可選）啟用 [!DNL Comscore validated Campaign Essentials (vCE)] 使用指定設定來測量和報告受眾驗證。 需支付額外費用。

* **[!UICONTROL Target Gender]:** 目標性別： *[!UICONTROL Both]* （預設）、 *[!UICONTROL Male]*，或 *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** 要定位的年齡範圍。 視需要使用左滑桿和右滑桿來縮小範圍。

* **[!UICONTROL Target Country]:** （選用）要定位的國家。 [!DNL Comscore] 只會測量在受支援國家/地區提供的曝光數。

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** 啟用第一方測量和檢視度報告，使用 [!DNL IAB Open Video Viewability (OpenVV)] 技術，根據指定的敏感度級別：

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [關於Campaign Management](campaign-about.md)
>* [建立促銷活動](campaign-create.md)
>* [編輯促銷活動](campaign-edit.md)

