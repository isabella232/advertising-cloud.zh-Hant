---
title: 使用 [!DNL Roku] 清單
description: '了解DSP與 [!DNL Roku], including inventory options, approved third-party tracking vendors, and best practices for [!DNL Roku]特定版位的合作關係。 '
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: 0cd42782-f006-4aa8-b879-322f86cfac4b
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# 使用[!DNL Roku]清單

Advertising Cloud DSP提供[!DNL Roku]上廣告的獨特功能。

## Advertising Cloud DSP與[!DNL Roku]夥伴關係

Roku和Advertising Cloud DSP有獨特的合作關係，可將您的[!DNL DSP]對象與[!DNL Roku] ID比對，以便在[!DNL Roku]庫存上鎖定1:1的確定性對象。

除了Roku自己的DSP(OneView),Advertising Cloud DSP只能存取這些鎖定目標功能。 Advertising Cloud DSP也是唯一有權測量[!DNL Roku]供應量的DSP，位於所有其他連線電視(CTV)清單旁。 因為[!DNL Roku]不共用所有標準RTB和曝光像素訊號，因此沒有其他DSP可以鎖定或測量所有Roku銷售的CTV供應。

## [!DNL Roku] 庫存選項

您可以a)直接使用[!DNL Roku]設定私人交易ID，然後將交易ID資料輸入DSP，或b)造訪[!DNL On Demand]圖庫以訂閱[!DNL Roku]設定檔：

>[!NOTE]
>
>[!DNL Roku] 未在開放市場和交易所中提供清單。

* 對於私人交易，您將[在DSP](/help/dsp/inventory/deal-id-create.md)中設定交易ID的相關資訊，然後在[!DNL Roku]版位中定位「[!UICONTROL Roku Network – Audience]」和「[!UICONTROL The Roku Channel – Audience]」。<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* 您可以[訂閱下列 [!DNL Roku] inventory within the [!DNL On Demand] Gallery](/help/dsp/inventory/on-demand-inventory-subscribe.md)，然後鎖定[!DNL Roku]版位內任何已核准的交易：

   * 「[!UICONTROL Roku Network – Audience]」，適用於具有優質內容合作夥伴（如[!DNL The CW]、[!DNL ABC]和[!DNL ESPN]）的[!DNL Roku]生態系統的詳細目錄。
   * 「[!UICONTROL The Roku Channel – Audience]」，適用於[!DNL Roku]擁有並運作(O&amp;O)的應用程式內容。

### 使用[!DNL Roku]自訂私人市場的優點

私人交易可讓您根據需求自訂交易參數。

* **協商定價：** 與銷售團 [!DNL Roku] 隊合作，商談並建構符合您促銷活動需求的交易。

* **規模優先順序：** 私人市場(PMP)獲得的優先順序高於一律開啟的交易( [!DNL On Demand] 例如交易)。

* **頻率管理：** 預 [!DNL Roku] 設頻率上限為每位使用者每30分鐘一(1)個廣告，但您可以依小時、日、周、月或整個飛行期間自訂頻率上限。<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]資料鎖定：** [!DNL Roku] 受眾是從裝置 [!DNL Roku] 和電視訊號建置，由追蹤的資料( [!DNL The Roku Channel] 例如電視類型相關性、串流電視行為和有線訂閱狀態)，以及來自客戶關係管理(CRM)系 [!DNL Roku] 統的其他資料。

* **[!DNL Roku]內容鎖定目標：** 私人交易可依類型、應用程式封鎖清單、季節性和趨勢事件來鎖定應用程式，且僅限 [!DNL The Roku Channel] 內顯示。

## [!DNL Roku] 版位

在DSP促銷活動中，您會使用版位類型「[!UICONTROL Connected TV (Roku)]」，建立 [!DNL Roku]特定版位](/help/dsp/campaign-management/placements/placement-create.md)。 [您將在[!DNL Roku]特定套件中包含[!DNL Roku]版位，並定義目標。

每個[!DNL Roku]版位必須至少定位一個[!DNL Roku]交易或源。 若要搭配[!DNL Roku]運用DSP的不重複對象比對，請加入一或多個可比對[!DNL Roku]（選擇加入）確定性資料集的對象區段。

### [!DNL Roku] — 核准的第三方追蹤廠商

[!DNL Roku] 版位可包含來自下列廠商的第三方事件像素和轉換像素：  [!DNL Acxiom]、  [!DNL comScore]、  [!DNL Data Plus Math]、  [!DNL Experian]、  [!DNL Factual]、  [!DNL Kantar]、  [!DNL Marketing Evolution]、  [!DNL Neustar]、  [!DNL Nielsen]、  [!DNL Nielsen Catalina Solutions]、  [!DNL NinthDecimal]、  [!DNL Oracle]、  [!DNL Placed]和 [!DNL Polk] [!DNL Research Now]。

### 依版位策略的最佳實務

以下是[!DNL Roku]特定版位的建議作法。

要最大化增量觸及：

* 透過排除已使用[!DNL The Roku Channel]觸及的對象，在[!DNL Roku O&O]上隱藏公開的對象。

* 排除已在[!DNL Roku]平台觸及的對象，以隱藏[!DNL All Roku]上公開的對象。

為速度最快的設定：

* 針對[[!DNL On Demand] Inventory](/help/dsp/inventory/on-demand-inventory-subscribe.md)中[!DNL The Roku Channel]的現有永續交易，以快速存取[!DNL Roku]自有及經營的庫存。
* 在[[!DNL On Demand] Inventory](/help/dsp/inventory/on-demand-inventory-subscribe.md)中針對[!DNL Roku Network]的現有、永遠開放交易進行定位，以快速實現[!DNL Roku]平台的規模。

要達到最大規模：

* 自訂[!DNL Roku]私有市場，以協商價格優先訪問[!DNL Roku]供應。

>[!MORELIKETHIS]
>
>* [手動建立交易ID詳細資訊](/help/dsp/inventory/deal-id-create.md)
> * [訂閱並請求對Premium [!DNL On Demand] 庫存交易的訪問](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [建立版位](/help/dsp/campaign-management/placements/placement-create.md)

