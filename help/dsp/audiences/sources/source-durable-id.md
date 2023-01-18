---
title: 向耐用ID合作夥伴啟用已驗證的區段
description: 了解如何透過持久ID解決方案啟用已驗證的受眾。
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# 向耐用ID合作夥伴啟用已驗證的區段

*測試版功能*

若要透過Advertising DSP內的持久ID解決方案啟用已驗證的受眾，您的區段必須翻譯為 [!DNL RampIDs]，在可買的環境中可辨識。 您可以執行下列任一操作：

* 善用DSP與 [!DNL Adobe Real-Time Customer Data Profile (CDP)] 和 [!DNL Adobe-LiveRamp Retrieval API].

* 手動傳送已驗證的區段至DSP [!DNL LiveRamp] [!DNL Connect] 控制面板。

## 工作

1. 若為任一選項，請聯絡 `adcloud-support@adobe.com` 若要在DSP中啟用下列設定，這可讓您在DSP促銷活動中定位已驗證的區段一次 [啟動工作流程中的所有步驟皆已完成](source-about.md#workflow-sources):

   1. [!DNL LiveRamp] [!DNL RampID] 從 [!DNL Real-Time CDP].

   1. 帳戶層級「[!UICONTROL LiveRamp segments]」。

1. (使用者手動共用已驗證的區段，來自 [!DNL LiveRamp])在 [!DNL LiveRamp] [!DNL Connect] 控制面板：

   1. 激活目標磁貼 **[!DNL AAC API 1P Onboarding]**.

   1. 設定 [!DNL Identifier Settings] to **[!DNL Ramp ID]** 只有。

      ![識別碼設定](/help/dsp/assets/liveramp-tile-settings.png)

   1. （選用）如果您仍要接收Cookie型識別碼，請建立第二個 [!DNL AAC API 1P Onboarding] 具有「[!DNL Cookies], &quot;[!DNL IDFA],&quot;和&quot;[!DNL AAID]」。

## 測試和資料驗證的最佳實務

* **目標 [!DNL RampID]個別促銷活動中的「以Cookie為基礎的區段」。**

   * 促銷活動設定僅允許排定優先順序一個識別碼。

   * 目前， [!DNL RampIDs] 在站點事件期間無法檢索。 這表示某些自訂目標（例如最低CPA和ROAS）無法使用已驗證的區段。 只有在您有限制的效能KPI時，才使用Cookie型區段。

* **在 [!DNL RampID] 和Cookie型行銷活動。**

   * 定位從共用的區段 [!DNL LiveRamp] 使用標準區段啟用程式。

   * 與您的Adobe廣告支援團隊合作，驗證資料的分送是否正確。

若要進一步了解DSP與 [!DNL LiveRamp]，聯絡 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [關於從受眾來源啟用已驗證的區段](source-about.md)
>* [建立對象來源以啟用第一方對象](source-create.md)
>* [對象來源設定](source-settings.md)
>* [AdobeAdvertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [關於Audience Management](/help/dsp/audiences/audience-about.md)

