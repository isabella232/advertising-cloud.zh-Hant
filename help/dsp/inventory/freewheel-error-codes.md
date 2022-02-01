---
title: 錯誤代碼 [!DNL FreeWheel] 廣告提交
description: 引用為廣告提交返回的錯誤代碼 [!DNL FreeWheel]。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 2eb93971-ba82-4de8-96c5-48524d628b70
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 2%

---

# 錯誤代碼 [!DNL FreeWheel] 廣告提交

失敗廣告提交的錯誤消息可能來自Advertising Cloud DSP或 [!DNL FreeWheel]。 錯誤消息顯示在 [!UICONTROL API Response] 列 [[!UICONTROL Freewheel Status] 對話](freewheel-check-status.md)。

## Advertising Cloud DSP內部錯誤

| 錯誤消息 | 說明 | 後續步驟 |
|--- |--- |--- |
| [!DNL Awaiting status response from [!DNL FreeWheel]] | [!DNL FreeWheel] 尚未答復提交成功或失敗。 | 10分鐘後再次檢查狀態。 |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] 不接受沒有指定時鐘號的英國廣告。 | 為廣告分配時鐘編號，然後重新提交廣告。 |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | 當您嘗試提交廣告時，代碼轉換器尚未完成廣告的代碼轉換。 | 等待10分鐘，然後重新提交廣告。 |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | 提交的交易並非作為計畫性保證交易而成立。 [!DNL FreeWheel] 只接受有保證的交易。 | 將交易ID設定為可寫程式保證交易。 廣告將自動提交到 [!DNL FreeWheel] 在交易ID工作流結束時保存寫程式保證的預設位置。 |
| [!DNL Invalid external_deal_id:] \&lt;deal_id> | 提交的交易ID在Adobe端不存在或未處於活動狀態。 | 確保交易處於活動狀態，然後重新提交廣告。 |
| [!DNL \[public_id=]\&lt;deal>]不存在 | 提交的交易ID在上 [!DNL FreeWheel] 結束。 | 聯繫您 [!DNL FreeWheel] 代表確認交易ID。 |
| [!DNL Ad with identifier] \&lt;*ad name（廣告名稱）*\> [!DNL was not found.] | 已提交的廣告鍵不存在或在Adobe端未處於活動狀態。 | 查找正確的廣告鍵，然後重新提交廣告。 |
| [!DNL Pending Submission] | 提交仍在等待。 | 刷新頁面。 |

{style=&quot;table-layout:auto&quot;&quot;

## [!DNL Freewheel] API錯誤

| 代碼 | 意義 | 說明 | 後續步驟 |
|--- |--- |--- |--- |
| 401 | 未授權 | 訪問憑據不正確、缺失或無效。 | 聯繫您 [!DNL Adobe] 客戶團隊。 |
| 403 | 禁止 | 伺服器理解請求，但拒絕授權。 | 聯繫您 [!DNL Adobe] 客戶團隊。 |
| 404 | 未找到 | 您請求的資源不可用。 如果在PUT操作中找不到Creative ID ，則返回404。 | 聯繫您 [!DNL Adobe] 客戶團隊。 |
| 405 | 不允許使用方法 | 使用該資源不支援的請求方法對資源發出請求(例如，對需要通過POST發送資料的方法使用GET，或對只讀資源使用PUT)。 | 聯繫您 [!DNL Adobe] 客戶團隊。 |
| 408 | 請求超時 | 處理此請求時發生超時。 超時通常由對特定資源的獨佔訪問的併發請求引起。 | 收到此狀態後重新提交請求。 如果問題仍然存在，請與 [!DNL Adobe] 客戶團隊。 |
| 422 | 不可處理實體 | 資源無效。 當請求正文無效或建立/更新的資源無效（例如，如果找不到交易ID）時，會發生此錯誤。 請參閱 [FreeWheel API 422錯誤](#freewheel-422-errors) 的子菜單。 | 聯繫您 [!DNL Adobe] 客戶團隊。 |
| 500 | 內部伺服器錯誤 | API系統錯誤。 | 聯繫您 [!DNL Adobe] 客戶團隊。 |

{style=&quot;table-layout:auto&quot;&quot;

## [!DNL Freewheel] API 422錯誤 {#freewheel-422-errors}

| 代碼 | HTTP代碼 | 說明 |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422 | 請求資料是無效的json格式。 檢查錯誤消息以瞭解詳細資訊。 |
| DATA_VALIDATION_FAILURE | 422 | 請求資料缺少必填欄位或資料類型無效。 檢查錯誤消息以瞭解詳細資訊。 |
| DATA_DEAL_INVALID | 422 | 交易配置不正確或不存在。 檢查錯誤消息以瞭解詳細資訊。 |
| DATA_DEAL_FAILURE_DEAL_GET_FAILURE | 422 | 找不到交易或其配置有問題。 檢查錯誤消息以瞭解詳細資訊。 |
| DATA_CREATIVE_INGEST_FAILURE | 422 | 建立URL無效。 檢查錯誤消息以瞭解詳細資訊。 |
| DATA_CREATIVE_LINK_FAILURE | 422 | 創意並未與交易的廣告單元節點關聯。 檢查錯誤消息以瞭解詳細資訊。 |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | 創意沒有更新。 檢查錯誤消息以瞭解詳細資訊。 |
| DATA_DSP_GET_失敗 | 422 | 系DSP統中不存在。 |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | 創意沒有與廣告單元脫鈎。 |
| DATA_CREATIVE_DELETE_失敗 | 422 | 創意未被刪除。 |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | 未檢測到URL。 |
| DATA_ENTITY_NOT_FOUND | 422 | 創意不存在。 |

{style=&quot;table-layout:auto&quot;&quot;

>[!MORELIKETHIS]
>
>* [中計畫保證交易設定概述 [!DNL Freewheel]](/help/dsp/inventory/freewheel-overview.md)
>* [在交易ID收件箱中接受交易](deal-id-inbox-accept.md)
>* [提交計畫保證交易的廣告以 [!DNL Freewheel]](/help/dsp/inventory/freewheel-submit.md)
>* [檢查廣告狀態 [!DNL FreeWheel] 計畫擔保交易](/help/dsp/inventory/freewheel-check-status.md)

