---
title: 之間的預期資料差異 [!DNL Analytics] 和Adobe廣告
description: 之間的預期資料差異 [!DNL Analytics] 和Adobe廣告
feature: Integration with Adobe Analytics
exl-id: 34685e04-d4f9-4e27-b83e-b56164244b2b
source-git-commit: 17482b831c5db7ef6c211f87b2e408443180746e
workflow-type: tm+mt
source-wordcount: '3278'
ht-degree: 0%

---

# 之間的預期資料差異 [!DNL Analytics] 和Adobe廣告

*廣告商與Adobe廣告 — 僅Adobe Analytics整合*

廣告商與 [!DNL Analytics for Advertising] <!-- (A4AdC) --> 整合可透過Adobe廣告和Adobe Analytics追蹤付費廣告。 當您透過多個系統追蹤媒體、行銷活動和管道時，來自不同系統的相同資料集很少會完全相符。 本檔案說明如何預期透過Adobe廣告販運的媒體的資料，會與追蹤媒體的不同系統中的資料進行比較 [!DNL Analytics].

>[!NOTE]
>
>本檔案著重於Adobe廣告和Analytics，但許多關鍵點也可轉讓至其他追蹤解決方案。

## 類似報表中的歸因差異

### 可能不同的回顧期間和歸因模型

此 [!DNL Analytics for Advertising] 整合使用兩個變數（eVar或rVars \[保留eVars]\）來擷取 [EF ID和AMO ID](ids.md). 這些變數的設定會包含單一回顧期間（點進和閱覽歸因的時間）和歸因模型。 除非另有指定，否則變數的設定將會與「Adobe廣告」中的預設廣告商層級點按回顧期間和歸因模型相符。

不過，回顧期間和歸因模型可在Analytics（透過eVar）和Adobe廣告中設定。 此外，在「Adobe廣告」中，歸因模型不僅可在廣告商層級（針對競標最佳化）設定，也可在個別資料檢視與報表（僅用於報表用途）中設定。 例如，組織可能偏好使用偶數分配歸因模型來進行最佳化，但對Advertising DSP或 [!DNL Advertising Search]. 變更歸因模型會變更歸因轉換的數量。

如果一個產品修改了報表回顧期間或歸因模型，而另一個產品修改了，則來自每個系統的相同報表會顯示不同的資料：

* **不同回顧期間所造成差異的範例：**

   假設Adobe廣告有60天的點按回顧期間，且 [!DNL Analytics] 有30天的回顧期間。 假設某個使用者透過Adobe廣告追蹤的廣告來到網站，離開，然後在第45天返回並轉換。 Adobe廣告會將轉換歸因於初次造訪，因為轉換發生在60天回顧期間內。 [!DNL Analytics]，但無法將轉換歸因於初始造訪，因為轉換發生在30天回顧期間過期之後。 在此範例中，Adobe廣告會報告比 [!DNL Analytics] 會的。

   ![Adobe廣告中屬於但非的轉換範例 [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **不同歸因模型造成差異的範例：**

   假設使用者在轉換前與三個不同的Adobe廣告互動，其中收入為轉換類型。 如果「Adobe廣告」報表使用偶數分配模型來歸因，則會平均歸因所有廣告的收入。 若 [!DNL Analytics] 不過，會使用上次接觸歸因模型，然後將收入歸因於上次廣告。 在下列範例中，「Adobe廣告」會將擷取到這三個廣告的30美元收入中的10美元歸因，但 [!DNL Analytics] 將全部30美元的收入歸因於使用者最後一次看到的廣告。 比較來自Adobe廣告的報表時， [!DNL Analytics]，您就會預期歸因差異的影響。

   ![來自Adobe之不同收入廣告及 [!DNL Analytics] 根據不同的歸因模型](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>最佳實務是在Adobe廣告和 [!DNL Analytics]. 與您的 [!DNL Adobe] 帳戶團隊，以識別目前的設定並保持設定同步。

這些相同概念適用於使用不同回顧期間或歸因模型的任何其他類似管道。

#### 檢視追蹤的不同回顧期間 {#impression-lookback}

在Adobe廣告中，歸因是根據點擊次數和曝光次數，您可以針對點擊次數和曝光次數設定不同的回顧期間。 在 [!DNL Analytics]但是，歸因是以點進次數和閱覽為基礎，且您無法針對點進次數和閱覽設定不同的歸因視窗；每個開始的追蹤。 曝光次數可能會在瀏覽發生的同一天或多天前發生，而這可能會影響歸因視窗在每個系統中的開始位置。

通常，大部分的閱覽轉換發生得足夠快，使得兩個系統都能歸因評分。 不過，某些轉換可能發生在Adobe廣告曝光回顧期間之外，但發生在 [!DNL Analytics] 回顧期間；這些轉換會歸因於 [!DNL Analytics] 但Adobe廣告中的印象則並非如此。

在下列範例中，假設訪客在第1天獲得廣告，在第2天執行閱覽造訪（亦即，未先按一下廣告即已造訪廣告的登陸頁面），並在第45天轉換。 在此情況下，Adobe廣告會追蹤從第1天到第14天（使用14天回顧）的使用者， [!DNL Analytics] 會追蹤從2天到61天（使用60天回顧）的使用者，而第45天的轉換會歸因於 [!DNL Analytics] 但不在Adobe廣告內。

![中歸因的檢視轉換範例 [!DNL Analytics] 但不Adobe廣告](/help/integrations/assets/a4adc-viewthrough-example.png)

不一致的另一個原因，是在Adobe廣告中，您可以指派閱覽轉換自訂 *檢視權數* 這相對於點按式轉換的權數。 預設的閱覽權數為40%，這表示閱覽轉換計為點按式轉換值的40%。 [!DNL Analytics] 不提供檢視轉換的這種加權。 例如，100美元的收入訂單 [!DNL Analytics] 如果您使用預設的檢視權數（差異為60美元），則「Adobe廣告」會貼現為40美元。

比較Adobe廣告和 [!DNL Analytics] 報表。

#### 可用歸因模型

| Adobe廣告歸因 | [!DNL Analytics] 歸因 | eVar/rVar配置 |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | n/a | n/a |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>別用* |
| [!UICONTROL Weight Last Event More] | n/a | n/a |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | n/a |
| n/a | [!UICONTROL J-Shaped] | n/a |
| n/a | [!UICONTROL Inverse-J] | n/a |
| n/a | [!UICONTROL Custom] | n/a |
| n/a | [!UICONTROL Participation] | n/a |
| n/a | [!UICONTROL Algorithmic] | n/a |

>[!NOTE]
>
>若為線性配置， [!DNL Analytics] 將成功事件平均歸因於單次造訪中的所有eVar值，因此請搭配「造訪」的eVar過期時間使用線性配置。 不過，對於廣告，使用線性歸因會導致配置並非真正線性，且會導致報表不理想。 例如，如果訪客在三個不同的瀏覽中轉換前，先與三個廣告互動，則只有上次瀏覽中看到的廣告會歸因於轉換，而非全部三個廣告。
>
>此外，將轉換配置切換為「線性」或從「線性」切換時，不會顯示歷史資料，而這可能會導致報表中的資料錯誤陳述。 例如，線性配置可能會將收入除以數個不同的eVar值。 如果您將配置變更為「最近」，則該收入的100%會與最近的單一值產生關聯。 這種關聯會導致你得出錯誤的結論。
>
>為了避免混淆， [!DNL Analytics] 使歷史資料無法在報表介面中使用。 如果您將eVar變更回初始配置設定，則可以檢視歷史資料，但您不應僅為了存取歷史資料而變更eVar配置設定。 Adobe建議，當您想要對已記錄的資料套用新的配置設定時，不要變更已具有大量歷史資料之eVar的配置設定，應使用新的eVar。

查看 [!DNL Analytics] 歸因模型及其定義 [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

如果您已登入 [!DNL Search]，您可以在
[https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm).

#### Adobe廣告中的事件日期歸因

在「Adobe廣告」中，您可以依相關的點按日期/事件日期（點按或曝光事件的日期）或交易日期（轉換日期）來報告轉換資料。 中不存在點按/事件日期報表的概念 [!DNL Analytics];追蹤的所有轉換 [!DNL Analytics] 按交易日期報告。 因此，相同的轉換可能會以不同的日期報告於Adobe廣告和 [!DNL Analytics]. 例如，假設使用者在1月1日點按廣告，並在1月5日轉換。 如果您是在「Adobe廣告」中依事件日期檢視轉換資料，則轉換將在1月1日發生點按時報告。 在 [!DNL Analytics]，則相同的轉換將於1月5日報告。

![歸因於不同日期的轉換範例](/help/integrations/assets/a4adc-conversions-based-on.png)

## 歸因於 [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] 報告](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) 可讓您設定規則，以根據點擊資訊的不同方面來識別不同的行銷管道。 您可以追蹤Adobe廣告追蹤的頻道([!UICONTROL Display Click Through], [!UICONTROL Display View Through]，和 [!UICONTROL Paid Search])作為 [!DNL Marketing Channels] 使用 `ef_id` 查詢字串參數以識別管道。 <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> 然而，即使 [!DNL Marketing Channels] 報表可以追蹤Adobe廣告管道，但資料可能因數原因不符合Adobe廣告報表。 如需詳細資訊，請參閱下列章節。

>[!NOTE]
>
> 下列核心概念也適用於任何涉及「Adobe廣告」中未追蹤之促銷活動的多管道追蹤，例如 [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) 變數(也稱為「追蹤程式碼」Dimension或「eVar0」)和自訂eVar追蹤。

### 中可能不同的歸因模型 [!DNL Marketing Channels]

最多 [!DNL Marketing Channels] 報表的設定方式為 [!UICONTROL Last Touch] 歸因，系統會將上次偵測到的行銷管道100%的轉換值指派給該歸因。 針對 [!DNL Marketing Channels] 報表和Adobe廣告報表會導致歸因轉換中的差異。

### 中可能不同的回顧期間 [!DNL Marketing Channels]

的回顧期間 [!DNL Marketing Channels] 可自訂。 在「Adobe廣告」中，雖然固定的60天視窗很常見，但點擊回顧視窗仍可設定。 如果這兩種產品使用不同的回顧期間，您可能會發現資料不一致。

### 中的不同管道歸因 [!DNL Marketing Channels]

Adobe廣告報表只會擷取透過Adobe廣告(付費搜尋， [!DNL Advertising Search] 廣告和顯示廣告)，而 [!DNL Marketing Channels] 報表可追蹤所有數位頻道。 這可能會導致轉換歸屬的管道不一致。

例如，付費搜尋和免費搜尋管道通常具有共生關係，而每個管道會互相協助。 此 [!DNL Marketing Channels] 報表會將部分轉換歸因於「Adobe廣告」不會進行的免費搜尋，因為它不追蹤免費搜尋。

也可以考慮檢視顯示廣告、點按付費搜尋廣告、點按電子郵件訊息內部，然後下30美元訂單的客戶。 即使Adobe廣告和 [!DNL Marketing Channels] 兩者都使用上次接觸歸因模型，轉換的歸因仍會不同。 Adobe廣告無法存取 [!UICONTROL Email] 管道，因此會評分轉換的付費搜尋。 [!DNL Marketing Channels]但是，卻可存取所有這三個管道，因此會評分 [!UICONTROL Email] 的上界。

![Adobe廣告中不同轉換歸因的範例，與 [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

如需量度可能有所差異的詳細說明，請參閱[為何Adobe廣告和 [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md).&quot;

## Adobe Analytics中的資料差異 [!DNL Paid Search Detection]

此 [舊版 [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) 功能 [!DNL Analytics] 允許公司 [定義追蹤付費和有機搜尋流量的規則](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) 的URL。 此 [!DNL Paid Search Detection] 規則會同時使用查詢字串和反向連結網域來識別付費和免費搜尋流量。 此 [!DNL Paid Search Detection] 報表是 [尋找方法](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) 報表，此報表會在指定事件（例如購物車結帳）發生時或瀏覽結束時到期。

以下是建立 [!DNL Paid Search Detection] 規則集：

![付費搜尋偵測規則集的範例，位於 [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

產生的 [!DNL Paid Search Detection] 報表包括 [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine]，和 [!UICONTROL Natural Search Keywords] 報表。

請注意以下兩個資料限制： [!DNL Paid Search Detection] 報表：

* 此 [!UICONTROL Paid Search Keywords] 和 [!UICONTROL Natural Search Keywords] 報表顯示由反向連結URL所識別的搜尋查詢，而非使用者競標的關鍵字。 Adobe廣告和 [!DNL Analytics] 報表會顯示實際關鍵字，因此請勿期望它們與 [!DNL Paid Search Detection] 關鍵字報表。

* 當 [!DNL Paid Search Detection] 最初建立的功能時，原始搜尋查詢（使用者在搜尋引擎的搜尋列中輸入的字元字串）更容易透過反向連結URL供廣告商使用。 如今，搜尋引擎在很大程度上會模糊化搜尋查詢和 [!DNL Paid Search Detection] 關鍵字報表的值有限，因為大多數查詢資料都屬於「未指定」。

   使用 [!DNL Analytics for Advertising]，廣告商仍可追蹤 [!DNL Analytics]. 反向連結網域會通知引擎報告哪個搜尋引擎帶動了流量。 由於廣告商專屬的帳戶資訊未系結至反向連結網域，因此所有流量都會列在搜尋引擎下。 在相同搜尋引擎中具有多個帳戶的廣告商，應指Adobe廣告或 [!DNL Analytics] 針對帳戶特定報表的報表。

### 為何配置 [!DNL Paid Search Detection]?

此 [!DNL Paid Search Detection] 報表可讓您識別 [[!DNL Analytics Marketing Channels] 報告](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). 區隔付費搜尋流量與免費搜尋流量是了解免費搜尋為完整行銷生態系統帶來價值的絕佳方式。

## 點進資料驗證 [!DNL Analytics for Advertising] {#data-validation}

針對您的整合，您應驗證點進資料，以確定您網站上的所有頁面都正確追蹤點進次數。

在 [!DNL Analytics]，是驗證的最簡單方法之一 [!DNL Analytics for Advertising] 追蹤是使用「點按AMO ID例項」計算量度來比較例項的點按次數，計算方式如下：

```Clicks to AMO ID Instances = (AMO ID Instances / AMO Clicks)```

[!UICONTROL AMO ID Instances] 代表AMO ID的次數(`s_kwcid` 參數)。 每次點按廣告時， `s_kwcid` 參數會新增至登陸頁面URL。 數量 [!UICONTROL AMO ID Instances]，因此類似於點按次數，可根據實際廣告點按加以驗證。 我們通常會看到 [!DNL Search] 和30%的匹配率 [!DNL DSP] 流量（篩選為僅包含點進時） [!UICONTROL AMO ID Instances])。 搜尋和顯示之間的期望差異可透過預期的流量行為來解釋。 搜尋會擷取目的，因此，使用者通常會從其查詢點選搜尋結果。 但是，看到顯示或線上視訊廣告的使用者更有可能無意中點按廣告，然後從網站跳出或放棄在追蹤頁面活動之前載入的新視窗。

在「Adobe廣告」報表中，您也可以使用「[!UICONTROL ef_id_instances]「 」量度而非 [!UICONTROL AMO ID Instances]:

```Clicks to [!UICONTROL EF ID Instances] = (ef_id_instances / Clicks)```

雖然AMO ID與EF ID之間的匹配率應該很高，但是不要期望100%的對等性，因為AMO ID與EF ID基本上會追蹤不同的資料，而這種差異可能會導致總數的細微差異 [!UICONTROL AMO ID Instances] 和 [!UICONTROL EF ID Instances]. 若總計 [!UICONTROL AMO ID Instances] in [!DNL Analytics] 不同於 [!UICONTROL EF ID Instances] 在Adobe廣告中的比例超過1%，但請連絡您的 [!DNL Adobe] 客戶團隊尋求協助。

如需AMO ID和EF ID的詳細資訊，請參閱 [AdobeAnalytics使用的Advertising ID](ids.md).

以下是追蹤例項點按次數的工作區範例。

![追蹤例項點按次數的工作區範例](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## 比較中的資料集 [!DNL Analytics for Advertising] 與Adobe廣告的比較

此 [AMO ID](ids.md) （s_kwcid查詢字串參數）用於 [!DNL Analytics]，和 [EF ID](ids.md) 用於Adobe廣告中的報告。 因為它們是不同的值，因此一個值可能已損毀或未新增至登錄頁面。

例如，假設我們有下列登陸頁面：

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id`

其中EF ID為「`test_ef_id`&quot;，而AMO ID為&quot;`test_amo_id`.&quot;

如果發生網站端重新導向，URL的結果可能會如下：

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag`

其中EF ID為「`test_ef_id`&quot;，而AMO ID為&quot;`test_amo_id#redirectAnchorTag`.&quot;

在此範例中，新增錨點標籤會在AMO ID中新增非預期的字元，導致Analytics無法辨識的值。 此AMO ID不會進行分類，因此與其相關聯的轉換會落在「[!UICONTROL unspecified]&quot;或&quot;[!UICONTROL none]在 [!DNL Analytics] 報表。

幸運的是，雖然這類問題很常見，但通常不會導致高比例的差異。 不過，若您發現 [!DNL Analytics] 和Adobe廣告中的EF ID，請連絡您的 [!DNL Adobe] 客戶團隊尋求協助。

## 其他量度考量事項

### 點按和造訪之間的差異 {#clicks-vs-visits}

它們看起來類似，但點按和造訪代表不同的資料：

* **按一下：** [!DNL DSP] 或者，當訪客點按發佈商網站上的廣告時，搜尋引擎會記錄點按。

* **瀏覽：** [!DNL Analytics] 定義 [造訪](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) 以使用者的一系列頁面檢視結束，會根據數個條件之一，例如30分鐘的閒置時間。

根據定義，按一下可導致多次造訪。

請考量下列範例：使用者1和使用者2都可按一下Adobe廣告來存取網站。 使用者1檢視了4個頁面，然後離開當天，因此初次點按會產生一次造訪。 用戶2次瀏覽2頁，45分鐘的午餐休息，返回，再瀏覽2頁，然後離開；在此情況下，初次點按會產生兩次造訪。

![點按和造訪之間差異的範例](/help/integrations/assets/a4adc-visits-example.png)

### 點進次數與點進次數之間的差異

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

點進次數和點進次數是兩種不同的量度：

* **按一下：** [!DNL DSP] 或者，當訪客點按發佈商網站上的廣告時，搜尋引擎會記錄點按。

* **點進次數：** [!DNL Analytics] 當訪客登陸目的地網站、登陸頁面載入，以及 [!DNL Analytics] 頁面底部的要求會將資料傳送至 [!DNL Analytics].

點進次數和點進次數可能會因為意外廣告點進而大不相同。 我們觀察到，顯示廣告上的大多數點按是意外點按，而這些意外訪客在登陸頁面載入前點擊了「上一步」按鈕，因此 [!DNL Analytics] 無法記錄點進。 對於意外點按較可能發生的廣告，例如行動廣告、視訊廣告和廣告，這些廣告會填滿螢幕，且必須在使用者檢視頁面之前先關閉，這個情況尤為常見。

在行動裝置上載入的網站也不太可能導致點進，因為頻寬或可用的處理能力較低，導致載入登錄頁面的時間較長。 50%至70%的點按不會導致點進，這種情況並不罕見。 在行動環境中，由於瀏覽器速度較慢，加上使用者在捲動頁面或嘗試關閉廣告時意外點按廣告的可能性較高，差異可能高達90%。

點進資料也可能記錄在無法透過目前追蹤機制（例如進入或從行動應用程式點進）記錄點進，或廣告商僅部署一種追蹤方法（例如使用閱覽JavaScript方法，封鎖第三方Cookie的瀏覽器會追蹤點進，但不會追蹤點進）的環境中。 Adobe建議同時部署點按URL追蹤和閱覽JavaScript追蹤方法的一個主要原因，是為了將可追蹤點進的涵蓋範圍最大化。

### 將Adobe廣告流量量度用於非Adobe廣告Dimension

Adobe廣告為Analytics提供 [DSP和[!DNL]中廣告專用的流量量度及相關維度 [!DNL Search]]](advertising-metrics-in-analytics.md). 由Adobe廣告提供的量度僅適用於指定的Adobe廣告維度，而且資料不適用於 [!DNL Analytics].

例如，如果您檢視 [!UICONTROL AMO Clicks] 和 [!UICONTROL AMO Cost] 「依帳戶」的量度(此為「Adobe廣告」維度)，您就會看到總計 [!UICONTROL AMO Clicks] 和 [!UICONTROL AMO Cost] 帳戶。

![使用Adobe廣告維度的報表中的Adobe廣告量度範例](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

不過，如果您檢視 [!UICONTROL AMO Clicks] 和 [!UICONTROL AMO Cost] 量度（例如「頁面」），而AdobeAdvertising未提供資料的維度，則 [!UICONTROL AMO Clicks] 和 [!UICONTROL AMO Cost] 每個頁面的值將為零(0)。

![使用不支援的維度的報表Adobe廣告量度範例](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### 使用 [!UICONTROL AMO ID Instances] 取代非Adobe廣告Dimension的點按

因為您無法使用 [!UICONTROL AMO Clicks] 若使用站上維度，您可能會想要找到與點按相同的值。 您可能會忍不住使用造訪作為替代，但並非最佳選項，因為每個訪客可能有多次造訪。 (請參閱「[點按和造訪之間的差異](#clicks-vs-visits).&quot; 建議改為使用 [!UICONTROL AMO ID Instances]，即為AMO ID被擷取的次數。 同時 [!UICONTROL AMO ID Instances] 不符合 [!UICONTROL AMO Clicks] 確切地說，這是測量網站上點按流量的最佳選項。 如需詳細資訊，請參閱[資料驗證 [!DNL Analytics for Advertising]](#data-validation).&quot;

![範例 [!UICONTROL AMO ID Instances] 而非 [!UICONTROL AMO Clicks] 針對不支援的維度](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising]](overview.md)
>* [Adobe廣告ID：使用者 [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [AdobeAnalysis Workspace中的Advertising量度](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe廣告中的資料](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [為何Adobe廣告和 [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)

