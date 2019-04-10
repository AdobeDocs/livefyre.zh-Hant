---
description: 本節說明如何產生userAuth JSON物件，以建立使用者登入您應用程式所需的使用者驗證Token。
seo-description: 本節說明如何產生userAuth JSON物件，以建立使用者登入您應用程式所需的使用者驗證Token。
seo-title: 使用者驗證Token
solution: Experience Manager
title: 使用者驗證Token
uuid: 6483debd-453c-4780-b19 c-1d8041693617
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 使用者驗證Token{#user-auth-token}

本節說明如何產生userAuth JSON物件，以建立使用者登入您應用程式所需的使用者驗證Token。

本節說明如何產生userAuth JSON物件，以建立使用者登入您應用程式所需的使用者驗證Token。

若要建立Token，請使用您偏好的語言庫傳遞下列參數：

| 參數 | Type | 說明 |
|---|---|---|
| socialName | *需要字串* | Livefyre網路的名稱(由Livefyre提供)。 |
| SocialKey | *需要字串* | 此特定網路的秘密金鑰(由Livefyre提供)。 |
| userId | *需要字串* | 使用者登入的ID會儲存在使用者管理系統中(僅允許英數、破折號、底線和點字元： [a-zA-Z0-9_-.]). **注意：** userId必須是唯一的。 |
| 過期 | Integer *required* | Token從現在起過期(以秒為單位)。**注意：** 此值也可以傳遞為浮動值。產生的JSON網頁代號將會在UNIX週期中儲存此值。 |
| DisplayName | *需要字串* | 在UI和留言中識別此使用者的文字。(字元數目上限：50.) |

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
>無法共用Livefyre網站帳戶的網路索引鍵。當Livefyre為您布建環境後，您將會收到網路金鑰。此金鑰應保持私密。

