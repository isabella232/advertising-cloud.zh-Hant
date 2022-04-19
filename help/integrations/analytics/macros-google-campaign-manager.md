---
title: 追加 [!DNL Analytics for Advertising Cloud] 宏到 [!DNL Google Campaign Manager 360] 廣告標籤
description: 瞭解添加原因和方法 [!DNL Analytics for Advertising Cloud] 宏 [!DNL Google Campaign Manager 360] ad標籤
feature: Integration with Adobe Analytics
source-git-commit: fe61dcd97d5509784a20bf8f68bea0ab2699dcfd
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# 追加 [!DNL Analytics for Advertising Cloud] 宏到 [!DNL Google Campaign Manager 360] 廣告標籤

*只有Advertising Cloud-Adobe Analytics整合的廣告商*

*僅適用於Advertising Cloud DSP*

如果使用廣告標籤 [!DNL Google Campaign Manager 360] 對於您的Advertising Cloud DSP廣告，使用 [`%p` 宏](https://support.google.com/campaignmanager/table/6096962)。 參數記錄 `s_kwcid` 和 `ef_id` 查詢登錄頁URL中的字串參數，使Advertising Cloud能夠將廣告的點擊資料發送到Adobe Analytics。

使用宏 [!DNL Campaign Manager 360] 以下類型的顯示和視頻廣告 [!DNL Analytics for Advertising Cloud] 實現：

* **廣告商 [!DNL Adobe] [!DNL Analytics for Advertising Cloud] 在其網站上實現的JavaScript代碼**:JavaScript代碼已記錄 `s_kwcid` 和 `ef_id` 查詢字串參數。 但是，當不支援第三方Cookie時，使用宏擴展了跟蹤以包括基於按一下的轉換。 最佳做法是將以下各節中的宏添加到廣告標籤中，以捕獲未通過JavaScript代碼捕獲的其他點擊式資料。

>[!NOTE]
>
>JavaScript代碼是僅在Cookie仍然可用時按一下跟蹤的解決方案。 一旦Cookie停止，就需要實施以下宏。

* **網站不使用廣告的廣告商 [!DNL Analytics for Advertising Cloud] JavaScript代碼，而是依賴 [!DNL Analytics] 伺服器端轉發僅用於點擊式資料** （沒有任何查看資料）:需要以下宏來報告您通過Advertising Cloud購買的廣告中的現場點擊活動。

## 將宏追加到 [!DNL Google Campaign Manager 360] 廣告

在 [!DNL Google Campaign Manager 360]，添加到登錄頁URL的以下參數： `%pamo=!;`

可以通過多種方式指定登錄頁URL。 以下子節中包含了每個選項的說明。

以下是帶尾碼的登錄頁URL的示例。

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>
>* 如果登錄頁URL包含不常見的散列符號(#)，則放置 `amo` 參數。
>* 如果在 `amo` 參數，然後在其後添加參數（例如，&amp;a=b）。 示例：`https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`


## 配置廣告商級登錄頁URL尾碼

1. 在主菜單中，按一下 [!UICONTROL Advertisers] 頁籤。
1. 按一下廣告商名稱。
1. 在 [!UICONTROL Landing page URL suffix] 設定，包括 `%pamo!;` 的 [!UICONTROL URL suffix] 的子菜單。

## 配置市場活動級別登錄頁URL尾碼

1. 在主菜單中，按一下 [!UICONTROL Campaigns] 頁籤。
1. 按一下市場活動名稱。
1. 按一下 [!UICONTROL Properties].
1. 在 [!UICONTROL Landing page URL suffix] 設定，包括 `%pamo!;` 的 [!UICONTROL URL suffix] 的子菜單。

## 配置創意級登錄頁URL尾碼

1. 在主菜單中，按一下 [!UICONTROL Campaigns] 頁籤。
1. 按一下市場活動名稱。
1. 在 [!UICONTROL Views] 菜單，選擇 [!UICONTROL Creatives]。
1. 按一下創作名稱。
1. 在 [!UICONTROL Click tags] 設定，包括 `%pamo!;` 的 [!UICONTROL Landing page] 的下界。

## 如何 [!DNL Analytics for Advertising Cloud] 宏在中展DSP開

在DSP中，建立包含 [!DNL Analytics for Advertising Cloud] 參數(`amo`) `ef_id` 和 `s_kwcid` 宏會自動附加到按一下的URL。 最佳做法是檢入標籤DSP以確保 `ef_id` 和 `s_kwcid` 宏存在。

以下是 [!DNL Google Campaign Manager 360] [ins標籤](https://support.google.com/campaignmanager/answer/6080468) 如所示DSP。

```
<ins class='dcmads' style='display:inline-block;width:160px;height:600px'
data-dcm-placement='N6482.2155306TUBEMOGUL/B23486129.261313631'
data-dcm-rendering-mode='iframe'
data-dcm-https-only
data-dcm-resettable-device-id=''
data-dcm-app-id='' data-dcm-click-tracker='${TM_CLICK_URL}'
data-dcm-param-amo='ef_id=${TM_USER_ID}:${TM_DATETIME}:d&s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}'>
<script src='https://www.googletagservices.com/dcm/dcmads.js'></script>
</ins>
```

當用戶點擊廣告時， [!DNL Google Campaign Manager 360] 看 `%pamo` 中，動態插入 `amo` 的雙曲餘切值。


>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising CloudID使用者 [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [追加 [!DNL Analytics for Advertising Cloud] 宏到 [!DNL Flashtalking] 廣告標籤](macros-flashtalking.md)

