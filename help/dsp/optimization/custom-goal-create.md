---
title: 建立自訂目標
description: 建立自訂目標
feature: DSP Optimization
exl-id: 440ded21-92d3-41ad-839f-ebc8376aa932
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# 建立自訂目標

>[!TIP]
>
>請參閱建立自訂目標的[最佳實務](custom-goal-best-practices.md)以取得如何設定自訂目標的秘訣。

1. 登入Advertising Cloud Search（美國公司）[`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com)或（所有其他國家/地區的公司）[`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com)。
1. 請確定您要包含在目標中的量度已受到追蹤、可在產品中使用，且包含顯示名稱：
   1. 在主菜單中，按一下「**[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**」。
   1. 找出量度，並確認已為量度啟用&#x200B;**[!UICONTROL Show in UI and Reports]**。
   1. 如果量度在&#x200B;**[!UICONTROL Display Name]**&#x200B;欄中沒有值，請按一下儲存格，輸入顯示名稱，然後按一下&#x200B;**[!UICONTROL Apply]。**
1. 將自訂目標建立為&#x200B;*objective*:
   1. 在主菜單中，按一下「**[!UICONTROL Search]> [!UICONTROL Optimization] >[!UICONTROL Objectives]**」。
   1. 在工具列中，按一下&#x200B;**[!UICONTROL Create objective]。**
   1. 輸入目標設定：
      1. 在&#x200B;**[!UICONTROL Change Objective Name]**&#x200B;欄位中，輸入目標名稱。

         目標名稱將顯示在Advertising Cloud DSP套件設定的[!UICONTROL Custom Goals]清單中。

      1. 將屬性與目標關聯：

         >[!NOTE]
         >
         > 預設情況下，[!UICONTROL Available Properties]清單會列出廣告商追蹤的所有交易屬性。

         * 若要匯入包含屬性和其權重的CSV檔案，請按一下&#x200B;**[!UICONTROL Import]**&#x200B;並找到要匯入的檔案。

            廣告商必須已有匯入的屬性；這些名字不區分大小寫。

            導入的屬性將替換任何指定的現有屬性。

         * 若要手動指定具有預設權重(1)的第一個屬性，請從為廣告商追蹤的所有交易屬性清單中選取。

         * 若要手動新增其他具有預設權數(1)的屬性，請按一下「**[!UICONTROL +]**」 。

            >[!TIP]
            >
            > 若要在清單中搜尋屬性，請從屬性名稱內的任何位置輸入字串。

         * 要手動添加多個屬性，請按一下&#x200B;**[!UICONTROL Add Multiple Properties]。** 針對您要新增的每個屬性，按一下欄中的屬性 [!UICONTROL Available Properties] 名稱，並將其拖曳至 [!UICONTROL Added Properties] 欄。添加完屬性後，按一下&#x200B;**[!UICONTROL Add]**。

            >[!TIP]
            >
            >* 若要在清單中搜尋屬性，請在輸入欄位中從屬性名稱內的任何位置輸入字串。
            >* 若要篩選清單以排除報表中排除的屬性，請選取選項&#x200B;**[!UICONTROL Hide properties excluded from reports]。**


         * （當目標包含多個屬性時）要更改屬性相對於目標中其他屬性的權重，請在&#x200B;**[!UICONTROL Weight]**&#x200B;欄位中輸入值。
      1. 在設定底部，按一下&#x200B;**[!UICONTROL Save]**。


建立目標後，當最佳化目標為「[!UICONTROL Highest ROAS - Custom Goal]」或「[!UICONTROL Lowest CPA - Custom Goal]」時，您可以將其指派給Advertising Cloud DSP套件，作為自訂目標。

>[!TIP]
>
>為了最佳化<!-- optimum? Or optimization won't happen at all w/out it? -->效能，自訂目標（目標）中的合併量度每天必須總計至少10次轉換。 如果沒有，最佳實務是將其他支援事件（交易屬性）（如產品頁面或應用程式啟動）新增至目標。 如需准則，請參閱[建立自訂目標的最佳實務](custom-goal-best-practices.md) 。

>[!MORELIKETHIS]
>
>* [關於自訂目標](custom-goal-about.md)
>* [建立自訂目標的最佳作法](custom-goal-best-practices.md)
>* [最佳化目標及其使用方式](optimization-goals.md)
>* [套件設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何最佳化您的行銷活動](optimization-how-dsp-optimizes-campaigns.md)

