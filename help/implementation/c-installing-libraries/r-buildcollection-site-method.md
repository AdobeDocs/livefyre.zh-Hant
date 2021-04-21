---
title: buildCollection網站方法
description: buildCollection網站方法
exl-id: d5c9a2fb-2d30-44f4-8ebf-24b0ec7babee
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 15%

---

# buildCollection網站方法{#buildcollection-site-method}

| 變數 | 類型 | 說明 |
|--- |--- |--- |
| type | CollectionType | 系列的類型。 |
| title | 字串 | 系列的標題。 |
| articleId | 字串 | 您選擇用來識別網站內系列的唯一文章ID。 |
| url | 字串 | 此系列的標準絕對URL。 |

## Java示例{#section_nyl_ycs_rz}

```
Collection collection = site.buildCollection(type, title, articleId, url); 
```

## NodeJS示例{#section_xkd_gds_rz}

```
var collection = site.buildCollection(type, title, articleId, url); 
```

## PHP示例{#section_ghf_gds_rz}

```
$collection = site->buildCollection(type, title, articleId, url); 
```

## Python示例{#section_dwg_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```

## Ruby示例{#section_enh_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```
