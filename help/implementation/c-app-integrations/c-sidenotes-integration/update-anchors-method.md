---
description: 用來為您網站上的Livefyre提供動力的核心Livefyre程式庫。
seo-description: 用來為您網站上的Livefyre提供動力的核心Livefyre程式庫。
seo-title: updateAnchors方法
solution: Experience Manager
title: Livefyre.js
uuid: null
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 1%

---


# updateAnchors方法{#updateAnchorsMethod}

使用updateAnchors方法，動態地將表示的內容新增至頁面。

此方法適用於分頁，或在動態將可顯示內容新增至頁面的其他情況下。 此方法會為相符的元素定義新的錨點，並使用單一引數：newSelectors。

**newSelectors**。要添加到Sidestrap的選擇器。 這可以是選擇器字串、jQuery物件或元素陣列（應用程式建構期間傳遞的選擇器參數所接受的任何類型）。
格式:

```
app.updateAnchors(newSelectors);
```

範例:

```
var app = new Livefyre.Sidenotes(convConfig);// Load more contentapp.updateAnchors('#content');
```
