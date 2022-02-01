---
title: 手動交易ID設定
description: 請參閱手動輸入的交易ID的設定說明。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 0cd5e9e8-2b13-4b1e-a2e0-b8b492f75acf
source-git-commit: cf08c97a6a9fecd637f1776b186a18a5c5cc6435
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%

---

# 手動交易ID設定

| 節 | 參數 | 說明 | 必需 | 可編輯 |
|---------|-----------|-------------|----------|----------|
| [交易詳細資訊] | [!UICONTROL Deal name] | 用於標識您 [!UICONTROL Deal ID] 在Advertising Cloud DSP。 輸入名稱或選擇 **[!UICONTROL Auto-name]** 讓Advertising Cloud根據交易細節生成一個名稱。<br><br>自動生成的名稱示例： `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | 是 | 是 |
|  | [!UICONTROL External deal ID] | 發佈者和SSP用於標識此交易的ID。 | 是 | 否 |
|  | [!UICONTROL Publisher] | 銷售此庫存的發佈者的名稱。 | 是 | 否 |
|  | [!UICONTROL SSP] | 此交易將通過的供應側平台(SSP)。 | 是 | 否 |
|  | [!UICONTROL Media type] | 通過此交易購買的媒體類型： *[!UICONTROL Desktop video]*。 *[!UICONTROL Mobile video]*。 *[!UICONTROL Connected TV]*。 *[!UICONTROL Display]*&#x200B;或 *[!UICONTROL Audio]*。 選項因SSP而異。<br><br> 如果交易允許多種介質類型，請在建立交易時選擇預設放置的介質類型。 稍後，您可以更改值，或者 [附加附加的媒體類型](deal-id-attach-placements.md)。<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | 是 | 否 |
|  | [!UICONTROL Deal type] | 交易承諾和定價結構：<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*:您和出版商沒有承諾提供固定數量的印象。 該交易規定了存貨的最低價格，儘管公司業績管理可能會根據市場情況而波動和增加。</li><li>*[!UICONTROL Non guaranteed (fixed)]*:您和出版商沒有承諾提供固定數量的印象。 定價按議定固定匯率釐定。</li><li>*[!UICONTROL Guaranteed (fixed)]*:您和出版商已就預定的印象、目標、航班日期和固定價格達成了一致。<br><br><b>注：</b> 有保證的交易要求有航班日期和特定數量的印象 [!UICONTROL Tracking] 的子菜單。 您還需要為交易建立預設的計畫保證(PG)放置，並且您可以選擇將交易用於其它放置。</li></ul> | 是 | 否 |
|  | [!UICONTROL CPM] | 每千次印數(CPM)的協商成本。 | 是 | 是 |
|  | [貨幣] | 交易的貨幣。<br><br>所有SSP都接受美元交易。 當SSP接受您帳戶的幣種DSP時，該幣種也可用。 | 是 | 否 |
|  | [!UICONTROL Billing method] | 所有交易ID [!DNL Adobe]融資和開票。 Advertising Cloud將根據使用情況向所有可用媒體供應商支付費用，管理與供應商之間的差異，並向帳戶發送一張合併發票。 此選項將產生額外費用，如客戶的費率卡中所述。 | 是 | 否 |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | 可以訪問交易的用戶帳戶的電子郵件地址。 | 否 | 是 |
|  | [!UICONTROL Advertisers that can access this deal] | 帳戶中可以訪問此交易的特定廣告商。<br><br><b>注：</b> 您可以與廣告商共用來自 [!UICONTROL Deals] 的子菜單。 在交易行中，按一下 **[!UICONTROL #]**&#x200B;按一下 **[!UICONTROL share]**，然後與電子郵件地址共用交易。 | 是 | 是 |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | 使用此交易的流量的開始和結束日期。 這些日期僅用於跟蹤，不影響和交付。<br><br><b>提示：</b> 在 [!UICONTROL Inventory] > [!UICONTROL Deals] 的 [!UICONTROL Pacing & Budget] 列將顯示交易如何朝著指定的飛行日期和印象目標前進。 如果交付時間不足或過長，請聯繫您的發行商，以調整它通過交易發送的數量。 | 有擔保的交易：是<br>無擔保交易：否 | 是 |
|  | [!UICONTROL Impressions] | （非保證交易可選）您預計使用此交易運行的印象估計數。 此值僅用於跟蹤；發佈者控制廣告分發。 | 有擔保的交易：是<br>無擔保交易：否 | 是 |

{style=&quot;table-layout:auto&quot;&quot;

>[!MORELIKETHIS]
>
>* [手動建立交易ID詳細資訊](deal-id-create.md)
>* [SSP合作夥伴](ssp-partners.md)
>* [關於專用清單](private-inventory-about.md)

