---
description: 允許使用者從單一頁面版面和URL點進系列。
seo-description: 允許使用者從單一頁面版面和URL點進系列。
seo-title: 變更系列
solution: Experience Manager
title: 變更系列
uuid: 69bafcc7-c55 e-47d6-bc79-b0 db80 fdf138
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 變更系列{#change-collection}

允許使用者從單一頁面版面和URL點進系列。

使用「變更系列委派」變更頁面上顯示的Collection，而不會變更URL，而Livefyre應用程式已載入。使用此功能可顯示像片或影片收藏館，或其他顯示的「應用程式」在使用者動作後應變更的其他應用程式。

例如，按一下收藏館中的影片或像片會載入特定於該選項的「系列」，而頁面的URL則不會變更。

從 [單一注釋計數](/help/implementation/c-advanced-topics/t-display-comment-count.md) 頁面載入三個系列之一：

```
<html> 
<head> 
<script src='//cdn.livefyre.com/Livefyre.js'></script> 
</head> 
<body> 
<script type="text/javascript"> 
convConfig1 = {"collectionMeta": <COLLECTION META 1>, 
             "checksum": <CHECKSUM 1>, 
             "siteId": <SITE ID>, 
             "articleId":"1", 
             "el":"livefyre"}; 
convConfig2 = {"collectionMeta": <COLLECTION META 2>, 
             "checksum": <CHECKSUM 2>, 
             "siteId": <SITE ID>, 
             "articleId":"2", 
             "el":"livefyre"}; 
convConfig3 = {"collectionMeta": <COLLECTION META 3>, 
             "checksum": <CHECKSUM 3>, 
             "siteId": <SITE ID>, 
             "articleId":"3", 
             "el":"livefyre"}; 
  
Livefyre.require(['fyre.conv#prod'],function(Conv) { 
    new Conv({"network": "<NETWORK NAME>"}, 
    [convConfig1], 
    function(app) {  
        window.changeConv = app.changeCollection; 
    } 
    ); 
}); 
</script> 
  
<div id="livefyre"></div> 
<button onclick="window.changeConv(convConfig1);">Conv 1</button> 
<button onclick="window.changeConv(convConfig2);">Conv 2</button> 
<button onclick="window.changeConv(convConfig3);">Conv 3</button> 
</body> 
</html>
```

