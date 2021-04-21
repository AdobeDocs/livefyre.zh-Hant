---
description: 通知Livefyre從先前設定的使用者同步URL提取使用者資訊。 傳回布林值。
title: syncUser Network Method
exl-id: a21ff487-2ab1-4788-b455-84941f03a98f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 5%

---

# syncUser Network Method{#syncuser-network-method}

通知Livefyre從先前設定的使用者同步URL提取使用者資訊。 傳回布林值。

| 變數 | 類型 | 說明 |
|--- |--- |--- |
| userId | 字串 | 要與Livefyre同步的使用者ID。 您必須先將使用者同步URL與Livefyre設定，才能呼叫此方法。 |

## Java示例{#section_nyl_ycs_rz}

```
network.syncUser(userId); 
```

輸出範例：

```
true
```

## NodeJS示例{#section_xkd_gds_rz}

```
network.syncUser(userId); 
```

輸出範例：

```
true
```

## PHP示例{#section_ghf_gds_rz}

```
$network->syncUser(userId); 
```

輸出範例：

```
true
```

## Python示例{#section_dwg_gds_rz}

```
network.sync_user(userId) 
```

輸出範例：

```
True
```

## Ruby示例{#section_enh_gds_rz}

```
network.sync_user(userId) 
```

輸出範例：

```
True
```
