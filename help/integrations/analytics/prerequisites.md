---
title: 實施的先決條件和關鍵資訊 [!DNL Analytics for Advertising Cloud]
description: 實施的先決條件和關鍵資訊 [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 08e54e2b-ed9b-4489-8de5-ab1379b7133c
source-git-commit: 11a13816ccd2ef0c47efa615c54c0f7ce2f83734
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 實施的先決條件和關鍵資訊 [!DNL Analytics for Advertising Cloud]

*Advertising Cloud DSP和Advertising Cloud Search的廣告商*

在將Advertising Cloud與Adobe Analytics整合之前，請查看以下資訊。

## 在中報告Advertising Cloud資料的要求 [!DNL Analytics]

* 以下任一項：
   * Adobe Experience PlatformWeb SDK: `alloy.js`
   * Experience Cloud身份服務： `visitorAPI.js` 2.0版或更高版本
* 任何版本的Adobe Analytics(包括 [!DNL Prime]。 [!DNL Premium]或 [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` 版本2.1或更高版本

>[!TIP]
>
>要提高資料保真度，請使用每個庫的最新版本。

## 與Advertising Cloud共用分析段的要求

* Experience Cloud身份服務： `visitorAPI.js` 版本2.1或更高版本
* Adobe Analytics: `!DNL appMeasurement.js` 1.8版或更高版本

## 報告要求 [!DNL Analytics] Advertising Cloud資料

向Advertising Cloud實施小組提供以下資訊：

* 的 [!DNL Analytics] 報告套件ID，用於報告付費媒體活動和為優化和報告提供網站活動的Advertising Cloud
* 公司的Experience Cloud組織ID（組織ID）。

您可以在 [Adobe Experience Cloud調試器的「摘要」頁籤](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)。

![Experience Cloud Debugger摘要螢幕](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Advertising Cloud資料 {#lookback-a4adc}

因為 [!DNL Analytics] 資料被發送到Advertising Cloud以進行報告和優化，資料受屬性規則的約束，包括為Advertising Cloud的廣告商配置的印象和點擊回望窗口。

![Advertising Cloud廣告商級回望窗口設定](/help/integrations/assets/a4adc-lookbacks.png)

* Advertising Cloud屬性按一下回望窗口：第一次按一下後的天數，在該天數內，按一下可歸屬於轉換。 預設情況下，此值為60天；最多90天
* Advertising Cloud歸因印象回顧窗口：廣告印象後的天數，其中印象可歸因於轉換。 預設情況下，此值為14天；最多30天

   >[!NOTE]
   >
   > 後視窗是Advertising Cloud特有的，不是 [!DNL Analytics for Advertising Cloud]，報告。

的 [!DNL Analytics for Advertising Cloud] JavaScript使用這些設定來確定將瀏覽條目或點擊站點條目視為有效的時間。 有關如何確定視圖檢查和點擊檢查的詳細資訊，請參閱[Advertising Cloud分析使用的ID](ids.md)&quot;

## Advertising Cloud資料 [!DNL Analytics]

[!DNL Analytics] 在分析命中項內設定Advertising CloudID(AMO ID)，但受廣告商的eVar持久性設定的影響，該設定既適用於點擊提取又適用於查看提取。 持久性設定配置在Advertising Cloud後端，並且 [!DNL Adobe] 客戶團隊可以更改它。

* [!DNL Analytics for Advertising Cloud] eVar過期：預設情況下，AMO ID為60天

>[!NOTE]
>
>要將資料分段到不同的時間段，您可以 [設定自定義段](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) 在Analysis Workspace有不同的後視窗。

## 支援的廣告環境

* 搜索
* 顯示
* 視頻
* 線上視頻
* 本機

聯繫您 [!DNL Adobe] 客戶團隊，瞭解每個渠道中最新支援的廣告環境。

## 實施前要瞭解的事

* Advertising Cloud實施小組將建立整合。

* 此整合不會收取額外成本，伺服器調用也不會導致額外成本 [!DNL Analytics] 或Advertising Cloud費。

* [!DNL Analytics for Advertising Cloud] 與ad伺服器無關：任何ad伺服器都可能出現查看或點擊操作，並在站點條目時生成正確的ID。

* 僅整合通過 [!DNL Analytics] 訂活動，以優化隨後付費媒體及廣告工作。 它沒有通過 [!DNL Analytics] 分段、計算度量和eVars到Advertising Cloud以進行投標優化。

* Advertising Cloud在 [!DNL Analytics] 根據用戶進入網站之前按一下或查看的上一個廣告， [按一下並查看全視回望窗口](#lookback-a4adc) 配置在Advertising Cloud。 如果站點訪問者在其配置檔案中具有兩種類型的站點條目交互，並且按一下處於回望期內，則訪問者的點擊ID將覆蓋站點報告的查看ID。

* [!DNL Analytics for Advertising Cloud] Adobe Analytics的轉換跟蹤使用可配置的跟蹤回望窗口（預設為60天）。 Advertising Cloud的報告反映了站點轉換和在跟蹤回望窗口末尾的參與。

* 支援所有廣告類型。 但是，並非所有廣告環境都受支援。

   例如，由於CTV中不發生點擊，並且同一設備上不能進行轉換，因此無法跟蹤連接的TV(CTV)廣告。 但是，如果廣告在案頭環境中查看，則可能會跟蹤一些通過查看的站點條目資料。

* [!DNL Analytics] 轉換當前僅被跟蹤並被歸屬於同一設備上的訪問者。

* [!DNL Analytics for Advertising Cloud] 不支援應用程式內查看到轉換。

* 對於使用伺服器端轉發實現的廣告商，不支援直觀跟蹤 [!DNL Analytics]。

### 補充ID

為站點實施Experience Cloud身份服務後，將命中包含來自 [!DNL Analytics] 或Advertising Cloud包含補充ID。

示例： `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

為實現準確的資料整合， [!DNL Analytics for Advertising Cloud] 傳遞內容或記錄目標度量的活動必須具有相應的 [!DNL Analytics] 擊到共用相同的補充ID。

在中進行故障排除時 [!DNL Analytics]，確保確認是否有補充ID [!DNL Analytics] 擊中。 在 [Adobe Experience Cloud調試器](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)，您可以在「Advertising Cloud」頁籤中將此ID作為 `sdid` 的下界。

>[!NOTE]
>
> 此實施與 [!DNL Analytics for Target] 整合。

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [用於Advertising Cloud分析的JavaScript代碼](/help/integrations/analytics/javascript.md)

