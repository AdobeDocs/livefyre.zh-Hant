---
description: 遵循類似核心應用程式的程序，整合SiteNotes應用程式。
seo-description: 遵循類似核心應用程式的程序，整合SiteNotes應用程式。
seo-title: Sitdones整合
solution: Experience Manager
title: Sitdones整合
uuid: 4aa14a-402a-482d-b43 e-96f37 afa6 c53
translation-type: tm+mt
source-git-commit: fcee9dc152e7f8284e64248fdcc5bf81d39618ff

---


# Sitdones整合{#sidenotes-integration}

遵循類似核心應用程式的程序，整合SiteNotes應用程式。

一般規則是，如果您的核心應用程式整合完成，則要產生該 `collectionMeta` 物件的程式碼可能會重復用於SiteNotes。

您也可以在(選用)欄位 `auth` 中提供使用SitedNotes建立的 `auth` 委派， `fyre.conv` 以重復使用現有委派 `authDelegate` 。

>[!NOTE]
>
>Sitenites可讓您包含 `network`、 `siteId`和 `articleId` 在單一物件中，而不是在建構函式的其他部分個別傳遞。

```
<!DOCTYPE html> 
<html> 
<head> 
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
</head> 
<body> 
<script type="text/javascript"> 
var convConfig = { 
 network: 'client-solutions.fyre.co', 
 selectors:'span.lyrics-sidenote', 
 siteId: '356373', 
 articleId: 'sidenotes-sample', 
 collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5zaWRlbm90ZXMtZGVtby5jb20vbHlyaWNzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAidHlwZSI6ICJzaWRlbm90ZXMiLCAiYXJ0aWNsZUlkIjogInNpZGVub3Rlc19zYW1wbGUiLCAidGl0bGUiOiAiQ2xpZW50IFNvbHV0aW9ucyBTaWRlbm90ZXMifQ.2gxnsM0TS8dfp-Jokb5uW1kuMl-DqIlqfJSCBwJgf1k' 
}; 
  
Livefyre.require(['sidenotes#1', 'auth'], function (Sidenotes, Auth) { 
 new Sidenotes(convConfig); 
 Auth.delegate({ 
 login: function (callback) { 
 callback(null,{livefyre:'<userauthtoken>'}); 
 } 
 }); 
 }); 
</script> 
</body> 
</html>
```

如「建立 `collectionMeta` 」區段中所示， `collectionMeta` 為編碼JSON物件。在上述範例中，JSON物件在JWT編碼之前採用下列格式。

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

如需詳細資訊，請參閱 `collectionMeta` 代號。

## 行動裝置設定

Sitents已最佳化，以便在行動裝置中使用。為獲得使用行動版Livefyre應用程式的最佳效果，請將使用者可縮放選項設為否。例如：

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
