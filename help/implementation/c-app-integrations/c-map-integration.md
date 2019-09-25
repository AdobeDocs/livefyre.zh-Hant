---
description: 將使用者內容繪製成互動式地圖。
seo-description: 將使用者內容繪製成互動式地圖。
seo-title: 地圖
solution: Experience Manager
title: 地圖
uuid: 1c3e399d-a610-4b80-a3b2-a5502b31480d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 地圖{#map}

將使用者內容繪製成互動式地圖。

Map可讓您將地理標籤內容串流至世界地圖，讓您找出有關最新消息或即時活動的社交熱門話題。 所有適用的內容都會顯示，包括文字、留言、像片和推文。

>[!NOTE]
>
>地圖由© openStreetMap [提供支援](https://www.openstreetmap.org/copyright),Livefyre用來呈現其地圖的資料。

## 整合 {#section_w2m_db2_d1b}

使用Map最快的方式是使用Livefyre CDN上代管的內建版本。

首先，將 [Livefyre.js新增至您的頁面](https://github.com/Livefyre/Livefyre.js) 。

```
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
```

然後，定位「地圖應用程式」將出現的元素。

```
<div id="map" style="height: 500px;"></div>
```

最後，使用Livefyre.require來建構地圖，並從streamhub-sdk取得要插入的集合。 請記住，「地圖」只能顯示含有地理標籤中繼資料的內容。 Twitter和Instagram組織支援此功能。 為確保最佳效能，請在系列的所有組織規則上加入地理位置篩選。

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

查看此即時 [範例](https://codepen.io/cheung31/pen/wkmbF)。

## 設定 {#section_jc5_gxb_c1b}

`initial`

從「系列」載入並顯示在地圖上的項目初始數。 載入此號碼後，使用者可以按一下按鈕以顯示更多。 (可選. 預設為50。)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    initial: 100 
});
```

`leafletMapOptions`

傳遞至基礎宣傳單地圖 [的選項](https://leafletjs.com/) ,Map會使用此圖來轉換。 使用此選項可設 [定宣傳單地圖選項](https://leafletjs.com/reference.html#map-options)，包括地圖的初始中心點，以及初始和最大縮放等級。 (可選.)

```
var map = new Map({ 
    el: document.getElementById('map'), 
    leafletMapOptions: { 
        center: [37.774, -122.4], 
        zoom: 15 
    } 
});
```

