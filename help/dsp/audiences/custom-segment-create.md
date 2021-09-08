---
title: 建立和實作自訂區段
description: 了解如何建立和實作自訂區段，以追蹤對廣告公開的使用者或瀏覽您網頁的使用者。
feature: Segments
exl-id: 691903e2-773e-4205-837e-822f435f57a7
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# 建立和實作自訂區段

您可以建立並實作自訂Advertising Cloud區段，以收集您自己的第一方對象資料。 您可以使用區段來追蹤a)從案頭、行動裝置和CTV裝置公開廣告的使用者，以及b)瀏覽特定網頁的使用者。 您之後可以透過其他廣告重新定位區段中的使用者，或防止區段中的使用者收到其他廣告。

>[!NOTE]
>
>若要在您的網站上追蹤來自消費者選擇退出銷售請求的使用者ID，請根據加州消費者隱私法(CCPA)，建立[CCPA選擇退出銷售區段](ccpa-opt-out-segment-create.md)。

1. 建立區段：

   1. 在主菜單中，按一下「**[!UICONTROL Audiences]>[!UICONTROL Segments]**」。

   1. 在資料表上方，按一下&#x200B;**[!UICONTROL Create]**。

   1. 輸入唯一&#x200B;**[!UICONTROL Segment Name]**。

   1. 對於[!UICONTROL Segment Type]，選擇&#x200B;**[!UICONTROL Custom]**。

   1. 輸入「區段視窗」，即使用者的Cookie在區段中停留的天數。

      預設視窗為45天。 輸入一(1)到365之間的值。

   1. 按一下 **[!UICONTROL Save]**.

1. 視需要複製並實作標籤以追蹤區段：

   1. 返回&#x200B;**[!UICONTROL Audiences]>[!UICONTROL Segments]**。

   2. 將游標停留在段行上，然後按一下&#x200B;**[!UICONTROL Get pixel]**。

      * 若要追蹤網頁的案頭和行動訪客：

         1. 複製標示為「[!UICONTROL Desktop or mobile websites]」的頁面檢視追蹤標籤。

         1. 將標籤提供給廣告商或網站連絡人以進行部署。

            廣告商的IT部門或其他群組可能需要排程標籤部署，或接收相關通知。
      * 若要追蹤在桌上型電腦、行動裝置或CTV裝置上對廣告單元公開的使用者：

         1. 複製標示為「[!UICONTROL Desktop or mobile ads]」的曝光追蹤標籤。

         1. 將標籤新增至任何廣告的[!UICONTROL Pixel]標籤。<!-- I'll add cross-reference to ad settings later. -->


實作追蹤標籤後，您就可以在對象目標或任何版位的排除項目中使用區段。

>[!TIP]
>
>追蹤使用者時，請持續追蹤區段大小。

>[!MORELIKETHIS]
>
>* [關於Audience Management](audience-about.md)
>* [建立和實作區 [!UICONTROL CCPA Opt-Out-of-Sale] 段](ccpa-opt-out-segment-create.md)
>* [建立可重複使用的受眾](reusable-audience-create.md)
>* [對象設定](audience-settings.md)
>* [可用的第三方資料提供者](third-party-data-providers.md)
>* [版位設定](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- I'll add x-ref to ad settings later.-->
