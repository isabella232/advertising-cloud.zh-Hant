---
title: 使用 [!DNL Last Event Service] JavaScript程式庫搭配 [!DNL Web SDK]
description: 了解從使用 [!DNL Analytics] [!DNL visitorAPI] library to the [!DNL Experience Platform] [!DNL Web SDK] library for your [!DNL Analytics for Advertising Cloud] 實作。
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 966a7d64c0a2c1ce6d26ff25f6a57384e527625a
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# 使用 [!DNL Last Event Service] JavaScript程式庫與Adobe Experience Platform [!DNL Web SDK]

*僅具有Advertising Cloud-Adobe Analytics整合的廣告商*

如果貴組織使用舊版Adobe Analytics `visitorAPI.js` 資料收集程式庫，您可以選擇切換至使用 [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) 程式庫(`alloy.js`)，可讓您透過與各種Experience Cloud服務互動 [!DNL Edge Network].

此 [!DNL Analytics for Advertising Cloud] [!DNL Last Event Service] JavaScript程式庫原樣會記錄閱覽和點進事件，並使用補充ID將它們拼接至相關的轉換(`SDID`)。 此 [!DNL Web SDK] 不過，程式庫不提供 [!DNL stitch ID]. 若要使用 [!DNL Web SDK] for [!DNL Analytics for Advertising Cloud]，您需要修改1) [!DNL Last Event Service] 標籤，以及 [!DNL Web SDK] `sendEvent` 命令。

## 步驟1:編輯您的 [!DNL Last Event Service] 要產生的標籤 `[!DNL StitchID]`

在 [!DNL Analytics for Advertising Cloud] [!DNL Last Event Service] 標籤，新增程式碼以產生 `[!DNL StitchID]` 使用程式庫中隨附的隨機ID產生器。

**舊標籤：**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

**新標籤：**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

## 步驟2:使用 [!DNL Web SDK] 若要傳送 [!DNL StitchID] 作為的XDM資料 [!DNL Analytics]

在您的 [!DNL Web SDK] `sendEvent` 命令 [!DNL StitchID] to [!DNL Experience Edge] as [!DNL Experience Data Model] (XDM)資料 [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] 將使用值作為 `SDID`.

**要添加的屬性：**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**範例：**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [適用於 [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/javascript.md)

