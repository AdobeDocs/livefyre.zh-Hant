---
description: 在「@提及功能下拉式選單」中變更 Livefyre 使用者的圖示。
title: 變更 @提及功能的圖示
exl-id: e078ef7f-7f16-4f5d-9152-95ae7fe7e4bd
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 19%

---

# 變更`@mention`圖示{#change-mention-icon}

在`@mention`下拉式選單中，變更Livefyre使用者所顯示的圖示。

將`@mention`下拉式選單中使用的Livefyre圖示變更為您選擇的圖示，讓您使用自己的圖示來指示社群成員。

## 範例

若要變更此圖示，請新增下列CSS至您的樣式表。 將您的資源&#x200B;*url取代為已選取取代預設Livefyre標章之影像的URL。*

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
