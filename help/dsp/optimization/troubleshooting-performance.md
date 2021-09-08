---
title: 效能疑難排解
description: 參考常見的效能問題，並了解如何進行疑難排解。
feature: Optimization
exl-id: adb32257-dede-4623-9840-33221c218443
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# 效能疑難排解

| 問題 | 可能的原因 | 要採取的動作 |
| --- | --- | --- |
| 在位置上無花費 | 版位不包含廣告，和/或廣告不作用中。 | 確認所有預期的廣告已附加至版位，且已核准且有效。<br><br>同時，查看版位是否包含自訂廣告排程，這可能會限制每個廣告的投放時間。若要從「版位」檢視查看版位的廣告排程，請按一下版位名稱旁的「**[!UICONTROL ...]>[!UICONTROL Ad schedule]**」 。 |
|  | 受影響的日期不在設定的飛行日期內。 | 檢查投放日期在促銷活動、封裝和版位層級有&#x200B;效。 |
|  | 預算目標已達到且/或不夠高。 | 在促銷活動、套件和版位層級檢查預算設定。 |
|  | 賬戶資金不足。 | 要查看您的帳戶是否有足夠的資金，請轉至&#x200B;**[!UICONTROL Settings]>[!UICONTROL Account]**&#x200B;並查看[!UICONTROL Usable Funds]的金額。 如果您需要新增更多資金，請連絡您的Adobe客戶經理。 |
|  | 沒有可用庫存。 | 驗證指定的庫存來源（[!UICONTROL Public]、[!UICONTROL Private]或[!UICONTROL On Demand]）是否為：<ul><li>正確設定。</li><li>通過拍賣活動和發送。</li><li>與適用的廣告和版位類型相容。</li></ul><br>如果庫存來源全部有效且有效，則盡可能定位其他或所有庫存來源。 |
|  | 沒有可用用戶。 | 檢查指定的對象目標是否包含足夠的作用中使用者。 如果沒有，請新增更多對象以展開目標。 |
| 投入少 | 版位診斷報表的[!UICONTROL Non Bids]區段會顯示版位未競標的可能原因。 | [檢閱報 [!UICONTROL Non Bids] ](/help/dsp/campaign-management/reports/placement-diagnostics.md) 表，了解版位未競標的原因。   <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
|  | 版位使用[預先出價篩選器](/help/dsp/campaign-management/placements/placement-settings.md)來限制出價。 | 將預先出價篩選器的臨界值降低5%，以評估支出與績效的平衡。 <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>請記得，使用多個版位目標（例如預先出價篩選器、地標、詳細目錄和對象）可能會累積限制出價和支出。 |
|  | 該位置的獲勝率很低。 | 增加[!UICONTROL Max Bid]以提高獲勝率。<br><br><b>注意：</b> 庫存價格可能因版位的目標而有所差異。<br><br>10%的贏率被認為是健康的。 |
|  | 可用庫存量較少。 | 如果可能，定位其他或所有庫存來源。<br><br>請記得，使用多個版位目標（例如預先出價篩選器、地標、詳細目錄和對象）可能會累積限制出價和支出。 |
|  | 可用的使用者人數不多。 | 檢查指定的對象目標是否包含足夠的作用中使用者。 如果沒有，請新增更多對象以展開目標。<br><br>請記得，使用多個版位目標（例如預先出價篩選器、地標、詳細目錄和對象）可能會累積限制出價和支出。 |
|  | 套件包含大量作用中版位。 | 減少包內的有效位置數或增加總體包預算。<br><br>如果套件有多個刊登版位，但預算不足，DSP可能無法為每個刊登版位分配足夠的預算。每個職位應該有機會每天至少花費2美元。 例如，若您的套件預算為每天10美元，則最好包含五個或更少版位。&#x200B; |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [版位設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [套件設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [促銷活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)

