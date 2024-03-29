---
description: 從反向連結流量追蹤回頁面的點按次數。
title: 反向連結追蹤
exl-id: 9955d4a4-184d-421f-bcde-b19342b0b181
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 2%

---

# 反向連結追蹤{#referral-tracking}

從反向連結流量追蹤回頁面的點按次數。

當留言張貼或分享至社交網路時，Livefyre會附加反向連結變數至URL，以及包含在Livefyre電子郵件中的永久連結。 使用此變數可追蹤從Livefyre應用程式到您社交或擁有屬性的反向連結流量。

Livefyre應用程式可讓您追蹤由反向連結流量產生的資料串流，讓您分析網站的流量。

## 追蹤Livefyre反向連結流量{#section_nsy_qp4_xz}

Livefyre來自社交網路和電子郵件的反向連結流量可透過檢查您頁面URL中的查詢字串參數，並在您的頁面上實作程式碼，透過您的分析供應商追蹤。 當留言張貼或分享至社交網路時，Livefyre會附加反向連結至URL，以及包含在Livefyre電子郵件中的永久連結。

## 實施範例 {#section_xvs_x44_xz}

如果流量來自StreamHub支援的通知，則會有hubRefSrc查詢字串參數，其值為電子郵件、facebook、twitter、linkedin或permalink。 您的Livefyre傳送團隊可在網路層級設定hubRefSrc參數名稱。

若要與分析平台整合，您的頁面必須在載入時尋找hubRefSrc，並記錄流量（如果有的話）。

例如：

```
(function () { 
   var qs = document.location.search.substring(1), 
      param = 'hubRefSrc', 
      valueRegex = new RegExp(param+'=([^&]+)'), 
      match = qs.match(valueRegex), 
      referrer; 
   if (match) { 
      // StreamHub generated traffic! 
      referrer = match[1]; 
      console.log('StreamHub referred via', referrer); 
   } else { 
      // StreamHub did not refer this traffic 
   } 
}())
```

使用此功能的應用程式：

* [聊天室](/help/using/c-about-apps/c-chat-app/c-chat-app.md)
* [意見](/help/using/c-about-apps/c-comments/c-comments.md)
* [評論](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md)
* [Siesors](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md)
