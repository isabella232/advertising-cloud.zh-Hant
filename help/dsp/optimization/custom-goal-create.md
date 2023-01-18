---
title: 建立自訂目標
description: 建立自訂目標
feature: DSP Optimization
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 0%

---

# 建立自訂目標

您可以將自訂目標建立為 *目標* with [!DNL Adobe Advertising Search].

若要建立自訂目標，DSP帳戶必須連結至 [!DNL Search] 帳戶(使用相同的Adobe Experience Cloud組織ID)，從 [!DNL Search] 用戶端設定。 如果您的DSP帳戶未連結至 [!DNL Search] 帳戶，請連絡您的 [!DNL Adobe] 客戶團隊。

>[!TIP]
>
>請參閱 [建立自訂目標的最佳作法](custom-goal-best-practices.md) 以取得如何設定自訂目標的秘訣。

1. 登入 [!DNL Adobe Advertising Search] at（美國公司） [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) 或（所有其他國家/地區的公司） [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. 請確定您要包含在目標中的量度已受到追蹤、可在產品中使用，且包含顯示名稱：
   1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.
   1. 找出量度，並確定 **[!UICONTROL Show in UI and Reports]** 已針對量度啟用。
   1. 如果量度在 **[!UICONTROL Display Name]** 欄，按一下儲存格，輸入顯示名稱，然後按一下 **[!UICONTROL Apply].**
1. 將自訂目標建立為 *目標*:
   1. 在主功能表中，按一下 **[!UICONTROL Search]> [!UICONTROL Optimization] >[!UICONTROL Objectives]**.
   1. 在工具列中，按一下 **[!UICONTROL Create objective].**
   1. 輸入目標設定：
      1. 在 **[!UICONTROL Change Objective Name]** 欄位，輸入目標名稱。

         目標名稱將顯示在 [!UICONTROL Custom Goals] 清單(位於DSP套件設定中)。

      1. 將屬性與目標關聯：

         >[!NOTE]
         >
         > 預設會將廣告商追蹤的所有交易屬性列在 [!UICONTROL Available Properties] 清單。

         * 若要匯入包含屬性和其權重的CSV檔案，請按一下 **[!UICONTROL Import]** 並找到要匯入的檔案。

            廣告商必須已有匯入的屬性；這些名字不區分大小寫。

            導入的屬性將替換任何指定的現有屬性。

         * 若要手動指定具有預設權數(1)的第一個屬性，請從為廣告商追蹤的所有交易屬性清單中選取。

         * 若要手動新增其他具有預設權數(1)的屬性，請按一下 **[!UICONTROL +]** .

            >[!TIP]
            >
            > 若要在清單中搜尋屬性，請從屬性名稱內的任何位置輸入字串。

         * 若要手動新增多個屬性，請按一下 **[!UICONTROL Add Multiple Properties].** 針對您要新增的每個屬性，按一下 [!UICONTROL Available Properties] 欄並拖曳至 [!UICONTROL Added Properties] 欄。 完成添加屬性後，按一下 **[!UICONTROL Add]**.

            >[!TIP]
            >
            >* 若要在清單中搜尋屬性，請在輸入欄位中從屬性名稱內的任何位置輸入字串。
            >* 若要篩選清單以排除報表中排除的屬性，請選取選項 **[!UICONTROL Hide properties excluded from reports].**


         * （當目標包含多個屬性時）要更改屬性相對於目標中其他屬性的權重，請在 **[!UICONTROL Weight]** 欄位。
      1. 在設定底部，按一下 **[!UICONTROL Save]**.


建立目標後，當最佳化目標為「[!UICONTROL Highest ROAS - Custom Goal]&quot;或&quot;[!UICONTROL Lowest CPA - Custom Goal].&quot;

>[!TIP]
>
>為獲得最佳效能，自訂目標（目標）中的合併量度每天必須至少有10次轉換。 如果沒有，最佳實務是將其他支援事件（交易屬性）（如產品頁面或應用程式啟動）新增至目標。 請參閱 [建立自訂目標的最佳作法](custom-goal-best-practices.md) 以取得指引。

>[!MORELIKETHIS]
>
>* [關於自訂目標](custom-goal-about.md)
>* [建立自訂目標的最佳作法](custom-goal-best-practices.md)
>* [最佳化目標及其使用方式](optimization-goals.md)
>* [套件設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何最佳化您的行銷活動](optimization-how-dsp-optimizes-campaigns.md)

