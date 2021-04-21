---
description: 使用Javascript事件來監聽在媒體塗鴉牆中發生的事件，並將它們傳送至您選擇的分析工具。
title: 媒體塗鴉牆的Javascript事件
exl-id: 3fe76467-65e2-4f8b-bd75-5a2ffc3e7e15
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# 媒體塗鴉牆的Javascript事件{#javascript-events-for-media-wall}

使用Javascript事件來監聽在媒體塗鴉牆中發生的事件，並將它們傳送至您選擇的分析工具。

Livefyre提供JavaScript事件，可追蹤Livefyre應用程式中的使用者活動。 例如，當使用者按贊或分享內容至Twitter或Facebook，或是張貼新內容時，您可能想要更新頁面。

以下是如何接收事件的範例。 將`console.log`取代為您的程式碼，以映射事件並傳送至您的分析整合(動態標籤管理、Adobe AnalyticsJS、Google Analytics等):

```
document.body.addEventListener('insights', function (data) { 
 console.log('Received:', data.detail.type, data); 
});
```

支援的媒體塗鴉牆事件清單：

## 媒體塗鴉牆事件

| 事件 | 定義 |
|---|---|
| `Init` | 當頁面包含媒體塗鴉牆時。 |
| `Load` | 在頁面上載入媒體塗鴉牆時，不論位置。 |
| `PostButtonClick` | 當使用者按一下媒體塗鴉牆上的「上傳按鈕」時。 |
| `RequestMore` | 當使用者在媒體塗鴉牆中載入更多內容時。 |
| `TwitterReplyClick` | 當使用者按一下「媒體牆」上的「Twitter回覆」按鈕時。 |
| `TwitterRetweetClick` | 當使用者按一下「媒體塗鴉牆」上的「Twitter回推」按鈕時。 |
| `TwitterLikeClick` | 當使用者按一下「媒體塗鴉牆」中的「Twitter贊／我的最愛」按鈕時。 |
| `ModalView` | 當使用者按一下以在較大的模型視窗中檢視「媒體牆」內容時。 |
| `Like` | 當使用者按一下「媒體塗鴉牆」上的「贊」按鈕時。 |
| `ShareButtonClick` | 只要使用者按一下「媒體牆」卡上的分享按鈕， |
| `ShareURL` | 從「媒體塗鴉牆」中選取／複製「共用至URL」文字區域時。 |
| `ShareFacebook` | 從媒體塗鴉牆按一下「分享到Facebook」時。 |
| `ShareTwitter` | 從媒體塗鴉牆按一下「分享到Twitter」時。 |
