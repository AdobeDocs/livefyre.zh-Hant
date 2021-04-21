---
description: 將自訂動作新增至您的Livefyre應用程式。
title: 新增自訂按鈕
exl-id: a62d8605-59c2-4214-af26-805c1989aca1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# 新增自訂按鈕{#add-custom-buttons}

將自訂動作新增至您的Livefyre應用程式。

Livefyre可讓您在內容的現有動作按鈕（例如&#x200B;**[!UICONTROL Share]**&#x200B;和&#x200B;**[!UICONTROL Flag]**）旁新增自訂按鈕。

使用mobile引數來定義按鈕是否會顯示在行動裝置上。

例如，若要為行動裝置介面新增自訂動作按鈕：

```
var convConfig = {...}; // Should have siteId, articleId, etc. 
convConfig.actionButtons = [ 
   { 
      mobile: true,  
      // (optional) sets whether the button will appear on mobile devices 
      key: 'Do Something', 
      callback: function(contentInfo) { 
         console.log('Author of content is ' + contentInfo.authorId); 
         console.log('id of content is ' + contentInfo.contentId); 
      } 
   }, 
    ... 
]; 
  
fyre.conv.load(networkConfig, [convConfig]);
```

1. 在名為actionButtons的ConvConfig物件中傳遞額外的引數，其中包含一組物件，以說明您要新增的每個按鈕。
1. 定義要針對每個按鈕顯示的文字索引鍵。
1. 新增回呼，此回呼將針對每個按鈕的點按事件被呼叫。

回呼由具有兩個鍵的對象調用：`authorId`和`contentId`。
