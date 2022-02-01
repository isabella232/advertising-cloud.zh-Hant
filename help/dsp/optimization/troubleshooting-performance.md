---
title: 排除效能故障
description: 參考常見效能問題並查看如何排除它們。
feature: DSP Optimization
exl-id: adb32257-dede-4623-9840-33221c218443
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# 排除效能故障

| 問題 | 可能的原因 | 要採取的操作 |
| --- | --- | --- |
| 不在職位安排上花費 | 該放置不包括廣告，和/或該廣告不活動。 | 驗證所有預期廣告是否都附加到放置位置，且是否已批准並處於活動狀態。<br><br>另外，查看該位置是否包括自定義廣告時間表，這可能會限制每個廣告的飛行時間。 要從「放置」視圖查看放置的廣告計畫，請按一下  **[!UICONTROL ...]>[!UICONTROL Ad schedule]** 的子菜單。 |
|  | 受影響的日期不在配置的航班日期內。 | 檢查航班日期在市場活動、包裝和職位安排級別&#x200B;是否有效。 |
|  | 預算目標已經實現，並且（或）不夠高。 | 在市場活動、包和職位安排層檢查預算設定。 |
|  | 帳戶沒有足夠的資金。 | 要查看您的帳戶是否資金充足，請轉到 **[!UICONTROL Settings]>[!UICONTROL Account]** 看看 [!UICONTROL Usable Funds]。 如果需要添加更多資金，請與 [!DNL Adobe] 客戶團隊。 |
|  | 沒有可用的庫存。 | 驗證指定的庫存來源([!UICONTROL Public]。 [!UICONTROL Private]或 [!UICONTROL On Demand]):<ul><li>設定正確。</li><li>通過拍賣進行活動和發送。</li><li>與適用的廣告和放置類型相容。</li></ul><br>如果庫存來源均有效且有效，則盡可能瞄準附加或所有庫存來源。 |
|  | 沒有可用用戶。 | 檢查指定的受眾目標是否包含足夠的活動用戶。 否則，通過增加更多觀眾來擴展目標。 |
| 在職位安排上花費較少 | 的 [!UICONTROL Non Bids] 放置診斷報告的部分顯示了放置未投標的可能原因。 | [查看 [!UICONTROL Non Bids] 報告](/help/dsp/campaign-management/reports/placement-diagnostics.md) 去理解為什麼這次發行沒有出價。  <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
|  | 放置使用 [預投標過濾器](/help/dsp/campaign-management/placements/placement-settings.md) 限價競標。 | 將投標前篩選器的閾值降低5%，以評估支出和績效的平衡。 <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>請記住，使用多個放置目標（如預投標篩選器、geos 、庫存和觀眾）可能累計限制投標和支出。 |
|  | 這次安排的獲勝率很低。 | 增加 [!UICONTROL Max Bid] 提高贏率。<br><br><b>注：</b> 庫存價格可能因配售目標而異。<br><br>10%的成功率被認為是健康的。 |
|  | 可用庫存數量較少。 | 盡可能瞄準其他或所有庫存來源。<br><br>請記住，使用多個放置目標（如預投標篩選器、geos 、庫存和觀眾）可能累計限制投標和支出。 |
|  | 可用用戶數很少。 | 檢查指定的受眾目標是否包含足夠的活動用戶。 否則，通過增加更多觀眾來擴展目標。<br><br>請記住，使用多個放置目標（如預投標篩選器、geos 、庫存和觀眾）可能累計限制投標和支出。 |
|  | 該包包含大量活動放置。 | 減少包內有效安置的數量或增加總的包預算。<br><br>如果一攬子計畫有許多安置但預算不足，DSP則可能無法為每次安置分配足夠的預算。 每份廣告應該有機會花費至少2美元/天。 例如，如果您的包預算為10美元/天，則最好包括五次或更少的安置。&#x200B; |

{style=&quot;table-layout:auto&quot;&quot;

>[!MORELIKETHIS]
>
>* [放置設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [包設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [市場活動設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)

