---
description: 透過遵循類似核心應用程式的程式來整合Sidesars應用程式。
title: Sides Integration
exl-id: 368951b1-fef2-46d8-b89c-68c46962e937
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---

# Sides Integration{#sidenotes-integration}

透過遵循類似核心應用程式的程式來整合Sidesars應用程式。

一般而言，如果您的核心應用程式整合完成，為產生`collectionMeta`物件所撰寫的程式碼可能會重複用於Sidestroms。

您也可以在（可選）`authDelegate`欄位中，將使用`fyre.conv`建立的`auth`委派提供給Sides，以重複使用現有的`auth`委派。

>[!NOTE]
>
>Sidesform可讓您將`network`、`siteId`和`articleId`加入單一物件中，而不需在建構函式的其他部分中個別傳遞。

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

如「建立`collectionMeta`」區段中所述，`collectionMeta`是編碼的JSON物件。 在上述範例中，JSON物件在進行JWT編碼前會採用下列格式。

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

如需詳細資訊，請參閱`collectionMeta`代號。

## 行動裝置設定

Sides已最佳化，可用於行動裝置。 為獲得行動版Livefyre應用程式的最佳效果，請將使用者可縮放選項設為no。 例如：

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
