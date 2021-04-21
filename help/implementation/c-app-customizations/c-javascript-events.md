---
description: 可用於繫結對話應用程式 (如 Comments、Chat、Live Blog、Reviews 和 Sidenotes) JavaScript 的事件。
title: JavaScript事件定義與範例
exl-id: 5b865974-69aa-4d51-ac26-60f1d8a114fc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 11%

---

# JavaScript事件定義與範例{#javascript-events-definitions-and-examples}

可用於繫結對話應用程式 (如 Comments、Chat、Live Blog、Reviews 和 Sidenotes) JavaScript 的事件。

Livefyre提供JavaScript事件，可追蹤Livefyre應用程式中的使用者活動。 例如，當使用者按贊或分享內容至Twitter或Facebook，或是張貼新內容時，您可能想要更新頁面。

Livefyre也可讓您將事件新增至協力廠商分析整合(Adobe AnalyticsJS、Google Analytics、動態標籤管理等)，以追蹤應用程式事件。 如需詳細資訊，請與您的協力廠商整合管理員合作，以提供正確的事件。

若要系結至這些事件，請在頁面上實例化您的應用程式時，將下列程式碼新增至頁面。 將事件名稱替換為`{eventName}`:

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
>所有事件處理常式都提供資料物件。 每個事件後面都會顯示範例資料物件。

## commentPosted {#section_qfr_51p_xz}

一位使用者張貼了評論。

* null的父代是新注釋。
* 「無」的父項是已編輯的注釋。
* 父代的編號是回覆的父ID。

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

## commentFlagd {#section_szy_s1p_xz}

使用者已標籤留言。

```
data = { 
   targetId: "789347" // The ID of the comment that was flagged 
   type: ["disagree"] // The type of flag 
   notes: ["I don't entirely agree with this post"] // A note/reason for the flag 
}
```

## commentLiked {#section_vc1_r1p_xz}

使用者對留言按贊。

```
data = { 
   targetId: "245625" // The ID of the comment that was liked 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was liked 
} 
```

## commentShared {#section_nqb_31p_xz}

使用者從串流共用註解。 （當使用者從「注釋」編輯器共用時，不會觸發此事件。） 當按一下「共用」按鈕時，會觸發此事件。

```
data = { 
   targetId: "256255" // The ID of the comment that was shared 
   sharedToFacebook:false // Whether the comment was shared to Facebook 
   sharedToTwitter:true // Whether the comment was shared to Twitter 
}
```

## commentCountUpdated {#section_qdq_f1p_xz}

此對話中可見留言的總數已變更（增加或減少）。

```
data: 34 // The total number of visible comments in the conversation (integer). 
```

## userLoggedIn {#section_yjt_vz4_xz}

使用者已登入。

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

## socialInterment {#section_a1w_tz4_xz}

使用者在留言中加入@提及。 傳回下列陣列：

```
data = { 
   id: '111111@fb.gw.livefyre.com' // ID of the mentioned user 
   displayName: 'testUser' // Display name of mentioned user 
   message: "@testUser Wow, I can't believe it either!"  
      // Message that was sent to the particular user 
   provider: 'twitter' // Provider to which the mention was shared 
} 
```

## commentFeatured

協調者使用者提供評論。 傳回下列陣列：

```
data = { 
   targetId: "134234" // The ID of the comment that was featured 
   targetAuthorId: "i_am_author@livefyre.com"  
      // The ID of the author of the comment that was featured 
}
```

## initialRenderComplete {#section_odc_4z4_xz}

注釋串流已載入，而初始內容集已從伺服器擷取並顯示給使用者。

資料未定義。

## showMore {#section_pqg_nz4_xz}

用戶按一下了&#x200B;**[!UICONTROL Show More]**&#x200B;按鈕。

資料未定義。

## userFlocked {#section_xxw_jz4_xz}

當使用者按一下&#x200B;**[!UICONTROL Follow]**&#x200B;按鈕時傳回true，當內容張貼至串流時傳回false。

```
data = { 
   id: 'authorId@livefyre.com', 
   optIn: true 
}
```

## userUnflocked {#section_wm1_gz4_xz}

當使用者按一下&#x200B;**Unfollow**&#x200B;按鈕時傳回true，當內容張貼至串流時傳回false。

```
data = { 
   id: 'authorId@livefyre.com', 
   optOut: true 
}
```
