---
title: 廣告商帳戶設定
description: 請參閱可用廣告商設定的說明。
source-git-commit: ee5621329aacf54777d28fa1c1f3d50949824cee
workflow-type: tm+mt
source-wordcount: '968'
ht-degree: 0%

---

# 廣告商帳戶設定

*只讀用戶不可用*

## [!UICONTROL General] 設定

**[!UICONTROL Advertiser Name]:** 廣告商名稱。

**[!UICONTROL Category]:** 廣告商業務運營的類別。 當您對清單進行投標時，該類別會傳達給發佈者。 確保您選擇與您的廣告相符的類別，否則發佈者可能會拒絕您的廣告。

>[!NOTE]
>
>如果選擇 *[!UICONTROL Other]*，則廣告商將無法訪DSP問 [!DNL On Demand Inventory]。

**[!UICONTROL Advertiser URL]:** 廣告商的首頁或主網站URL(從 `http://` 或 `https://`)。

**[!UICONTROL Share all private exchange feeds into this advertiser]:** （僅限新廣告商帳戶）使為組織帳戶配置的所有私DSP人交換源可供廣告商使用。

### [!UICONTROL Adobe IMS IDs]

使用Adobe Experience Cloud公司獨特產品的廣告商可以在某些產品之間共用資料 [!DNL Organization ID] Experience Cloud。 您可以在 [!UICONTROL Integrations] 的子菜單。

**[!UICONTROL Account IMS org and ID]:** (具有通過多個廣告商的Experience Cloud帳戶獲得許可的附加Experience Cloud產品的廣告商；可選)帳戶的Experience Cloud [!DNL Organization ID]。

**[!UICONTROL Advertiser IMS org and ID]:** (直接獲得附加Experience Cloud產品許可的廣告商；可選)廣告商的Experience Cloud [!DNL Organization ID]。

### [!UICONTROL Integrations]

（可選）連結到帳戶的其他Experience CloudDSP產品。 產品必須與同一Experience Cloud關聯 [!DNL Organization ID] 提供 [!UICONTROL Adobe IMS IDs] 的子菜單。

**[!UICONTROL Adobe Media Optimizer]:** (具有Advertising Cloud Search或使用Advertising Cloud轉換像素的廣告主)A [!DNL Search] 與之交DSP換屬性資料的帳戶。

**[!UICONTROL Adobe Device Co-op or 3rd Party Graph]:** (使用Advertising Cloud轉換像素的廣告商；可選)您可以使用設備圖表，根據Advertising Cloud Search廣告商的帳戶設定進行基於個人的屬性測量。

>[!NOTE]
>
> * 設備屬性僅可用於使用Advertising Cloud轉換跟蹤服務跟蹤的轉換，而不適用於Adobe Analytics跟蹤的轉換。
> * 您還可以選擇基於個人的設備圖形，以便在 [活動級別](/help/dsp/campaign-management/campaigns/campaign-settings.md)。 然後，可以設定跨設備目標 [放置級別](/help/dsp/campaign-management/placements/placement-settings.md) 還有更多的頻率 [包級別](/help/dsp/campaign-management/packages/package-settings.md) 和 [放置級別](/help/dsp/campaign-management/placements/placement-settings.md)。 跨設備目標和頻率管理不需要廣告商級別的屬性測量；相反，它們使用在市場活動設定中指定的設備圖形。


**[!UICONTROL Adobe Analytics]:** (Adobe Analytics的廣告商；可選；僅適用於使用包括Advertising Cloud轉換跟蹤標籤的 [!DNL EF Redirect] 和僅標籤)一個或多個 [!DNL Analytics] 報告套件，DSP將向其發送從發行商和供應方合作夥伴收集的資料。 分析還會將它從客戶端站點收集的資料發送到DSP。

要使資料顯示在報表套件中， [!DNL Search] 廣告商級設定為「」[!UICONTROL Enable tracking for SAINT feeds]必須啟用「 」。 此外，廣告商 [!DNL Analytics] 必須將帳戶配置為從Advertising Cloud接收資料。 <!-- from Advertising Cloud or DSP in particular? Add cross-reference to file in Integrations section. -->

>[!WARNING]
>
>如果刪除以前連結的報表套件，DSP則不再與該套件交換資料。 預計會看到資料波動。 <!-- Fluctuations where? Clarify -->

**[!UICONTROL Adobe Analytics Cloud]:** (Adobe Audience Manager或Adobe Analytics的廣告商；可選)Audience Manager或 [!DNL Analytics] 從中獲取DSP廣告商所有Adobe受眾的段元資料、層次資料和唯一受眾資料的帳戶。 這包括以下資料：

* Audience Manager段
* [!DNL Analytics] 發表給Adobe Experience Cloud的部分
* 在Adobe Experience Cloud使用 [!DNL People core service]
* 在Adobe Experience Platform建立並通過Audience Manager發送到Advertising Cloud的段

初始同步大約需要24小時。 之後，資料即時同步，延遲一到兩秒。
<!-- I don't think this is true anymore:
Segment membership data is sent to Advertising Cloud only after one of the following:

* The segment is targeted in an Advertising Cloud placement or audience library
* The segment is added to the Advertising Cloud batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] 設定

您可以選擇為廣告商的新投放配置預設目標。 用戶可以覆蓋任何新放置的預設目標。

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** 每個放置的地理位置目標的預設國家（地區）。 用戶可以更改國家/地區，並為每個位置配置更具體的地理目標。

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** 預設情況下要隱藏的任何受眾或段。 用戶可以更改每個位置的排除項。

### [!UICONTROL Media Quality]

#### [!UICONTROL Contextual Filtering]

類型 [!DNL Comscore]。 [!DNL DoubleVerify]。 [!DNL Integral Ad Science], [!DNL Peer39] 要應用的上下文篩選器。 您可以在 [放置級別](/help/dsp/campaign-management/placements/placement-settings.md)。

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** （可選）預設情況下要阻止的一種或多種類型的庫存上下文。 可能需要額外收費。

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** （可選）預設情況下目標的一種或多種庫存屬性類型。 可能需要額外收費。

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** （可選）預設情況下要阻止的一種或多種庫存屬性類型。 可能需要額外收費。

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** （可選）預設情況下要阻止廣告的成人內容的程度： *[!UICONTROL Do Not Block]* （預設值）, *[!UICONTROL Standard]*&#x200B;或 *[!UICONTROL Strict]*。 可能需要額外收費。

**[!UICONTROL Alcohol Content]:** （可選）預設情況下要阻止廣告的酒精含量程度： *[!UICONTROL Do Not Block]* （預設值）, *[!UICONTROL Standard]*&#x200B;或 *[!UICONTROL Strict]*。 可能需要額外收費。

#### [!UICONTROL Pre-Bid Fraud Blocking]

根據通過測量的欺詐性流量和可疑活動來阻止的站點類型 [!DNL DoubleVerify]。 [!DNL Integral Ad Science], [!DNL Peer39]。 您可以在 [放置級別](/help/dsp/campaign-management/placements/placement-settings.md)。

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** 預設情況下，會阻止所有100%的無效通信，包括被劫持設備上的通信，以便進行新放置。 可能需要額外收費。

**[!UICONTROL Also block sites with]:** （可選）預設情況下會導致阻止廣告的額DSP外欺詐和無效流量：  *[!UICONTROL None]* （預設值，不阻止其他通信）, *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*。 *[!UICONTROL >4% Average Fraud/IVT levels]*。 *[!UICONTROL >6% Average Fraud/IVT levels]*。 *[!UICONTROL >10% Average Fraud/IVT levels]*&#x200B;或 *[!UICONTROL >25% Average Fraud/IVT levels]*。 可能需要額外收費。

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** （可選）預設情況下導致阻止廣告的DSP一種或多種欺詐： *[!UICONTROL Fraud]* （它阻止所有站點存在欺詐） *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*，和 *[!UICONTROL Fraud: Zero Ads]*。 可能需要額外收費。

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** （可選）預設情況下導致阻止廣告的可疑網DSP站或應用活動類型： *[!UICONTROL None]* （預設，不根據可疑活動阻止廣告）, *[!UICONTROL Suspicious Activity - High Risk]*&#x200B;或 *[!UICONTROL Suspicious Activity - High or Moderate Risk]*。 可能需要額外收費。

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** 預設情況下， [[!DNL Ads.txt] 預標過濾](https://iabtechlab.com/ads-txt-about/) 通過利用每個發佈者 [!DNL Authorized Digital Sellers] 清單：
* *[!UICONTROL Opt out of ads.txt (default)]*:向所有賣家購買存貨。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*:優先購買域授權直銷商和轉銷商的庫存。
* *[!UICONTROL Ads.txt sellers only]*:僅從域的授權直銷商和轉銷商購買庫存。
* *[!UICONTROL Ads.txt sellers only]*:僅從域的授權直銷商購買庫存。

您可以在 [放置級別](/help/dsp/campaign-management/placements/placement-settings.md)。

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** 預設情況下，啟用即時投標後篩選器，以確保廣告在廣告商所瞄準的站點上服務。 <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Safety]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] 僅限客戶；可選)與組織關聯的品牌安全段ID [!DNL DoubleVerify] 帳戶。

**[!UICONTROL Enable Authentic Brand Safety]:** （可選）預設情況下，啟用 [!DNL DoubleVerify] 真品品牌安全，它使用為指定段ID配置的自定義品牌安全規則阻止在投標後觀感。 為段DSPID的使用記帳。

您可以覆蓋廣告商級別的位置設定。

>[!MORELIKETHIS]
>
>* [建立廣告商帳戶](/help/dsp/admin/advertiser-create.md)


<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
