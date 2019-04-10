---
description: 建立媒體塗鴉牆，即時進行內容串流。
seo-description: 建立媒體塗鴉牆，即時進行內容串流。
seo-title: Media Wall
solution: Experience Manager
title: Media Wall
uuid: c6087c80-a35 b-44d2-9dd4-ba9 cd471172 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Media Wall{#media-wall}

建立媒體塗鴉牆，即時進行內容串流。

Media Wall可讓您建立網站的即時社交牆。使用Livefyre JavaScript SDK的簡化套件，將Livefyre社交饋送顯示為視覺吸引人、全螢幕、拼貼的內容體驗，這種體驗非常適合用於涵蓋即時活動、代管像片比賽以及賦予網站的社交區段。

## 整合 {#section_jfm_bwb_c1b}

新增Media塗鴉牆最快的方法，就是使用Livefyre的CDN代管的版本。

首先，將 [Livefyre. js](https://github.com/Livefyre/Livefyre.js) 新增至您的網站。

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

然後，定位Media塗鴉牆所在的元素。

```
<div id="wall"></div>
```

最後，使用 `Livefyre.require` 建構元件。

```
<script> 
Livefyre.require([ 
    'streamhub-wall#5' 
], function(MediaWall) {     
    var wall = window.wall = new MediaWall({ 
        el: document.getElementById("wall"), 
        collection: { 
            "network": "client-solutions.fyre.co", 
            "siteId": "364309", 
            "articleId": "answers-mediawall" 
        } 
    }); 
}); 
</script>
```

您現在有了塗鴉牆！在 [此範例](https://codepen.io/gobengo/pen/dFwDL)中檢視這一切的實際運作。

**點擊錯誤？** 請檢查以確定您傳遞正確的環境參數。選項包括 `livefyre.com` (生產)或 `t402.livefyre.com` (UAT)。

>[!NOTE]
>
>您的媒體塗鴉牆應用程式演算推文的任何樣式自訂，都必須依照Twitter [的顯示需求](https://dev.twitter.com/terms/display-requirements)進行。

## 設定選項 {#section_ucv_qvb_c1b}

`columns`

可讓您定義「媒體牆」建立塗鴉牆時的欄數。如果設定此選項，每欄的寬度會自動配合Media塗鴉牆的容器大小調整，同時維持指定的欄數。

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5 
});
```

`initial`

在頁面載入時演算的內容項目數目。預設為50。

```
var wallView = new MediaWall({ 
   el: document.getElementById('wall'), 
   initial: 10 
});
```

`minContentWidth`

可讓您為媒體塗鴉牆物件元素內的每個欄設定最低(像素)寬度。(您的Media Wall會根據容器元素的寬度自動選取適當的欄數。依預設，Media Wall的寬度除以最低內容寬度(300px(若未定義)會決定欄數)。

>[!NOTE]
>
>請勿搭配欄選項使用此選項。

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    minContentWidth: 300 
});
```

`modal`

依預設，當內容有附件時，媒體塗鴉牆會顯示可點按的縮圖。在按下後，應用程式會開啓一個模型，顯示像片/視訊附件完整顯示。若要停用此選項，請將模式設為false。

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

定義 [!UICONTROL Post Content] 按鈕顯示在您的塗鴉牆上。此選項需要您傳入，並新增Livefyre. js `opts.collection`Ath整合至頁面。

`postButton` 參數：

* `false` (預設)：不要顯示「貼文內容」按鈕。(建立唯讀媒體塗鴉牆)。
* `true` (或 `LiveMediaWall.postButtons.contentWithPhotos`)：加入一個按鈕，讓使用者新增文字內容，並加上附加的像片。

* `LiveMediaWall.postButtons.content`：包含可讓使用者新增文字內容但不附加像片的按鈕。
* `LiveMediaWall.postButtons.photo`：包含可讓使用者新增像片但沒有文字的按鈕。

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

定義 [!UICONTROL Show More] 按下按鈕時，內容項目要新增至塗鴉牆的次數。

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## 樣式設定選項 {#section_ztv_dvb_c1b}

此外，Media Wall還提供一些設定選項，可讓您自訂文字色彩、樣式和大小。若要實施這些選項，請使用下列語法：

```
var wall2 = window.wall2 = new MediaWall({ 
   el: document.getElementById("listView1"), 
   collection: collection, 
   cardBackgroundColor: '#333', 
   textColor: 'magenta', 
   linkColor: 'orange', 
   footerTextColor: 'lime', 
   displayNameColor: 'cyan', 
   usernameColor: 'red', 
   fontFamily: 'Helvetica, Arial', 
   linkAttachmentBackgroundColor: '#555', 
   linkAttachmentBorderColor: '#888' 
}); 
```

如需有效輸入，請參閱W3C標準系列 [](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family)、 [字體大小](https://www.w3.org/TR/CSS2/fonts.html#font-size-props)、 [線條高度和](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height)[色彩](https://www.w3.org/TR/css3-color/#colorunits) 屬性的W3C標準。

* **boyFontSize***(CSS字型大小字串)* 內容內文文字的字型大小。

* **bodyLinheight***(CSS線條高度字串)* 內容內文文字的線條高度。

* **按鈕activeBackgroundColor***(CSS色彩字串)**作用中按鈕背景的顏色。

* **按鈕BorderColor***(CSS色彩字串)**按鈕邊框的顏色。

* **按鈕hoverbackgroundColor***(CSS色彩字串)* 滑鼠停留時按鈕背景的顏色。

* **按鈕textColor***(CSS色彩字串)* 按鈕標籤的顏色。

* **CardbackgroundColor***(CSS色彩字串)* 媒體塗鴉牆中內容卡片的背景顏色。

* **DisplayNameColor***(CSS色彩字串)* 在署名中顯示名稱的顏色。

* **FontFamily***(CSS字型系列字串)* 內文的字體系列。

* **頁尾色彩(***CSS色彩字串)* 次要文字的顏色(例如頁尾文字，以及署名中的使用者名稱)。

* **linktachmentBackgroundColor***(CSS色彩字串)* 連結附件(堆疊附件)的背景顏色。

* **linkAttachmentBorderColor***(CSS色彩字串)* 連結附件的邊框顏色(堆疊附件)。

* **linktachmentTextColor***(CSS色彩字串)* 連結附件文字的顏色。

* **linkColor***(CSS色彩字串)* 超連結的顏色(例如內文中的連結，以及顯示名稱連結)。

* **TextColor***(CSS色彩字串)* 內文文字的顏色。

* **titleFontSize***(CSS字型大小字串)* 內容標題的字型大小。

* **titleHeight***(CSS線條高度字串)* 內容標題的線條高度。

* **SourceLogocolor***(CSS色彩字串)* 來源標誌的顏色。

* **usernameColor***(CSS色彩字串)* 在署名中的使用者名稱顏色。
