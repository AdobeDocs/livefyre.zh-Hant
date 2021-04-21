---
description: 傳回實例化為「注釋」類型的Collection物件。 從Collection物件執行createOrUpdate()以完成建置程式。
title: buildCommentsCollection網站方法
exl-id: 9534c25a-fd1c-4a09-92e2-d196ac218ef3
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 8%

---

# buildCommentsCollection網站方法{#buildcommentscollection-site-method}

傳回實例化為「注釋」類型的Collection物件。 從Collection物件執行createOrUpdate()以完成建置程式。

| 變數 | 類型 | 說明 |
|--- |--- |--- |
| title | 字串 | 系列的標題。 |
| articleId | 字串 | 您選擇用來識別網站內系列的唯一文章ID。 |
| url | 字串 | 此系列的標準絕對URL。 |

## Java示例{#section_nyl_ycs_rz}

```
Collection collection = site.buildCommentsCollection(title, articleId, url);
```

## NodeJS示例{#section_xkd_gds_rz}

```
var collection = site.buildCommentsCollection(title, articleId, url); 
```

## PHP示例{#section_ghf_gds_rz}

```
$collection = site->buildCommentsCollection(title, articleId, url); 
```

## Python示例{#section_dwg_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```

## Ruby示例{#section_enh_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```
