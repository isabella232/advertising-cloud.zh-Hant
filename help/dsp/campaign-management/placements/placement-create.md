---
title: 建立放置
description: 瞭解如何建立放置。
feature: DSP Placements
exl-id: 4e37b571-9af4-4897-bff2-035a5f2600a5
source-git-commit: a30f3bffaf63a79bb7aead69e52524419ed54ed0
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 1%

---

# 建立放置

>[!TIP]
>
>根據特定市場活動目標或報告需求建立投放。

1. 在主菜單中，按一下 **[!UICONTROL Campaigns]**。

1. 按一下將包含放置的市場活動的名稱。

1. 在資料表上方，按一下 **[!UICONTROL Create]**。 在 [!UICONTROL Placement Types] ，按一下放置類型。

   放置類型確定放置可以包括的放置類型。

1. 輸入 [放置設定](placement-settings.md):

   1. 指定 [!UICONTROL Basics] 的子菜單。

   1. 在 [!UICONTROL Goals] ，指定 [!UICONTROL Gross Budget] （可選）指定附加的放置目標。

      某些欄位具有可覆蓋的預設值。

      如果分配放置的包具有包級別調節，則您的目標和調節設定將反映包設定。

   1. （可選）在 [!UICONTROL Geo-Targeting] 的下界。

      如果您未標識特定位置，則所有位置都是目標位置。

      >[!NOTE]
      >
      >城市和DMA位置不適用於Roku放置。

   1. 在 [!UICONTROL Inventory Targeting] 部分，縮小要包括或排除的庫存來源。

      對於大多數放置類型，預設情況下包括所有庫存類型和每種類型的所有來源。 對於 [!DNL Roku] 放置，您必須指定庫存類型和來源。

   1. （可選）在 [!UICONTROL Site Targeting] 部分，縮小要目標的站點範圍，並指定要排除的任何站點。

   1. （可選）在 [!UICONTROL Audience Targeting] 部分：

      1. 縮小觀眾範圍。 這包括選擇要在放置中瞄準的受眾段。

         對於 [!DNL] Roku放置，你可以 [唯DSP一的受眾匹配 [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) 包括一個或多個可與之匹配的受眾段 [!DNL Roku] 確定性資料集。
   1. (針對具有人員級跨設備目標的活動；可選)當放置針對一個或多個特定的觀眾時，啟用基於人的跨設備定位來放置。

      提供基於人的跨設備目標 [!DNL LiveRamp] 僅使用美國資料。 該服務以0.35美元CPM的價格向所有廣告商提供，用於使用 [!DNL LiveRamp] 設備圖（即，在目標受眾段中找不到的設備）。

   1. （可選）在 [!DNL Brand Safety and Media Targeting] 部分，對您的放置應用品牌安全限制。

   1. （可選）在 [!DNL Tracking] 部分，輸入放置中廣告的第三方事件像素或轉換像素。

      >[!NOTE]
      >
      >([!DNL Roku] 放置)由批准的第三方像素供應商 [!DNL Roku] 包括 [!DNL Acxiom]。 [!DNL comScore]。 [!DNL Data Plus Math]。 [!DNL Experian]。 [!DNL Factual]。 [!DNL Kantar]。 [!DNL Marketing Evolution]。 [!DNL Neustar]。 [!DNL Nielsen]。 [!DNL Nielsen Catalina Solutions]。 [!DNL NinthDecimal]。 [!DNL Oracle]。 [!DNL Placed]。 [!DNL Polk], [!DNL Research Now]。


1. 按一下 **[!UICONTROL Create Placement]**.

1. （可選）將廣告附加到位置：

   1. 按一下 **[!UICONTROL Attach an ad]**.

   1. 執行下列任一操作：
   * 要建立新廣告：

      1. 按一下 **[!UICONTROL Create a New Ad].**

      1. 指定廣告設定 [音頻廣告](/help/dsp/campaign-management/ads/ad-settings-audio.md)。 [連接電視](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)。 [顯示廣告](/help/dsp/campaign-management/ads/ad-settings-display.md)。 [移動廣告](/help/dsp/campaign-management/ads/ad-settings-mobile.md)。 [原生廣告](/help/dsp/campaign-management/ads/ad-settings-native.md)或 [預卷廣告](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)。

      1. 按一下 **[!UICONTROL Save & Submit for Review]**.

      1. （可選）對於要為放置建立的每個附加廣告，按一下 **[!UICONTROL Attach Another Ad]**，然後重複步驟1-3。

      1. 如果不附加任何現有廣告，請按一下 **[!UICONTROL I'm done for now]**。
   * 要在市場活動中附加現有廣告，請執行以下操作：

      1. 按一下 **[!UICONTROL Select an Ad]**.
      1. 執行下列任一操作：
         * 要一次添加一個廣告，請執行以下操作：
            1. 在廣告名稱旁，按一下 **[!UICONTROL Select]。**
            1. （可選）對於要附加的每個附加廣告，按一下 **[!UICONTROL Attach Another Ad]**，然後重複該過程。
         * 每次最多添加20個廣告：
            1. 選中廣告清單上方的複選框。
            1. 選中要添加的每個廣告旁邊的複選框。
            1. 按一下 **[!UICONTROL Attach]**.
            1. 在廣告名稱旁，按一下 **[!UICONTROL Select]**。
      1. （可選）要覆蓋放置中特定廣告的預設飛行時段和廣告輪轉：
         1. 按一下 **[!UICONTROL Custom Schedule Ads]**.

         1. 執行下列任一操作：

            * 要添加航班，請按一下 **[!UICONTROL Add Flight]**，然後指定開始日期和結束日期。

            * 要將現有航班添加到廣告，請按一下 **[!UICONTROL +]** 的下界。

            * 要從廣告中刪除現有航班，請按一下 **[!UICONTROL x]** 的下界。

            * （當多個廣告具有相同的飛行時）要使廣告不均勻地旋轉，請按一下 **[!UICONTROL Even Rotation]** 在飛行資訊中，然後輸入每個廣告的相對重量（百分比）。

               總重量必須等於100。
         1. 在右上角，按一下 **[!UICONTROL Continue]**。

         1. 查看航班詳細資訊，然後按一下 **[!UICONTROL Save & Finish]**。




>[!MORELIKETHIS]
>
>* [關於放置管理](placement-about.md)
>* [編輯放置](placement-edit.md)
>* [編輯放置廣告計畫](placement-edit-ad-schedule.md)
>* [暫停或激活放置](placement-pause-activate.md)
>* [放置設定](placement-settings.md)
>* [鍵盤快捷鍵](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)

   >*[排除效能故障](/help/dsp/optimization/troubleshooting-performance.md)
>* [視頻：如何建立標準顯示放置](https://video.tv.adobe.com/v/340454)

