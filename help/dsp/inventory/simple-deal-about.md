---
title: 關於 [!UICONTROL Simple Ad Serving]
description: 了解 [!UICONTROL Simple Ad Serving] 交易使用事件追蹤像素。
feature: DSP Simple Ad Serving
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# 關於 [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] 使用單一專屬版位，為指定的發佈商和單一廣告類型提供有保證的未決策廣告傳送和報表。 使用 [!DNL Simple Ad Serving] 當您的發行者無法透過交易ID執行交易時。 所有鎖定目標、預算調整和上限以及頻率限定均由發佈者處理。 透過事件追蹤像素執行這些交易。

使用 [!UICONTROL Simple Ad Serving]，則每個廣告都由發佈者（網站服務）直接提供，而DSP提供事件追蹤像素以傳送給發佈者，發佈者必須實作像素並傳送DSP廣告。 視詳細目錄類型而定，事件像素會測量曝光數、點進次數和視訊播放事件。

可使用下列廣告類型：

* 案頭標準前段
* 平板電腦和行動標準前段
* 連接電視標準前段
* 顯示
* 音訊

您可以建立 [!UICONTROL Simple Ad Serving] 交易 [!UICONTROL Inventory] > [!UICONTROL Deals] 檢視。 DSP會自動產生子類型為「[!DNL Simple ad serving]」。 版位會鎖定交易，但不允許額外鎖定目標、預算或頻率限定。 您只能編輯某些交易設定，例如交易名稱、CPM、曝光數和投放日期。<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving] 刊登版位不符合帳戶的可用資金或行銷活動和封裝預算。 但是，會追蹤支出並計入這些預算。 即使CPM為$0，事件資料也一律會受到追蹤。

>[!MORELIKETHIS]
>
>* [建立 [!UICONTROL Simple Ad Serving] 交易](simple-deal-create.md)
>* [編輯 [!UICONTROL Simple Ad Serving] 交易設定](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving] 設定](simple-deal-settings.md)
>* [查看交易的詳細報表](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
