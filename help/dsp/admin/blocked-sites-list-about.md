---
type: Documentation
cloud: Experience Cloud
solution: Advertising Cloud
product: advertising cloud
title: 關於帳戶層級和廣告商層級封鎖的網站清單
description: 關於帳戶層級和廣告商層級封鎖的網站清單
source-git-commit: ac35677ef4832177b7a7e735bbbbf24454371496
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# 關於帳戶層級和廣告商層級封鎖的網站清單

<!-- Can you just add domains for your acct profile or advertiser to which you have access? It doesn't look like you can remove or edit any existing domains. Or can you with a specific syntax? -->

<!-- For domains, sub-domains,...? Specify what is valid. -->
您可以編輯用於整個Advertising Cloud帳戶的已封鎖網站清單，以及帳戶中個別廣告商的其他清單。

封鎖的網站清單會定義要針對您的版位排除的目標集。 每個清單都可由頂層網站網域和任何層級組成 <!--- verify --> 子網域（例如example.com、my.example.com或my.new.example.com）)和行動應用程式名稱(例如???)<!-- package names/app IDs, the full URL in Google Play/iTunes? Specify what is valid. -->.

廣告商層級清單會覆寫帳戶層級清單。

>[!NOTE]
>
>* 除了Advertising Cloud DSP外，還會套用帳戶層級和廣告商層級封鎖的網站清單 [全局阻止的站點清單](/help/dsp/introduction/features/brand-safety-media-quality.md)，包括廣告認為不安全的網站。
>* 使用者也可以將目標網站新增至任何版位。
>* 被阻止的站點清單始終覆蓋目標站點清單。 如果版位同時排除和包含廣告的相同目標，則會排除該目標。 <!-- Verify -->


>[!MORELIKETHIS]
<!--
>* [Edit an Account-level or Advertiser-level Blocked Site List](/help/dsp/admin/blocked-sites-list-edit.md)
[Brand Safety and Media Quality](/help/dsp/introduction/features/brand-safety-media-quality.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
-->
