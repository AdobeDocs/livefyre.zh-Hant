---
description: 使用Javascript事件監聽媒體塗鴉牆中發生的事件，並傳送至您所選擇的分析工具。
seo-description: 使用Javascript事件監聽媒體塗鴉牆中發生的事件，並傳送至您所選擇的分析工具。
seo-title: 媒體塗鴉牆的Javascript事件
solution: Experience Manager
title: 媒體塗鴉牆的Javascript事件
uuid: 8afc0529-4640-476a-b207-91b2 c70101 f0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 媒體塗鴉牆的Javascript事件{#javascript-events-for-media-wall}

使用Javascript事件監聽媒體塗鴉牆中發生的事件，並傳送至您所選擇的分析工具。

Livefyre提供JavaScript事件來追蹤Livefyre應用程式中的使用者活動。例如，您可能想要在使用者按贊或分享內容至Twitter或Facebook時更新頁面，或是在張貼新內容時更新頁面。

以下是如何接收事件的範例。以 `console.log` 您的程式碼取代，以便映射並傳送事件至您的分析整合(動態標籤管理、Adobe Analytics JS、Google Analytics等)：

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

支援的媒體塗鴉牆事件清單：

## 媒體塗鴉牆事件

| Event | 定義 |
|---|---|
| `Init` | 當媒體塗鴉牆包含在頁面上時。 |
| `Load` | 在頁面上載入媒體牆時，不論位置為何。 |
| `PostButtonClick` | 當使用者按一下媒體塗鴉牆上的「上傳按鈕」時。 |
| `RequestMore` | 當使用者在媒體塗鴉牆載入更多內容時。 |
| `TwitterReplyClick` | 當使用者從Media塗鴉牆按一下「Twitter回覆」按鈕時。 |
| `TwitterRetweetClick` | 當使用者從Media塗鴉牆按一下「Twitter回推」按鈕時。 |
| `TwitterLikeClick` | 當使用者按一下媒體塗鴉牆上的「Twitter贊/最愛」按鈕時。 |
| `ModalView` | 當使用者點按以檢視大型模式視窗中的媒體塗鴉牆內容時。 |
| `Like` | 當使用者按一下「媒體牆」中的「贊」按鈕時。 |
| `ShareButtonClick` | 每當使用者按下媒體塗鴉牆上的分享按鈕時。 |
| `ShareURL` | 「共用至URL」文字區域是從Media塗鴉牆選取/複製。 |
| `ShareFacebook` | 從Media塗鴉牆按一下「分享至Facebook」。 |
| `ShareTwitter` | 從Media塗鴉牆按一下「分享至Twitter」。 |
