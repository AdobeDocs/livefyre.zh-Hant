---
description: 傳回「注釋」類型的「系列」物件。從Collection物件執行CreateOrdUpdate()以完成建置程序。
seo-description: 傳回「注釋」類型的「系列」物件。從Collection物件執行CreateOrdUpdate()以完成建置程序。
seo-title: buildCommentScollection網站方法
solution: Experience Manager
title: buildCommentScollection網站方法
uuid: 0e5c062e-960d-4ab0-ba32-0965731a1571
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# buildCommentScollection網站方法{#buildcommentscollection-site-method}

傳回「注釋」類型的「系列」物件。從Collection物件執行CreateOrdUpdate()以完成建置程序。

| 變數 | Type | 說明 |
|--- |--- |--- |
| title | 字串 | 系列的標題。 |
| articleID | 字串 | 您選擇在您的網站內識別系列的唯一文章ID。 |
| url | 字串 | 此系列的標準絕對URL。 |

## Java範例 {#section_nyl_ycs_rz}

```
Collection collection = site.buildCommentsCollection(title, articleId, url);
```

## nodeJS範例 {#section_xkd_gds_rz}

```
var collection = site.buildCommentsCollection(title, articleId, url); 
```

## PHP範例 {#section_ghf_gds_rz}

```
$collection = site->buildCommentsCollection(title, articleId, url); 
```

## Python範例 {#section_dwg_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```

## Ruby範例 {#section_enh_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```
