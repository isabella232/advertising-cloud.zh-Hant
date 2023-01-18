---
title: 品牌安全與媒體品質
description: 進一步了解品牌安全和媒體品質功能。
feature: DSP Introduction
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '1350'
ht-degree: 0%

---

# 品牌安全與媒體品質

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising DSP提供一套品牌保護功能，確保您的每個行銷活動都能在品牌安全的環境中觸及真正的使用者。

我們的欺詐監控團隊與業界領先合作夥伴(例如 [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)]，和 [!DNL WhiteOps]，以謹慎組織平台上的詳細目錄。 透過主動管理我們的供應，DSP可確保平台上的所有廣告商不受非人類流量（機器人、編目程式、資料中心流量和詐騙）的保護，並只在品牌安全的環境中傳送。

除了提供集中品質管理外，我們相信讓廣告商能夠設計符合其品牌的控制項。 DSP提供與 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud]，和 [!DNL Peer39]，確保每個廣告商都能選擇其所需的詐騙保護、情境篩選和關鍵字鎖定目標等級。

## 質量計畫

### 清單驗證 [!DNL Ads.txt] 支援

[[!DNL Ads.txt]，代表 [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) 是由 [!DNL Interactive Advertising Bureau] ([!DNL IAB])，以促進存貨在公開市場上的適當代表，從而打擊非法的流量來源及網域欺騙。 參與的發行商和分銷商會公開宣佈獲授權銷售其數位庫存的公司，以及這些關係的性質，方法是維持 `ads.txt` 頁面(例如 `example.com/ads.txt`)。

DSP支援 [!DNL ads.txt] 閱讀每個出版商的 `ads.txt` 檔案，並提供您僅從已驗證 [!DNL ads.txt] 賣家。 例如，透過比對我們看到可存取的賣家 `nytimes.com` 《紐約時報》 `ads.txt` 檔案中，我們可以識別哪些是合法的，哪些不是，而且，如果將版位設定為僅向經過驗證的賣家購買，我們將阻止違規者。 <!-- can we actually mention NY Times? -->

您可以設定預設值 [!DNL ads.txt] 每個廣告商的控制<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然後選擇性 [自訂每個版位的設定](/help/dsp/campaign-management/placements/placement-settings.md) 至：

* 僅向域的授權直銷商購買庫存

* 僅向域的授權直銷商和經銷商購買庫存

* 優先向域的授權直銷商和經銷商購買庫存

* 從所有賣家處購買庫存

### 平台欺詐監視

DSP與業界領先的廠商(例如 [!DNL Whiteops] 和 [!DNL Integral Ad Science].

此外，Adobe與 [!DNL IAB] 和 [!DNL TAG] 以利用工具(例如 [!DNL ads.txt] （請參閱上一節）、 [!DNL IAB] 機器人與編目程式清單，以及 [!DNL TAG] 資料中心IP清單。

透過我們的多維度品質方法，我們的團隊會監控異常和無效的流量模式，確保受保護庫存上的無效流量少於3%。 任何可疑的清單（包括特定域的清單或特定發佈商或銷售商的清單）都會立即在整個平台上被阻止。

### 庫存映射、分層和分類

庫存對應是所有新庫存新增至我們的平台之前，所需的詳細審核及上線程式。 此程式的設計目的，是確保DSP上所有庫存的安全與品質。

* **對應：** 我們的庫存團隊會仔細檢查每個網域，並評估以下方面：

   * 品牌安全

   * 廣告類型驗證

   * 一般內容、重複網域和假廣告服務

* **分層：** 我們會全面檢查整體生態系統中的品牌存在性，以便跨不同層級分類存貨。 您可以 [定位您的投放位置](/help/dsp/campaign-management/placements/placement-settings.md) 到這些層，以滿足所需的觸及級別：

   * **[!UICONTROL T1]**  — 品牌名稱、國際知名網站

   * **[!UICONTROL T2]**  — 美觀的網站，是最新、不含使用者產生的內容，且通常缺乏全球認可

   * **[!UICONTROL T3]**  — 用戶生成的內容和小眾內容

* **站點分類：** 為了確保輕鬆鎖定和封鎖內容，我們會根據屬性的內容，以DSP定義的網站類別標籤每個屬性。 您可以 [定位或排除每個位置的這些網站類別](/help/dsp/campaign-management/placements/placement-settings.md) 根據投放目標。

### 全面支援站點阻止

DSP提供全域封鎖的網站清單，以及為廣告商和帳戶建立自訂封鎖網站清單的選項。

#### DSP全域封鎖的網站清單 {#global-blocked-sites}

DSP會維護一個被全域封鎖的網站清單，列出在上執行廣告時認為不安全的網站。 此清單包含具有不良內容（例如仇恨或恐怖）的網站，以及受機器人、假前段、不相符的網域和其他欺詐活動感染的網站。

作為我們品牌安全計畫的一部分，以根除詐騙廣告商的活動，系統會使用圖表中已封鎖網站清單的測量來篩選所有網站。 未通過品牌安全檢查的所有網站都會新增至全域封鎖的網站清單。 由於DSP會以動態方式管理此清單，因此網站可能會根據最新的品牌安全分析隨時從清單上移動或移出。

當您在全域封鎖的網站清單中加入網站作為版位目標時，系統會以紅色驚嘆號(!)標籤該網站。 這表示廣告不會在已標幟的網站上執行。

>[!NOTE]
>
>您可以啟用「[!UICONTROL Allow unscreened sites]」選項 [版位設定](/help/dsp/campaign-management/placements/placement-settings.md). 如有必要， [!DNL Adobe] 客戶團隊還可以選擇在交易的發佈者設定中停用公開（拍賣層級）交易的網站封鎖。

#### 帳戶層級和廣告商層級封鎖的網站清單

使用者也可以維護帳戶層級和廣告商層級的封鎖網站清單<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->，會自動用於所有版位。 除了全局阻止的站點清單外，還會應用較低級別的阻止的站點清單。

## 協力廠商整合

### 內容篩選

內容篩選可讓您根據廣告將提供的頁面內容來鎖定或封鎖廣告機會。 Adobe透過與業界領先廠商的整合提供內容篩選： [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]，和 [!DNL Peer39]. 目前的篩選器範例包括 [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics]，和 [!UICONTROL G-rated Sites].

您可以為每個廣告商設定預設的內容篩選控制項<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然後選擇性 [自訂每個版位的設定](/help/dsp/campaign-management/placements/placement-settings.md). 使用此功能時，可能需支付額外費用。

![Comscore標誌](/help/dsp/assets/comscore-logo.png) ![DoubleVerify徽標](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science標誌](/help/dsp/assets/ias-logo.png) ![Peer39徽標](/help/dsp/assets/peer39-logo.png)

### 投標前欺詐阻止

透過 [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]，和 [!DNL Peer39] 封鎖來自您促銷活動的非人類流量。 這些整合提供領先業界的出價前封鎖功能，以將行銷活動中的一般和複雜的無效流量（GIVT和SIVT）降到最低。

您可以為每個廣告商設定預設的出價前欺詐封鎖控制項<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然後選擇性 [自訂每個版位的設定](/help/dsp/campaign-management/placements/placement-settings.md). 使用此功能時，可能需支付額外費用。

如需功能的詳細資訊，請直接聯絡您偏好的廠商，或聯絡您的 [!DNL Adobe] 客戶團隊。

![Comscore標誌](/help/dsp/assets/comscore-logo.png) ![DoubleVerify徽標](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science標誌](/help/dsp/assets/ias-logo.png) ![Peer39徽標](/help/dsp/assets/peer39-logo.png)

### 預先出價的可檢視性 {#pre-bid-viewability}

由我們領先業界的合作夥伴提供技術支援的出價前可檢視性篩選條件 [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat])和 [!DNL Integral Ad Science] 可讓廣告商確保其促銷活動符合其所需的視訊可檢視性效能目標，並顯示詳細目錄。

您可以為每個廣告商設定預設的可檢視性篩選條件<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然後選擇性 [自訂每個版位的設定](/help/dsp/campaign-management/placements/placement-settings.md). 使用此功能時，可能需支付額外費用。

![DoubleVerify徽標](/help/dsp/assets/doubleverify-logo.png) ![Oracle廣告標誌](/help/dsp/assets/oracle-advertising-logo.png) ![Integral Ad Science標誌](/help/dsp/assets/ias-logo.png)

### 主題定位

DSP主題鎖定目標可讓您利用我們領先業界的情境合作夥伴來鎖定或封鎖關鍵字清單 [!DNL Comscore] 和 [!DNL Oracle Data Cloud] ([!DNL Grapeshot])。 主題鎖定目標可協助您確保廣告總是在符合您品牌的環境中提供，包括封鎖有害內容或確保在可確保更佳結果的環境中花費。

主題鎖定目標需要您直接使用 [!DNL Comscore] 或 [!DNL Grapeshot] (使用 [!DNL Oracle Data Cloud])。 在合作夥伴平台中建立這些檔案後，您就可以 [在 [!UICONTROL Audience Targeting] 每個放置的區段](/help/dsp/campaign-management/placements/placement-settings.md). 此功能可能需額外付費。

若要建立自訂主題區段：

* 建立 [!DNL Comscore] 帳戶和建立自訂區段時，您可以要求登入 [!DNL Activation Segment Manager] at [https://agents.comscore.com](https://agents.comscore.com). 請參閱 [[!DNL Comscore] 協助中心](https://comscoreactivation.zendesk.com/hc/) 以取得設定自訂區段的完整指示。 自訂區段的費用會顯示在 [!DNL Segment Manager] 當您建立時。

* 若要開始使用 [!DNL Oracle Data Cloud]，聯絡 [!DNL Oracle Data Cloud] 或 [!DNL Adobe] 客戶團隊。

![Comscore標誌](/help/dsp/assets/comscore-logo.png) ![Grapeshot標誌](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP與 [!DNL DoubleVerify] 提供 [!DNL Authentic Brand Safety] 鎖定目標解決方案，可讓您建立一組集中的品牌安全需求，以針對所有購買平台，以保持一致。

一旦您建立 [!DNL DoubleVerify] 品牌安全區段搭配必要的定位，您可以在DSP內使用該區段，在網路環境中以預先出價複製您的出價後區塊規則。

您可以指定 [!DNL DoubleVerify] 每個廣告商的區段ID<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然後選擇性 [啟用或禁用 [!UICONTROL Authentic Brand Safety] 每個版位](/help/dsp/campaign-management/placements/placement-settings.md). DSP會向您的帳戶收取區段ID的使用金額。

如需功能的詳細資訊，請聯絡 [!DNL DoubleVerify] 直接聯繫，或 [!DNL Adobe] 客戶團隊。

![DoubleVerify徽標](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [版位設定](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
