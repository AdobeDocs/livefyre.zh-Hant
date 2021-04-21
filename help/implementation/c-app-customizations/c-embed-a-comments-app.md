---
description: 內嵌注釋應用程式會遵循內嵌核心應用程式的程式。
title: 內嵌注釋應用程式
exl-id: 5eb191f8-ee52-4a9d-9180-90457a49fd4e
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---

# 內嵌注釋應用程式{#embed-a-comments-app}

內嵌注釋應用程式會遵循內嵌核心應用程式的程式。

內嵌注釋應用程式會遵循內嵌核心應用程式（如[內嵌應用程式](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)所述）的程式

## 範例

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: 'domainName' 
    }; 
    var convConfig = { 
      siteId: 'siteId', 
      articleId: 'articleId', 
      el: 'livefyre', 
      collectionMeta: 'collectionMeta', 
      checksum: 'checksum' 
    }; 
    
    Livefyre.require(['fyre.conv#3', 'auth'], function(Conv, auth) { 
        new Conv(networkConfig, [convConfig], function(commentsWidget) {}); 
        auth.delegate({ 
            login: function (callback) { 
                callback(null,{livefyre:'<userauthtoken>'}); 
            }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

如「建立系列元」區段中所述，CollectionMeta是編碼的JSON物件。 在上述範例中，JSON物件在進行JWT編碼前會採用下列格式：

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```
