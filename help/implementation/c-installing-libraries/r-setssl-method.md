---
description: 將API呼叫的SSL設為開啟或關閉。
seo-description: 將API呼叫的SSL設為開啟或關閉。
seo-title: setSSL網路方法
solution: Experience Manager
title: setSSL網路方法
uuid: 8d989e63-c859-456a-99ca-8d87933913ba
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# setSSL網路方法{#setssl-network-method}

將API呼叫的SSL設為開啟或關閉。

| 變數 | 類型 | 說明 |
|--- |--- |--- |
| ssl | 布林值 | 預設為true。 如果您要開啟SSL，否則為false。 <br><ul><li>True - SSL on </li><li>False —— 關閉SSL</li></ul> |

## Java示例 {#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## NodeJS範例 {#section_xkd_gds_rz}

```
network.ssl = false; 
```

## PHP範例 {#section_ghf_gds_rz}

```
$network->setSsl(false); 
```

## Python示例 {#section_dwg_gds_rz}

```
network.ssl = False 
```

## Ruby示例 {#section_enh_gds_rz}

```
network.ssl = false 
```
