---
description: 傳回實例化為計數類型的Collection物件。 從Collection物件執行create_or_update()以完成建置程式。
seo-description: 傳回實例化為計數類型的Collection物件。 從Collection物件執行create_or_update()以完成建置程式。
seo-title: buildCountingCollection網站方法
title: buildCountingCollection網站方法
uuid: e293d66a-0025-4230-997e-295ce4625713
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 6%

---


# buildCountingCollection網站方法{#buildcountingcollection-site-method}

傳回實例化為計數類型的Collection物件。 從Collection物件執行create_or_update()以完成建置程式。

| 變數 | 類型 | 說明 |
|--- |--- |--- |
| title | 字串 | 系列的標題。 |
| articleId | 字串 | 您選擇用來識別網站內系列的唯一文章ID。 |
| url | 字串 | 此系列的標準絕對URL。 |

## Java示例{#section_nyl_ycs_rz}

```
Collection collection = site.buildCountingCollection(title, articleId, url); 
```

## NodeJS示例{#section_xkd_gds_rz}

```
var collection = site.buildCountingCollection(title, articleId, url); 
```

## PHP示例{#section_ghf_gds_rz}

```
$collection = site->buildCountingCollection(title, articleId, url); 
```

## Python示例{#section_dwg_gds_rz}

```
collection = site.build_counting_collection(title, articleId, url) 
```

## Ruby示例{#section_enh_gds_rz}

```
collection = site.build_counting_collection(title, articleId, url) 
```

