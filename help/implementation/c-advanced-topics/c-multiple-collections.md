---
description: 在單一頁面上展示多個系列。
seo-description: 在單一頁面上展示多個系列。
seo-title: 多個系列
solution: Experience Manager
title: 多個系列
uuid: 9675ffd7-1a59-42a1-b3 ba-40af1744 CFD1
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# 多個系列 {#multiple-collections}

在單一頁面上展示多個系列。

您可以在網站上的單一頁面上包含多個系列。例如，若要發佈事件，您可以在事件中進行即時部落格或聊天討論，並在頁面一側使用個別的應用程式，從社交網路顯示相關的組織內容。或者，您可以在文章下方加入「注釋應用程式」，並附帶「聊天」。

若要在頁面上取得多個對話，請在陣列中新增一或多個設定，並將陣列傳送至載入呼叫。例如，

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
