---
description: 從您的應用程式移除標準Livefyre應用程式元件。
title: 隱藏應用程式元素
exl-id: f8bbed2c-d009-41b8-927d-8d6ac4a63571
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 1%

---

# 隱藏應用程式元素{#hide-app-elements}

從您的應用程式移除標準Livefyre應用程式元件。

使用CSS在您的頁面中隱藏預設的Livefyre應用程式元素，讓您自訂使用者體驗以符合您的需求。

若要隱藏應用程式中的元素，只需將顯示設為無即可。

範例:

```
/* Hide the 'reply' button */ 
.fyre-comment-reply { 
    display: none !important; 
} 
  
/* Hide all user avatars */ 
.fyre-comment-user .fyre-mention-item-avatar .fyre-listener-avatars .fyre-avatar fyre-user-avatar-25 { 
    display: none !important; 
} 
.fyre-comment-head .fyre-comment-body .fyre-comment-footer .fyre-comment-divider { 
    margin-left: 0; 
} 
  
/* Hide 'Edit Profile' link */ 
.fyre-edit-profile-link { 
    display: none !important; 
} 
  
/* Hide 'Logout' link */ 
.fyre-logout-link { 
    display: none; 
} 
  
/* Hide 'Comment Notifier' */ 
.fyre-notifier-message { 
    display:none; 
}
```
