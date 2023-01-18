---
title: 編輯可重複使用的對象
description: 了解如何編輯可重複使用的對象。
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# 編輯可重複使用的對象

當您編輯任何版位或其他可重複使用對象中使用的對象時，變更會立即套用至這些版位和對象。<!-- verify -->

1. 在主功能表中，按一下 **[!UICONTROL Audiences]>[!UICONTROL All audiences]**.

1. 將游標停留在對象列上，然後按一下 **[!UICONTROL Edit]**.

1. 編輯對象設定的方式如下：

   >[!NOTE]
   >
   >如果您編輯對象區段邏輯，請詳細 [對象大小資料](audience-about.md) 會在右側面板中更新。

   * （選用）若要編輯 **[!UICONTROL Audience Name]** 按一下 ![編輯](/help/dsp/assets/edit.png) 在對象名稱旁，輸入唯一的對象名稱，然後按一下 **[!UICONTROL Apply]**.

   * （選用）若要手動編輯區段邏輯，請使用 [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments]，和 [!UICONTROL Saved Audiences] 標籤](audience-settings.md)，請執行下列動作。

      * 若要將區段新增至現有區段群組：
      1. 按一下右側面板中的區段群組。

      1. （選用）將群組邏輯變更為 *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*，或 *[!UICONTROL Exclude All]*，視需要。

         *[!UICONTROL Exclude All]* 不適用於第一個區段群組。 針對僅包含排除的對象，將此對象建置為 *[!UICONTROL Include Any]* 然後在版位中，從「排除的對象」功能表中選取該對象。

      1. 在左側面板中找出新區段，並選取區段名稱旁的核取方塊。

         區段群組會自動以新區段更新。
   * 若要新增區段群組：

      1. 按一下 **[!UICONTROL + New Group]** 中。

      1. （選用）將上一個群組和新群組之間的邏輯變更為 *[!UICONTROL And]* 或 *[!UICONTROL Or]*，視需要。

      1. 在左側面板中找出新群組的區段，並選取區段名稱旁的核取方塊。

      1. （選用）將群組邏輯變更為 *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*，或 *[!UICONTROL Exclude All]*，視需要。
   * 若要使用現有對象的區段邏輯：

      1. 以下列任何方式複製現有對象的區段邏輯：

         * 在「所有對象」檢視中，將游標停留在對象列上方，然後按一下 **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * 在現有對象的設定中，在區段邏輯面板頂端，按一下 **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * 在文字編輯器中，使用英數字元區段ID手動建立區段邏輯，並 [布林語法](audience-segment-logic-syntax.md)，並複製到剪貼簿。
      1. 按一下 **[!UICONTROL paste in an audience rule to begin building]**，將現有的區段邏輯貼入輸入欄位，然後按一下 **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >如果對象已包含任何區段邏輯，則貼入新區段邏輯會覆寫現有邏輯。





1. 按一下 **[!UICONTROL Save]**.

1. 在確認訊息中，按一下 **[!UICONTROL Continue]**.

>[!MORELIKETHIS]
>
>* [關於Audience Management](audience-about.md)
>* [建立可重複使用的受眾](reusable-audience-create.md)
>* [複製可重複使用的對象](reusable-audience-duplicate.md)
>* [檢視可重複使用對象的詳細資訊](reusable-audience-view-details.md)
>* [共用可重複使用的受眾](reusable-audience-share.md)
>* [匯出可重複使用的對象](reusable-audience-export.md)
>* [將可重複使用對象的區段索引鍵複製到剪貼簿](reusable-audience-clipboard.md)
>* [刪除可重複使用的對象](reusable-audience-delete.md)
>* [對象設定](audience-settings.md)
>* [對象區段邏輯語法](audience-segment-logic-syntax.md)
>* [可用的第三方資料提供者](third-party-data-providers.md)

