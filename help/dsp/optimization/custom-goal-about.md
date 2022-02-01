---
title: 關於自定義目標
description: 瞭解自定義目標，以在針對最低CPA或最高ROAS優化的包中定義成功事件。
feature: DSP Optimization
exl-id: 623cb1ef-85ab-4535-aa3a-8e6ec8ae15ee
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# 關於自定義目標

自定義目標定義廣告商滿足其業務目標所需的成功事件。 每個使用優化目標&#39;&#39;的包[!UICONTROL Highest ROAS - Custom Goal]&quot;或&quot;[!UICONTROL Lowest CPA - Custom Goal]必須包括有助於實現總體優化目標的自定義目標。 您可以建立自定義目標 *目標* 在Advertising Cloud Search。

![自定義目標](/help/dsp/assets/objective-goals.png)

每個自定義目標都由一個或多個度量組成，或 *事務處理屬性*，以及這些事務屬性的相對權重。 可用事務屬性包括使用Advertising Cloud轉換像素和通過Adobe Analytics跟蹤的所有度量。

>[!NOTE]
>
>* [!DNL Analytics] 尺寸和段不可用於Advertising Cloud優化。
>* 要在中使用分析事DSP件，請使用 [!DNL Adobe] 客戶團隊來配置廣告商級整合。
>* [!DNL Analytics] 自定義事件遵循此命名約定： `custom_event_[*event #*]_[*Analytics report suite ID*]`。 示例： `custom_event_16_examplersid`


例如，假設三個指標（事務處理屬性）與您的其中一個市場活動中的特定包相關：&quot;PDF下載&quot;價值20美元，&quot;電子郵件註冊&quot;價值30美元，&quot;訂單確認&quot;價值40美元。 如果您想根據客戶活動的一次性貨幣價值賦予權重，則屬性的相對權重為1、2和1.5。

查看 [建立自定義目標的最佳實踐](custom-goal-best-practices.md) 有關如何配置自定義目標的提示。

一旦 [建立自定義目標](custom-goal-create.md), [將其分配給包](/help/dsp/campaign-management/packages/package-settings.md) 報告和算法優化的Adobe Sensei。

>[!MORELIKETHIS]
>
>* [建立自定義目標](custom-goal-create.md)
>* [構建自定義目標的最佳做法](custom-goal-best-practices.md)
>* [優化目標及其使用方法](optimization-goals.md)
>* [包設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [如何優DSP化您的市場活動](optimization-how-dsp-optimizes-campaigns.md)

