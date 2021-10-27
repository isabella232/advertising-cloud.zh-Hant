---
title: 報表目的地設定
description: 依目的地類型，請參閱報表目的地所需的詳細資訊。
feature: DSP Custom Reports
source-git-commit: ff14691fd2b6fa56c303dca3ac0e4c897c322f72
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---


# 報表目的地設定

非電子郵件報表目的地所需的詳細資訊會依目的地類型而異。

>[!NOTE]
>
> 您也可以將自訂報表傳送給不需要儲存報表目的地的電子郵件收件者。 您可以在報表設定中指定電子郵件收件者，而非儲存的目的地。

## [!UICONTROL S3]

**[!UICONTROL Name]:** 可協助您識別目的地的名稱。

**[!UICONTROL S3 Bucket URL]:** 上資料夾的完整路徑 [!DNL Amazon Simple Storage Service] (S3)要上傳報表的貯體。 範例： `s3://adcloud_account/reports`

**[!UICONTROL Access Key ID]:** ([!DNL Amazon S3])貯體（提供者） [!DNL Amazon])。

**[!UICONTROL Secret Access Key]:** ([!DNL Amazon S3])貯體（提供者） [!DNL Amazon])。

## [!UICONTROL FTP]

**[!UICONTROL Name]:** 可協助您識別目的地的名稱。

**[!UICONTROL Server]:** 伺服器的主機名。

**[!UICONTROL Port]:** 要在伺服器上使用的埠號。 預設為 *[!UICONTROL 21]*.

**[!UICONTROL Username]:** 要登入伺服器的使用者名稱。

**[!UICONTROL Password]:** 登入伺服器的密碼。

**[!UICONTROL Path (Optional)]:** 要上傳檔案的伺服器路徑。

## [!UICONTROL SFTP]

**[!UICONTROL Name]:** 可協助您識別目的地的名稱。

**[!UICONTROL Server]:** 伺服器的主機名。

**[!UICONTROL Port]:** 要在伺服器上使用的埠號。 預設為 *[!UICONTROL 21]*.

**[!UICONTROL Username]:** 要登入伺服器的使用者名稱。

**[!UICONTROL Password]:** 登入伺服器的密碼。

**[!UICONTROL Path (Optional)]:** 要上傳檔案的伺服器路徑。

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]:** 可協助您識別目的地的名稱。

**[!UICONTROL Server]:** 伺服器的主機名。

**[!UICONTROL Port]:** 要在伺服器上使用的埠號。 預設為 *[!UICONTROL 21]*.

**[!UICONTROL Username]:** 要登入伺服器的使用者名稱。

**[!UICONTROL Password]:** 登入伺服器的密碼。

**[!UICONTROL Path (Optional)]:** 要上傳檔案的伺服器路徑。

>[!MORELIKETHIS]
>
>* [關於 [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [建立 [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [編輯 [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [刪除 [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-delete.md)

