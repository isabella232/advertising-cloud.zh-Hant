---
title: 複製套件
description: 了解如何複製套件。
feature: DSP Packages
exl-id: 4c37883f-5feb-4513-9573-ed4e32606132
source-git-commit: 5ed402a7c83072a7af6a06757050486c6d7d7080
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# 複製套件

複製套件以建立具有類似設定的套件。 您可以：

* 在原始廣告商和行銷活動內或不同廣告商內複製套件
* （可選）複製套件中的版位
* （適用於原始促銷活動內重複的套件）選擇性地複製原始廣告和版位層級事件像素
* 修改新包的投放日期

請參閱「[未重複的項目](#package-not-duplicated)「 」，以取得未複製的版位設定清單。

1. 在主功能表中，按一下 **[!UICONTROL Campaigns]**.
1. 按一下促銷活動的名稱以開啟 [!UICONTROL Packages] 檢視。
1. 在套件名稱旁，按一下  **[!UICONTROL ...]>[!UICONTROL Duplicate]**.
1. 指定新包設定：
   1. 輸入新包名。
   1. （選用）變更預設設定。

      依預設：

      * 新套件會指派給原始廣告商和促銷活動。
      * 新套件在當天開始作用。<!-- and the flight continues for NN  days. -->
      * 原始套件中的版位會複製到新套件。
      * 廣告和版位層級事件像素不會複製到新套件。
1. 按一下 **[!UICONTROL Submit]**.

## 未重複的項目 {#package-not-duplicated}

原始版位中的所有設定都會重複，但是：

* 實驗設定
* （如果您變更投放日期）自訂廣告排程
* （若未附加廣告）自訂廣告加權和排程
* 程式化保證(PG)交易的預設刊登版位和刊登版位 [!UICONTROL Simple Ad Serving] 交易
* （如果您將版位複製到不同的促銷活動）:
   * 地理目標
   * 事件像素
   * 廣告
   * 版位層級 [!DNL DoubleVerify Authentic Brand Safety] 區段（會覆寫廣告商層級的區段）

>[!MORELIKETHIS]
>
>* [關於套件管理](package-about.md)
>* [建立套件](package-create.md)
>* [編輯套件](package-edit.md)
>* [查看包的更改日誌](package-change-log.md)
>* [套件設定](package-settings.md)

