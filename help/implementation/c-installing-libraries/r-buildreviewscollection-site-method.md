---
description: 傳回做為評論類型的系列物件。從Collection物件執行_ or_ update()以完成建置程序。
seo-description: 傳回做為評論類型的系列物件。從Collection物件執行_ or_ update()以完成建置程序。
seo-title: BuildDreviewScollection網站方法
solution: Experience Manager
title: BuildDreviewScollection網站方法
uuid: 88af4c68-57de-4ae9-9394-550c94ede48f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# BuildDreviewScollection網站方法{#buildreviewscollection-site-method}

傳回做為評論類型的系列物件。從Collection物件執行_ or_ update()以完成建置程序。

| 變數 | Type | 說明 |
|--- |--- |--- |
| title | 字串 | 系列的標題。 |
| articleID | 字串 | 您選擇在您的網站內識別系列的唯一文章ID。 |
| url | 字串 | 此系列的標準絕對URL。 |


## Java範例 {#section_nyl_ycs_rz}

```
Collection collection = site.buildReviewsCollection(title, articleId, url); 
```

## nodeJS範例 {#section_xkd_gds_rz}

```
var collection = site.buildReviewsCollection(title, articleId, url); 
```

## PHP範例 {#section_ghf_gds_rz}

```
$collection = site->buildReviewsCollection(title, articleId, url); 
```

## Python範例 {#section_dwg_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

## Ruby範例 {#section_enh_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

