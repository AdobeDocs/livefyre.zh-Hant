---
description: 使用 .js 實作來實作 Sidenotes.
seo-description: 使用 .js 實作來實作 Sidenotes.
seo-title: Sitdones實施
solution: Experience Manager
title: Sitdones實施
uuid: aa13852e-e2 b0-4a86-97cd-d08 ab5 e cfab
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Sitdones實施{#sidenotes-implementation}

## 使用 .js 實作來實作 Sidenotes

若要實施此功能，請傳遞您要覆寫至Javascript組態物件之字串的1-1物件對應。如果您未提供欄位，則會使用預設文字。

### 範例

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
