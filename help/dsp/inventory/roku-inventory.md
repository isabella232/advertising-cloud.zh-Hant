---
title: 使用 [!DNL Roku] 庫存
description: '瞭解與的DSP合作關係 [!DNL Roku]包括庫存選項、經批准的第三方跟蹤供應商和 [!DNL Roku] — 特定放置。 '
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: 0cd42782-f006-4aa8-b879-322f86cfac4b
source-git-commit: 39f491a39bdc9d8dd820eb4c69594dda71d8b3c2
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# 使用 [!DNL Roku] 庫存

Advertising Cloud DSP提供廣告的獨特功能 [!DNL Roku]。

## Advertising Cloud DSP [!DNL Roku] 夥伴關係

Roku和Advertising Cloud DSP有獨特的合作關係 [!DNL DSP] 觀眾 [!DNL Roku] 針對1:1確定性受眾的ID [!DNL Roku] 庫存。

除了Roku自己(OneView)DSP之外，Advertising Cloud DSP只能訪問這些瞄準功能。 Advertising Cloud DSP也是唯一DSP有權測量 [!DNL Roku] 「supply（供應）」旁邊的所有其它連接的電視(CTV)清單。 因為 [!DNL Roku] 沒有共用所有標準RTB和印象像素信號，沒有其DSP他供應商可以針對Roku銷售的CTV供應進行測量。

## [!DNL Roku] 庫存選項

您可以a)直接與 [!DNL Roku] 然後將交易ID資料輸入DSP或b)訪問 [!DNL On Demand] 要訂閱的庫 [!DNL Roku] 配置檔案：

>[!NOTE]
>
>[!DNL Roku] 庫存在開放式市場和交易所中不可用。

* 為了你的私人交易， [設定有關中的交易ID的信DSP息](/help/dsp/inventory/deal-id-create.md) 然後瞄準&quot;[!UICONTROL Roku Network – Audience]&quot;和&quot;[!UICONTROL The Roku Channel – Audience]在 [!DNL Roku] 的下界。<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* 你可以 [訂閱以下內容 [!DNL Roku] 庫存 [!DNL On Demand] 庫](/help/dsp/inventory/on-demand-inventory-subscribe.md)，然後瞄準所有批准的交易 [!DNL Roku] 放置：

   * &quot;[!UICONTROL Roku Network – Audience]&quot;用於整個庫存 [!DNL Roku] 具有高級內容合作夥伴的生態系統，如 [!DNL The CW]。 [!DNL ABC], [!DNL ESPN]。
   * &quot;[!UICONTROL The Roku Channel – Audience]&quot; [!DNL Roku] 自有和操作(O&amp;O)應用程式內容。

### 定制專用市場的優勢 [!DNL Roku]

私有交易允許您根據您的需要自定義交易參數。

* **協商定價：** 使用 [!DNL Roku] 銷售團隊來協商和構建滿足您市場活動需要的交易。

* **縮放優先順序：** 與始終線上交易(如 [!DNL On Demand] 交易)。

* **頻率管理：** 的 [!DNL Roku] 預設頻率上限是每用戶每30分鐘一(1)個，但您可以按小時、天、周、月或整個飛行時段自定義頻率上限。<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]資料目標：** [!DNL Roku] 觀眾由 [!DNL Roku] 設備和電視信號，由 [!DNL The Roku Channel] （如TV流派關係、流式電視行為和有線訂閱狀態），以及來自 [!DNL Roku] 客戶關係管理(CRM)系統。

* **[!DNL Roku]內容目標：** 私人交易可以按類型、應用程式區塊清單、季節性和極點事件的應用程式，並在內部展示 [!DNL The Roku Channel] 只是。

## [!DNL Roku] 放置

在活DSP動中， [建立 [!DNL Roku]特定位置](/help/dsp/campaign-management/placements/placement-create.md) 使用放置類型「[!UICONTROL Connected TV (Roku)]&quot; 包括 [!DNL Roku] 放置 [!DNL Roku] — 具有已定義目標的特定包。

每個 [!DNL Roku] 放置必須針對至少一個 [!DNL Roku] 交易或來源。 使用唯DSP一的受眾與 [!DNL Roku]，包括一個或多個可與之匹配的受眾段 [!DNL Roku] 確定性資料集。

### [!DNL Roku] — 批准的第三方跟蹤供應商

[!DNL Roku] 放置可以包括來自以下供應商的第三方事件像素和轉換像素：  [!DNL Acxiom]。 [!DNL comScore]。 [!DNL Data Plus Math]。 [!DNL Experian]。 [!DNL Factual]。 [!DNL Kantar]。 [!DNL Marketing Evolution]。 [!DNL Neustar]。 [!DNL Nielsen]。 [!DNL Nielsen Catalina Solutions]。 [!DNL NinthDecimal]。 [!DNL Oracle]。 [!DNL Placed]。 [!DNL Polk], [!DNL Research Now]。

### 按職位安排策略列出的最佳做法

以下是 [!DNL Roku] — 特定放置。

要最大限度地提高增量訪問：

* 禁止顯示的觀眾 [!DNL Roku O&O] 排除您已使用的受眾 [!DNL The Roku Channel]。

* 禁止顯示的觀眾 [!DNL All Roku] 排除您已經訪問的受眾 [!DNL Roku] 平台。

對於最快的設定：

* 針對現有的、始終線上的交易 [!DNL The Roku Channel] 在 [[!DNL On Demand] 庫存](/help/dsp/inventory/on-demand-inventory-subscribe.md) 快速訪問 [!DNL Roku] 庫存。
* 針對現有的、始終線上的交易 [!DNL Roku Network] 在 [[!DNL On Demand] 庫存](/help/dsp/inventory/on-demand-inventory-subscribe.md) 快速實現跨越 [!DNL Roku] 平台。

要達到最大規模：

* 自定義 [!DNL Roku] 用於優先訪問的私有市場 [!DNL Roku] 按協定價格供應。

>[!MORELIKETHIS]
>
>* [手動建立交易ID詳細資訊](/help/dsp/inventory/deal-id-create.md)
> * [訂閱和請求訪問 [!DNL On Demand] 高級庫存交易](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [建立放置](/help/dsp/campaign-management/placements/placement-create.md)

