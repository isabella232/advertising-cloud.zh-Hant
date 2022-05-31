---
title: '從持久ID夥伴激活經過驗證的段 '
description: 瞭解如何通過持久ID解決方案激活經過驗證的受眾。
feature: DSP Audiences
source-git-commit: 8550b539676588c3a6bc07abe088b38bd4251725
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 從持久ID夥伴激活經過驗證的段

*Beta功能*

要通過Advertising Cloud DSP內的持久ID解決方案激活經過驗證的受眾，必須將您的網段翻譯成 [!DNL RampIDs]，在易買的環境中可識別。 您可以通過以下任一方法完成此任務：

* 利用與DSP [!DNL Adobe Real-Time Customer Data Profile (CDP)] 和 [!DNL Adobe-LiveRamp Retrieval API]。

* 手動將已驗證的段DSP從 [!DNL LiveRamp] [!DNL Connect] 控制項欄。

## 任務

1. 對於任一選項，請聯繫 `adcloud-support@adobe.com` 在中啟用以下設DSP置，這將允許您在市場活動中針對經過驗證DSP的段 [激活工作流中的所有步驟都已完成](source-about.md#workflow-sources):

   1. [!DNL LiveRamp] [!DNL RampID] 市場活動配置，然後從 [!DNL Real-Time CDP]。

   1. 帳戶級別&quot;[!UICONTROL LiveRamp segments]選項。

1. (用戶手動共用已驗證的段 [!DNL LiveRamp])完成以下步驟 [!DNL LiveRamp] [!DNL Connect] 儀表板：

   1. 激活目標磁貼 **[!DNL AAC API 1P Onboarding]**。

   1. 設定 [!DNL Identifier Settings] 至 **[!DNL Ramp ID]** 只是。

      ![標識符設定](/help/dsp/assets/liveramp-tile-settings.png)

   1. （可選）如果仍要接收基於cookie的標識符，請建立第二個 [!DNL AAC API 1P Onboarding] 目標磁貼（帶「」）[!DNL Cookies]「」[!DNL IDFA],&quot;和&quot;[!DNL AAID]的下界。

## 測試和資料驗證的最佳做法

* **目標 [!DNL RampID]不同市場活動中基於Cookie的市場細分。**

   * 市場活動設定只允許一個標識符按優先順序排列。

   * 目前， [!DNL RampIDs] 無法在現場事件期間檢索。 這意味著某些自定義目標（如最低CPA和ROAS）在使用經過身份驗證的段時不可用。 僅當具有限制性效能KPI時，才使用基於cookie的段。

* **在兩個 [!DNL RampID] 和基於曲奇的活動。**

   * 瞄準共用的段 [!DNL LiveRamp] 使用標準段激活過程。

   * 與您的Advertising Cloud支援團隊合作，驗證正確的資料分發。

瞭解有關與整合的DSP詳細資訊 [!DNL LiveRamp]，聯繫人 `adcloud-support@adobe.com`。

>[!MORELIKETHIS]
>
>*[關於從受眾源激活經過驗證的段](source-about.md)
>* [建立受眾源以激活第一方受眾](source-create.md)
>* [受眾源設定](source-settings.md)
>* [Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [關於受眾管理](/help/dsp/audiences/audience-about.md)

