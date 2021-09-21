---
title: 建立可重複使用的受眾
description: 了解如何建立可重複使用的對象，這些對象包含對象區段和其他儲存的對象。
feature: DSP Audiences
exl-id: 48e3dc4c-6e2d-452c-8d69-7e6211d808e0
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# 建立可重複使用的受眾

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

您可以儲存和管理可重複使用的對象，這些對象是對象區段群組，甚至是其他已儲存的對象，您可將這些對象用作多個版位的目標或排除項目。

1. 在主菜單中，按一下「**[!UICONTROL Audiences]>[!UICONTROL All Audiences]**」。

1. 在資料表上方，按一下&#x200B;**[!UICONTROL Create]**。

1. 輸入唯一[!UICONTROL Audience Name]。

1. （選用）取消選取&#x200B;**[!UICONTROL Share with all advertisers in my account]**&#x200B;選項。

   當您共用對象時，該對象將成為帳戶內所有廣告商的目標或排除項目。 不過，受眾中的個別區段僅供共用區段的使用者使用。 例如，如果您與未對應至相同[!DNL Analytics]帳戶的廣告商共用包含Adobe Analytics區段的對象，則該區段不會預覽於該廣告商的該對象。 只有該廣告商可用的區段才會在受眾中預覽。

1. 按一下 **[!UICONTROL Save]**.

1. 建立對象：

   >[!NOTE]
   >
   >當您建立對象時，會在右側面板中更新詳細的[對象大小資料](audience-about.md)。

   * 若要手動建立區段邏輯，請使用[[!UICONTROL Third Party Segments]、[!UICONTROL First Party Segments]、[!UICONTROL Adobe Segments]、[!UICONTROL Custom Segments]和[!UICONTROL Saved Audiences]標籤](audience-settings.md)上可用的區段，執行下列操作。

      * 若要新增第一個區段，請在左側面板中找出區段，然後選取區段名稱旁的核取方塊。

      * 若要將區段新增至現有區段群組：

         1. 按一下右側面板中的區段群組。

         1. （可選）視需要將群組邏輯變更為&#x200B;*[!UICONTROL Include Any]*、*[!UICONTROL Include All]*&#x200B;或&#x200B;*[!UICONTROL Exclude All]*。

            *[!UICONTROL Exclude All]* 不適用於第一個區段群組。針對僅包含排除的對象，將此對象建置為&#x200B;*[!UICONTROL Include Any]*，然後在版位內，從「排除的對象」功能表中選取該對象。

         1. 在左側面板中找出新區段，並選取區段名稱旁的核取方塊。

            區段群組會自動以新區段更新。
      * 若要新增區段群組：

         1. 按一下右側面板中的&#x200B;**[!UICONTROL + New Group]**。

         1. （可選）視需要將上一個群組和新群組之間的邏輯變更為&#x200B;*[!UICONTROL And]*&#x200B;或&#x200B;*[!UICONTROL Or]*。

         1. 在左側面板中找出新群組的區段，並選取區段名稱旁的核取方塊。

         1. （可選）視需要將群組邏輯變更為&#x200B;*[!UICONTROL Include Any]*、*[!UICONTROL Include All]*&#x200B;或&#x200B;*[!UICONTROL Exclude All]*。
   * 若要使用現有對象的區段邏輯：

      1. 以下列任何方式複製現有對象的區段邏輯：

         * 在「所有對象」檢視中，將游標停留在對象列上，然後按一下&#x200B;**[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**。

         * 在現有對象的設定中，在區段邏輯面板頂端，按一下「**[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**」。

         * 在文字編輯器中，使用英數字元區段ID和[布林語法](audience-segment-logic-syntax.md)手動建立區段邏輯，並將其複製到剪貼簿。
      1. 按一下「**[!UICONTROL paste in an audience rule to begin building]**」，將現有區段邏輯貼入輸入欄位，然後按一下「**[!UICONTROL Apply]**」。

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
>* [建立和實作區 [!UICONTROL CCPA Opt-Out-of-Sale] 段](ccpa-opt-out-segment-create.md)
>* [版位設定](/help/dsp/campaign-management/placements/placement-settings.md)

