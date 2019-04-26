---
description: 傳回屬於「評分」類型的系列物件。從Collection物件執行_ or_ update()以完成建置程序。
seo-description: 傳回屬於「評分」類型的系列物件。從Collection物件執行_ or_ update()以完成建置程序。
seo-title: BuildratingScollection網站方法
title: BuildratingScollection網站方法
uuid: eea2ba3-48e1-4cd2-aa73-ea81788 af1 df
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# BuildratingScollection網站方法{#buildratingscollection-site-method}

傳回屬於「評分」類型的系列物件。從Collection物件執行_ or_ update()以完成建置程序。

| 變數 | Type | 說明 |
|--- |--- |--- |
| title | 字串 | 系列的標題。 |
| articleID | 字串 | 您選擇在您的網站內識別系列的唯一文章ID。 |
| url | 字串 | 此系列的標準絕對URL。 |

## Java範例 {#section_nyl_ycs_rz}

```
Collection collection = site.buildRatingsCollection(title, articleId, url); 
```

## nodeJS範例 {#section_xkd_gds_rz}

```
var collection = site.buildRatingsCollection(title, articleId, url); 
```

## PHP範例 {#section_ghf_gds_rz}

```
$collection = site->buildRatingsCollection(title, articleId, url); 
```

## Python範例 {#section_dwg_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```

## Ruby範例 {#section_enh_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```

