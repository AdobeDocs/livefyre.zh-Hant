---
description: 通知Livefyre，將網路使用者同步URL更新為所提供的URL。傳回布林值。
seo-description: 通知Livefyre，將網路使用者同步URL更新為所提供的URL。傳回布林值。
seo-title: setUserSyncURL網路方法
solution: Experience Manager
title: setUserSyncURL網路方法
uuid: cd067e90-a2 da-4e3 d-8e60-7eabfd86 fc7 f
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# setUserSyncURL網路方法{#setusersyncurl-network-method}

通知Livefyre，將網路使用者同步URL更新為所提供的URL。傳回布林值。

| 變數 | Type | 說明 |
|--- |--- |--- |
| URLTemplate | 字串 | 用Livefyre註冊使用者ID的URL。需要「`{id}`」做為所提供URL字串的一部分。 |

## Java範例 {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

輸出範例：

```
true
```

## nodeJS範例 {#section_xkd_gds_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

輸出範例：

```
true
```

## PHP範例 {#section_ghf_gds_rz}

```
$network->setUserSyncUrl(urlTemplate); 
```

輸出範例：

```
true
```

## Python範例 {#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

輸出範例：

```
True
```

## Ruby範例 {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

輸出範例：

```
True
```
