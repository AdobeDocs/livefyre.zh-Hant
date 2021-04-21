---
description: 將API呼叫的SSL設為開啟或關閉。
title: setSSL網路方法
exl-id: 5682b84a-0b4d-479b-af40-60d2c6c38155
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---

# setSSL Network Method{#setssl-network-method}

將API呼叫的SSL設為開啟或關閉。

| 變數 | 類型 | 說明 |
|--- |--- |--- |
| ssl | 布林值 | 預設為true。 如果您要開啟SSL，否則為false。<br><ul><li>True - SSL on </li><li>False —— 關閉SSL</li></ul> |

## Java示例{#section_nyl_ycs_rz}

```
network.setSsl(ssl); 
```

## NodeJS示例{#section_xkd_gds_rz}

```
network.ssl = false; 
```

## PHP示例{#section_ghf_gds_rz}

```
$network->setSsl(false); 
```

## Python示例{#section_dwg_gds_rz}

```
network.ssl = False 
```

## Ruby示例{#section_enh_gds_rz}

```
network.ssl = false 
```
