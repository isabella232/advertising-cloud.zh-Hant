---
title: 建立可重用的受眾
description: 瞭解如何建立由受眾段和其他已保存的受眾組成的可重用受眾。
feature: DSP Audiences
exl-id: 48e3dc4c-6e2d-452c-8d69-7e6211d808e0
source-git-commit: 37e5a4fbb7e2ccda77ab0afd49054ec4d1dabf76
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# 建立可重用的受眾

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

您可以保存和管理可重複使用的受眾，這些受眾是受眾段的組，甚至是其他已保存的受眾，您可以將其用作多個放置的目標或排除。

1. 在主菜單中，按一下 **[!UICONTROL Audiences]>[!UICONTROL All Audiences]**。

1. 在資料表上方，按一下 **[!UICONTROL Create]**。

1. 輸入唯一 [!UICONTROL Audience Name]。

1. （可選）取消選擇選項以 **[!UICONTROL Share with all advertisers in my account]**。

   當您共用受眾時，受眾將成為帳戶內所有廣告商的目標或排除對象。 但是，受眾中的各個段僅對共用這些段的用戶可用。 例如，如果您與未映射到同一廣告商共用包含Adobe Analytics網段的受眾 [!DNL Analytics] 帳戶，則該網段將不會在該廣告商的受眾中預覽。 只有該廣告商可用的網段才會在觀眾中預覽。

1. 按一下 **[!UICONTROL Save]**.

1. 構建受眾：

   >[!NOTE]
   >
   >在構建受眾時， [受眾大小資料](audience-about.md) 在右面板中更新

   * 要手動建立段邏輯，請使用 [[!UICONTROL Third Party Segments]。 [!UICONTROL First Party Segments]。 [!UICONTROL Adobe Segments]。 [!UICONTROL Custom Segments], [!UICONTROL Saved Audiences] 頁籤](audience-settings.md)，執行以下操作。

      * 要添加第一個段，請在左面板中找到該段，然後選中段名稱旁邊的複選框。

      * 要將段添加到現有段組，請執行以下操作：

         1. 按一下右面板中的段組。

         1. （可選）將組邏輯更改為 *[!UICONTROL Include Any]*。 *[!UICONTROL Include All]*&#x200B;或 *[!UICONTROL Exclude All]*，根據需要。

            *[!UICONTROL Exclude All]* 不可用於第一個段組。 對於僅包括排除的受眾，將此受眾構建為 *[!UICONTROL Include Any]* 然後，在放置中，從「排除的受眾」菜單中選擇該受眾。

         1. 在左面板中找到新段，然後選中段名稱旁邊的複選框。

            段組將自動使用新段更新。
      * 要添加新段組，請執行以下操作：

         1. 按一下 **[!UICONTROL + New Group]** 的下界。

         1. （可選）將上一個組和新組之間的邏輯更改為 *[!UICONTROL And]* 或 *[!UICONTROL Or]*，根據需要。

         1. 在左面板中找到新組的段，然後選中段名稱旁邊的複選框。

         1. （可選）將組邏輯更改為 *[!UICONTROL Include Any]*。 *[!UICONTROL Include All]*&#x200B;或 *[!UICONTROL Exclude All]*，根據需要。
   * 要使用現有受眾的段邏輯：

      1. 以下列任何方式從現有受眾複製段邏輯：

         * 在「所有受眾」視圖中，將游標懸停在受眾行上，然後按一下 **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**。

         * 在現有受眾的設定中，在段邏輯面板頂部，按一下 **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**。

         * 在文本編輯器中，使用字母數欄位ID手動建立段邏輯， [布爾語法](audience-segment-logic-syntax.md)，然後複製到剪貼簿。
      1. 按一下 **[!UICONTROL paste in an audience rule to begin building]**，將現有段邏輯貼上到輸入欄位，然後按一下 **[!UICONTROL Apply]**。

         >[!NOTE]
         >
         >如果受眾已經包括任何段邏輯，則貼上到新段邏輯會覆蓋現有邏輯。




1. 按一下 **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [關於受眾管理](audience-about.md)
>* [受眾設定](audience-settings.md)
>* [受眾段邏輯的語法](audience-segment-logic-syntax.md)
>* [可用的第三方資料提供程式](third-party-data-providers.md)
>* [建立和實施自定義段](custom-segment-create.md)
>* [建立和實施 [!UICONTROL CCPA Opt-Out-of-Sale] 段](ccpa-opt-out-segment-create.md)
>* [放置設定](/help/dsp/campaign-management/placements/placement-settings.md)

