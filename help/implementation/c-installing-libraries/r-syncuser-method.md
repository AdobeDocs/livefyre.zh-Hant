---
description: 通知Livefyre從先前設定的使用者同步URL提取使用者資訊。傳回布林值。
seo-description: 通知Livefyre從先前設定的使用者同步URL提取使用者資訊。傳回布林值。
seo-title: SyncUser Network方法
solution: Experience Manager
title: SyncUser Network方法
uuid: 2affb03d-3907-4b01-9a64-02ba1b06da14
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# SyncUser Network方法{#syncuser-network-method}

通知Livefyre從先前設定的使用者同步URL提取使用者資訊。傳回布林值。

| 變數 | Type | 說明 |
|--- |--- |--- |
| userId | 字串 | 與Livefyre同步的使用者ID。在呼叫此方法之前，您必須先與Livefyre同步URL設定。 |

## Java範例 {#section_nyl_ycs_rz}

```
network.syncUser(userId); 
```

輸出範例：

```
true
```

## nodeJS範例 {#section_xkd_gds_rz}

```
network.syncUser(userId); 
```

輸出範例：

```
true
```

## PHP範例 {#section_ghf_gds_rz}

```
$network->syncUser(userId); 
```

輸出範例：

```
true
```

## Python範例 {#section_dwg_gds_rz}

```
network.sync_user(userId) 
```

輸出範例：

```
True
```

## Ruby範例 {#section_enh_gds_rz}

```
network.sync_user(userId) 
```

輸出範例：

```
True
```
