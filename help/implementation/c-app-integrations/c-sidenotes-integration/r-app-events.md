---
description: 您可以監聽Sitents例項上的事件。
seo-description: 您可以監聽Sitents例項上的事件。
seo-title: Sitdones應用程式事件
solution: Experience Manager
title: Sitdones應用程式事件
uuid: afca4b03-c370-41ca-aa12-45bc357517 ca
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Sitdones應用程式事件 {#sidenotes-app-events}

您可以監聽Sitents例項上的事件。

回呼可使用 `onmethod``removeListener` 方法註冊並取消註冊。如果回呼只被呼叫一次，然後未註冊，則可使用此 `once` 方法。

```
var app = Livefyre.Sidenotes(convConfig); 
   app.once('sidenotes.initialized', function () { 
     // Sidenotes initialized!  
});
```

如需Livefyre事件的詳細資訊，請參閱「參考」區段中的「JavaScript事件」頁面。

| 索引鍵 | 說明 |
|--- |--- |
| sidents. initialization | 應用程式初始化、擁有資料且位於頁面上時引發。 |
| sidents. comments標幟 | 在標記備注時引發。資料包含： <br><ul><li>`targetId`：已標記之留言的ID</li><li>`type`：標幟類型字串 `(offensive, off-topic, spam, disagree)`</li></ul> |
| `sidenotes.commentPosted` | 張貼意見時引發。資料包含： <br><ul><li> `authorId`：注釋作者id </li><li>`bodyHtml`：註解內文 </li><li> `parent`：備注的父項，或null</li></ul> |
| `sidenotes.commentShared` | 已共用評論時引發。資料包含： <br><ul><li>`targetId`：共用留言的ID </li><li> `sharedToFacebook`：該留言是否與Facebook共用 </li><li>`sharedToTwitter`：該留言是否與Twitter共用</li></ul> |
| `sidenotes.commentVoted` | 在已投票意見時引發。資料包含： <br><ul><li>`targetId`：已投票給 </li><li> `targetAuthorId`：已投票給該作者的作者id</li><li> `type`：數值投票類型：0：'clear'，1：'upcote'或2：「投票」</li></ul> |
| `sidenotes.userLoggedIn` | 使用者登入時引發。資料包含： <br><ul><li>`avatar`：使用者的頭像URL </li><li>`displayName`：使用者的顯示名稱</li><li>`id`：使用者id</li><li> `isModerator`：使用者是否為目前系列的協調者</li></ul> |
| `sidenotes.userLoggedOut` | 使用者登出時引發 |
