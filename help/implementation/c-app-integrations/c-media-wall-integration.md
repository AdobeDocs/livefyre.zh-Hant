---
description: 建立即時串流內容的媒體牆。
seo-description: 建立即時串流內容的媒體牆。
seo-title: 媒體牆
solution: Experience Manager
title: 媒體牆
uuid: c6087c80-a35b-44d2-9dd4-ba9cd471172d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---


# 介質牆{#media-wall}

建立即時串流內容的媒體牆。

「媒體塗鴉牆」可讓您為網站建立即時的社交塗鴉牆。 使用Livefyre JavaScript SDK的串流桌布套件，將Livefyre社交動態消息顯示為視覺化、全螢幕、並排的內容體驗，非常適合於報導即時活動、主持像片競賽，並為您網站的社交區段提供動力。

## 整合 {#section_jfm_bwb_c1b}

新增媒體塗鴉牆最快的方式，就是使用Livefyre CDN上代管的內建版本。

首先，將[Livefyre.js](https://github.com/Livefyre/Livefyre.js)新增至您的網站。

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
```

然後，定位將顯示介質牆的元素。

```
<div id="wall"></div>
```

最後，使用`Livefyre.require`來建構元件。

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

你現在有牆了！ 請參閱[此範例](https://codepen.io/gobengo/pen/dFwDL)中的所有實際運作。

**是否點擊錯誤？** 請檢查，以確定您正在傳遞正確的環境參數。選項包括`livefyre.com`（生產）或`t402.livefyre.com`(UAT)。

>[!NOTE]
>
>您的媒體塗鴉牆應用程式所呈現之推文的任何樣式自訂，都必須依照Twitter的「顯示要求」[進行。](https://dev.twitter.com/terms/display-requirements)

## 配置選項{#section_ucv_qvb_c1b}

`columns`

可讓您在建立塗鴉牆時，定義媒體牆的欄數。 如果設定此選項，則每欄的寬度會自動調整為媒體塗鴉牆的容器大小，同時維持指定的欄數。

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5 
});
```

`initial`

載入頁面時要演算的內容項目數。 預設為50。

```
var wallView = new MediaWall({ 
   el: document.getElementById('wall'), 
   initial: 10 
});
```

`minContentWidth`

可讓您在「媒體牆」容器元素中設定每欄的最小（像素）寬度。 (您的「媒體牆」會根據容器元素的寬度自動選取適當的欄數。 依預設，「媒體牆」的寬度除以最小內容寬度（若未定義，則為300像素）會決定欄數。)

>[!NOTE]
>
>請勿將此選項與columns選項組合使用。

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    minContentWidth: 300 
});
```

`modal`

依預設，當內容有附件時，「媒體牆」會顯示可點選的縮圖。 當按一下時，應用程式會開啟一個模型，顯示整個像片／視訊附件。 若要停用此選項，請將modal設為false。

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    columns: 5, 
    modal: false 
});
```

`postButton`

定義要顯示在塗鴉牆上的[!UICONTROL Post Content]按鈕。 此選項要求您傳入`opts.collection`，並新增Livefyre.js Auth整合至頁面。

`postButton` 參數:

* `false` （預設值）:請勿顯示「貼文內容」按鈕。（建立只讀介質牆。）
* `true` (或 `LiveMediaWall.postButtons.contentWithPhotos`):加入按鈕，讓使用者可新增文字內容及附加的像片。

* `LiveMediaWall.postButtons.content`:加入可讓使用者新增文字內容，但不附加像片的按鈕。
* `LiveMediaWall.postButtons.photo`:加入可讓使用者新增像片但無文字的按鈕。

```
var wallView = new MediaWall({ 
    el: document.getElementById('wall'), 
    collection: collection, 
    postButton: true, 
    minContentWidth: 300 
});
```

`showMore`

定義當您的[!UICONTROL Show More]按鈕被點按時要新增至塗鴉牆的內容項目數。

```
var wallView = new LiveMediaWall({ 
    el: document.getElementById('wall'), 
    showMore: 10 
});
```

## 樣式配置選項{#section_ztv_dvb_c1b}

Media Wall也提供數種設定選項，可讓您自訂文字色彩、樣式和大小。 若要實作這些選項，請使用下列語法：

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

如需有效輸入，請參閱CSS [字型系列](https://www.w3.org/TR/CSS2/fonts.html#propdef-font-family)、[字型大小](https://www.w3.org/TR/CSS2/fonts.html#font-size-props)、[行高、](https://www.w3.org/TR/CSS2/visudet.html#propdef-line-height)和[Color](https://www.w3.org/TR/css3-color/#colorunits)屬性的W3C標準。

* **bodyFontSize** *（CSS字型大小字串）內* 容內文的字型大小。

* **bodyLineHeight** *（CSS線條高度字串）內* 容內文的線條高度。

* **buttonActiveBackgroundColor** *（CSS色彩字串）**作用中按鈕背景的色彩。

* **buttonBorderColor** *（CSS色彩字串）**按鈕邊框的色彩。

* **buttonHoverBackgroundColor** *（CSS色彩字串）暫* 留時按鈕背景的色彩。

* **buttonTextColor** *（CSS色彩字串）* 按鈕標籤的色彩。

* **cardBackgroundColor** *（CSS色彩字串）* 媒體塗鴉牆內容卡片的背景色彩。

* **displayNameColor** *（CSS色彩字串）* 位元中顯示名稱的色彩。

* **fontFamily** *（CSS字型系列字串）內* 文的字型系列。

* **footerTextColor** *（CSS色彩字串）* 次要文字的色彩（例如頁尾文字和位元中的使用者名稱）。

* **linkAttachmentBackgroundColor** *（CSS色彩字串）連* 結附件（堆疊附件）的背景色彩。

* **linkAttachmentBorderColor** *（CSS色彩字串）連* 結附件（堆疊附件）的邊框色彩。

* **linkAttachmentTextColor** *（CSS色彩字串）連結* 附件文字的色彩。

* **linkColor** *（CSS色彩字串）超* 連結的色彩（例如內文中的連結和顯示名稱連結）。

* **textColor** *（CSS色彩字串）* 內文的色彩。

* **titleFontSize** *（CSS字型大小字串）內* 容標題的字型大小。

* **titleLineHeight** *（CSS線條高度字串）內* 容標題的線條高度。

* **sourceLogoColor** *（CSS色彩字串）* 來源標誌的色彩。

* **usernameColor** *（CSS顏色字串）* 位元中使用者名稱的顏色。
