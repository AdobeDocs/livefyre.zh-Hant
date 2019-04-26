---
description: 可用於繫結對話應用程式 (如 Comments、Chat、Live Blog、Reviews 和 Sidenotes) JavaScript
  的事件。
seo-description: 可用於繫結對話應用程式 (如 Comments、Chat、Live Blog、Reviews 和 Sidenotes) JavaScript
  的事件。
seo-title: JavaScript事件定義和範例
solution: Experience Manager
title: JavaScript事件定義和範例
uuid: 61da2e2e-8fcd-482d-93df-c946 f0475277
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# JavaScript事件定義和範例{#javascript-events-definitions-and-examples}

可用於繫結對話應用程式 (如 Comments、Chat、Live Blog、Reviews 和 Sidenotes) JavaScript 的事件。

Livefyre提供JavaScript事件來追蹤Livefyre應用程式中的使用者活動。例如，您可能想要在使用者按贊或分享內容至Twitter或Facebook時更新頁面，或是在張貼新內容時更新頁面。

Livefyre也可讓您將事件新增至第三方分析整合(Adobe Analytics JS、Google Analytics、動態標籤管理等)來追蹤應用程式事件。如需詳細資訊，請與第三方整合管理員合作以提供正確的事件。

若要系結至這些事件，請在頁面上實例化您的應用程式時，將下列程式碼新增至頁面。取代以下項目的事件名稱 `{eventName}`：

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('{eventName}', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

>[!NOTE]
>
>資料物件是針對所有事件處理常式提供。資料物件範例會遵循每個事件。

## 注釋 {#section_qfr_51p_xz}

使用者張貼了評論。

* null的父項為新留言。
* 父項的父項是已編輯的留言。
* 父項的數字是回覆的父ID。

```
data = { 
   authorId: "_u2012@livefyre.com" // The ID of the author of the comment  
   parent: "893549"  
      // The ID of the comment that this new comment is in reply to, else null 
   bodyHtml: "<p>42</>" // The HTML of the submitted Content 
   sharedToFacebook:true // Whether the comment was also posted to Facebook 
   sharedToTwitter:false // Whether the comment was also posted to Twitter 
   title: "demo title" // The title of the review (exists only for Reviews) 
   rating: [90] // Array of ratings for the review (exists only for Reviews) 
} 
```

## 註解已標記 {#section_szy_s1p_xz}

使用者標幟了評論。

```
data = { 
   targetId: "789347" // The ID of the comment that was flagged 
   type: ["disagree"] // The type of flag 
   notes: ["I don't entirely agree with this post"] // A note/reason for the flag 
}
```

## 評論贊 {#section_vc1_r1p_xz}

使用者喜歡評論。

```
data = { 
   targetId: "245625" // The ID of the comment that was liked 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was liked 
} 
```

## CommentShared {#section_nqb_31p_xz}

使用者從串流共用評論。(當使用者從「留言」編輯器共用時，此事件不會引發。)按一下「共用」按鈕時，會觸發此事件。

```
data = { 
   targetId: "256255" // The ID of the comment that was shared 
   sharedToFacebook:false // Whether the comment was shared to Facebook 
   sharedToTwitter:true // Whether the comment was shared to Twitter 
}
```

## 注釋日期 {#section_qdq_f1p_xz}

此對話中的可見留言總數已變更(增量或遞減)。

```
data: 34 // The total number of visible comments in the conversation (integer). 
```

## userLoggedIn {#section_yjt_vz4_xz}

使用者登入。

```
data = { 
   avatar: "https://gravatar.com/avatar/50.jpg"  
      // Link to logged in user's avatar image 
   displayName: "NewUser" // Display name of the logged in user 
   id: "newuser@livefyre.com" // ID of the logged in user 
   isModerator:false // Boolean indicating whether logged in user is a moderator 
}
```

## userLoggedOut {#section_tsg_5z4_xz}

使用者已登出。

資料未定義。

## SocialReference {#section_a1w_tz4_xz}

使用者在評論中包含@提及。傳回下列陣列：

```
data = { 
   id: '111111@fb.gw.livefyre.com' // ID of the mentioned user 
   displayName: 'testUser' // Display name of mentioned user 
   message: "@testUser Wow, I can't believe it either!"  
      // Message that was sent to the particular user 
   provider: 'twitter' // Provider to which the mention was shared 
} 
```

## 評論證言

協調者使用者專題評論。傳回下列陣列：

```
data = { 
   targetId: "134234" // The ID of the comment that was featured 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was featured 
}
```

## initialRenderComplete {#section_odc_4z4_xz}

評論串流已載入，並從伺服器擷取初始內容集，並向使用者顯示。

資料未定義。

## 展示更多資訊 {#section_pqg_nz4_xz}

使用者按下 **[!UICONTROL Show More]** 按鈕。

資料未定義。

## 使用者關注 {#section_xxw_jz4_xz}

當使用者按下 **[!UICONTROL Follow]** 按鈕時傳回true，當內容張貼至串流時，則會傳回false。

```
data = { 
   id: 'authorId@livefyre.com', 
   optIn: true 
}
```

## 使用者後續 {#section_wm1_gz4_xz}

當使用者按一下 **「取消關注** 」按鈕時傳回true，而內容張貼至串流時則會傳回true。

```
data = { 
   id: 'authorId@livefyre.com', 
   optOut: true 
}
```

