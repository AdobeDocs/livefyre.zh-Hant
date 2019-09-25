---
description: 通知Livefyre將網路的使用者同步URL更新至提供的URL。 傳回布林值。
seo-description: 通知Livefyre將網路的使用者同步URL更新至提供的URL。 傳回布林值。
seo-title: setUserSyncUrl網路方法
solution: Experience Manager
title: setUserSyncUrl網路方法
uuid: cd067e90-a2da-4e3d-8e60-7eabfd86fc7f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# setUserSyncUrl網路方法{#setusersyncurl-network-method}

通知Livefyre將網路的使用者同步URL更新至提供的URL。 傳回布林值。

| 變數 | 類型 | 說明 |
|--- |--- |--- |
| urlTemplate | 字串 | 要向Livefyre註冊以同步使用者ID的URL。 需要`{id}`""作為提供之URL字串的一部分。 |

## Java示例 {#section_nyl_ycs_rz}

```
network.setUserSyncUrl(urlTemplate); 
```

輸出範例：

```
true
```

## NodeJS範例 {#section_xkd_gds_rz}

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

## Python示例 {#section_dwg_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

輸出範例：

```
True
```

## Ruby示例 {#section_enh_gds_rz}

```
network.set_user_sync_url(urlTemplate) 
```

輸出範例：

```
True
```
