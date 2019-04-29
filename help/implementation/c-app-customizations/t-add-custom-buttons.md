---
description: 將自訂動作新增至Livefyre應用程式。
seo-description: 將自訂動作新增至Livefyre應用程式。
seo-title: 新增自訂按鈕
solution: Experience Manager
title: 新增自訂按鈕
uuid: 27d24c21-d83 f-49df-3b3 f-15d7 abbd2 bd7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 新增自訂按鈕{#add-custom-buttons}

將自訂動作新增至Livefyre應用程式。

Livefyre可讓您在內容的現有動作按鈕(例如 **[!UICONTROL Share]**，和 **[!UICONTROL Flag]** )上新增自訂按鈕。

使用行動引數來定義按鈕是否將顯示在行動裝置上。

例如，為您的行動裝置介面新增自訂動作按鈕：

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

1. 在您的Config物件中傳遞另一個名為ActionButton的引數，其中包含一組物件，說明您要新增的每個按鈕。
1. 定義要顯示每個按鈕之文字的索引鍵。
1. 新增將在每個按鈕的點擊事件上叫用的回呼。

回呼會以兩個索引鍵呼叫物件： `authorId``contentId`以及
