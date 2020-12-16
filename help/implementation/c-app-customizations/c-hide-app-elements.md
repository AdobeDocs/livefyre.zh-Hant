---
description: 從您的應用程式移除標準Livefyre應用程式元件。
seo-description: 從您的應用程式移除標準Livefyre應用程式元件。
seo-title: 隱藏應用程式元素
solution: Experience Manager
title: 隱藏應用程式元素
uuid: ea090b6e-99f5-4bd7-aa9e-d39a4dff1543
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '67'
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

