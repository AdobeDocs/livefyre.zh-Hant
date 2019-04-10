---
description: 傳回來自所呼叫網路的加密用戶驗證Token。
seo-description: 傳回來自所呼叫網路的加密用戶驗證Token。
seo-title: BuilduserAuthToken網路方法
solution: Experience Manager
title: BuilduserAuthToken網路方法
uuid: 8828d356-c3 c6-46a6-91bb-83bd59 e35050
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# BuilduserAuthToken網路方法{#builduserauthtoken-network-method}

傳回來自所呼叫網路的加密用戶驗證Token。

| 變數 | Type | 說明 |
|--- |--- |--- |
| userId | 字串 | 此代號所屬之使用者的使用者ID。 |
| DisplayName | 字串 | 使用者的顯示名稱。 |
| 過期 | 雙重 | 當Token在數秒內過期時。 |

## Java範例 {#section_nyl_ycs_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

輸出範例：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## nodeJS範例 {#section_xkd_gds_rz}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

輸出範例：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo 
```

## PHP範例 {#section_ghf_gds_rz}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

輸出範例：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Python範例 {#section_dwg_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

輸出範例：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```

## Ruby範例 {#section_enh_gds_rz}

```
network.build_user_auth_token(userId, displayName, expires) 
```

輸出範例：

```
eyJhbGciOiJIUzI1NiJ9.eyJkb21haW4iOiJ0ZXN0LmZ5cmUuY29tIiwidXNlcl9pZCI6InN5c3RlbSIsImRpc3BsYXlfbmFtZSI6InN5c3RlbSIsImV4cGlyZXMiOjEzOTY2NTUwODN9.33GuJF_ou2O6CCV22Y3PlLUgP2Igy9vAXfmLONkt-Yo
```
