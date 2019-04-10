---
description: 重新定位頁面上的Livefyre標誌。
seo-description: 重新定位頁面上的Livefyre標誌。
seo-title: 移動Livefyre標誌
solution: Experience Manager
title: 移動Livefyre標誌
uuid: 807304ae-6070-4505-87db-169a925f714c
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 移動Livefyre標誌{#move-the-livefyre-logo}

重新定位頁面上的Livefyre標誌。

如果您與Livefyre的合約允許，您可以將Livefyre標誌從內容串流頂端移至底部。

例如，在包含Livefyre應用程式的元素後面，立即新增下列HTML至您的頁面：

```
<div id="powered_by_livefyre_new"><a href="https://livefyre.com" target="_blank">Powered by Livefyre</a></div>
```

然後，將下列項目新增至頁面的樣式表：

```
/* Hide the top logo */ 
.fyre-widget .fyre-logo-drop, .fyre-widget .fyre-logo-help, .fyre-widget .fyre-help { 
    display:none !important; 
} 
  
/* Style the bottom logo */ 
#powered_by_livefyre_new a {    background: url(https://cdn.livefyre.com/libs/fyre.conv/v3.0.0/images/poweredbylivefyre.png) no-repeat left top; 
    display: block; 
    height: 24px; 
    font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
} 
#powered_by_livefyre_new a:hover { 
    text-decoration: underline; 
}
```

