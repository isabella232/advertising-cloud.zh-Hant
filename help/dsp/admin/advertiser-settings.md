---
title: 廣告商帳戶設定
description: 請參閱可用廣告商設定的說明。
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# 廣告商帳戶設定

*不適用於只讀用戶*

## [!UICONTROL General] 設定

**[!UICONTROL Advertiser Name]:** 廣告商名稱。

**[!UICONTROL Category]:** 廣告商業務運作的類別。 當您按庫存出價時，類別會傳送給發佈者。 請確定您選擇符合廣告的類別，否則發佈者可能會拒絕您的廣告。

>[!NOTE]
>
>如果您選取 *[!UICONTROL Other]*，則廣告商將無法存取DSP [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]:** 廣告商的首頁或主要網站URL(從 `http://` 或 `https://`)。

**[!UICONTROL Share all private exchange feeds into this advertiser]:** （僅限新廣告商帳戶）讓廣告商可使用為組織DSP帳戶設定的所有私人交換摘要。

### [!UICONTROL Adobe IMS IDs]

廣告商若有其他Adobe Experience Cloud產品，則可使用組織的不重複ID在某些產品間共用資料以供Experience Cloud。 您可以在 [!UICONTROL Integrations] 區段。

**[!UICONTROL Account IMS org and ID]:** (廣告商，其他Experience Cloud產品是透過具有多個廣告商的Experience Cloud帳戶授權；選用)廣告商的Experience Cloud組織ID。

**[!UICONTROL Advertiser IMS org and ID]:** (具有其他Experience Cloud產品直接許可的廣告商；選用)廣告商的Experience Cloud組織ID。

### [!UICONTROL Integrations]

（選用）連結至DSP帳戶的其他Experience Cloud產品。 產品必須與中提供的相同Experience Cloud組織ID相關聯， [!UICONTROL Adobe IMS IDs] 區段。

**[!UICONTROL Attribution services]> [!UICONTROL Adobe Media Optimizer]:** (廣告商與 [!DNL Adobe Advertising Search] 或使用Adobe廣告轉換像素) [!DNL Search] DSP將與其交換歸因資料的帳戶。

**[!UICONTROL Report suites]> [!UICONTROL Adobe Analytics]:** (廣告商與Adobe Analytics;可選；僅適用於使用Adobe廣告轉換追蹤標籤所收集的資料，這些標籤包含 [!DNL EF Redirect] 和代號)一或多個 [!DNL Analytics] DSP將向發佈商和供應方合作夥伴傳送其收集資料的報表套裝。 Analytics也會將其從用戶端網站收集的資料傳送至DSP。

若要讓資料顯示在報表套裝中， [!DNL Search] 廣告商層級設定為「[!UICONTROL Enable tracking for SAINT feeds]」。 此外，廣告商 [!DNL Analytics] 帳戶必須設定為從Adobe廣告接收資料。

>[!WARNING]
>
>如果您移除先前連結的報表套裝，DSP將不再與該套裝交換資料。 預期會出現資料波動。

如需與整合的詳細資訊 [!DNL Analytics]，請參閱「[概觀 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).&quot;

**[!UICONTROL Audiences]> [!UICONTROL Adobe Analytics Cloud]:** (廣告商包含Adobe Audience Manager或Adobe Analytics;選用)Audience Manager或 [!DNL Analytics] DSP將從中提取廣告商所有Adobe對象之區段中繼資料、階層資料和不重複對象資料的帳戶。 這包括下列項目的資料：

* Audience Manager區段
* [!DNL Analytics] 發佈至Adobe Experience Cloud的區段
* 在Adobe Experience Cloud中建立的區段使用 [!DNL People core service]
* 在Adobe Experience Platform中建立並透過Audience Manager傳送至Adobe廣告的區段

初始同步約需24小時。 之後，資料會即時同步，延遲一至兩秒。
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] 設定

您可以選擇為廣告商的新版位設定預設目標。 使用者可以覆寫任何新位置的預設目標。

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** 每個版位的地理定位預設國家/地區。 使用者可以變更國家，並針對每個版位設定更具體的地理定位。

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** 依預設要隱藏的任何對象或區段。 使用者可以變更每個版位的排除項目。

### [!UICONTROL Media Quality]

#### [!UICONTROL Contextual Filtering]

類型 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]，和 [!DNL Peer39] 要套用的內容篩選。 您可以在 [刊登層級](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** （可選）預設要封鎖的一或多種庫存內容類型。 可能需支付額外費用。

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** （可選）預設要定位的一或多種庫存屬性類型。 可能需支付額外費用。

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** （可選）預設要封鎖的一或多種庫存屬性類型。 可能需支付額外費用。

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** （可選）預設要封鎖廣告的成人內容程度： *[!UICONTROL Do Not Block]* （預設）、 *[!UICONTROL Standard]*，或 *[!UICONTROL Strict]*. 可能需支付額外費用。

**[!UICONTROL Alcohol Content]:** （可選）預設要封鎖廣告的酒精含量程度： *[!UICONTROL Do Not Block]* （預設）、 *[!UICONTROL Standard]*，或 *[!UICONTROL Strict]*. 可能需支付額外費用。

#### [!UICONTROL Pre-Bid Fraud Blocking]

根據欺詐性流量和通過 [!DNL DoubleVerify], [!DNL Integral Ad Science]，和 [!DNL Peer39]. 您可以在 [刊登層級](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** 依預設，會封鎖所有100%無效的流量，包括被劫持裝置上的流量，以用於新版位。 可能需支付額外費用。

**[!UICONTROL Also block sites with]:** （選用）預設情況下，會導致DSP封鎖廣告的額外欺詐和無效流量：  *[!UICONTROL None]* （預設值，不會封鎖其他流量）, *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]*，或 *[!UICONTROL >25% Average Fraud/IVT levels]*. 可能需支付額外費用。

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** （選用）依預設會導致DSP封鎖廣告的一或多種欺詐類型： *[!UICONTROL Fraud]* （會以欺詐方式阻止所有網站）, *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*，和/或 *[!UICONTROL Fraud: Zero Ads]*. 可能需支付額外費用。

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** （可選）預設導致DSP封鎖廣告的可疑網站或應用程式活動類型： *[!UICONTROL None]* （預設值，不會根據可疑活動封鎖廣告）, *[!UICONTROL Suspicious Activity - High Risk]*，或 *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. 可能需支付額外費用。

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** 依預設， [[!DNL Ads.txt] 預先競標篩選](https://iabtechlab.com/ads-txt-about/) 若要使用，請利用每個發佈者的 [!DNL Authorized Digital Sellers] 清單：
* *[!UICONTROL Opt out of ads.txt (default)]*:向所有賣家購買庫存。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*:優先購買域授權的直銷商和經銷商的庫存。
* *[!UICONTROL Ads.txt sellers only]*:僅向域授權的直銷商和經銷商購買庫存。
* *[!UICONTROL Ads.txt sellers only]*:僅向域的授權直銷商購買庫存。

您可以在 [刊登層級](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** 依預設，會啟用即時的出價後篩選，以確保廣告提供給廣告商所定位的網站。 <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Safety]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] 僅限客戶；選用)與組織關聯的品牌安全區段ID [!DNL DoubleVerify] 帳戶。

**[!UICONTROL Enable Authentic Brand Safety]:** （選用）依預設，啟用 [!DNL DoubleVerify] Authentic Brand Safety，可使用針對指定區段ID設定的自訂品牌安全規則來封鎖出價後曝光數。 DSP會向您的帳戶收取區段ID的使用金額。

您可以在版位層級覆寫廣告商層級的設定。

>[!MORELIKETHIS]
>
>* [建立廣告商帳戶](/help/dsp/admin/advertiser-create.md)


<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
