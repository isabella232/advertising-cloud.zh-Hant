---
title: 的錯誤代碼 [!DNL FreeWheel] 廣告提交
description: 參考為廣告提交傳回的錯誤代碼 [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: null
source-git-commit: d2ad7d47d9cf13411fc831526a6fa4ff698b0a15
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 2%

---

# 的錯誤代碼 [!DNL FreeWheel] 廣告提交

失敗廣告提交的錯誤訊息可能來自Advertising Cloud DSP或 [!DNL FreeWheel]. 錯誤訊息會顯示在 [!UICONTROL API Response] 欄中 [[!UICONTROL Freewheel Status] 對話](freewheel-check-status.md).

## Advertising Cloud DSP內部錯誤

| 錯誤訊息 | 說明 | 後續步驟 |
|--- |--- |--- |
| [!DNL正在等待狀態響應 [!DNL FreeWheel]] | [!DNL FreeWheel] 尚未回應提交是否成功。 | 10分鐘後再次檢查狀態。 |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] 不接受沒有指定時鐘號的英國廣告。 | 為廣告指派時鐘編號，然後重新提交廣告。 |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | 當您嘗試提交廣告時，轉碼器尚未完成轉碼廣告。 | 等待10分鐘，然後重新提交廣告。 |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | 提交的交易不是作為程式保證的交易而設定的。 [!DNL FreeWheel] 僅接受有保證的交易。 | 將交易ID設定為程式化的保證交易。 廣告會自動提交至 [!DNL FreeWheel] 當您在交易ID工作流程結束時儲存程式化保證的預設位置時。 |
| [!DNL Invalid external_deal_id:] \&lt;deal_id> | 提交的交易ID不存在或在Adobe結束時未生效。 | 確定交易處於有效狀態，然後重新提交廣告。 |
| [!DNL \[public_id=]\&lt;deal>]不存在 | 提交的交易ID不存在於 [!DNL FreeWheel] 結束。 | 請連絡您的 [!DNL FreeWheel] 確認交易ID的代表。 |
| [!DNL Ad with identifier] \&lt;*廣告名稱*\> [!DNL was not found.] | 已提交的廣告金鑰不存在或在Adobe結束時未作用中。 | 找到正確的廣告金鑰，然後重新提交廣告。 |
| [!DNL Pending Submission] | 提交仍在等待中。 | 重新整理頁面。 |

{style=&quot;table-layout:auto&quot;}

## FreeWheel API錯誤

| 程式碼 | 意義 | 說明 | 後續步驟 |
|--- |--- |--- |--- |
| 401 | 未授權 | 訪問憑據不正確、缺失或無效。 | 請連絡您的 [!DNL Adobe] 客戶經理。 |
| 403 | 禁止 | 伺服器理解請求，但拒絕授權。 | 請連絡您的 [!DNL Adobe] 客戶經理。 |
| 404 | 找不到 | 您請求的資源不可用。 如果在PUT操作中找不到創作ID，則會傳回404。 | 請連絡您的 [!DNL Adobe] 客戶經理。 |
| 405 | 不允許的方法 | 已使用該資源不支援的請求方法對資源提出請求(例如，在需要由POST傳送資料的方法上使用GET，或在唯讀資源上使用PUT)。 | 請連絡您的 [!DNL Adobe] 客戶經理。 |
| 408 | 請求逾時 | 處理此請求時發生超時。 逾時通常是由同時請求獨佔特定資源所導致。 | 在您收到此狀態時重新提交請求。 如果問題持續存在，請聯絡您的 [!DNL Adobe] 客戶經理。 |
| 422 | 不可處理的實體 | 資源無效。 當請求內文無效或建立/更新的資源無效（例如，如果找不到交易ID）時，就會發生此錯誤。 請參閱 [FreeWheel API 422錯誤](#freewheel-422-errors) 以取得更多資訊。 | 請連絡您的 [!DNL Adobe] 客戶經理。 |
| 500 | 內部伺服器錯誤 | API系統錯誤。 | 請連絡您的 [!DNL Adobe] 客戶經理。 |

{style=&quot;table-layout:auto&quot;}

## FreeWheel API 422錯誤 {#freewheel-422-errors}

| 程式碼 | HTTP程式碼 | 說明 |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422 | 請求資料的json格式無效。 檢查錯誤訊息以取得詳細資訊。 |
| DATA_VALIDATION_FAILURE | 422 | 請求資料缺少必需欄位或資料類型無效。 檢查錯誤訊息以取得詳細資訊。 |
| DATA_DEAL_INVALID | 422 | 交易配置不正確或不存在。 檢查錯誤訊息以取得詳細資訊。 |
| DATA_DEAL_FAILUREGET | 422 | 未找到交易或其配置有問題。 檢查錯誤訊息以取得詳細資訊。 |
| DATA_CREATIVE_INGEST_FAILURE | 422 | 創作URL無效。 檢查錯誤訊息以取得詳細資訊。 |
| DATA_CREATIVE_LINK_FAILURE | 422 | 創意素材與交易的廣告單位節點沒有連結。 檢查錯誤訊息以取得詳細資訊。 |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | 創意內容尚未更新。 檢查錯誤訊息以取得詳細資訊。 |
| DATA_DSP_GET_失敗 | 422 | DSP不存在於系統內。 |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | 創意內容未與廣告單位解除連結。 |
| DATA_CREATIVE_CATIVE_FAILURE_FAILURE | 422 | 創意內容沒有刪除。 |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | 未檢測到URL。 |
| DATA_ENTITY_NOT_FOUND | 422 | 創意不存在。 |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [在FreeWheel中建立程式保證交易概述](/help/dsp/inventory/freewheel-overview.md)
>* [在交易ID收件匣中接受交易](deal-id-inbox-accept.md)
>* [向FreeWheel提交程式化保證交易的廣告](/help/dsp/inventory/freewheel-submit.md)
>* [檢查廣告的狀態 [!DNL FreeWheel] 程式化保證交易](/help/dsp/inventory/freewheel-check-status.md)

