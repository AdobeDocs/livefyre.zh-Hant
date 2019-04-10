---
description: 變更 @mention 功能下拉式選單中 Livefyre 使用者的圖示。
seo-description: 在「@提及功能下拉式選單」中變更 Livefyre 使用者的圖示。
seo-title: 變更 @提及功能的圖示
solution: Experience Manager
title: 變更 @mention 圖示
uuid: a395f4ff-a774-454a-8d94-4a3371 d8 c
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 變更 `@mention` 圖示 {#change-mention-icon}

變更 `@mention` 下拉式選單中Livefyre使用者的顯示圖示。

將 `@mention` 下拉式選單中使用的Livefyre圖示變更為您所選擇的圖示，讓您可以用自己的圖示指出社群成員。

## 範例

若要變更此圖示，請將下列CSS新增至您的樣式表。將<*您的資源*> URL取代為所選影像的URL，以取代預設的Livefyre徽章。

```
.fyre-editor-container .fyre-editor-toolbar > .fyre-mention-menu .fyre-mention-item .fyre-mention-item-livefyre { 
    background: url(<your resource url>) no-repeat center; 
    background-position: 0px 0px; 
    background-size: 22px 22px; 
}
```
