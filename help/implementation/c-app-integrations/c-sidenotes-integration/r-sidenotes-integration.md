---
description: 透過遵循類似核心應用程式的程式，整合Sidesars應用程式。
seo-description: 透過遵循類似核心應用程式的程式，整合Sidesars應用程式。
seo-title: Sides Integration
solution: Experience Manager
title: Sides Integration
uuid: 4aa14ada-402a-482d-b43e-96f37afa6c53
translation-type: tm+mt
source-git-commit: fcee9dc152e7f8284e64248fdcc5bf81d39618ff

---


# Sides Integration{#sidenotes-integration}

透過遵循類似核心應用程式的程式，整合Sidesars應用程式。

一般而言，如果您的核心應用程式整合完成，為產生物件所撰寫的程式碼可 `collectionMeta` 能會重複用於Sidestraps。

您也可以在（可選）欄 `auth` 位中，提供以Sides `auth` 建立 `fyre.conv` 的委派，以重複使用現有委派 `authDelegate` 。

>[!NOTE]
>
>Sidesars可讓您將、 `network``siteId`和 `articleId` 包含在單一物件中，而不需在建構函式的其他部分中個別傳遞。

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

如「建立」區段 `collectionMeta` 中所 `collectionMeta` 述，是編碼的JSON物件。 在上述範例中，JSON物件在進行JWT編碼前會採用下列格式。

```
{ 
"title":"Client Solutions Sidenotes", 
"url":"http:\/\/www.livefyre.com\/sidenotes", 
"articleId":"sidenotes_sample", 
"siteId":"304059", 
"type":"sidenotes" 
}
```

如需詳細資訊，請參閱 `collectionMeta` Token。

## 行動裝置設定

Sides已最佳化，可用於行動裝置。 為獲得行動版Livefyre應用程式的最佳效果，請將使用者可縮放選項設為no。 例如:

```
<meta name="viewport" content="width=device-width, user-scalable=no">
```
