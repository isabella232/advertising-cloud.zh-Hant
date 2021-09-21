---
title: 手動交易ID設定
description: 請參閱手動輸入交易ID之設定的說明。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 0cd5e9e8-2b13-4b1e-a2e0-b8b492f75acf
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# 手動交易ID設定

| 區段 | 參數 | 說明 | 必填 | 可編輯 |
|---------|-----------|-------------|----------|----------|
| [交易詳細資訊] | [!UICONTROL Deal name] | 在Advertising Cloud DSP中識別[!UICONTROL Deal ID]的名稱。 輸入名稱或選取[!UICONTROL Auto-name] ，讓Advertising Cloud根據交易詳細資訊產生名稱。<br><br>自動產生的名稱範例： [!DNL *DEAL_ID*  — 交易ID — 保證固定 — 美元 — 5 - 24廚房 — 私人] | 是 | 是 |
|  | [!UICONTROL External deal ID] | 發佈商和SSP用來識別此交易的ID。 | 是 | 否 |
|  | [!UICONTROL Publisher] | 銷售此庫存的發佈商的名稱。 | 是 | 否 |
|  | [!UICONTROL SSP] | 此交易將透過的供應端平台(SSP)。 | 是 | 否 |
|  | [!UICONTROL Media type] | 通過此交易購買的媒體類型：[!UICONTROL Desktop video]、[!UICONTROL Mobile video]、[!UICONTROL Connected TV]、[!UICONTROL Display]或[!UICONTROL Audio]。 選項因SSP而異。 | 是 | 否 |
|  | [!UICONTROL Deal type] | 交易承諾和定價結構：<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*:您和發佈商未承諾傳送固定數量的曝光。交易指定存貨的最低價格，但CPM可能會隨市場狀況而波動和增加。</li><li>*[!UICONTROL Non guaranteed (fixed)]*:您和發佈商未承諾傳送固定數量的曝光。定價採用議定的固定費率。</li><li>*[!UICONTROL Guaranteed (fixed)]*:您和發佈商已同意預先定義的曝光數、目標、投放日期和固定價格。<br><br><b>注意：</b> 保證交易需要投放日期以及區段中的指定曝光 [!UICONTROL Tracking] 次數。您還需要為交易建立預設的程式化保證(PG)版位，並可選擇將交易用於其他版位。</li></ul> | 是 | 否 |
|  | [!UICONTROL CPM] | 每千次曝光的議定成本(CPM)。 | 是 | 是 |
|  | [貨幣] | 交易的貨幣。<br><br>所有SSP都接受美元交易。當SSP接受您DSP帳戶的貨幣時，該貨幣也可供使用。 | 是 | 否 |
|  | [!UICONTROL Billing method] | 所有交易ID均為[!DNL Adobe]融資和 — invoided。 Advertising Cloud會根據使用情況支付所有可用的媒體廠商、管理與廠商的差異，並傳送一張合併發票給帳戶。 此選項會產生額外費用，如帳戶的利率卡中所述。 | 是 | 否 |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | 可存取交易之使用者帳戶的電子郵件地址。 | 否 | 是 |
|  | [!UICONTROL Advertisers that can access this deal] | 帳戶中可存取此交易的特定廣告商。<br><br><b>注意：</b> 您可以從檢視與其他帳戶中的廣告商共 [!UICONTROL Deals] 用交易。在交易列中，按一下&#x200B;**[!UICONTROL #]**，按一下&#x200B;**[!UICONTROL share]**，然後與電子郵件地址共用交易。 | 是 | 是 |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | 使用此交易的流量的開始和結束日期。 這些日期僅供追蹤之用，不會影響廣告傳送。<br><br><b>提示： </b> 在>檢 [!UICONTROL Inventory] 視 [!UICONTROL Deals] 中，欄將 [!UICONTROL Pacing & Budget] 顯示交易進度如何達到指定的投放日期和曝光目標。如果傳送進度不佳或過於謹慎，請連絡您的發行商，以調整透過交易傳送的數量。 | 有擔保的交易：是<br>無擔保交易：否 | 是 |
|  | [!UICONTROL Impressions] | （非保證交易可選）您使用此交易預計要執行的曝光次數。 此值僅用於追蹤目的；發佈者會控制廣告傳送。 | 有擔保的交易：是<br>無擔保交易：否 | 是 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [手動建立交易ID詳細資訊](deal-id-create.md)
>* [SSP合作夥伴](ssp-partners.md)

<!-- >* [About Private Inventory](private-inventory-about.md) -->
