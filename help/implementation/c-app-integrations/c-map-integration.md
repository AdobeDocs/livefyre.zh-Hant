---
description: 將使用者內容繪制到互動式地圖上。
seo-description: 將使用者內容繪制到互動式地圖上。
seo-title: 地圖
solution: Experience Manager
title: 地圖
uuid: 1c3e399d-a610-4b80-a3 b2-a5502 b31480 d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 地圖{#map}

將使用者內容繪制到互動式地圖上。

地圖可讓您將地理位置的內容串流化在世界地圖上，讓您在最新消息或即時活動中找到社交熱門話題。所有適用內容將會顯示，包括文字、留言、像片和推文。

>[!NOTE]
>
>地圖由 [© openStreetMap](https://www.openstreetmap.org/copyright)提供，它提供Livefyre用來演算地圖的資料。

## 整合 {#section_w2m_db2_d1b}

使用地圖最快的方法就是使用Livefyre的CDN代管的版本。

首先，將 [Livefyre. js](https://github.com/Livefyre/Livefyre.js) 新增至您的頁面。

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

然後，定位Map App將顯示的元素。

```
<div id="map" style="height: 500px;"></div>
```

最後，使用Livefyre來建立地圖，並讓系列從簡化-sdk中插入管道。請記住，地圖只能顯示具有地理圍欄中繼資料的內容。Twitter和Instagram組織支援此功能。若要確保最佳效能，請在所有的Collect規則中加入地理位置篩選。

```
<script> 
Livefyre.require(['streamhub-map#1', 'streamhub-sdk#2'], 
function (Map, SDK) { 
    var map = new Map({ 
        el: document.getElementById('map') 
    }); 
    var collection = new SDK.Collection({ 
        network: 'strategy-prod.fyre.co', 
        siteId: 340628, 
        articleId: 'custom-1389845009515' 
    }); 
    collection.pipe(map); 
}); 
</script>
```

查看這 [個即時範例](https://codepen.io/cheung31/pen/wkmbF)。

## 設定 {#section_jc5_gxb_c1b}

`initial`

從系列載入並顯示在地圖上的初始項目數。載入此數目後，使用者可按一下按鈕以顯示更多。(可選)。預設為50。)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

傳遞至基礎 [Leaflet](https://leafletjs.com/) 地圖的選項，地圖會用來演算。使用此選項可設定 [「宣傳單地圖選項](https://leafletjs.com/reference.html#map-options)」，包括地圖的初始中心點，以及初始和最大縮放等級。(可選)。

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```

