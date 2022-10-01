---
title: 對象區段邏輯語法
description: 參考可用來定義受眾區段邏輯的語法。
feature: DSP Audiences
exl-id: 3a51b1b5-1eef-453b-9be5-0694e27491a8
source-git-commit: efd04189de975f8f075dec7851a3a06d2d647ded
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# 對象區段邏輯語法

建立可重複使用的對象時，您可以使用英數字元區段ID（索引鍵）和下列語法手動定義區段邏輯：

* (1)指明一組
* `||` for [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp; [!DNL AND]
* ! for [!DNL NOT] （排除）

>[!NOTE]
>
>* 除非前面有！，否則會包含所有指定的區段群組 （不包括這些）。
>* 您可以 [尋找對象的區段ID](reusable-audience-clipboard.md) 從 [!UICONTROL Audiences] > [!UICONTROL All audiences].


例如，下列邏輯：

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

（英語）

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>在版位設定中，您可以使用儲存的對象作為明確鎖定的對象，或作為要從鎖定中排除的個別對象。 請確定您的區段邏輯會反映您將使用對象的目的。

>[!MORELIKETHIS]
>
>* [將可重複使用對象的區段索引鍵複製到剪貼簿](reusable-audience-clipboard.md)
>* [關於Audience Management](audience-about.md)
>* [建立可重複使用的受眾](reusable-audience-create.md)
>* [對象設定](audience-settings.md)
>* [可用的第三方資料提供者](third-party-data-providers.md)

