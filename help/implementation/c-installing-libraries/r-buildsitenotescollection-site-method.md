---
description: 傳回做為Sit列舉類型的系列物件。從Collection物件執行_ or_ update()以完成建置程序。
seo-description: 傳回做為Sit列舉類型的系列物件。從Collection物件執行_ or_ update()以完成建置程序。
seo-title: BuildSitenoteCollection網站方法
solution: Experience Manager
title: BuildSitenoteCollection網站方法
uuid: 2bfbc032-4c0c-48d2-8ce6-02460b38bd6c
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# BuildSitenoteCollection網站方法{#buildsitenotescollection-site-method}

傳回做為Sit列舉類型的系列物件。從Collection物件執行_ or_ update()以完成建置程序。

| 變數 | Type | 說明 |
|--- |--- |--- |
| title | 字串 | 系列的標題。 |
| articleID | 字串 | 您選擇在您的網站內識別系列的唯一文章ID。 |
| url | 字串 | 此系列的標準絕對URL。 |

## Java範例 {#section_nyl_ycs_rz}

```
Collection collection = site.buildSidenotesCollection(title, articleId, url); 
```

## nodeJS範例 {#section_xkd_gds_rz}

```
var collection = site.buildSidenotesCollection(title, articleId, url); 
```

## PHP範例 {#section_ghf_gds_rz}

```
$collection = site->buildSidenotesCollection(title, articleId, url); 
```

## Python範例 {#section_dwg_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```

## Ruby範例 {#section_enh_gds_rz}

```
collection = site.build_sidenotes_collection(title, articleId, url) 
```
