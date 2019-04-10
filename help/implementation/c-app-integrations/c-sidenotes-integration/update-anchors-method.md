---
description: 用來提升網站上Livefyre能力的核心Livefyre庫。
seo-description: 用來提升網站上Livefyre能力的核心Livefyre庫。
seo-title: UpdateCHANchers方法
solution: Experience Manager
title: Livefyre. js
uuid: null
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# UpdateCHANchers方法 {#updateAnchorsMethod}

使用UpdateCHarchs方法，動態新增已顯示的內容至頁面。

此方法對分頁很有用，或在動態消息中動態新增sidenote內容的情況下。此方法會定義符合元素的新錨點，並使用單一引數：新選擇器。

**新選擇器**。要新增至SiteNotes的選擇器。這可以是選擇器字串、jQuery物件或元素陣列(在應用程式建構期間傳遞的選擇器引數所接受的類型中)。
格式：

```
app.updateAnchors(newSelectors);
```

範例:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
