---
title: 使用 [!DNL Roku] 庫存
description: 了解DSP與 [!DNL Roku]，包括庫存選項、已核准的第三方追蹤廠商，以及 [!DNL Roku]特定版位。
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: 0cd42782-f006-4aa8-b879-322f86cfac4b
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# 使用 [!DNL Roku] 庫存

Advertising DSP為 [!DNL Roku].

## DSP和 [!DNL Roku] 合作夥伴

Roku和DSP有獨特的合作關係，符合您的 [!DNL DSP] 對象 [!DNL Roku] 1:1確定性對象鎖定目標的ID，在 [!DNL Roku] 詳細目錄。

在Roku自己的DSP(OneView)之外，Advertising DSP可以完全存取這些鎖定目標功能。 Advertising DSP也是唯一有權測量的DSP [!DNL Roku] 在所有其它連接電視(CTV)清單旁邊提供。 因為 [!DNL Roku] 不會共用所有標準RTB和曝光像素訊號，其他DSP無法在Roku銷售的CTV供應中鎖定或測量。

## [!DNL Roku] 庫存選項

您可以a)直接使用 [!DNL Roku] 然後將交易ID資料輸入DSP或b)造訪 [!DNL On Demand] 要訂閱的庫 [!DNL Roku] 設定檔：

>[!NOTE]
>
>[!DNL Roku] 未在開放市場和交易所中提供清單。

* 為了你的私下交易， [在DSP中設定交易ID的相關資訊](/help/dsp/inventory/deal-id-create.md) 然後定位&quot;[!UICONTROL Roku Network – Audience]&quot;和&quot;[!UICONTROL The Roku Channel – Audience]在 [!DNL Roku] 版位。<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* 您可以 [訂閱以下內容 [!DNL Roku] 清單 [!DNL On Demand] 圖庫](/help/dsp/inventory/on-demand-inventory-subscribe.md)，然後將目標定位於 [!DNL Roku] 版位：

   * &quot;[!UICONTROL Roku Network – Audience]」， [!DNL Roku] 具有進階內容合作夥伴的生態系統，例如 [!DNL The CW], [!DNL ABC]，和 [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel – Audience]」 [!DNL Roku] 擁有和操作(O&amp;O)應用程式內容。

### 使用自訂私人市場的優點 [!DNL Roku]

私人交易可讓您根據需求自訂交易參數。

* **協商定價：** 使用 [!DNL Roku] 銷售團隊，協商和構建滿足您的促銷活動需求的交易。

* **縮放優先順序：** 私人市場(PMP)的優先順序高於永遠在上的交易(例如 [!DNL On Demand] 交易)。

* **頻率管理：** 此 [!DNL Roku] 預設頻率上限為每位使用者每30分鐘一(1)個廣告，但您可以依小時、日、周、月或整個飛行期間自訂頻率上限。<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]資料鎖定：** [!DNL Roku] 對象是從 [!DNL Roku] 裝置和電視訊號，由 [!DNL The Roku Channel] （例如電視類型相關性、串流電視行為和有線訂閱狀態），以及 [!DNL Roku] 客戶關係管理(CRM)系統。

* **[!DNL Roku]內容鎖定：** 私人交易可依類型、應用程式封鎖清單、季節性和趨勢事件等來鎖定應用程式，並在內顯示 [!DNL The Roku Channel] 只有。

## [!DNL Roku] 版位

在DSP促銷活動中， [建立 [!DNL Roku] — 特定位置](/help/dsp/campaign-management/placements/placement-create.md) 使用放置類型「[!UICONTROL Connected TV (Roku)].&quot; 包括 [!DNL Roku] 版位 [!DNL Roku]具有已定義目標的特定包。

每個 [!DNL Roku] 版位必須至少鎖定一個 [!DNL Roku] 交易或來源。 若要使用DSP不重複受眾比對，請搭配 [!DNL Roku]，包含一或多個可比對的對象區段 [!DNL Roku] （選擇加入）確定性資料集。

### [!DNL Roku] — 核准的第三方追蹤廠商

[!DNL Roku] 版位可包含來自下列廠商的第三方事件像素和轉換像素：  [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]，和 [!DNL Research Now].

### 依版位策略的最佳實務

以下是 [!DNL Roku]特定版位。

要最大化增量觸及：

* 在上隱藏公開的對象 [!DNL Roku O&O] 排除您已使用 [!DNL The Roku Channel].

* 在上隱藏公開的對象 [!DNL All Roku] 排除您已在 [!DNL Roku] 平台。

為速度最快的設定：

* 針對現有、隨時待命的交易 [!DNL The Roku Channel] in [[!DNL On Demand] 庫存](/help/dsp/inventory/on-demand-inventory-subscribe.md) 快速存取 [!DNL Roku] 自有及經營的存貨。
* 針對現有、隨時待命的交易 [!DNL Roku Network] in [[!DNL On Demand] 庫存](/help/dsp/inventory/on-demand-inventory-subscribe.md) 快速實現跨 [!DNL Roku] 平台。

要達到最大規模：

* 自訂 [!DNL Roku] 優先訪問私有市場 [!DNL Roku] 按協定價格供應。

>[!MORELIKETHIS]
>
>* [手動建立交易ID詳細資訊](/help/dsp/inventory/deal-id-create.md)
> * [訂閱並要求存取 [!DNL On Demand] 高級庫存交易](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [建立版位](/help/dsp/campaign-management/placements/placement-create.md)

