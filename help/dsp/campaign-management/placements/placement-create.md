---
title: 建立版位
description: 了解如何建立版位。
feature: DSP Placements
exl-id: 4e37b571-9af4-4897-bff2-035a5f2600a5
source-git-commit: 608774723f865c22bfdd5c911ac818600a495114
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 建立版位

>[!TIP]
>
>根據特定促銷活動目標或報表需求建立版位。

1. 在主菜單中，按一下&#x200B;**[!UICONTROL Campaigns]**。

1. 按一下要包含版位之促銷活動的名稱。

1. 在資料表上方，按一下&#x200B;**[!UICONTROL Create]**。 在功能表的[!UICONTROL Placement Types]區段中，按一下放置類型。

   版位類型決定版位可包含的廣告類型。

1. 輸入[位置設定](placement-settings.md):

   1. 指定[!UICONTROL Basics]設定。

   1. 在[!UICONTROL Goals]區段中，指定[!UICONTROL Gross Budget]，並選擇性地指定其他版位目標。

      有些欄位有您可以覆寫的預設值。

      如果分配位置的包具有包級步調，則您的目標和步調設定將反映包設定。

   1. （選用）在[!UICONTROL Geo-Targeting]區段中，縮小已包含或排除的位置。

      如果您未識別特定位置，則會鎖定所有位置。

      >[!NOTE]
      >
      >城市和DMA位置無法用於Roku位置。

   1. 在[!UICONTROL Inventory Targeting]區段中，縮小要包含或排除的庫存來源。

      對於大多數版位類型，預設會包含每種類型的所有庫存類型和所有來源。 對於[!DNL Roku]版位，必須指定庫存類型和來源。

   1. （可選）在[!UICONTROL Site Targeting]區段中，縮小您要定位的網站，並指定您要排除的任何網站。

   1. （選用）在[!UICONTROL Audience Targeting]區段中：

      1. 縮小閱聽眾範圍。 這包括選取要在版位內定位的對象區段。

         對於[!DNL] Roku版位，您可以加入一或多個可與[!DNL Roku]（選擇加入）確定性資料集相符的對象區段，以運用[ DSP的不重複對象符合 [!DNL Roku]](/help/dsp/inventory/roku-inventory.md)。
   1. (適用於具有人員層級跨裝置定位的促銷活動；選用)當版位鎖定一或多個特定對象時，請為版位啟用以人物為基礎的跨裝置鎖定目標。

      [!DNL LiveRamp]僅使用美國資料提供以人物為基礎的跨裝置鎖定目標。 對於透過[!DNL LiveRamp]裝置圖表傳送的曝光數（亦即，針對在目標受眾區段內找不到的裝置），所有廣告商皆可以$0.35 CPM使用此服務。

   1. （選用）在[!DNL Brand Safety and Media Targeting]區段中，對版位套用品牌安全限制。

   1. （選用）在[!DNL Tracking]區段中，為位置中的廣告輸入第三方事件像素或轉換像素。

      >[!NOTE]
      >
      >（[!DNL Roku]版位）由[!DNL Roku]核准的第三方像素供應商包括[!DNL Acxiom]、[!DNL comScore]、[!DNL Data Plus Math]、[!DNL Experian]、[!DNL Factual]、[!DNL Kantar]、[!DNL Marketing Evolution]、[!DNL Neustar]、[!DNL Nielsen]、[!DNL Nielsen Catalina Solutions]、[!DNL NinthDecimal]、[!DNL Oracle]、[!DNL Placed]、[!DNL Polk]和[!DNL Research Now]。


1. 按一下 **[!UICONTROL Create Placement]**.

1. （選用）將廣告附加至版位：

   1. 按一下 **[!UICONTROL Attach an ad]**.

   1. 執行下列任一操作：
   * 若要建立新廣告：

      1. 按一下 **[!UICONTROL Create a New Ad].**

      1. 指定[音訊廣告](/help/dsp/campaign-management/ads/ad-settings-audio.md)、[連接的TV](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)、[顯示廣告](/help/dsp/campaign-management/ads/ad-settings-display.md)、[行動廣告](/help/dsp/campaign-management/ads/ad-settings-mobile.md)、[原生廣告](/help/dsp/campaign-management/ads/ad-settings-native.md)或[前段廣告](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)的廣告設定。

      1. 按一下 **[!UICONTROL Save & Submit for Review]**.

      1. （可選）對於要為版位建立的每個附加廣告，按一下&#x200B;**[!UICONTROL Attach Another Ad]**，然後重複步驟1-3。

      1. 如果不附加任何現有廣告，請按一下&#x200B;**[!UICONTROL I'm done for now]**。
   * 若要附加行銷活動中的現有廣告：

      1. 按一下 **[!UICONTROL Select an Ad]**.
      1. 執行下列任一操作：
         * 一次新增一個廣告：
            1. 在廣告名稱旁，按一下&#x200B;**[!UICONTROL Select]。**
            1. （可選）對於要附加的每個附加廣告，按一下&#x200B;**[!UICONTROL Attach Another Ad]**，然後重複該過程。
         * 一次最多新增20個廣告：
            1. 選取廣告清單上方的核取方塊。
            1. 選取每個要新增的廣告旁的核取方塊。
            1. 按一下 **[!UICONTROL Attach]**.
            1. 在廣告名稱旁，按一下&#x200B;**[!UICONTROL Select]**。
      1. （選用）若要覆寫版位中特定廣告的預設投放期間和廣告輪換：
         1. 按一下 **[!UICONTROL Custom Schedule Ads]**.

         1. 執行下列任一操作：

            * 若要新增投放，請按一下&#x200B;**[!UICONTROL Add Flight]**，然後指定開始日期和結束日期。

            * 若要將現有投放新增至廣告，請按一下投放欄廣告列中的&#x200B;**[!UICONTROL +]**。

            * 若要從廣告中移除現有投放，請按一下投放欄廣告列中的&#x200B;**[!UICONTROL x]**。

            * （當多個廣告具有相同的投放時）若要不均勻地轉動廣告，請按一下投放資訊中的&#x200B;**[!UICONTROL Even Rotation]**，然後輸入要以百分比旋轉每個廣告的相對權重。

               總重量必須等於100。
         1. 按一下右上角的&#x200B;**[!UICONTROL Continue]**。

         1. 查看飛行詳細資訊，然後按一下&#x200B;**[!UICONTROL Save & Finish]**。




>[!MORELIKETHIS]
>
>* [關於版位管理](placement-about.md)
>* [編輯位置](placement-edit.md)
>* [編輯投放位置的廣告排程](placement-edit-ad-schedule.md)
>* [暫停或啟動位置](placement-pause-activate.md)
>* [版位設定](placement-settings.md)
>* [鍵盤快速鍵](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)

   >*[疑難排解效能](/help/dsp/optimization/troubleshooting-performance.md)

