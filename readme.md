---
source-git-commit: d3e36cef27fce533e9435717d428d54b982fd427
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---
# Advertising Cloud的協作檔案

這是Adobe Advertising Cloud的檔案存放庫，包括跨產品、DSP和電視檔案。 （稍後將提供創意與搜尋的檔案）。

**注意：此頁面未發佈在面向客戶的檔案中。**

## 目錄

+ `TOC.md` 位於任何使用手冊的根目錄，提供手冊中所包含主題的組織。
+ 每個使用手冊都有一個唯一的`TOC.md`，您可以視需要排序所有頁面/主題。


## 使用手冊

+ 使用手冊的簡介稱為`overview.md`
+ 使用手冊中的每個主題都有各自的不同目錄。
   + 如果指南中有一個名為&#x200B;*Implementation*&#x200B;的主題，則相應目錄為`/implementation`
+ 所有影像資產都儲存在使用手冊根目錄的`/assets`中。
   + `/assets`目錄中的所有影像都將本地化。
   + `/no-localize`目錄中的任何影像都不會翻譯（令人驚訝！）。 這可用來確保在loc版本中特定資產不會不必要地重現。

## 使用手冊層級中繼資料

+ 描述使用手冊的元資料儲存在`TOC.md`中。 這包括：
   + 產品 — 產品/功能名稱。
   + 雲端 — 此產品所屬的雲端。
   + 對象 — 指南鎖定目標的對象或原型。
   + 使用手冊 — 使用手冊名稱。

## 頁面層級中繼資料

+ 說明檔案所需的中繼資料會儲存為每個個別頁面的一部分。 這包括：
   + 標題 — 頁面標題
   + 說明 — 頁面說明
   + seo-title - seo替代標題
   + seo-description - SEO用途的替代標題
   + short-title — （可選欄位）
   + 索引 — 是/否 — 頁面是否會根據Adobe的搜尋平台編列索引
   + 翻譯 — 是/否 — 此頁面是否會翻譯
   + 測試版 — 此產品是否為測試版？
   + 重新導向 — 可視需要用來建立新頁面的參照
   + doc-type:參考（預設）/疑難排解/開發人員/教學課程/ kb /白皮書

## 更多資訊

如需更多發佈指示、樣式指南、範例和其他資源，請參閱：

+ [特別為Advertising Cloud **貢獻作者准則**](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=EfficientFrontier&amp;title=Contributing+Author+Guidelines+for+Advertising+Cloud+Help)
+ [為所有Adobe撰寫人員協作編寫](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/home.html)

另請參閱：

+ contributing.md如何協助撰寫本說明檔案的概述。

<!-- * guidelines.md For an overview on what is expected in contributions and how to compose your documentation contributions. -->
+ code-of-conduct.md我們期望在您貢獻本說明檔案專案時的行為標準概述。
