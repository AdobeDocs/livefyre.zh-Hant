---
description: 設定API呼叫的SSL呼叫開啓或關閉。
seo-description: 設定API呼叫的SSL呼叫開啓或關閉。
seo-title: setSSL網路方法
solution: Experience Manager
title: setSSL網路方法
uuid: 8d989e63-c859-456a-99ca-8d8793913 ba
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# setSSL網路方法{#setssl-network-method}

設定API呼叫的SSL呼叫開啓或關閉。

| 變數 | Type | 說明 |
|--- |--- |--- |
| ssl | 布林值 | 預設為true。如果您想要SSL上的SSL，則為false。 <br><ul><li>True- SSL上的 </li><li>False-關閉SSL</li></ul> |

## Java範例 {#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## nodeJS範例 {#section_xkd_gds_rz}

```
network.ssl = false; 
```

## PHP範例 {#section_ghf_gds_rz}

```
$network->setSsl(false); 
```

## Python範例 {#section_dwg_gds_rz}

```
network.ssl = False 
```

## Ruby範例 {#section_enh_gds_rz}

```
network.ssl = false 
```
