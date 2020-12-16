---
description: 本節說明如何產生UserAuth JSON物件，以建立使用者登入應用程式所需的使用者驗證Token。
seo-description: 本節說明如何產生UserAuth JSON物件，以建立使用者登入應用程式所需的使用者驗證Token。
seo-title: 使用者驗證Token
solution: Experience Manager
title: 使用者驗證Token
uuid: 6483debd-453c-4780-b19c-1d8041693617
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 2%

---


# 使用者驗證Token{#user-auth-token}

本節說明如何產生UserAuth JSON物件，以建立使用者登入應用程式所需的使用者驗證Token。

本節說明如何產生UserAuth JSON物件，以建立使用者登入應用程式所需的使用者驗證Token。

若要建立Token，請使用您偏好的語言庫來傳入下列參數：

| 參數 | 類型 | 說明 |
|---|---|---|
| networkName | 字串&#x200B;*required* | Livefyre網路的名稱（由Livefyre提供）。 |
| networkKey | 字串&#x200B;*required* | 此特定網路的機密金鑰（由Livefyre提供）。 |
| userId | 字串&#x200B;*required* | 以儲存在您的使用者管理系統中的方式登入的使用者ID（僅允許使用英數字元、破折號、底線和點字元）:[a-zA-Z0-9_-。])。**注意：** userId必須是唯一的。 |
| 過期 | 整數&#x200B;*required* | Token應從現在開始過期（以秒為單位）。 **注意：** 此值也可以作為浮點數傳遞。產生的JSON網頁Token會在UNIX紀元時間中儲存此值。 |
| displayName | 字串&#x200B;*required* | 在UI和注釋中識別此使用者的文字。 (字元數上限：50.) |

## Java {#section_b42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
 
```

## NodeJS {#section_c42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

## PHP {#section_d42_mjz_1cb}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

## Python {#section_e42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

## Ruby {#section_f42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

>[!NOTE]
>
>網路金鑰不會共用給Livefyre分組網站帳戶。 一旦Livefyre為您布建環境，您就會收到網路金鑰。 此金鑰應保持私密。

