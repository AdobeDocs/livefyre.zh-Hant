---
description: 傳回實例化為聊天類型的Collection物件。 從Collection物件執行create_or_update()以完成建置程式。
seo-description: 傳回實例化為聊天類型的Collection物件。 從Collection物件執行create_or_update()以完成建置程式。
seo-title: buildChatCollection網站方法
solution: Experience Manager
title: buildChatCollection網站方法
uuid: 39ee32d0-29c9-47a8-a458-a3cf7a96db30
translation-type: tm+mt
source-git-commit: 2908c6988c706a49c391f0e607bb641bce3a7f0d

---


# buildChatCollection網站方法{#buildchatcollection-site-method}

傳回實例化為聊天類型的Collection物件。 從Collection物件執行create_or_update()以完成建置程式。

| 變數 | 類型 | 說明 |
|--- |--- |--- |
| title | 字串 | 系列的標題。 |
| articleId | 字串 | 您選擇用來識別網站內系列的唯一文章ID。 |
| url | 字串 | 此系列的標準絕對URL。 |

## Java示例 {#section_nyl_ycs_rz}

```
Collection collection = site.buildChatCollection(title, articleId, url); 
```

## NodeJS範例 {#section_xkd_gds_rz}

```
var collection = site.buildChatCollection(title, articleId, url); 
```

## PHP範例 {#section_ghf_gds_rz}

```
$collection = site->buildChatCollection(title, articleId, url); 
```

## Python示例 {#section_dwg_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url) 
```

## Ruby示例 {#section_enh_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url)
```
