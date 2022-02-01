---
title: 預期資料差異 [!DNL Analytics] 和Advertising Cloud
description: 預期資料差異 [!DNL Analytics] 和Advertising Cloud
feature: Integration with Adobe Analytics
exl-id: 34685e04-d4f9-4e27-b83e-b56164244b2b
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '3282'
ht-degree: 0%

---

# 預期資料差異 [!DNL Analytics] 和Advertising Cloud

*只有Advertising Cloud-Adobe Analytics整合的廣告商*

廣告商 [!DNL Analytics for Advertising Cloud] <!-- (A4AdC) --> 整合跟蹤通過Advertising Cloud和Adobe Analytics的付費廣告。 當您通過多個系統跟蹤媒體、活動和渠道時，來自不同系統的相同資料集很少完全匹配。 本文檔說明了您如何期望通過Advertising Cloud傳輸的介質與跟蹤介質的不同系統中的資料進行比較 [!DNL Analytics]。

>[!NOTE]
>
>本文檔主要針對Advertising Cloud和分析，但許多關鍵點也可轉移到其他跟蹤解決方案。

## 類似報告的歸因差異

### 可能不同的回望窗口和屬性模型

的 [!DNL Analytics for Advertising Cloud] 整合使用兩個變數（eVars或rVars \[保留的eVars]\）捕獲 [EF ID和AMO ID](ids.md)。 這些變數配置有單個回望窗口（將點擊檢查和查看檢查被歸屬的時間）和一個屬性模型。 除非另有指定，否則這些變數將配置為與Advertising Cloud的預設廣告商級按一下回望窗口和屬性模型相匹配。

但是，在分析（通過eVars）和Advertising Cloud，都可配置回望窗口和屬性模型。 此外，在Advertising Cloud，不僅可在廣告商級別（用於投標優化）配置該歸屬模型，而且可在單個資料視圖和報告（僅用於報告目的）內配置。 例如，組織可能更願意使用均勻分配屬性模型進行優化，但對Advertising Cloud DSP或 [!DNL Search]。 更改屬性模型會更改屬性轉換的數量。

如果在一個產品中修改了報告回望窗口或屬性模型，而在另一個產品中修改了，則來自每個系統的相同報告將顯示不同的資料：

* **不同回望窗口導致差異的示例：**

   假設Advertising Cloud有一個60天的點擊回望窗口 [!DNL Analytics] 有30天的回望窗口。 假設一個用戶通過一個Advertising Cloud追蹤的廣告來到網站，離開，然後在第45天返回，然後轉信。 Advertising Cloud將將轉換屬於初次訪問，因為轉換發生在60天回望窗口內。 [!DNL Analytics]但是，無法將轉換屬性化為初始訪問，因為轉換發生在30天回望窗口過期之後。 在此示例中，Advertising Cloud報告的轉換數比 [!DNL Analytics] 會的。

   ![屬於Advertising Cloud但不屬於的轉換示例 [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **不同屬性模型導致差異的示例：**

   假設用戶在轉換前與三個不同的Advertising Cloud廣告交互，並將收入作為轉換類型。 如果Advertising Cloud的報告使用均勻分佈模型來分配，那麼它將在所有廣告中均勻地分配收入。 如果 [!DNL Analytics] 然而，使用最後一個觸摸屬性模型，則將收益歸結於最後一個廣告。 在下例中，Advertising Cloud將30美元收入中的10美元歸於三個廣告中的每一個，而 [!DNL Analytics] 將所有30 USD的收入屬性為用戶看到的最後一個廣告。 當你比較Advertising Cloud和 [!DNL Analytics]你可以看到不同歸因的影響。

   ![歸屬於Advertising Cloud及 [!DNL Analytics] 基於不同的屬性模型](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>最佳做法是在Advertising Cloud和 [!DNL Analytics]。 與 [!DNL Adobe] 帳戶組（根據需要），以確定當前設定並保持配置同步。

這些相同的概念適用於使用不同回望窗口或屬性模型的任何其它類似通道。

#### 不同的查看跟蹤窗口 {#impression-lookback}

在Advertising Cloud，根據點擊和觀感進行歸屬，您可以配置不同的點擊和觀感回視窗口。 在 [!DNL Analytics]但是，屬性是基於點擊瀏覽和視圖瀏覽的，並且您沒有選擇為點擊瀏覽和視圖瀏覽設定不同的屬性窗口；在初始站點訪問時開始跟蹤每個站點。 在進行查看之前的同一天或多天可能會產生一種印象，這可能會影響每個系統中屬性窗口的開始位置。

通常，大多數直觀轉換發生得足夠快，以至於兩個系統都屬於信用。 然而，某些轉換可能發生在Advertising Cloud印象回望窗口之外，但發生在 [!DNL Analytics] 後視窗；此轉換歸因於 [!DNL Analytics] 但Advertising Cloud的印象卻並非如此。

在以下示例中，假設訪問者在第1天收到廣告，在第2天執行瀏覽訪問（即，訪問廣告登錄頁而不先按一下廣告），然後在第45天轉換。 在這種情況下，Advertising Cloud將從第1天到第14天（使用14天的回望）跟蹤用戶， [!DNL Analytics] 將從第2天到第61天（使用60天的回顧）跟蹤用戶，第45天的轉換將歸因於廣告 [!DNL Analytics] 但不在Advertising Cloud。

![屬於的直觀轉換示例 [!DNL Analytics] 但Advertising Cloud](/help/integrations/assets/a4adc-viewthrough-example.png)

出現差異的另一個原因是，在Advertising Cloud，您可以為自定義 *透視權重* 與基於按一下的轉換所屬的權重相關。 預設的「查看」權重為40%，這意味著「查看」轉換被計為基於按一下的轉換值的40%。 [!DNL Analytics] 不提供視圖轉換的這種加權。 例如，一個100美元的收入訂單 [!DNL Analytics] 如果您使用預設查看權重，則在Advertising Cloud將折現為40美元 — 差60美元。

在比較Advertising Cloud和 [!DNL Analytics] 報告。

#### 可用屬性模型

| Advertising Cloud歸因 | [!DNL Analytics] 歸因 | eVar/風險分配 |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | n/a | n/a |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>不要使用* |
| [!UICONTROL Weight Last Event More] | n/a | n/a |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | n/a |
| n/a | [!UICONTROL J-Shaped] | n/a |
| n/a | [!UICONTROL Inverse-J] | n/a |
| n/a | [!UICONTROL Custom] | n/a |
| n/a | [!UICONTROL Participation] | n/a |
| n/a | [!UICONTROL Algorithmic] | n/a |

>[!NOTE]
>
>對於線性分配， [!DNL Analytics] 將成功事件在單個訪問中的所有eVar值中均等地屬性，因此使用「訪問」eVar到期時的線性分配。 但是，對廣告來說，使用線性屬性會導致分配不是真正的線性，並導致報告不理想。 例如，如果訪問者在進行三次單獨訪問之前與三個廣告進行交互，則只有上次訪問時看到的廣告被歸因於轉換，而不是全部三個廣告。
>
>此外，將轉換分配切換到或從「線性」防止顯示歷史資料，這可能導致報告中資料陳述錯誤。 例如，線性分配可能會將收入劃分為多個不同的eVar值。 如果將分配更改為「最近」，則100%的收入將與最近的單個值相關聯。 這種關聯會導致您得出錯誤的結論。
>
>為了防止混亂， [!DNL Analytics] 使歷史資料在報告介面中不可用。 如果將eVar更改回初始分配設定，則可以查看歷史資料，儘管您不應僅僅為了訪問歷史資料而更改eVar分配設定。 Adobe建議在要為已記錄的資料應用新分配設定時使用新eVar，而不是更改已具有大量歷史資料的eVar的分配設定。

請參閱 [!DNL Analytics] 歸屬模型及其定義 [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html)。

如果您登錄Advertising Cloud，可以在
[https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)。

#### Advertising Cloud事件日期歸屬

在Advertising Cloud，您可以按關聯的按一下日期/事件日期（按一下或印象事件的日期）或按事務處理日期（轉換日期）報告轉換資料。 中不存在按一下/事件日期報告的概念 [!DNL Analytics];跟蹤的所有轉換 [!DNL Analytics] 按交易記錄日期報告。 因此，同樣的轉換可以在Advertising Cloud和 [!DNL Analytics]。 例如，考慮在1月1日按一下廣告並在1月5日轉換廣告的用戶。 如果按Advertising Cloud事件日期查看轉換資料，則轉換將在1月1日按一下時報告。 在 [!DNL Analytics]1月5日將報告相同的轉換。

![屬於不同日期的轉換實例](/help/integrations/assets/a4adc-conversions-based-on.png)

## 在 [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] 報告](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html) 允許您配置規則以根據擊中資訊的不同方面來識別不同的市場營銷渠道。 您可以跟蹤Advertising Cloud跟蹤頻道([!UICONTROL Display Click Through]。 [!UICONTROL Display View Through], [!UICONTROL Paid Search]) [!DNL Marketing Channels] 使用 `ef_id` 查詢字串參數以標識通道。 <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> 然而，儘管 [!DNL Marketing Channels] 報告可以跟蹤Advertising Cloud頻道，資料可能與Advertising Cloud報告不符，原因有幾。 有關詳細資訊，請參閱以下各節。

>[!NOTE]
>
> 以下核心概念也適用於任何涉及未在Advertising Cloud跟蹤的活動的多渠道跟蹤，如 [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) 變數(也稱為「跟蹤代碼」Dimension或「eVar0」)和自定義eVar跟蹤。

### 可能不同的歸因模型 [!DNL Marketing Channels]

最多 [!DNL Marketing Channels] 報告配置為 [!UICONTROL Last Touch] 屬性，為其分配100%的轉換值，最後檢測到的營銷渠道。 使用不同的屬性模型 [!DNL Marketing Channels] 報告和Advertising Cloud報告將導致屬性轉換的差異。

### 中可能不同的回望窗口 [!DNL Marketing Channels]

用於 [!DNL Marketing Channels] 可以定制。 在Advertising Cloud，按一下回望窗口是可配置的，但固定60天窗口是常見的。 如果這兩種產品使用不同的回望窗口，則您可能會發現資料差異。

### 不同通道屬性 [!DNL Marketing Channels]

Advertising Cloud報導僅捕獲通過Advertising Cloud販運的付費媒體(以付費方式搜索Advertising Cloud Search廣告和展示Advertising Cloud DSP廣告)，而 [!DNL Marketing Channels] 報告可以跟蹤所有數字通道。 這可能導致轉換所屬的渠道出現差異。

例如，付費搜索和自然搜索通道往往具有共生關係，每個通道互相協助。 的 [!DNL Marketing Channels] 報告會將一些轉換歸結於自然搜索，而Advertising Cloud不會，因為它不跟蹤自然搜索。

再考慮一下查看顯示廣告、按一下付費搜索廣告、在電子郵件內按一下，然後下30美元訂單的客戶。 即使Advertising Cloud和 [!DNL Marketing Channels] 兩者都使用最後一個觸摸歸屬模型，轉換的屬性仍然不同。 Advertising Cloud沒有 [!UICONTROL Email] channel，因此它將對轉換進行付費搜索。 [!DNL Marketing Channels]但是，它可以進入所有三個渠道，因此它會 [!UICONTROL Email] 的子菜單。

![Advertising Cloud不同轉化歸因實例 [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

有關度量可能不同的原因的詳細說明，請參見「[為什麼通道資料會因Advertising Cloud和 [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md)&quot;

## Adobe Analytics的資料差異 [!DNL Paid Search Detection]

的 [舊 [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html) 特徵 [!DNL Analytics] 允許公司 [定義跟蹤付費和有機搜索流量的規則](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) 指定的搜索引擎。 的 [!DNL Paid Search Detection] 規則使用查詢字串和引用域來標識付費和自然搜索流量。 的 [!DNL Paid Search Detection] 報告是 [查找方法](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) 報告，在指定事件（如Cart Checkout）發生或訪問結束時過期。

以下是建立 [!DNL Paid Search Detection] 規則集：

![中的付費搜索檢測規則集的示例 [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

結果 [!DNL Paid Search Detection] 報告包括 [!UICONTROL Paid Search Engine]。 [!UICONTROL Paid Search Keywords]。 [!UICONTROL Natural Search Engine], [!UICONTROL Natural Search Keywords] 報告。

請注意以下兩個限制，其中的資料 [!DNL Paid Search Detection] 報告：

* 的 [!UICONTROL Paid Search Keywords] 和 [!UICONTROL Natural Search Keywords] 報告顯示由引用URL標識的搜索查詢，而不是用戶出價的關鍵字。 Advertising Cloud [!DNL Analytics] 報告顯示實際關鍵字，因此不要期望它們與 [!DNL Paid Search Detection] 關鍵字報告。

* 當 [!DNL Paid Search Detection] 最初建立了特徵，原始搜索查詢（用戶輸入到搜索引擎搜索欄中的字串）通過參考URL更容易地提供給廣告商。 如今，搜索引擎在很大程度上模糊了搜索查詢， [!DNL Paid Search Detection] 關鍵字報告的值有限，因為大多數查詢資料都屬於「未指定」。

   與 [!DNL Analytics for Advertising Cloud]廣告商仍然可以跟蹤付費關鍵字 [!DNL Analytics]。 所述參考域通知引擎報告哪個搜索引擎驅動了所述業務。 由於廣告商特定帳戶資訊不與參考域相關，所以所有通信都列在搜索引擎下。 在同一搜索引擎中具有多個帳戶的廣告主應參考Advertising Cloud或 [!DNL Analytics] 針對特定於帳戶的報告進行報告。

### 為什麼配置 [!DNL Paid Search Detection]?

的 [!DNL Paid Search Detection] 報告允許您識別自然搜索通信 [[!DNL Analytics Marketing Channels] 報告](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html)。 將付費搜索流量與自然搜索流量分開，是理解自然搜索給整個營銷生態系統帶來的價值的絕佳途徑。

## 點擊式資料驗證 [!DNL Analytics for Advertising Cloud] {#data-validation}

對於您的整合，您應驗證您的點擊資料，以確保站點上的所有頁面都正確跟蹤點擊瀏覽。

在 [!DNL Analytics]，驗證的最簡單方法之一 [!DNL Analytics for Advertising Cloud] 跟蹤是使用「按一下到AMO ID Instances」計算度量將按一下與實例進行比較，該度量按如下計算：

```Clicks to AMO ID Instances = (AMO ID Instances / AMO Clicks)```

[!UICONTROL AMO ID Instances] 表示AMO ID的次數(`s_kwcid` 參數)。 每次點擊廣告， `s_kwcid` 參數將添加到登錄頁URL。 數 [!UICONTROL AMO ID Instances]因此，它與點擊次數類似，可以根據實際廣告點擊進行驗證。 我們通常會看到80%的匹配率 [!DNL Search] 和30%的匹配率 [!DNL DSP] 流量(過濾後僅包括按一下 [!UICONTROL AMO ID Instances])。 搜索和顯示之間的期望值差異可以通過預期的通信行為來解釋。 搜索捕獲目的，因此用戶通常打算按一下其查詢中的搜索結果。 但是，看到顯示或線上視頻廣告的用戶更有可能無意中點擊該廣告，然後從站點退出，或放棄在跟蹤頁面活動之前載入的新窗口。

在Advertising Cloud報告中，您同樣可以將按一下與使用「 」[!UICONTROL ef_id_instances]&quot;度量而不是 [!UICONTROL AMO ID Instances]:

```Clicks to [!UICONTROL EF ID Instances] = (ef_id_instances / Clicks)```

雖然您應該期望AMO ID和EF ID之間的匹配率較高，但不要期望100%奇偶校驗，因為AMO ID和EF ID從根本上跟蹤不同的資料，而這種差異可能導致總資料的細微差異 [!UICONTROL AMO ID Instances] 和 [!UICONTROL EF ID Instances]。 如果總 [!UICONTROL AMO ID Instances] 在 [!DNL Analytics] 不同 [!UICONTROL EF ID Instances] 但是，在Advertising Cloud，超過1%的人會聯繫您 [!DNL Adobe] 客戶團隊提供幫助。

有關AMO ID和EF ID的詳細資訊，請參見 [Advertising Cloud分析使用的ID](ids.md)。

下面是一個工作區的示例，用於跟蹤對實例的按一下。

![跟蹤對實例的按一下的工作區示例](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## 比較中的資料集 [!DNL Analytics for Advertising Cloud] VSAdvertising Cloud

的 [AMO ID](ids.md) （s_kwcid查詢字串參數）用於報告 [!DNL Analytics]的 [EF ID](ids.md) 用於Advertising Cloud報導。 因為它們是不同的值，所以可能有一個值被損壞或未添加到登錄頁。

例如，假設我們有以下登錄頁：

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id`

其中EF ID為&quot;`test_ef_id`&quot;和AMO ID為&quot;`test_amo_id`&quot;

如果發生站點端重定向，則URL可能會以下方式結束：

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag`

其中EF ID為&quot;`test_ef_id`&quot;和AMO ID為&quot;`test_amo_id#redirectAnchorTag`&quot;

在本示例中，添加錨點標籤會向AMO ID添加意外字元，導致Analytics無法識別的值。 此AMO ID不會被分類，與其關聯的轉換將屬於「」[!UICONTROL unspecified]&quot;或&quot;[!UICONTROL none]&quot; [!DNL Analytics] 報告。

幸運的是，儘管這類問題很常見，但通常不會導致高比例的差異。 但是，如果您注意到中的AMO ID之間存在很大差異 [!DNL Analytics] 和Advertising Cloud的EF ID聯繫 [!DNL Adobe] 客戶團隊提供幫助。

## 其他度量注意事項

### 點擊與訪問的區別 {#clicks-vs-visits}

它們看起來很類似，但點擊和訪問代表著不同的資料：

* **按一下：** [!DNL DSP] 或者，當訪問者點擊發佈者網站上的廣告時，搜索引擎會記錄點擊。

* **訪問：** [!DNL Analytics] 定義 [訪問](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) 作為用戶的一系列頁面視圖，根據以下幾個條件之一結束，例如30分鐘的不活動。

從定義上講，點擊可能導致多次訪問。

請考慮以下示例：用戶1和用戶2都通過按一下Advertising Cloud廣告訪問站點。 用戶1查看四頁，然後離開一天，因此初始按一下將導致一次訪問。 用戶2查看兩頁，離開45分鐘午餐，返回，再查看兩頁，然後離開；在這種情況下，初始按一下會導致兩次訪問。

![點擊和訪問之間差異的示例](/help/integrations/assets/a4adc-visits-example.png)

### 點擊與點擊的區別

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

點擊和點通是兩種不同的度量：

* **按一下：** [!DNL DSP] 或者，當訪問者點擊發佈者網站上的廣告時，搜索引擎會記錄點擊。

* **點通：** [!DNL Analytics] 當訪問者到達目標網站、登錄頁載入和 [!DNL Analytics] 頁面底部的請求將資料發送到 [!DNL Analytics]。

點擊和點擊免提可能因廣告的意外點擊而有很大不同。 我們注意到，顯示廣告上的大多數點擊都是偶然的點擊，這些偶然的訪問者在登錄頁載入之前點擊了「後退」按鈕，因此 [!DNL Analytics] 無法記錄點擊。 對於意外點擊的可能性更大的廣告尤其如此，例如移動廣告、視頻廣告和廣告，這些廣告填充了螢幕，在用戶查看頁面之前必須關閉。

在移動設備上載入的站點也不太可能導致點擊穿越，因為頻寬較低或可用的處理能力較低，導致載入登錄頁的時間更長。 50%到70%的點擊率不會導致點擊免檢的情況並不少見。 在移動環境中，差異可能高達90%，因為瀏覽器速度較慢，而且用戶在瀏覽頁面或嘗試關閉廣告時意外點擊廣告的可能性較高。

點擊資料也可以記錄在無法使用當前跟蹤機制（例如進入或從移動應用的點擊）記錄點擊瀏覽的環境中，或廣告商只部署了一種跟蹤方法（例如，使用通過查看的JavaScript方法，阻止第三方cookie的瀏覽器將跟蹤點擊，但不會跟蹤點擊瀏覽）。 Adobe建議同時部署點擊URL跟蹤和通過JavaScript查看跟蹤方法的一個關鍵原因是最大化可跟蹤點擊瀏覽的覆蓋範圍。

### 將Advertising Cloud流量指標用於非Advertising CloudDimension

Advertising Cloud提供分析 [廣告特定的流量指標以及來自和搜索的DSP相關維](advertising-cloud-metrics-in-analytics.md)。 Advertising Cloud提供的指標僅適用於指定的Advertising Cloud維，資料不適用於 [!DNL Analytics]。

例如，如果您查看 [!UICONTROL AMO Clicks] 和 [!UICONTROL AMO Cost] 按帳戶列出的度量(即Advertising Cloud維)，您將看到 [!UICONTROL AMO Clicks] 和 [!UICONTROL AMO Cost] 按帳戶。

![使用Advertising Cloud維的報告中的Advertising Cloud度量示例](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

但是，如果您查看 [!UICONTROL AMO Clicks] 和 [!UICONTROL AMO Cost] 按頁維（如頁）(Advertising Cloud不提供資料)的度量，然後 [!UICONTROL AMO Clicks] 和 [!UICONTROL AMO Cost] 每頁將為零(0)。

![使用不支援的維度的報告中的Advertising Cloud度量示例](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### 使用 [!UICONTROL AMO ID Instances] 用非Advertising CloudDimension代替點擊

因為你不能 [!UICONTROL AMO Clicks] 使用現場維度時，您可能希望找到與按一下相同的內容。 你可能會忍不住想用「訪問」來代替「訪問」，但它們不是最佳選擇，因為每個訪問者可能有多次訪問。 (請參閱「[點擊與訪問的區別](#clicks-vs-visits)&quot; 相反，我們建議使用 [!UICONTROL AMO ID Instances]，即捕獲AMO ID的次數。 同時 [!UICONTROL AMO ID Instances] 不匹配 [!UICONTROL AMO Clicks] 確切地說，它們是測量站點上點擊流量的最佳選項。 有關詳細資訊，請參閱「」[資料驗證 [!DNL Analytics for Advertising Cloud]](#data-validation)&quot;

![示例 [!UICONTROL AMO ID Instances] 而不是 [!UICONTROL AMO Clicks] 不支援的維](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising CloudID使用者 [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Advertising CloudAnalysis Workspace度量](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Advertising Cloud資料](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)
>* [為什麼資料可能因Advertising Cloud和 [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)

