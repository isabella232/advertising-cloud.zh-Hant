---
title: 手動交易ID設定
description: 請參閱手動輸入交易ID之設定的說明。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 0cd5e9e8-2b13-4b1e-a2e0-b8b492f75acf
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# 手動交易ID設定

| 區段 | 參數 | 說明 | 必填 | 可編輯 |
|---------|-----------|-------------|----------|----------|
| [交易詳細資訊] | [!UICONTROL Deal name] | 識別您 [!UICONTROL Deal ID] 在Advertising DSP中。 輸入名稱或選擇 **[!UICONTROL Auto-name]** 讓DSP根據交易詳細資訊產生名稱。<br><br>自動產生的名稱範例： `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | 是 | 是 |
|  | [!UICONTROL External deal ID] | 發佈商和SSP用來識別此交易的ID。 | 是 | 否 |
|  | [!UICONTROL Publisher] | 銷售此庫存的發佈商的名稱。 | 是 | 否 |
|  | [!UICONTROL SSP] | 此交易執行的供應端平台(SSP)。 | 是 | 否 |
|  | [!UICONTROL Media type] | 透過此交易購買的媒體類型： *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]*，或 *[!UICONTROL Audio]*. 選項因SSP而異。<br><br> 如果交易允許多種媒體類型，請在建立交易時為預設版位選擇媒體類型。 稍後，您可以變更值，或只 [附加新版位，並附加其他媒體類型](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | 是 | 否 |
|  | [!UICONTROL Deal type] | 交易承諾和定價結構：<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*:您和發佈商未承諾傳送固定數量的曝光。 交易指定存貨的最低價格，但CPM可能會隨市場狀況而波動和增加。</li><li>*[!UICONTROL Non guaranteed (fixed)]*:您和發佈商未承諾傳送固定數量的曝光。 定價採用議定的固定費率。</li><li>*[!UICONTROL Guaranteed (fixed)]*:您和發佈商已同意預先定義的曝光數、目標、投放日期和固定價格。<br><br><b>注意：</b> 有保證的交易需要投放日期和 [!UICONTROL Tracking] 區段。 您也必須為交易建立預設的程式化保證(PG)版位，並可選擇將交易用於其他版位。</li></ul> | 是 | 否 |
|  | [!UICONTROL CPM] | 每1000次曝光的議定成本(CPM)。 | 是 | 是 |
|  | [貨幣] | 交易的貨幣。<br><br>所有SSP都接受美元交易。 當SSP接受您DSP帳戶的貨幣時，該貨幣也可供使用。 | 是 | 否 |
|  | [!UICONTROL Billing method] | 所有交易ID為 [!DNL Adobe] — 融資和開票。 DSP會根據使用情況支付所有可用的媒體廠商、管理與廠商的差異，並傳送一張合併發票給帳戶。 此選項會產生額外費用，如帳戶的利率卡中所述。 | 是 | 否 |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | 可存取交易之使用者帳戶的電子郵件地址。 | 否 | 是 |
|  | [!UICONTROL Advertisers that can access this deal] | 帳戶中可存取此交易的特定廣告商。<br><br><b>注意：</b> 您可以透過 [!UICONTROL Deals] 檢視。 在交易列中，按一下 **[!UICONTROL #]**，按一下 **[!UICONTROL share]**，然後與電子郵件地址共用交易。 | 是 | 是 |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | 使用此交易的流量的開始和結束日期。 這些日期僅用於追蹤用途，不會影響廣告傳送。<br><br><b>提示：</b> 在 [!UICONTROL Inventory] > [!UICONTROL Deals] 檢視， [!UICONTROL Pacing & Budget] 欄顯示交易進度如何達到指定的飛行日期和曝光目標。 如果傳送進度不佳或過於謹慎，請連絡您的發行商，以調整透過交易傳送的數量。 | 有擔保的交易：是<br>無擔保交易：否 | 是 |
|  | [!UICONTROL Impressions] | （非保證交易可選）您使用此交易預計要執行的曝光次數。 此值僅用於追蹤；發佈者會控制廣告傳送。 | 有擔保的交易：是<br>無擔保交易：否 | 是 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [手動建立交易ID詳細資訊](deal-id-create.md)
>* [SSP合作夥伴](ssp-partners.md)
>* [關於私有清單](private-inventory-about.md)

