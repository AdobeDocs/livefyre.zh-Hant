---
description: 'null'
seo-description: 'null'
seo-title: buildCollection網站方法
solution: Experience Manager
title: buildCollection網站方法
uuid: 52abc42a-9506-4492-b219-f2e05eb79c5f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildCollection網站方法{#buildcollection-site-method}

| 變數 | 類型 | 說明 |
|--- |--- |--- |
| type | CollectionType | 系列的類型。 |
| title | 字串 | 系列的標題。 |
| articleId | 字串 | 您選擇用來識別網站內系列的唯一文章ID。 |
| url | 字串 | 此系列的標準絕對URL。 |

## Java示例 {#section_nyl_ycs_rz}

```
Collection collection = site.buildCollection(type, title, articleId, url); 
```

## NodeJS範例 {#section_xkd_gds_rz}

```
var collection = site.buildCollection(type, title, articleId, url); 
```

## PHP範例 {#section_ghf_gds_rz}

```
$collection = site->buildCollection(type, title, articleId, url); 
```

## Python示例 {#section_dwg_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```

## Ruby示例 {#section_enh_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```
