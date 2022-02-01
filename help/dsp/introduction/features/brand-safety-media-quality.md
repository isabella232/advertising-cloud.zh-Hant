---
title: 品牌安全與媒體質量
description: 瞭解有關品牌安全和媒體質量功能的更多資訊。
feature: DSP Introduction
exl-id: df5be5d4-490e-479f-b76d-4fda4acd4201
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '1315'
ht-degree: 0%

---

# 品牌安全與媒體質量

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising Cloud DSP提供一套品牌保護功能，確保您的每項活動都能在一個品牌安全的環境中接觸到真正的用戶。

我們的欺詐監控團隊與業界領先的合作夥伴(如 [!DNL Interactive Advertising Bureau]。 [!DNL Trust and Accountability Group] [!DNL (TAG)], [!DNL WhiteOps]，以在我們的平台上仔細地管理清單。 通過主動預防性地管理我們的供應DSP，確保平台上的所有廣告商都免受非人為流量（bot 、 Crawler 、資料中心流量和欺詐）的侵擾，並僅在品牌安全的環境中交付。

除了提供中央質量管理，我們還相信讓廣告商設計與其品牌相一致的控制。 Adobe Advertising Cloud提供整合 [!DNL Comscore]。 [!DNL DoubleVerify]。 [!DNL Integral Ad Science]。 [!DNL Oracle Data Cloud], [!DNL Peer39]確保每個廣告商都能夠選擇其所需的欺詐保護、上下文過濾和關鍵字目標。

## Advertising Cloud DSP質量計畫

### 庫存驗證 [!DNL Ads.txt] 支援

[[!DNL Ads.txt]，表示 [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) 是由 [!DNL Interactive Advertising Bureau] ([!DNL IAB])，以促進在公開市場上正確顯示庫存，從而打擊非法的流量來源及域欺騙。 參與的發行商和分銷商通過維護 `ads.txt` 在域的頂層(如 `example.com/ads.txt`)。

DSP支 [!DNL ads.txt] 通過閱讀每家出版商的 `ads.txt` 檔案，並提供僅從驗證的 [!DNL ads.txt] 賣家。 例如，通過匹配我們看到的銷售商 `nytimes.com` 《紐約時報》 `ads.txt` 檔案，我們可以識別哪些是合法的，哪些是不合法的，並且如果配置為只向經驗證的賣家購買，我們會阻止違規者。 <!-- can we actually mention NY Times? -->

可以設定預設值 [!DNL ads.txt] 控制<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然後可選 [定制每個放置的設定](/help/dsp/campaign-management/placements/placement-settings.md) 至：

* 僅從域的授權直銷商購買庫存

* 僅從域的授權直接銷售商和轉銷商購買庫存

* 優先從域的授權直銷商和轉銷商購買庫存

* 向所有賣家購買庫存

### 平台欺詐監控

DSP與業界領先供應商合作，如 [!DNL Whiteops] 和 [!DNL Integral Ad Science]。

此外，Adobe與 [!DNL IAB] 和 [!DNL TAG] 確保通過利用工具(如 [!DNL ads.txt] （請參閱上一節）, [!DNL IAB] 《機器人與蜘蛛》 [!DNL TAG] 資料中心IP清單。

通過我們的多維質量方法，我們的團隊可監控異常和無效的通信模式，確保受保護清單上的無效通信少於3%。 任何可疑的清單 — 包括特定域或特定發佈者或銷售者的清單 — 都會立即在整個平台上被阻止。

### 清單映射、分層和分類

清單映射是所有新清單添加到我們的平台之前所需的詳細審核和上門流程。 此流程旨在確保所有庫存的安全和質DSP量。

* **映射：** 我們的Inventory團隊仔細審查了每個域，評估了以下方面：

   * 品牌安全

   * 廣告類型驗證

   * 一般內容、重複域和虛假廣告服務

* **分層：** 我們全面地檢查整個生態系統中的品牌存在情況，以跨不同層對庫存進行分類。 你可以 [瞄準定位](/help/dsp/campaign-management/placements/placement-settings.md) 到這些層以達到所需的訪問級別：

   * **[!UICONTROL T1]**  — 品牌名稱，國際知名站點

   * **[!UICONTROL T2]**  — 外觀精美的站點，這些站點是最新的，沒有用戶生成的內容，通常缺乏全球識別

   * **[!UICONTROL T3]**  — 用戶生成的內容和小眾內容

* **站點分類：** 為確保輕鬆確定內容目標和阻止，我們根據屬性的內容為每個屬性添加一個Advertising Cloud定義的站點類別。 你可以 [每個放置的目標或排除這些站點類別](/help/dsp/campaign-management/placements/placement-settings.md) 根據投放目標。

### 全面支援站點阻止

Advertising Cloud DSP提供了全局阻止的網站清單和為廣告商和帳戶建立自定義阻止的網站清單的選項。

#### Advertising Cloud DSP全球阻止的站點清單 {#global-blocked-sites}

Advertising Cloud DSP維護一個被全球屏蔽的網站清單，列出在上運行廣告時被認為不安全的網站。 此清單包含包含令人反感內容（如仇恨或恐怖）的站點，以及受bot 、假預滾、不匹配的域和其他欺詐活動感染的站點。

作為我們的品牌安全計畫的一部分，我們將根除欺詐廣告商的活動，使用圖表阻止站點清單中的度量來篩選所有站點。 所有未通過品牌安全檢查的站點都將添加到全局阻止的站點清單中。 由於Advertising Cloud DSP動態管理此清單，因此根據最新的品牌安全分析，站點可能隨時會在清單上移動或移出。

當您將一個站點作為放置目標包含在全局阻止的站點清單中時，該站點將標籤為紅色感嘆號(!)。 這表示廣告不會在標籤的站點上運行。

#### 帳戶級和廣告商級被阻止的站點清單

用戶還可以維護帳戶級和廣告商級被阻止的站點清單<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->，它將自動用於所有放置。 除了全局阻止的站點清單外，還應用低級阻止的站點清單。

## 第三方整合

### 上下文篩選

上下文過濾允許您根據廣告所服務的頁面的上下文來定位或阻止廣告機會。 Adobe通過與業界領先供應商的整合提供上下文過濾： [!DNL Comscore]。 [!DNL DoubleVerify]。 [!DNL Integral Ad Science], [!DNL Peer39]。 當前篩選器的示例包括 [!UICONTROL Adult Content]。 [!UICONTROL Natural Disasters]。 [!UICONTROL Legal Drinking Age]。 [!UICONTROL MANGA]。 [!UICONTROL Epidemics], [!UICONTROL G-rated Sites]。

您可以為每個廣告商設定預設上下文篩選控制項<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然後可選 [定制每個放置的設定](/help/dsp/campaign-management/placements/placement-settings.md)。 使用此功能時可能需要額外付費。

![Comscore徽標](/help/dsp/assets/comscore-logo.png) ![DoubleVerify徽標](/help/dsp/assets/doubleverify-logo.png) ![整合廣告科學標識](/help/dsp/assets/ias-logo.png) ![Peer39徽標](/help/dsp/assets/peer39-logo.png)

### 投標前欺詐阻止

利用我們與第三方的整合 [!DNL Comscore]。 [!DNL DoubleVerify]。 [!DNL Integral Ad Science], [!DNL Peer39] 阻止非人類的流量。 這些整合提供了業界領先的投標前阻止功能，可最大限度地減少營銷活動中的一般和複雜的無效流量（GIVT和SIVT）。

您可以為每個廣告商設定預設的投標前欺詐阻止控制<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然後可選 [定制每個放置的設定](/help/dsp/campaign-management/placements/placement-settings.md)。 使用此功能時可能需要額外付費。

有關功能的詳細資訊，請直接與首選供應商聯繫，或與 [!DNL Adobe] 客戶團隊。

![Comscore徽標](/help/dsp/assets/comscore-logo.png) ![DoubleVerify徽標](/help/dsp/assets/doubleverify-logo.png) ![整合廣告科學標識](/help/dsp/assets/ias-logo.png) ![Peer39徽標](/help/dsp/assets/peer39-logo.png)

### 投標前可查看性 {#pre-bid-viewability}

由我們業界領先的合作夥伴提供支援的預標價可查看性過濾器 [!DNL DoubleVerify]。 [!DNL Oracle Advertising] ([!DNL Moat])和 [!DNL Integral Ad Science] 允許廣告商確保其廣告活動在視頻和顯示清點中滿足其期望的可視性效能目標。

您可以為每個廣告商設定預設的可查看性篩選器<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然後可選 [定制每個放置的設定](/help/dsp/campaign-management/placements/placement-settings.md)。 使用此功能時可能需要額外付費。

![DoubleVerify徽標](/help/dsp/assets/doubleverify-logo.png) ![Oracle廣告標識](/help/dsp/assets/oracle-advertising-logo.png) ![整合廣告科學標識](/help/dsp/assets/ias-logo.png)

### 主題目標

主題DSP目標允許您通過利用我們業界領先的上下文合作夥伴來確定或阻止關鍵字清單 [!DNL Comscore] 和 [!DNL Oracle Data Cloud] ([!DNL Grapeshot])。 主題目標可幫助您確保您的廣告始終在與您的品牌相符的環境中提供，無論這包括阻止有害內容還是確保在確保獲得更大效果的上下文中進行花費。

主題目標要求您直接使用 [!DNL Comscore] 或 [!DNL Grapeshot] (使用 [!DNL Oracle Data Cloud])。 在合作夥伴平台中建立後，您可以 [目標或排除 [!UICONTROL Audience Targeting] 每個放置的截面](/help/dsp/campaign-management/placements/placement-settings.md)。 此功能可能需要額外費用。

要建立自定義主題段：

* 建立 [!DNL Comscore] 帳戶和建立自定義段，您可以請求登錄 [!DNL Activation Segment Manager] 在 [https://agents.comscore.com](https://agents.comscore.com)。 查看 [[!DNL Comscore] 幫助中心](https://comscoreactivation.zendesk.com/hc/) 的子菜單。 自定義段的費用可在 [!DNL Segment Manager] 建立它們。

* 開始 [!DNL Oracle Data Cloud]，聯繫人 [!DNL Oracle Data Cloud] 或 [!DNL Adobe] 客戶團隊。

![Comscore徽標](/help/dsp/assets/comscore-logo.png) ![Grapeshot徽標](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP與 [!DNL DoubleVerify] 提供 [!DNL Authentic Brand Safety] 瞄準解決方案，它允許您建立一套集中的品牌安全要求，以跨所有購買平台瞄準一致性。

一旦你建了 [!DNL DoubleVerify] 具有必要目標的品牌安全網段，您可以在DSP中使用它來跨Web環境複製投標後的塊規則和投標前。

可以指定 [!DNL DoubleVerify] 每個廣告商的段ID<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->，然後可選 [啟用或禁用 [!UICONTROL Authentic Brand Safety] 每個放置](/help/dsp/campaign-management/placements/placement-settings.md)。 為段DSPID的使用記帳。

有關功能的詳細資訊，請與 [!DNL DoubleVerify] 直接聯繫您 [!DNL Adobe] 客戶團隊。

![DoubleVerify徽標](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [放置設定](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
