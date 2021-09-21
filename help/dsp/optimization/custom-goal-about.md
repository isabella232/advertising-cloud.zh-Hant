---
title: 關於自訂目標
description: 了解自訂目標，以在針對最低CPA或最高ROAS最佳化的套件中定義成功事件。
feature: DSP Optimization
exl-id: 623cb1ef-85ab-4535-aa3a-8e6ec8ae15ee
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# 關於自訂目標

自訂目標會定義廣告商達成其業務目標所需的成功事件。 每個使用最佳化目標「[!UICONTROL Highest ROAS - Custom Goal]」或「[!UICONTROL Lowest CPA - Custom Goal]」的套件都必須包含有助於實現整體最佳化目標的自訂目標。 您可以在Advertising Cloud Search中將自訂目標建立為&#x200B;*目標*。

![自訂目標](/help/dsp/assets/objective-goals.png)

每個自訂目標都包含一或多個量度，或&#x200B;*交易屬性*，以及這些交易屬性的相對權重。 可用的交易屬性包含所有使用Advertising Cloud轉換像素和透過Adobe Analytics追蹤的量度。

>[!NOTE]
>
>* [!DNL Analytics] 維度和區段無法用於Advertising Cloud最佳化。
>* 若要在DSP中使用Analytics事件，請與您的Adobe帳戶管理員合作，以設定廣告商層級的整合。
>* [!DNL Analytics] 自訂事件會遵循此命名慣例： `custom_event_[*event #*]_[*Analytics report suite ID*]`.範例：`custom_event_16_examplersid`


例如，假設三個量度（交易屬性）與其中一個促銷活動中的特定套件相關：價值20美元的「PDF下載」、價值30美元的「電子郵件註冊」和價值40美元的「訂單確認」。 如果您想根據客戶動作的一次性貨幣值賦予權重，則屬性的相對權重會是1、2和1.5。

請參閱建立自訂目標的[最佳實務](custom-goal-best-practices.md)以取得如何設定自訂目標的秘訣。

在您[建立自訂目標](custom-goal-create.md)後，您就可以[將其指派給套件](/help/dsp/campaign-management/packages/package-settings.md)，以利用Adobe Sensei進行報表和演算法最佳化。

>[!MORELIKETHIS]
>
>* [建立自訂目標](custom-goal-create.md)
>* [建立自訂目標的最佳作法](custom-goal-best-practices.md)
>* [最佳化目標及其使用方式](optimization-goals.md)
>* [套件設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何最佳化您的行銷活動](optimization-how-dsp-optimizes-campaigns.md)

