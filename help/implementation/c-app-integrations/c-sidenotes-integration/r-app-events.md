---
description: 您可以監聽Sidesirs例項上的事件。
seo-description: 您可以監聽Sidesirs例項上的事件。
seo-title: Sidesars應用程式事件
solution: Experience Manager
title: Sidesars應用程式事件
uuid: afca4b03-c370-41ca-aa12-45bc357517ca
translation-type: tm+mt
source-git-commit: 987e682f9c7cd94543fd269f386fd2a971ee9934
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# Siestroms App Events {#sidenotes-app-events}

您可以監聽Sidesirs例項上的事件。

回呼可以用`onmethod`註冊，用`removeListener`方法註冊。 如果回呼僅被呼叫一次，然後取消註冊，則`once`方法可方便使用。

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

如需Livefyre事件的詳細資訊，請參閱「參考」區段中的「JavaScript事件」頁面。

| 金鑰 | 說明 |
|--- |--- |
| sidenotes.initialized | 當應用程式實例化、有資料且位於頁面上時引發。 |
| sidenotes.commentFlagged | 當注釋已標幟時引發。 資料包含：<br><ul><li>`targetId`:標幟之留言的ID</li><li>`type`:標籤字串  `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | 張貼留言時引發。 資料包含：<br><ul><li> `authorId`:評論作者的ID </li><li>`bodyHtml`:評論正文 </li><li> `parent`:注釋的父項ID，或null</li></ul> |
| `sidenotes.commentShared` | 已共用留言時引發。 資料包含：<br><ul><li>`targetId`:已共用之留言的ID </li><li> `sharedToFacebook`:評論是否與Facebook分享 </li><li>`sharedToTwitter`:評論是否已分享給Twitter</li></ul> |
| `sidenotes.commentVoted` | 在對評論投票時引發。 資料包含：<br><ul><li>`targetId`:已投票的評論ID </li><li> `targetAuthorId`:對其評論投票的作者的ID</li><li> `type`:數值投票類型：0:『clear』, 1:「upvote」或2:「下投」</li></ul> |
| `sidenotes.userLoggedIn` | 使用者登入時引發。 資料包含：<br><ul><li>`avatar`:使用者的頭像URL </li><li>`displayName`:使用者的顯示名稱</li><li>`id`:使用者的ID</li><li> `isModerator`:使用者是否為目前系列的協調者</li></ul> |
| `sidenotes.userLoggedOut` | 當使用者登出時引發 |
