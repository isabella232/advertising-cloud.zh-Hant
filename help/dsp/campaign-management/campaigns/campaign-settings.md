---
title: 市場活動設定
description: 請參閱可用市場活動設定的說明。
feature: DSP Campaigns
exl-id: ff2e22ff-8073-4532-884b-36e0c1f22641
source-git-commit: d7afcc2200adc41e583d21712226cb25f35aab66
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 0%

---

# 市場活動設定

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** 市場活動名稱。

**[!UICONTROL Advertiser]:** （現有活動的只讀）適用的廣告商（品牌）。 選擇現有廣告商或建立新廣告商。

**[!UICONTROL Advertiser URL]:** 廣告商的官方頁面。 此欄位可加快您與庫存合作夥伴的廣告審批流程。

**[!UICONTROL Timezone]:** （現有市場活動的只讀）報告和投標的時區。

**[!UICONTROL Customer PO]:** （可選）插入訂單/採購訂單的客戶採購訂單。

**[市場活動日期]:** 市場活動起始日期和終止日期。

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** 是否管理市場活動的邊距： *[!UICONTROL Yes]* 或 *[!UICONTROL No]* （預設）。

當您選擇 *[!UICONTROL Yes]。* 指定毛利類型和金額：

* **[!UICONTROL Margin Type]:** 邊距的類型。 啟用毛利管理並保存市場活動後，您就無法更改毛利類型。

   * *[!UICONTROL Fixed]:* （預設）允許Advertising Cloud DSP根據固定利潤百分比自動計算和限制支出 [!UICONTROL Gross Budget]。

   * *[!UICONTROL Dynamic]:* 允許您通過指定單獨的邊距來管理下至放置級別的邊距 [!UICONTROL Budget Reserve %] 和 [!UICONTROL Gross Budget] 每個包裹和廣告。 Advertising Cloud DSP根據每次配售的財務效率進行優化，而不保證一定的利潤。 對於由多個行項目組成的插入訂單，您可以使用此訂單以固定費率交付固定數量的單位或單位類型。

* **[!UICONTROL Fixed Margin %]:** （僅具有固定邊距的市場活動）每個插入訂單的預設加價 <!-- impression? -->的下界。 此金額從 [!UICONTROL Gross Budget] 定義淨市場活動預算。

* **[!UICONTROL Budget Reserve %]:** (僅具有固定利潤的活動；可選)保留指定百分比 [!UICONTROL Gross Budget] 作為保障。 此金額從 [!UICONTROL Gross Budget] 定義淨市場活動預算。

**[!UICONTROL Gross Budget]:** （僅具有毛利管理的市場活動）在應用指定的邊際調整之前的市場活動總預算。

您可以根據需要添加附加的每日、每週或每月總預算：

1. 按一下 **[!UICONTROL Add an additional Gross Budget]**.

1. 輸入 **[!UICONTROL Gross Budget]** 並選擇預算間隔： *[!UICONTROL Daily]。* *[!UICONTROL Weekly]。* 或 *[!UICONTROL Monthly]*。

總淨預算（即市場活動的支出上限）是根據毛利設定自動計算的，並在此值下面指明。

**[!UICONTROL Budget]:** （沒有毛利管理的市場活動）總體市場活動預算。

**[!UICONTROL Estimated Tax Withholding]:** 在國家/地方稅的帳戶級別中佔廣告費、廣告服務費和/或資料費總支出的百分比。 稅率是用於預算和調整用途的估計，因此開票的稅率可能有所不同。

要估計預扣的稅，請執行以下操作：

1. 按一下 **[!UICONTROL Update rates here]**.

1. 指定 **[!UICONTROL Estimated tax rate]**&#x200B;的下界。

1. 選中要預繳稅金的每個費用類型旁邊的複選框。 費用類型包括：

   * *[!UICONTROL Include estimated tax - ads fee]:* 適用於Advertising Cloud DSP所有媒體支出，包括競選管理費稅。

   * *[!UICONTROL Include estimated tax - ad serving fee]:* 適用於除媒體和資料外在Advertising Cloud DSP的所有支出。 它不包括促銷管理費的稅

   * *[!UICONTROL Include estimated tax - data fee]:* 適用於所有在Advertising Cloud DSP上花費的資料。

1. 按一下 **[!UICONTROL Submit]**.

>[!NOTE]
>
>* 在美國，州在將稅費納入廣告、廣告服務和資料時可能會有所不同。 對於其他國家/地區的組織，應將全部三類稅費納入增值稅。
>
>* 您也可以在帳戶的費用設定中配置這些值。<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->


**[!UICONTROL Cross Device Level]:** (2020年6月22日以來為現有活動建立的只讀活動；2020年6月22日之前建立的活動不可用)Advertising Cloud將投放廣告並應用頻率上限的級別： *相同設備* 目標設備或 *人物* 瞄準所有已知設備上的人。

**[!UICONTROL Device Graph]:** (現有市場活動只讀；僅使用基於人的跨設備目標的活動)用於跨設備目標和頻率管理的設備圖：

* *[!UICONTROL LiveRamp - U.S. only]:* 向所有廣告商提供以0.35美元CPM為目標的跨設備產品，供使用 [!DNL LiveRamp] 設備圖（即，在目標受眾段中找不到的設備）。 可以在放置級別設定跨設備目標。

   此選項也可供所有廣告商使用，無需任何費用，用於頻率管理和屬性測量。

**[!UICONTROL Frequency Cap]:** （可選）唯一設備或人員的次數(取決於指定的 [!UICONTROL Cross Device Level])將獲得競選廣告。 選項包括 *[!UICONTROL Unlimited]* 或每天、每週或每月的特定金額。

>[!NOTE]
>
> 您可以在市場活動、包裝和放置層設定頻率上限。 會DSP尊重市場活動等級中最嚴格的頻率限制。

**[!UICONTROL Packages]:** 的 [軟體包](/help/dsp/campaign-management/packages/package-about.md) 將其納入競選。 選擇現有包和/或建立要包括的包。 如果建立包，請參閱有關 [包設定](/help/dsp/campaign-management/packages/package-settings.md) 的子菜單。

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>以下設定僅啟用測量和報告功能。 效能優化僅在包和放置級別執行。

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:** （可選）啟用 [!DNL IAS] 使用指定設定測量和報告可視性、欺詐、品牌安全和觀眾驗證。 額外收費。

* **[!UICONTROL Measure On]:** 要衡量的庫存： *[!UICONTROL Display and VPAID video inventory]* （預設）或 *[!UICONTROL Display, VPAID & VAST video inventory]*。

   >[!NOTE]
   >
   >視頻可視性僅在VPAID清單上可測量。

* **[!UICONTROL IAS Account ID (AnID)]:** (擁有自己的廣告商 [!DNL IAS] 賬戶；可選)組織 [!DNL IAS] 帳戶ID, [!DNL IAS] 將直接收取使用費。

* **[!UICONTROL IAS Team ID]:** (擁有自己的廣告商 [!DNL IAS] 賬戶；可選)組織的團隊ID [!DNL IAS] 帳戶， [!DNL IAS] 將直接收取使用費。 <!-- verify -->

**[!UICONTROL MOAT]:** （可選）啟用 [!DNL MOAT] 可視性、欺詐、品牌安全以及觀眾驗證的計量和報告。 額外收費。

#### 受眾驗證

**[!UICONTROL Nielsen]:** （可選）啟用 [!DNL Nielsen] 使用指定的設定測量和報告觀眾驗證。 額外收費。

* **[!UICONTROL Target Gender]:** 目標性別： *[!UICONTROL Both]* （預設值）, *[!UICONTROL Male]*&#x200B;或 *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** 目標的年齡範圍。 使用左滑塊和右滑塊根據需要縮小範圍。

* **[!UICONTROL Target Country]:** （可選）要瞄準的國家。 [!DNL Nielsen] 將僅衡量在受支援國家所受影響。

**[!UICONTROL comScore vCE]:** （可選）啟用 [!DNL Comscore validated Campaign Essentials (vCE)] 使用指定的設定測量和報告觀眾驗證。 額外收費。

* **[!UICONTROL Target Gender]:** 目標性別： *[!UICONTROL Both]* （預設值）, *[!UICONTROL Male]*&#x200B;或 *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** 目標的年齡範圍。 使用左滑塊和右滑塊根據需要縮小範圍。

* **[!UICONTROL Target Country]:** （可選）要瞄準的國家。 [!DNL Comscore] 將僅衡量在受支援國家所受影響。

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** 使用 [!DNL IAB Open Video Viewability (OpenVV)] 技術，根據指定敏感度級別：

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [關於Campaign Management](campaign-about.md)
>* [建立市場活動](campaign-create.md)
>* [編輯市場活動](campaign-edit.md)

