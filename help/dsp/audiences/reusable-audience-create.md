---
title: 建立可重複使用的受眾
description: 了解如何建立可重複使用的對象，這些對象包含對象區段和其他儲存的對象。
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# 建立可重複使用的受眾

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

您可以儲存和管理可重複使用的對象，這些對象是對象區段群組，甚至是其他已儲存的對象，您可將這些對象用作多個版位的目標或排除項目。

1. 在主功能表中，按一下 **[!UICONTROL Audiences]>[!UICONTROL All Audiences]**.

1. 在資料表格上方，按一下 **[!UICONTROL Create]**.

1. 輸入唯一 [!UICONTROL Audience Name].

1. （選用）取消選取 **[!UICONTROL Share with all advertisers in my account]**.

   當您共用對象時，該對象將成為帳戶內所有廣告商的目標或排除項目。 不過，受眾中的個別區段僅供共用區段的使用者使用。 例如，如果您與未對應至相同廣告商共用包含Adobe Analytics區段的對象 [!DNL Analytics] 帳戶，則區段將不會預覽該廣告商在該對象中。 只有該廣告商可用的區段才會在受眾中預覽。

1. 按一下 **[!UICONTROL Save]**.

1. 建立對象：

   >[!NOTE]
   >
   >當您建立受眾時，會詳細 [對象大小資料](audience-about.md) 會在右側面板中更新

   * 若要手動建立區段邏輯，請使用 [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments]，和 [!UICONTROL Saved Audiences] 標籤](audience-settings.md)，請執行下列動作。

      * 若要新增第一個區段，請在左側面板中找出區段，然後選取區段名稱旁的核取方塊。

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




1. 按一下 **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [關於Audience Management](audience-about.md)
>* [對象設定](audience-settings.md)
>* [對象區段邏輯語法](audience-segment-logic-syntax.md)
>* [可用的第三方資料提供者](third-party-data-providers.md)
>* [建立和實作自訂區段](custom-segment-create.md)
>* [建立和實作 [!UICONTROL CCPA Opt-Out-of-Sale] 區段](ccpa-opt-out-segment-create.md)
>* [版位設定](/help/dsp/campaign-management/placements/placement-settings.md)

