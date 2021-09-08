---
title: ' [!DNL Analytics] 和Advertising Cloud之間的預期資料差異'
description: ' [!DNL Analytics] 和Advertising Cloud之間的預期資料差異'
feature: Integration with Adobe Analytics
exl-id: 34685e04-d4f9-4e27-b83e-b56164244b2b
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '3285'
ht-degree: 0%

---

# [!DNL Analytics]和Advertising Cloud之間的預期資料差異

*僅具有Advertising Cloud-Adobe Analytics整合的廣告商*

具有[!DNL Analytics for Advertising Cloud] <!-- (A4AdC) -->整合的廣告商會透過Advertising Cloud和Adobe Analytics追蹤付費廣告。 當您透過多個系統追蹤媒體、行銷活動和管道時，來自不同系統的相同資料集很少會完全相符。 本檔案說明如何預期透過Advertising Cloud傳輸的媒體資料，與[!DNL Analytics]內追蹤媒體的不同系統中的資料進行比較。

>[!NOTE]
>
>本檔案的重點在於Advertising Cloud和Analytics，但許多關鍵點也可轉讓至其他追蹤解決方案。

## 類似報表中的歸因差異

### 可能不同的回顧期間和歸因模型

[!DNL Analytics for Advertising Cloud]整合使用兩個變數（eVar或rVars \[保留eVars]\）來擷取[EF ID和AMO ID](ids.md)。 這些變數的設定是單一回顧期間（點進和閱覽歸因的時間）和歸因模型。 除非另有指定，否則變數的設定將會與Advertising Cloud中的預設廣告商層級點按回顧期間和歸因模型相符。

不過，回顧期間和歸因模型可在Analytics（透過eVar）和Advertising Cloud中設定。 此外，在Advertising Cloud中，歸因模型不僅可在廣告商層級（針對競標最佳化）設定，也可在個別資料檢視和報表中設定（僅供報表使用）。 例如，組織可能偏好使用偶數分配歸因模型來進行最佳化，但對Advertising Cloud DSP或[!DNL Search]中的報表使用上次接觸歸因。 變更歸因模型會變更歸因轉換的數量。

如果一個產品修改了報表回顧期間或歸因模型，而另一個產品修改了，則來自每個系統的相同報表會顯示不同的資料：

* **不同回顧期間所造成差異的範例：**

   假設Advertising Cloud有60天的點擊回顧期間，而[!DNL Analytics]有30天的回顧期間。 假設某個使用者透過Advertising Cloud追蹤的廣告來到網站，離開，然後在第45天返回並轉換。 Advertising Cloud會將轉換歸因於初次造訪，因為轉換發生在60天回顧期間內。 [!DNL Analytics]，但無法將轉換歸因於初始造訪，因為轉換發生在30天回顧期間過期之後。在此範例中，Advertising Cloud會報告比[!DNL Analytics]更高的轉換數。

   ![在Advertising Cloud中歸因於但非的轉換範例  [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **不同歸因模型造成差異的範例：**

   假設使用者在轉換前與三個不同的Advertising Cloud廣告互動，轉換類型為收入。 如果Advertising Cloud報表使用偶數分配模型進行歸因，則會平均歸因所有廣告的收入。 不過，如果[!DNL Analytics]使用上次接觸歸因模型，則會將收入歸因於上次廣告。 在下列範例中，Advertising Cloud會將擷取到的30美元收入中的30美元歸因為偶數10美元，而[!DNL Analytics]將全部30美元收入歸因於使用者最後看到的廣告。 比較Advertising Cloud和[!DNL Analytics]的報表時，您會發現歸因差異的影響。

   ![歸因於Advertising Cloud的不同收入， [!DNL Analytics] 且根據不同的歸因模型](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>最佳實務是在Advertising Cloud和[!DNL Analytics]中使用相同的回顧期間和歸因模型。 視需要與您的Adobe客戶經理合作，識別目前的設定並保持設定同步。

這些相同概念適用於使用不同回顧期間或歸因模型的任何其他類似管道。

#### 檢視追蹤的不同回顧期間 {#impression-lookback}

在Advertising Cloud中，歸因是根據點按和曝光數，您可以針對點按和曝光數設定不同的回顧期間。 但在[!DNL Analytics]中，歸因是以點進次數和閱覽為基礎，且您沒有選項可針對點進次數和閱覽設定不同的歸因視窗；每個開始的追蹤。 曝光次數可能會在瀏覽發生的同一天或多天前發生，而這可能會影響歸因視窗在每個系統中的開始位置。

通常，大部分的閱覽轉換發生得足夠快，使得兩個系統都能歸因評分。 不過，有些轉換可能發生在Advertising Cloud曝光回顧期間之外，但發生在[!DNL Analytics]回顧期間內；這類轉換會歸因於[!DNL Analytics]中的閱覽，而非Advertising Cloud中的曝光。

在下列範例中，假設訪客在第1天收到廣告，在第2天執行閱覽造訪（亦即，未先按一下廣告就瀏覽了廣告的登陸頁面），並在第45天轉換。 在此情況下，Advertising Cloud會從第1天到第14天（使用14天回顧）追蹤使用者，[!DNL Analytics]會從第2天到第61天（使用60天回顧）追蹤使用者，而第45天的轉換將歸因於[!DNL Analytics]內的廣告，但不屬於Advertising Cloud。

![歸因於(而非Advertising Cloud)的閱覽 [!DNL Analytics] 轉換範例](/help/integrations/assets/a4adc-viewthrough-example.png)

不一致的另一個原因，是在Advertising Cloud中，您可以指派自訂&#x200B;*閱覽權數*&#x200B;來自點按式轉換的權數。 預設的閱覽權數為40%，這表示閱覽轉換計為點按式轉換值的40%。 [!DNL Analytics] 不提供檢視轉換的這種加權。因此，例如，如果您使用預設的閱覽權數，在[!DNL Analytics]中擷取的100美元收入訂單將折現為40美元，差值為60美元。

比較Advertising Cloud和[!DNL Analytics]報表之間的閱覽轉換時，請考量這些差異。

#### 可用歸因模型

| Advertising Cloud歸因 | [!DNL Analytics] 歸因 | eVar/rVar配置 |
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
>對於線性配置，[!DNL Analytics]會將成功事件平均歸因於單一造訪中的所有eVar值，因此請搭配「造訪」的eVar過期時間使用線性配置。 不過，對於廣告，使用線性歸因會導致配置並非真正線性，且會導致報表不理想。 例如，如果訪客在三個不同的瀏覽中轉換前，先與三個廣告互動，則只有上次瀏覽中看到的廣告會歸因於轉換，而非全部三個廣告。
>
>此外，將轉換配置切換為「線性」或從「線性」切換時，不會顯示歷史資料，而這可能會導致報表中的資料錯誤陳述。 例如，線性配置可能會將收入除以數個不同的eVar值。 如果您將配置變更為「最近」，則該收入的100%會與最近的單一值產生關聯。 這種關聯會導致你得出錯誤的結論。
>
>為避免混淆，[!DNL Analytics]會使報表介面中的歷史資料無法使用。 如果您將eVar變更回初始配置設定，則可以檢視歷史資料，但您不應僅為了存取歷史資料而變更eVar配置設定。 Adobe建議，當您想要對已記錄的資料套用新的配置設定時，不要變更已具有大量歷史資料之eVar的配置設定，應使用新的eVar。

請參閱[https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html)中的[!DNL Analytics]歸因模型及其定義清單。

如果您已登入Advertising Cloud，可在
[https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)。

#### Advertising Cloud中的事件日期歸因

在Advertising Cloud中，您可以依相關的點按日期/事件日期（點按或曝光事件的日期）或交易日期（轉換日期）來報告轉換資料。 [!DNL Analytics]中不存在點按/事件日期報告的概念；[!DNL Analytics]中追蹤的所有轉換都會依交易日期報告。 因此，在Advertising Cloud和[!DNL Analytics]中，可能會以不同日期報告相同的轉換。 例如，假設使用者在1月1日點按廣告，並在1月5日轉換。 如果您是在Advertising Cloud中依事件日期檢視轉換資料，則轉換將在1月1日（發生點按時）報告。 在[!DNL Analytics]中，將於1月5日報告相同的轉換。

![歸因於不同日期的轉換範例](/help/integrations/assets/a4adc-conversions-based-on.png)

## [!DNL Analytics Marketing Channels]中的歸因

[[!DNL Analytics Marketing Channels] ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html) 報表可讓您設定規則，以根據點擊資訊的不同方面來識別不同的行銷管道。您可以使用`ef_id`查詢字串參數來識別通道，將Advertising Cloud追蹤的通道（[!UICONTROL Display Click Through]、[!UICONTROL Display View Through]及[!UICONTROL Paid Search]）追蹤為[!DNL Marketing Channels]。 <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> 不過，即使報表可 [!DNL Marketing Channels] 以追蹤Advertising Cloud管道，資料仍可能因數原因不符合Advertising Cloud報表。如需詳細資訊，請參閱下列章節。

>[!NOTE]
>
> 下列核心概念也適用於任何涉及未在Advertising Cloud中追蹤之促銷活動的多管道追蹤，例如[`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html)變數(也稱為「追蹤代碼」Dimension或「eVar0」)和自訂eVar追蹤。

### [!DNL Marketing Channels]中可能不同的歸因模型

大部分的[!DNL Marketing Channels]報表都以[!UICONTROL Last Touch]歸因進行設定，系統會將上次偵測到的行銷管道指派100%的轉換值。 對[!DNL Marketing Channels]報表和Advertising Cloud報表使用不同的歸因模型，將導致歸因轉換中的差異。

### [!DNL Marketing Channels]中可能不同的回顧期間

可自訂[!DNL Marketing Channels]的回顧期間。 在Advertising Cloud中，雖然固定的60天視窗很常見，但點擊回顧視窗仍可設定。 如果這兩種產品使用不同的回顧期間，您可能會發現資料不一致。

### [!DNL Marketing Channels]中的不同管道歸因

Advertising Cloud報表只會擷取透過Advertising Cloud流量的付費媒體(Advertising Cloud Search廣告的付費搜尋，以及Advertising Cloud DSP廣告的顯示)，而[!DNL Marketing Channels]報表可追蹤所有數位頻道。 這可能會導致轉換歸屬的管道不一致。

例如，付費搜尋和免費搜尋管道通常具有共生關係，而每個管道會互相協助。 [!DNL Marketing Channels]報表會將部分轉換歸因於Advertising Cloud不會追蹤免費搜尋的自然搜尋。

也可以考慮檢視顯示廣告、點按付費搜尋廣告、點按電子郵件訊息內部，然後下30美元訂單的客戶。 即使Advertising Cloud和[!DNL Marketing Channels]都使用上次接觸歸因模型，轉換的歸因仍會不同。 Advertising Cloud無權存取[!UICONTROL Email]管道，因此會將轉換的付費搜尋評為評分。 [!DNL Marketing Channels]但是，卻可存取所有三個管道，因此會評 [!UICONTROL Email] 分轉換。

![Advertising Cloud和  [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

如需量度可能有所差異的詳細說明，請參閱「[為何管道資料可能在Advertising Cloud和 [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md)之間變更」。

## Adobe Analytics中的資料差異[!DNL Paid Search Detection]

[!DNL Analytics]中的[legacy [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html)功能可讓公司[定義規則，以追蹤指定搜尋引擎的付費和有機搜尋流量](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html)。 [!DNL Paid Search Detection]規則會同時使用查詢字串和反向連結網域來識別付費和免費搜尋流量。 [!DNL Paid Search Detection]報表是較大[尋找方法](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html)報表群組的一部分，該群組會在指定事件（例如購物車結帳）發生時或瀏覽結束時到期。

建立[!DNL Paid Search Detection]規則集的介面如下：

![付費搜尋偵測規則集的範例，位於  [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

產生的[!DNL Paid Search Detection]報表包括[!UICONTROL Paid Search Engine]、[!UICONTROL Paid Search Keywords]、[!UICONTROL Natural Search Engine]和[!UICONTROL Natural Search Keywords]報表。

請注意[!DNL Paid Search Detection]報表中資料的下列兩項限制：

* [!UICONTROL Paid Search Keywords]和[!UICONTROL Natural Search Keywords]報表會顯示由反向連結URL所識別的搜尋查詢，而非使用者競標的關鍵字。 Advertising Cloud和[!DNL Analytics]報表會顯示實際的關鍵字，因此請勿期望它們與[!DNL Paid Search Detection]關鍵字報表一致。

* 最初建立[!DNL Paid Search Detection]功能時，原始搜尋查詢（使用者在搜尋引擎的搜尋列中輸入的字元字串）可透過反向連結URL更容易供廣告商使用。 如今，搜尋引擎在很大程度上模糊化了搜尋查詢，而[!DNL Paid Search Detection]關鍵字報表的值有限，因為大多數查詢資料都屬於「未指定」。

   透過[!DNL Analytics for Advertising Cloud]，廣告商仍可追蹤[!DNL Analytics]中的付費關鍵字。 反向連結網域會通知引擎報告哪個搜尋引擎帶動了流量。 由於廣告商專屬的帳戶資訊未系結至反向連結網域，因此所有流量都會列在搜尋引擎下。 在相同搜尋引擎中具有多個帳戶的廣告商，應參考Advertising Cloud或[!DNL Analytics]報表，以取得帳戶特定報表。

### 為何配置[!DNL Paid Search Detection]?

[!DNL Paid Search Detection]報表可讓您識別[[!DNL Analytics Marketing Channels] 報表](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html)中的免費搜尋流量。 區隔付費搜尋流量與免費搜尋流量是了解免費搜尋為完整行銷生態系統帶來價值的絕佳方式。

## [!DNL Analytics for Advertising Cloud]的點進資料驗證 {#data-validation}

針對您的整合，您應驗證點進資料，以確定您網站上的所有頁面都正確追蹤點進次數。

在[!DNL Analytics]中，驗證[!DNL Analytics for Advertising Cloud]追蹤的最簡單方式之一，是使用「點按AMO ID例項」計算量度來比較例項的點按次數，計算方式如下：

```Clicks to AMO ID Instances = (AMO ID Instances / AMO Clicks)```

[!UICONTROL AMO ID Instances] 代表網站上追蹤AMO ID(`s_kwcid` 參數)的次數。每次點按廣告時，都會將`s_kwcid`參數新增至登陸頁面URL。 因此，[!UICONTROL AMO ID Instances]的數量類似於點按次數，可根據實際廣告點按加以驗證。 我們通常會看到[!DNL Search]的80%符合率和[!DNL DSP]流量的30%符合率（篩選為僅包含點進[!UICONTROL AMO ID Instances]時）。 搜尋和顯示之間的期望差異可透過預期的流量行為來解釋。 搜尋會擷取目的，因此，使用者通常會從其查詢點選搜尋結果。 但是，看到顯示或線上視訊廣告的使用者更有可能無意中點按廣告，然後從網站跳出或放棄在追蹤頁面活動之前載入的新視窗。

在Advertising Cloud報表中，您也可以以類似方式比較使用「[!UICONTROL ef_id_instances]」量度（而非[!UICONTROL AMO ID Instances]）的例項的點按次數：

```Clicks to [!UICONTROL EF ID Instances] = (ef_id_instances / Clicks)```

雖然AMO ID與EF ID之間的匹配率應較高，但請勿預期100%的同位比，因為AMO ID與EF ID基本上會追蹤不同的資料，而此差異可能會導致總[!UICONTROL AMO ID Instances]和[!UICONTROL EF ID Instances]中的細微差異。 如果[!DNL Analytics]中的總計[!UICONTROL AMO ID Instances]與Advertising Cloud中的[!UICONTROL EF ID Instances]差異超過1%，請聯絡您的Adobe客戶經理以取得協助。

如需AMO ID和EF ID的詳細資訊，請參閱[Analytics使用的Advertising Cloud ID](ids.md)。

以下是追蹤例項點按次數的工作區範例。

![追蹤例項點按次數的工作區範例](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## 比較[!DNL Analytics for Advertising Cloud]中的資料集與Advertising Cloud中的資料集

[AMO ID](ids.md)（s_kwcid查詢字串參數）用於[!DNL Analytics]中的報表，而[EF ID](ids.md)則用於Advertising Cloud中的報表。 因為它們是不同的值，因此一個值可能已損毀或未新增至登錄頁面。

例如，假設我們有下列登陸頁面：

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id`

其中EF ID為「`test_ef_id`」，而AMO ID為「`test_amo_id`」。

如果發生網站端重新導向，URL的結果可能會如下：

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag`

其中EF ID為「`test_ef_id`」，而AMO ID為「`test_amo_id#redirectAnchorTag`」。

在此範例中，新增錨點標籤會在AMO ID中新增非預期的字元，導致Analytics無法辨識的值。 此AMO ID不會進行分類，因此與其相關聯的轉換會落在[!DNL Analytics]報表中的「[!UICONTROL unspecified]」或「[!UICONTROL none]」下。

幸運的是，雖然這類問題很常見，但通常不會導致高比例的差異。 不過，若您發現[!DNL Analytics]中的AMO ID與Advertising Cloud中的EF ID之間出現大量不一致，請聯絡您的Adobe客戶經理以取得協助。

## 其他量度考量事項

### 點按和造訪之間的差異 {#clicks-vs-visits}

它們看起來類似，但點按和造訪代表不同的資料：

* **點按：** [!DNL DSP] ，或當訪客點按發佈商網站上的廣告時，搜尋引擎會記錄點按。

* **造訪：** [!DNL Analytics] 定義使 [](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) 用者對一系列頁面檢視的造訪，根據數個條件之一（例如閒置30分鐘）結束。

根據定義，按一下可導致多次造訪。

請考量下列範例：使用者1和使用者2都可按一下Advertising Cloud廣告來存取網站。 使用者1檢視了4個頁面，然後離開當天，因此初次點按會產生一次造訪。 用戶2瀏覽了兩頁，離開45分鐘的午餐，返回，再瀏覽兩頁，然後離開；在此情況下，初次點按會產生兩次造訪。

![點按和造訪之間差異的範例](/help/integrations/assets/a4adc-visits-example.png)

### 點進次數與點進次數之間的差異

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

點進次數和點進次數是兩種不同的量度：

* **點按：** [!DNL DSP] ，或當訪客點按發佈商網站上的廣告時，搜尋引擎會記錄點按。

* **點進次數：** [!DNL Analytics] 會記錄訪客登陸目的地網站時的點進、登陸頁面載入，而 [!DNL Analytics] 頁面底部的要求會將資料傳送至 [!DNL Analytics]。

點進次數和點進次數可能會因為意外廣告點進而大不相同。 我們觀察到，顯示廣告上的大多數點按是意外點按，而這些意外訪客在登陸頁面載入前點擊了「上一步」按鈕，因此[!DNL Analytics]無法記錄點進。 對於意外點按較可能發生的廣告，例如行動廣告、視訊廣告和廣告，這些廣告會填滿螢幕，且必須在使用者檢視頁面之前先關閉，這個情況尤為常見。

在行動裝置上載入的網站也不太可能導致點進，因為頻寬或可用的處理能力較低，導致載入登錄頁面的時間較長。 50%至70%的點按不會導致點進，這種情況並不罕見。 在行動環境中，由於瀏覽器速度較慢，加上使用者在捲動頁面或嘗試關閉廣告時意外點按廣告的可能性較高，差異可能高達90%。

點進資料也可能記錄在無法透過目前追蹤機制（例如進入或從行動應用程式點進）記錄點進，或廣告商僅部署一種追蹤方法（例如使用閱覽JavaScript方法，封鎖第三方Cookie的瀏覽器會追蹤點進，但不會追蹤點進）的環境中。 Adobe建議同時部署點按URL追蹤和閱覽JavaScript追蹤方法的一個主要原因，是為了將可追蹤點進的涵蓋範圍最大化。

### 將Advertising Cloud流量量度用於非Advertising CloudDimension

Advertising Cloud提供DSP和Search的[廣告專用流量量度及相關維度。 ](advertising-cloud-metrics-in-analytics.md)Advertising Cloud提供的量度僅適用於指定的Advertising Cloud維度，且資料無法用於[!DNL Analytics]中的其他維度。

例如，如果您依帳戶檢視[!UICONTROL AMO Clicks]和[!UICONTROL AMO Cost]量度(此為Advertising Cloud維度)，則會依帳戶查看總計[!UICONTROL AMO Clicks]和[!UICONTROL AMO Cost]。

![使用Advertising Cloud維度的報表中的Advertising Cloud量度範例](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

不過，如果您依頁面維度（例如Page）檢視[!UICONTROL AMO Clicks]和[!UICONTROL AMO Cost]量度(Advertising Cloud未針對其提供資料)，則每個頁面的[!UICONTROL AMO Clicks]和[!UICONTROL AMO Cost]將為零(0)。

![使用不支援維度的報表中Advertising Cloud量度範例](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### 使用[!UICONTROL AMO ID Instances]取代非Advertising CloudDimension的點按

由於您無法對站上維度使用[!UICONTROL AMO Clicks]，因此您可能想要找到與點按相同的值。 您可能會忍不住使用造訪作為替代，但並非最佳選項，因為每個訪客可能有多次造訪。 (請參閱「[點按與造訪之間的差異](#clicks-vs-visits)」。 建議您改為使用[!UICONTROL AMO ID Instances]，即為AMO ID被擷取的次數。 雖然[!UICONTROL AMO ID Instances]不會完全符合[!UICONTROL AMO Clicks]，但它們是測量網站點擊流量的最佳選項。 如需詳細資訊，請參閱「[ [!DNL Analytics for Advertising Cloud]](#data-validation)的資料驗證」。

![不支 [!UICONTROL AMO ID Instances] 援維 [!UICONTROL AMO Clicks] 度的範例](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [概觀 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud使用的ID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Advertising CloudAnalysis Workspace量度](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Advertising Cloud中的資料](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)
>* [為何Advertising Cloud和 [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)

