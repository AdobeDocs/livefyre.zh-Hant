---
description: 使用 .js 實作來實作 Sidenotes.
seo-description: 使用 .js 實作來實作 Sidenotes.
seo-title: Sides Implementation
solution: Experience Manager
title: Sides Implementation
uuid: aa13852e-e2b0-4a86-97cd-d08ab5e2cfab
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 28%

---


# Siestroms Implementation{#sidenotes-implementation}

## 使用 .js 實作來實作 Sidenotes

若要實作此功能，請傳入您要覆寫之字串的1-1物件對應至Javascript設定物件。 如果您未提供欄位，則會使用預設文字。

### 範例

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
