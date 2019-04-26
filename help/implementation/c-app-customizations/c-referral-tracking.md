---
description: 追蹤從反向連結流量回到頁面的點按次數。
seo-description: 追蹤從反向連結流量回到頁面的點按次數。
seo-title: 反向連結追蹤
solution: Experience Manager
title: 反向連結追蹤
uuid: 5206cc16-9671-4b3d-a013-be3 e8 c029 d
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# 反向連結追蹤{#referral-tracking}

追蹤從反向連結流量回到頁面的點按次數。

當留言張貼或分享至社交網路，以及Livefyre電子郵件中所包含的權限時，Livefyre會附加反向連結變數至URL。使用此變數可追蹤從Livefyre應用程式到您的社交或擁有屬性的反向連結流量。

Livefyre應用程式可讓您追蹤由反向連結流量產生的資料串流，讓您分析網站流量。

## 追蹤Livefyre反向連結流量 {#section_nsy_qp4_xz}

社交網路和電子郵件的Livefyre反向連結流量可透過檢查頁面URL中的查詢字串參數，並在您的頁面上實施程式碼來追蹤，以便透過您的分析提供者追蹤。Livefyre會在貼文張貼或分享至社交網路時附加反向連結連結，以及Livefyre電子郵件中包含的權限連結。

## 實施範例 {#section_xvs_x44_xz}

如果流量來自StreamHub驅動的通知，則會有HubeBrefsz查詢字串參數，內含電子郵件、Facebook、Twitter、LinkedIn或超連結的值。HubeBrefsz參數名稱可由Livefyre傳送團隊在網路層級設定。

若要與分析平台整合，您的頁面必須在載入時尋找HubeBrefsz，並記錄流量(如果存在)。

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
* [注釋](/help/using/c-about-apps/c-comments/c-comments.md)
* [評論](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md)
* [Sitents](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md)