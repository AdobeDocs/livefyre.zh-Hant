---
description: 內嵌評論應用程式會遵循內嵌核心應用程式的程序。
seo-description: 內嵌評論應用程式會遵循內嵌核心應用程式的程序。
seo-title: 內嵌注釋應用程式
solution: Experience Manager
title: 內嵌注釋應用程式
uuid: e4982ad3-cab1-4805-a55 c-594ca3 b7203
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 內嵌注釋應用程式{#embed-a-comments-app}

內嵌評論應用程式會遵循內嵌核心應用程式的程序。

內嵌評論應用程式遵循內嵌應用程式中所述核心應用程式 [的程序](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)

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

如「Building CollectionMeta」區段中所示，CollectionMeta是編碼的JSON物件。在上述範例中，JSON物件採用下列格式，JWT編碼之前：

```
{ 
"url": "articleUrl",  
"articleId": "articleId",  
"type": "livecomments",  
"title": "articleTitle" 
}
```

