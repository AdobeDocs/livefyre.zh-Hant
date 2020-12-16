---
description: 變更 @mention 功能下拉式選單中 Livefyre 使用者的圖示。
seo-description: 在「@提及功能下拉式選單」中變更 Livefyre 使用者的圖示。
seo-title: 變更 @提及功能的圖示
solution: Experience Manager
title: 變更 @mention 圖示
uuid: a395f4ff-a774-454a-8d94-4a3371d8cc2c
translation-type: tm+mt
source-git-commit: 0d2ff61b1db6100de1d59e6e20c1175f015a78c5
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 31%

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
