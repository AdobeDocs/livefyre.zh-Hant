---
description: 在您的網站或網路上展示最活躍的系列。
seo-description: 在您的網站或網路上展示最活躍的系列。
seo-title: 趨勢分析
solution: Experience Manager
title: 趨勢分析
uuid: 3031523d-b487-4ea-bba6-1d8 f9971874 f
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 趨勢分析{#trending}

在您的網站或網路上展示最活躍的系列。

使用趨勢來展示「網站」或「網路」中最新活動的系列。

## 整合 {#section_wtz_whb_c1b}

要與Trending整合最快的方式，就是使用Livefyre的CDN代管的版本。

首先，將 [Livefyre. js](https://github.com/Livefyre/Livefyre.js) 新增至您的頁面。

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

然後，定位應用程式出現的元素。

```
<div id="trending"></div>
```

最後，使用 `Livefyre.require` 建構元件。

```
<script> 
Livefyre.require([ 
   'streamhub-hot-collections#0' 
], function(Trending) {     
   var app = new Trending({ 
      el: document.getElementById("trending"), 
      network: 'livefyre.com' 
   }); 
   app.start(); 
}); 
</script>
```

您現在有一個趨勢應用程式！在 [此範例](https://codepen.io/gobengo/pen/GijEy)中檢視這一切的實際運作。

## 設定 {#section_k5k_qhb_c1b}

`network`

將提取系列的網路。(必要。)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

提供網站ID，只顯示網路內單一網站的系列。(可選)。

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

提供單一系列標籤，只顯示具有該標記的系列。(可選)。

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```

