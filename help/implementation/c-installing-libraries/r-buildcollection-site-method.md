---
description: null
seo-description: null
seo-title: BuildCollection網站方法
solution: Experience Manager
title: BuildCollection網站方法
uuid: 52c42a-9506-4492-b219-f2 e05 eb79 c5 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# BuildCollection網站方法{#buildcollection-site-method}

| 變數 | Type | 說明 |
|--- |--- |--- |
| type | collectionType | 系列的類型。 |
| title | 字串 | 系列的標題。 |
| articleID | 字串 | 您選擇在您的網站內識別系列的唯一文章ID。 |
| url | 字串 | 此系列的標準絕對URL。 |

## Java範例 {#section_nyl_ycs_rz}

```
Collection collection = site.buildCollection(type, title, articleId, url); 
```

## nodeJS範例 {#section_xkd_gds_rz}

```
var collection = site.buildCollection(type, title, articleId, url); 
```

## PHP範例 {#section_ghf_gds_rz}

```
$collection = site->buildCollection(type, title, articleId, url); 
```

## Python範例 {#section_dwg_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```

## Ruby範例 {#section_enh_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```
