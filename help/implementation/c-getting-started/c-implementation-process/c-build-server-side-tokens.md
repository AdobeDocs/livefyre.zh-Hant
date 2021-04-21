---
description: 建立collectionMeta和auth Token的指南。
title: 建立伺服器端Token
exl-id: f709b79e-9236-443e-b862-c7d281815d91
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 1%

---

# 建立伺服器端Token{#build-server-side-tokens}

建立collectionMeta和auth Token的指南。

建立Livefyre用來驗證請求的Token，可確保只有您才能更新Livefyre網路。

## CollectionMeta Token

瞭解如何建立代號以建立新對話並顯示現有對話。

## 驗證Token

瞭解如何建立用於驗證使用者的Token，這是整合程式中的必要步驟（如果您不使用Janrain Capture來管理使用者）。

## 使用者驗證Token {#section_l5l_hwt_bbb}

本節說明如何產生UserAuth JSON物件，以建立使用者登入應用程式所需的使用者驗證Token。

若要建立Token，請使用您偏好的語言庫來傳入下列參數：

| 參數 | 類型 | 說明 |
|---|---|---|
| networkName | 字串&#x200B;*required* | Livefyre網路的名稱（由Livefyre提供）。 |
| networkKey | 字串&#x200B;*required* | 此特定網路的機密金鑰（由Livefyre提供）。 |
| userId | 字串&#x200B;*required* | 以儲存在您的使用者管理系統中的方式登入的使用者ID（僅允許使用英數字元、破折號、底線和點字元）:`[a-zA-Z0-9_-.]`)。 **注意：** userId必須是唯一的。 |
| 過期 | 整數&#x200B;*required* | Token應從現在開始過期（以秒為單位）。 **注意：** 此值也可以作為浮點數傳遞。產生的JSON網頁Token會在UNIX紀元時間中儲存此值。 |
| displayName | 字串&#x200B;*required* | 在UI和注釋中識別此使用者的文字。 (字元數上限：50.) |
