---
title: 促銷活動設定
description: 請參閱可用促銷活動設定的說明。
feature: Campaigns
exl-id: ff2e22ff-8073-4532-884b-36e0c1f22641
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '990'
ht-degree: 0%

---

# 促銷活動設定

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** 促銷活動名稱。

**[!UICONTROL Advertiser]:** （現有促銷活動的唯讀）適用的廣告商（品牌）。選取現有廣告商或建立新廣告商。

**[!UICONTROL Advertiser URL]:** 廣告商的官方頁面。此欄位可加速您與詳細目錄合作夥伴的廣告核准程式。

**[!UICONTROL Timezone]:** （現有促銷活動的唯讀）報表與競標的時區。

**[!UICONTROL Customer PO]:** （可選）插入訂單/採購訂單的客戶採購訂單。

**[促銷活動日期]:** 促銷活動的開始和結束日期。

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** 是否管理促銷活動的邊距： *[!UICONTROL Yes]* 或( *[!UICONTROL No]* 預設值)。

選擇&#x200B;*[!UICONTROL Yes]時，*&#x200B;指定邊界類型和金額：

* **[!UICONTROL Margin Type]:** 邊界的類型。一旦啟用毛利管理並儲存促銷活動，便無法變更毛利類型。

   * *[!UICONTROL Fixed]:* （預設值）允許Advertising Cloud DSP根據的固定利潤百分比自動計算和限制支 [!UICONTROL Gross Budget]出。

   * *[!UICONTROL Dynamic]:* 可讓您為促銷活動中的每個套件和版位指 [!UICONTROL Budget Reserve %] 定 [!UICONTROL Gross Budget] 個別的和，以深入管理版位層級。Advertising Cloud DSP會根據每次配售的財務效率來最佳化，而無須保證特定利潤。 對於由多個行項組成的插入訂單，您同意以固定費率交付固定數量的件數或件數類型，請使用此選項。

* **[!UICONTROL Fixed Margin %]:** （僅具有固定邊距的促銷活動）每個插入順序的預 <!-- impression? -->設標籤（以百分比表示）。此金額會從[!UICONTROL Gross Budget]中扣除，以定義淨促銷活動預算。

* **[!UICONTROL Budget Reserve %]:** (僅具有固定邊距的促銷活動；可選)保留指定百分比 [!UICONTROL Gross Budget] 作為保護。此金額會從[!UICONTROL Gross Budget]中扣除，以定義淨促銷活動預算。

**[!UICONTROL Gross Budget]:** （僅限具有毛利管理的促銷活動）在套用指定的邊際調整之前的促銷活動預算總額。

您可以選擇新增額外的每日、每週或每月總預算：

1. 按一下 **[!UICONTROL Add an additional Gross Budget]**.

1. 輸入&#x200B;**[!UICONTROL Gross Budget]**&#x200B;並選擇預算間隔：*[!UICONTROL Daily]、* *[!UICONTROL Weekly]、*&#x200B;或&#x200B;*[!UICONTROL Monthly]*。

總淨預算（即促銷活動的支出上限）會根據利潤設定自動計算，並在此值下方指出。

**[!UICONTROL Budget]:** （無毛利管理的促銷活動）整體促銷活動預算。

**[!UICONTROL Estimated Tax Withholding]:** 在國家/地區或地方稅的帳戶層級，保留廣告費、廣告服務費和/或資料費的總支出百分比。稅率是預算和步調的估計，因此開具發票的稅率可能有所不同。

要估計預扣的稅，請執行以下操作：

1. 按一下 **[!UICONTROL Update rates here]**.

1. 以百分比形式指定&#x200B;**[!UICONTROL Estimated tax rate]**。

1. 選擇要預扣稅的每個費用類型旁邊的複選框。 費用類型包括：

   * *[!UICONTROL Include estimated tax - ads fee]:* 適用於所有Advertising Cloud DSP媒體支出，包括行銷活動管理費稅。

   * *[!UICONTROL Include estimated tax - ad serving fee]:* 適用於除媒體和資料外的所有Advertising Cloud DSP支出。它不包括競選管理費的稅

   * *[!UICONTROL Include estimated tax - data fee]:* 套用至所有資料支出Advertising Cloud DSP。

1. 按一下 **[!UICONTROL Submit]**.

>[!NOTE]
>
>* 在美國，各州在將稅費納入廣告、廣告服務和資料時可能會有所不同。 對於其他國家/地區的組織，包括所有三類稅費，以計算增值稅。
>
>* 您也可以在帳戶的費用設定中配置這些值。<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->


**[!UICONTROL Cross Device Level]:** (2020年6月22日以來建立之現有促銷活動的唯讀；2020年6月22日之前建立的促銷活動無法使用)Advertising Cloud將定位廣告並套用頻率上限的層級： *將目* 標鎖定於裝置的相 ** 同裝置，或將目標鎖定於其所有已知裝置上的人員。

**[!UICONTROL Device Graph]:** (現有促銷活動的唯讀；僅限使用以人物為基礎的跨裝置鎖定目標的促銷活動)用於跨裝置鎖定目標和頻率管理的裝置圖表：

* *[!UICONTROL LiveRamp - U.S. only]:* 對於跨裝置鎖定目標的所有廣告商，請以$0.35 CPM使用裝置圖表所傳遞的曝光數(亦即在目標受眾區 [!DNL LiveRamp] 段內找不到的裝置)。您可以在放置層級設定跨裝置定位。

   此選項也可供所有廣告商使用，不需支付任何費用，便可用於頻率管理和歸因測量。

* *[!UICONTROL Adobe Co-op U.S. and Canada only]:* 僅供Adobe Experience Cloud參 [!DNL Device Co-op] 與者使用，不需額外付費。

>[!TIP]
>
>如果廣告商也使用跨裝置歸因，則最佳實務是使用與廣告商的跨裝置歸因設定中指定的相同裝置圖表設定來進行定位和頻率管理。 如果您為此促銷活動選取不同的裝置圖表，則可能會發生不一致的報表。

**[!UICONTROL Frequency Cap]:** （選用）從促銷活動向不重複裝置或人員(視指 [!UICONTROL Cross Device Level]定)提供廣告的次數。選項包括&#x200B;*[!UICONTROL Unlimited]*&#x200B;或每天、每週或每月的特定數量。

>[!NOTE]
>
> 您可以在促銷活動、封裝和位置層級設定頻率上限。 DSP將遵循促銷活動階層中最嚴格的頻率上限。

**[!UICONTROL Packages]:** 要 [](/help/dsp/campaign-management/packages/package-about.md) 包含在促銷活動中的套件。選擇現有包和/或建立要包含的包。 如果您建立包，請參閱[包設定](/help/dsp/campaign-management/packages/package-settings.md)的相關說明以了解詳細資訊。

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>下列設定僅啟用測量和報告功能。 效能最佳化只會在封裝和放置層級執行。

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** （選用）啟用 [!DNL IAS] 可檢視性、詐騙、品牌安全性和受眾驗證的測量與報告，使用指定的設定。需支付額外費用。

* **[!UICONTROL Measure On]:** 要測量的庫存： *[!UICONTROL Display and VPAID video inventory]* （預設值）或 *[!UICONTROL Display, VPAID & VAST video inventory]*。

   >[!NOTE]
   >
   >視訊可檢視性僅可在VPAID詳細目錄中測量。

* **[!UICONTROL IAS Account ID (AnID)]:** (具有其自有帳戶的廣告 [!DNL IAS] 商；選用)組織的帳 [!DNL IAS] 戶ID，會 [!DNL IAS] 直接計費以供使用。

* **[!UICONTROL IAS Team ID]:** (具有其自有帳戶的廣告 [!DNL IAS] 商；選用)組織帳戶的團隊ID, [!DNL IAS] 會直 [!DNL IAS] 接收費以取用。  <!-- verify -->

**[!UICONTROL MOAT]:** （選用）啟用可 [!DNL MOAT] 見度、詐騙、品牌安全性和受眾驗證的測量與報告功能。需支付額外費用。

#### 受眾驗證

**[!UICONTROL Nielsen]:** （選用）啟 [!DNL Nielsen] 用使用指定設定的測量和報表對象驗證。需支付額外費用。

* **[!UICONTROL Target Gender]:** 要定位的性別： *[!UICONTROL Both]* （預設）、  *[!UICONTROL Male]*&#x200B;或  *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** 要定位的年齡範圍。視需要使用左滑桿和右滑桿來縮小範圍。

* **[!UICONTROL Target Country]:** （選用）要定位的國家/地區。[!DNL Nielsen] 只會測量在受支援國家/地區提供的曝光數。

**[!UICONTROL comScore vCE]:** （選用）啟 [!DNL Comscore validated Campaign Essentials (vCE)] 用使用指定設定的測量和報表對象驗證。需支付額外費用。

* **[!UICONTROL Target Gender]:** 要定位的性別： *[!UICONTROL Both]* （預設）、  *[!UICONTROL Male]*&#x200B;或  *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** 要定位的年齡範圍。視需要使用左滑桿和右滑桿來縮小範圍。

* **[!UICONTROL Target Country]:** （選用）要定位的國家/地區。[!DNL Comscore] 只會測量在受支援國家/地區提供的曝光數。

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** 根據指定的敏感度級別，啟用使用 [!DNL IAB Open Video Viewability (OpenVV)] 技術進行第一方測量和檢視度報告：

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [關於促銷活動管理](campaign-about.md)
>* [建立促銷活動](campaign-create.md)
>* [編輯促銷活動](campaign-edit.md)

