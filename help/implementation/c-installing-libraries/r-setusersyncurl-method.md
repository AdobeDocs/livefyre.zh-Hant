---
description: 通知Livefyre將網路的使用者同步URL更新至提供的URL。 傳回布林值。
title: setUserSyncUrl網路方法
exl-id: 8124ac0f-013f-4943-a33c-6cf8fe696f95
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---

# setUserSyncUrl Network Method{#setusersyncurl-network-method}

通知Livefyre將網路的使用者同步URL更新至提供的URL。 傳回布林值。

| 變數 | 類型 | 說明 |
|--- |--- |--- |
| urlTemplate | 字串 | 要向Livefyre註冊以同步使用者ID的URL。 要求&quot;`{id}`&quot;是提供之URL字串的一部分。 |

## Java示例{#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

輸出範例：

```
true
```

## NodeJS示例{#section_xkd_gds_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

輸出範例：

```
true
```

## PHP示例{#section_ghf_gds_rz}

```
$network->setUserSyncUrl(urlTemplate); 
```

輸出範例：

```
true
```

## Python示例{#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

輸出範例：

```
True
```

## Ruby示例{#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

輸出範例：

```
True
```
