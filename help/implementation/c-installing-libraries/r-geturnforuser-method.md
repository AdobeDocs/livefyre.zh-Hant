---
description: 此方法會傳回此網路使用者的URN。
seo-description: 此方法會傳回此網路使用者的URN。
seo-title: getEnfor使用者網路方法
solution: Experience Manager
title: getEnfor使用者網路方法
uuid: b70b8b0f-2b3a-4a-1d-90d0-93a97a137ad
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# getEnfor使用者網路方法{#geturnforuser-network-method}

此方法會傳回此網路使用者的URN。

| 變數 | Type | 說明 |
|--- |--- |--- |
| userId | 字串 | 用於URN的userId。 |

## Java範例 {#section_nyl_ycs_rz}

```
network.getUrnForUser(userId);
```

輸出範例：

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## nodeJS範例 {#section_xkd_gds_rz}

```
network.getUrnForUser(userId);
```

輸出範例：

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## PHP範例 {#section_ghf_gds_rz}

```
$network->getUrnForUser(userId); 
```

輸出範例：

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Python範例 {#section_dwg_gds_rz}

```
network.get_urn_for_user(userId) 
```

輸出範例：

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```

## Ruby範例 {#section_enh_gds_rz}

```
network.get_urn_for_user(userId) 
```

輸出範例：

```
"urn:livefyre:network=`example.fyre.co`:user=tester" 
```
