---
description: 展示您網站或網路上最活躍的系列。
title: 趨勢分析
exl-id: a3129e95-90e7-4107-bfd9-ed3b0dce20aa
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 5%

---

# 趨勢分析{#trending}

展示您網站或網路上最活躍的系列。

使用趨勢分析可展示您網站或網路中具有最新活動的系列。

## 整合 {#section_wtz_whb_c1b}

與趨勢整合的最快方式，就是使用Livefyre CDN上代管的內建版本。

首先，將[Livefyre.js](https://github.com/Livefyre/Livefyre.js)新增至您的頁面。

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

然後，定位應用程式將出現的元素。

```
<div id="trending"></div>
```

最後，使用`Livefyre.require`來建構元件。

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

您現在有趨勢應用程式！ 請參閱[此範例](https://codepen.io/gobengo/pen/GijEy)中的所有實際運作。

## 設定 {#section_k5k_qhb_c1b}

`network`

提取系列的網路。 (必填.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com' 
});
```

`siteId`

提供網站ID，僅顯示網路內單一網站的系列。 (可選.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4 
});
```

`tag`

提供單一「系列」標籤，僅顯示具有該標籤的「系列」。 (可選.)

```
var trending = new Trending({ 
   el: document.getElementById('trending'), 
   network: 'livefyre.com', 
   siteId: 4, 
   tag: 'basketball' 
});
```
