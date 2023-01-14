---
title: 建立自訂目標的最佳作法
description: 了解建立自訂目標以定義成功事件的最佳實務。
feature: DSP Optimization, DSP Best Practices
exl-id: 54b16325-4b72-48a3-a2e0-4e342229211c
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# 建立自訂目標的最佳作法

## 具有單一屬性的自訂目標

下列範例說明如何設定以單一屬性（量度）為目標的目標。

### 具有「[!UICONTROL Highest ROAS - Custom Goal]&quot;最佳化目標

如果您的促銷活動目標是收入([!UICONTROL Highest ROAS - Custom Goal])，則您的自訂目標（目標）將包含「[!UICONTROL Revenue]」重量為一(1)的屬性。

![具有單一屬性的ROAS自訂目標範例](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] 相當於每個$1收入所追蹤的值為1。
>
> 例如，250美元的轉換（權重為1）會報告為$250。 如果轉換量度的權重為0.5，則$250的轉換在Adobe廣告中會報告為$125（$250的轉換* 0.5） [!UICONTROL Property Weight] = $125)。

### 具有「[!UICONTROL Lowest CPA - Custom Goal]&quot;最佳化目標

如果您的促銷活動目標是每次贏取(CPA)成本最低，而且只需要一個成功事件，則您會納入該個量度（在以下範例中為「應用程式提交」）。 最佳實務是將權重設為一(1)。

![單一屬性的CPA自訂目標範例](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] 等於每個追蹤轉換的值為1。
>
> 例如，如果追蹤了10個「應用程式提交」轉換，則會報告10個「應用程式提交」轉換。  如果轉換量度的加權為0.5，則10次轉換在Adobe廣告（10次轉換* 0.5）中會報告為五(5)次 [!UICONTROL Property Weight] = 5)。

## 具有多個屬性的自訂目標

在兩種情況下，您會在自訂目標中使用多個屬性：

* 您的促銷活動目標有多個成功事件。 例如，您可能是為了多個站上動作而做廣告，而且所有動作都歸因於您的CPA目標。 下列範例目標包含三個不同的屬性(PDF下載、聯絡我們和電子郵件註冊)，每個屬性的權重為一(1)，這會告訴 [!DNL Adobe Sensei] 每個屬性具有同等重要性的演算法。 如果您包含具有不同成本或重要性的屬性，則可以相應地調整其相對權重。

   ![具有多個屬性的自訂目標範例](/help/dsp/assets/custom-goal-multiple-properties.png)

* 自訂目標中的單一屬性未達到最佳化效能所需的每日至少10次轉換。 這可能是因為每日套件支出最少，或自然轉換次數有限。 新增其他支援屬性至自訂目標，可協助您達到每天10次轉換的臨界值。 即使每個重量都低於一(1)，十個支援事件仍可協助套件達到10/天臨界值。 但您可能不需要新增這麼多事件。

   將支援屬性新增至自訂目標時，請根據其對主要成功事件的相對重要性來加以加權，並記住資料點的數量。 這可讓Adobe Sensei演算法平衡多個屬性，並針對您的目標進行最佳化。

   下列範例目標包含三個屬性，每個屬性的權重不同：應用程式提交= 1，應用程式開始= 0.1，廣告商登陸頁面= 0.01。這表示每個應用程式提交轉換對您的業務具有與平均10個應用程式開始轉換和100個廣告商登陸頁面轉換相同的值。

   ![具有多個屬性的自訂目標範例](/help/dsp/assets/custom-goal-multiple-properties2.png)

   相反地，如果您對應用程式提交的著陸頁面瀏覽次數加權平均，則自然較高的著陸頁面瀏覽次數可能會壓倒您的目標，並扭曲至著陸頁面瀏覽次數。<!--reword-->

>[!MORELIKETHIS]
>
>* [關於自訂目標](custom-goal-about.md)
>* [建立自訂目標](custom-goal-create.md)
>* [最佳化目標及其使用方式](optimization-goals.md)
>* [套件設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP如何最佳化您的行銷活動](optimization-how-dsp-optimizes-campaigns.md)

