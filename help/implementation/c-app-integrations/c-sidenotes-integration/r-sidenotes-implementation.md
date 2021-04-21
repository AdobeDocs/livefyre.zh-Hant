---
description: 使用 .js 實作來實作 Sidenotes.
title: Sides Implementation
exl-id: 07a68677-c67e-4128-8cb7-c5fb9e0ecc60
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 22%

---

# Siestroms Implementation{#sidenotes-implementation}

## 使用 .js 實作來實作 Sidenotes

若要實作此功能，請傳入您要覆寫之字串的1-1物件對應至Javascript設定物件。 如果您未提供欄位，則會使用預設文字。

### 範例

```
var customStrings = { postAsButton: "New Post As Text", postEditButton: "New Post Edit Text"};networkConfig["strings"] = customStrings; fyre.conv.load( networkConfig, [convConfig], function(){});
```
