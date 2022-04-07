---
title: 將廣告附加到放置
description: 瞭解如何將廣告附加到位置。
feature: DSP Ads
exl-id: 4d85b89b-217f-46eb-a8b2-27da4c220be7
source-git-commit: af5e9449802c98b92a3d0107a00c47fe2b2031ca
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 1%

---

# 將廣告附加到放置

## 從 [!UICONTROL Ads] 視圖

1. 在主菜單中，按一下 **[!UICONTROL Campaigns]**。
1. 按一下市場活動的名稱。
1. 在子菜單中，按一下 **[!UICONTROL Ads]**。
1. 在廣告名稱旁，按一下  **...>[!UICONTROL Add to Placements]**。
1. 在「放置廣告」螢幕中，執行下列任一操作：
   * 要為廣告建立新位置：
      1. 按一下 **[!UICONTROL Create New Placement]**.
      1. 輸入 [放置設定](/help/dsp/campaign-management/placements/placement-settings.md)，然後按一下 **[!UICONTROL Create Placement]**。
   * 要將廣告添加到一個或多個現有放置：
      1. 按一下 **[!UICONTROL Select a Placement].**
      1. 執行下列任一操作：
         * 要一次添加一個廣告，請執行以下操作：
            1. 在廣告名稱旁，按一下 **[!UICONTROL Select]。**
            1. （可選）對於要附加的每個附加廣告，按一下 **[!UICONTROL Attach to Other Placement]**。 在廣告名稱旁，按一下 **[!UICONTROL Select]。**
         * 要一次將廣告附加到最多20個位置，請執行以下操作：
            1. 選中**批量選擇旁邊的複選框。&quot;
            1. 選中要將廣告附加到的每個位置旁邊的複選框。
            1. 按一下 **[!UICONTROL Attach]**.
      1. 在「完成和審閱」(Complete &amp; Review)頁籤上，選擇以下選項之一：
         * 要返回到廣告視圖，請按一下 **[!UICONTROL I'm done for now]**。
         * 要將廣告附加到其他位置，請按一下 **[!UICONTROL Attach To Other Placement]**。

## 從附加新廣告或現有廣告 [!UICONTROL Placements] 視圖

1. 在主菜單中，按一下 **[!UICONTROL Campaigns]**。
1. 按一下市場活動的名稱。
1. 在子菜單中，按一下 **[!UICONTROL Placements]**。
1. 在放置名稱旁，按一下  **...> [!UICONTROL Attach Ads]。**
1. 在 [!UICONTROL Add Ad to Placement] 螢幕，執行下列任一操作：
   * 要建立新廣告：
      1. 按一下 **[!UICONTROL Create a New Ad]**.
      1. 輸入廣告設定 [音頻廣告](ad-settings-audio.md)。 [連接電視](ad-settings-connected-tv.md)。 [顯示廣告](ad-settings-display.md)。 [移動廣告](ad-settings-mobile.md)。 [原生廣告](ad-settings-native.md)或 [預卷廣告](ad-settings-pre-roll.md)。
      1. 按一下 **[!UICONTROL Save & Submit for Review]**.

         的 [審閱](ad-about.md) 對於新廣告，需要24至48個小時並包括對敏感類別的檢查，按一下URL功能，然後預覽呈現。 的 [!UICONTROL Status] 列指DSP示是否已批准廣告。 斷開的廣告可能具有超過24-48小時的掛起狀態，因此您有時間修復錯誤，然後才被拒絕。

         >[!NOTE]
         >
         >只有雙方和SSP都批准DSP了創意，您的廣告才會送達。 每個SSP都有自己的批准要求和流程。
   * 要選擇現有廣告：
      1. 按一下 **[!UICONTROL Select an Ad].**
      1. 指定廣告：
         * 要一次添加一個廣告，請執行以下操作：
            1. 在廣告名稱旁，按一下 **[!UICONTROL Select]。**
            1. （可選）對於要附加的每個附加廣告，按一下 **[!UICONTROL Add Another Ad]**。 在廣告名稱旁，按一下 **[!UICONTROL Select]。**
         * 每次最多添加20個廣告：
            1. 選中旁邊的複選框 **[!UICONTROL Bulk Select]**&quot;
            1. 選中要添加的每個廣告旁邊的複選框。
            1. 按一下 **[!UICONTROL Attach]**.
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
      1. 按一下 **[!UICONTROL I'm done for now]**.


>[!MORELIKETHIS]
>
>* [關於廣告管理](ad-about.md)
>* [建立單個廣告](ad-create.md)
>* [建立多個第三方廣告](ad-create-multiple.md)
>* [編輯廣告](ad-edit.md)
>* [列出與廣告關聯的放置](ad-list-placements.md)
>* [編輯放置廣告計畫](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)

