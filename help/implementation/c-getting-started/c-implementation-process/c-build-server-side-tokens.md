---
description: 建立CollectionMeta和驗證Token的指南。
seo-description: 建立CollectionMeta和驗證Token的指南。
seo-title: 建置伺服器端Token
solution: Experience Manager
title: 建置伺服器端Token
uuid: 8313f26e-5ceb-414e-a61 a-480bb7 a8 ba66
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 建置伺服器端Token{#build-server-side-tokens}

建立CollectionMeta和驗證Token的指南。

建立Livefyre用來驗證請求的Token，確保只有您可以更新Livefyre網路。

## CollectionMeta Token

瞭解如何建立Token來建立新的和顯示現有的對話。

## Auth Token

瞭解如何建立Token來驗證使用者，這是如果您不使用Janrain Capture進行使用者管理的必要步驟。

## 使用者驗證Token {#section_l5l_hwt_bbb}

本節說明如何產生userAuth JSON物件，以建立使用者登入您應用程式所需的使用者驗證Token。

若要建立Token，請使用您偏好的語言庫傳遞下列參數：

| 參數 | Type | 說明 |
|---|---|---|
| socialName | *需要字串* | Livefyre網路的名稱(由Livefyre提供)。 |
| SocialKey | *需要字串* | 此特定網路的秘密金鑰(由Livefyre提供)。 |
| userId | *需要字串* | 使用者登入的ID會儲存在使用者管理系統中(僅允許英數、破折號、底線和點字元： `[a-zA-Z0-9_-.]`)。**注意：** userId必須是唯一的。 |
| 過期 | Integer *required* | Token從現在起過期(以秒為單位)。**注意：** 此值也可以傳遞為浮動值。產生的JSON網頁代號將會在UNIX週期中儲存此值。 |
| DisplayName | *需要字串* | 在UI和留言中識別此使用者的文字。(字元數目上限：50.) |

