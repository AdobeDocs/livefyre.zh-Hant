---
description: 通知Livefyre從先前設定的使用者同步URL提取使用者資訊。 傳回布林值。
seo-description: 通知Livefyre從先前設定的使用者同步URL提取使用者資訊。 傳回布林值。
seo-title: syncUser Network Method
solution: Experience Manager
title: syncUser Network Method
uuid: 2affb03d-3907-4b01-9a64-02ba1b06da14
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

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
