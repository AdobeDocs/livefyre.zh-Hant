---
description: 允許使用者從單一頁面版面和URL點進「系列」。
seo-description: 允許使用者從單一頁面版面和URL點進「系列」。
seo-title: 變更系列
solution: Experience Manager
title: 變更系列
uuid: 81c8a554-375f-4659-9e25-5b3618824633
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# 變更系列{#change-collection}

允許使用者從單一頁面版面和URL點進「系列」。

當Livefyre應用程式已載入時，使用「變更系列委派」來變更頁面上顯示的系列，而不變更URL。 使用此功能可顯示像片或視訊收藏館，或其他應用程式，在使用者動作後顯示的系列應該會變更。

例如，按一下圖庫中的影片或像片會載入該選取範圍專屬的「系列」，而頁面的URL則不會變更。

若要從單一頁面[載入三個系列中的其中一個](../c-advanced-topics/t-display-comment-count.md#t_display_comment_count):

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
