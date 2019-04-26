---
description: 傳回「聊天」類型的系列物件。從Collection物件執行_ or_ update()以完成建置程序。
seo-description: 傳回「聊天」類型的系列物件。從Collection物件執行_ or_ update()以完成建置程序。
seo-title: BuildchatCollection網站方法
solution: Experience Manager
title: BuildchatCollection網站方法
uuid: 39ee32d0-29c9-47a8-a8-a458-a3 cf7 a96 db30
translation-type: tm+mt
source-git-commit: 2908c6988c706a49c391f0e607bb641bce3a7f0d

---


# BuildchatCollection網站方法{#buildchatcollection-site-method}

傳回「聊天」類型的系列物件。從Collection物件執行_ or_ update()以完成建置程序。

| 變數 | Type | 說明 |
|--- |--- |--- |
| title | 字串 | 系列的標題。 |
| articleID | 字串 | 您選擇在您的網站內識別系列的唯一文章ID。 |
| url | 字串 | 此系列的標準絕對URL。 |

## Java範例 {#section_nyl_ycs_rz}

```
Collection collection = site.buildChatCollection(title, articleId, url); 
```

## nodeJS範例 {#section_xkd_gds_rz}

```
var collection = site.buildChatCollection(title, articleId, url); 
```

## PHP範例 {#section_ghf_gds_rz}

```
$collection = site->buildChatCollection(title, articleId, url); 
```

## Python範例 {#section_dwg_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url) 
```

## Ruby範例 {#section_enh_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url)
```
