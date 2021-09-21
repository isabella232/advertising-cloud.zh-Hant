---
title: 關於Campaign管理的常見問題集
description: 進一步了解行銷活動管理，包括變更的延遲期間，以及在飛行期間進行預算變更時會發生什麼事。
feature: DSP Packages, DSP Placements
exl-id: 9034ab2c-b8b0-4759-bc87-5f73857bb062
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# 關於Campaign管理的常見問題集

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## 設定變更的延遲

* 當您更改放置或包設定時，更改何時生效？

   設定變更通常會立即生效，但最多可能需要12小時。

   如果是傳送的最後一天，請在當天早上進行變更，讓DSP有充足的時間根據變更重新校準套件。 例如，如果您從步調調整到前載步調，DSP需要重新評估其在剩餘飛行時間中如何分配支出。 如果在航班的最後一天只剩一個小時，那就別做這種改變。

## 飛行期間預算更新

* 當您變更版位時，DSP需要多久才能重新分配套件預算？

   預算分配是以刊登版位績效為基礎，而刊登版位績效是使用14天平均值評估。 版位的變更只會在14天平均期間導致效能變更時，才導致預算分配的變更。

   當效能變更發生時，DSP會在下一個預算最佳化週期(大約在促銷活動時區的午夜(00:00))內，相應地重新分配版位之間的套件預算。

* 從套件移除版位並新增至其他套件時，如何重新分配預算？

   版位的整個支出歷史記錄會附加至版位，並隨之從套件移動至套件。

   當您從套件中移除版位時，套件不再具有版位支出的任何記錄。 包預算將變成（包預算 — 刪除的版位預算）/剩餘時間間隔。 然後將包預算分配給包中剩餘的位置。

   同樣地，如果將相同版位新增至不同套件，當DSP為新套件中的所有版位分配預算時，會考量該版位的支出歷史記錄。

* 在飛行的最後一天，包裝的步調會如何改變？

   在飛行的最後一天，該天從24小時縮短為23小時，以便不超出包預算。 此外，包的步調填充策略會自動更改為&quot;[!UICONTROL Frontload]&quot;，即使它設定為&quot;[!UICONTROL even]&quot;。 這意味著65%的日預算應在美國東部標準時間上午11:30前交付。

>[!MORELIKETHIS]
>
>* [套件設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [版位設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [設定效能行銷活動的最佳實務](/help/dsp/optimization/campaign-best-practices-performance.md)

