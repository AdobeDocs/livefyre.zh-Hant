---
description: 傳回做為計算類型的系列物件。從Collection物件執行_ or_ update()以完成建置程序。
seo-description: 傳回做為計算類型的系列物件。從Collection物件執行_ or_ update()以完成建置程序。
seo-title: BuildIdentijectCollection網站方法
title: BuildIdentijectCollection網站方法
uuid: e293d66a-0025-4230-997e-295ce4625713
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# BuildIdentijectCollection網站方法{#buildcountingcollection-site-method}

傳回做為計算類型的系列物件。從Collection物件執行_ or_ update()以完成建置程序。

| 變數 | Type | 說明 |
|--- |--- |--- |
| title | 字串 | 系列的標題。 |
| articleID | 字串 | 您選擇在您的網站內識別系列的唯一文章ID。 |
| url | 字串 | 此系列的標準絕對URL。 |

## Java範例 {#section_nyl_ycs_rz}

```
Collection collection = site.buildCountingCollection(title, articleId, url); 
```

## nodeJS範例 {#section_xkd_gds_rz}

```
var collection = site.buildCountingCollection(title, articleId, url); 
```

## PHP範例 {#section_ghf_gds_rz}

```
$collection = site->buildCountingCollection(title, articleId, url); 
```

## Python範例 {#section_dwg_gds_rz}

```
collection = site.build_counting_collection(title, articleId, url) 
```

## Ruby範例 {#section_enh_gds_rz}

```
collection = site.build_counting_collection(title, articleId, url) 
```
