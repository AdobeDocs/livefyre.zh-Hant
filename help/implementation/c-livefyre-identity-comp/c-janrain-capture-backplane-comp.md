---
description: 使用Janrain Capture和Backplane的客戶可能會使用Livefyre Auth for Single Sign On(SSO)，讓使用者在登入您的網站時立即與您的Livefyre應用程式互動。
seo-description: 使用Janrain Capture和Backplane的客戶可能會使用Livefyre Auth for Single Sign On(SSO)，讓使用者在登入您的網站時立即與您的Livefyre應用程式互動。
seo-title: Janrain Capture/底板
solution: Experience Manager
title: Janrain Capture/底板
uuid: 776e9626-db04-4c34-adfe-681a71b552c5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Janrain Capture/底板{#janrain-capture-backplane}

使用Janrain Capture和Backplane的客戶可能會使用Livefyre Auth for Single Sign On(SSO)，讓使用者在登入您的網站時立即與您的Livefyre應用程式互動。

若要受益於此內建的Capture/Backplane整合，您必須對Capture應用程式和Livefyre.js整合進行設定變更。

>[!NOTE]
>
>如果您不使用Janrain Capture，請略過本節。

如需詳細資訊，請 [參閱Janrain的底板檔案](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/)。

1. [設定捕獲。](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. （可選）將 [Livefyre預設值新增至您的Capture應用程式](#c_janrain_capture_backplane/section_z2s_txt_bbb)。
1. [建立AuthDelegate物件。](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [使用Ping for Pull同步至Livefyre。](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## 步驟1:設定捕獲 {#section_r2f_kxt_bbb}

Livefyre需要您Janrain Capture應用程式的特定認證。

1. 設定Janrain Capture應用程式。
1. 收集Livefyre的下列資訊：

   * 存取您的Janrain Capture實例。
   * 存取您的Janrain Engage儀表板。
   * 您的Capture設定和認證。
   * 您的參與認證。
   * 您的身分URL。

>[!NOTE]
>
>Livefyre直接從CNAME接收資料；因此，此識別URL不能是解析為Janrain Capture實際CNAME的CNAMEd記錄（虛名URL CNAME）。

## 步驟2:（選用）將Livefyre預設值新增至您的Capture應用程式 {#section_z2s_txt_bbb}

將Livefyre預設值新增至儲存在Capture應用程式中的使用者，讓您傳送電子郵件通知給使用者，或讓使用者自動關注使用者評論的對話。

1. 完 [整步驟1:設定捕獲](#c_janrain_capture_backplane/section_r2f_kxt_bbb)。
1. 新增下列Livefyre預設欄位。 所有欄位皆為選填欄位。

| 參數 | 類型 | 說明 |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | 字串 | 當有人對文章提出意見時，通知使用者他們正在關注。 可以立即、經常或永遠不能。 |
| **[!UICONTROL livefyre_likes]** | 字串 | 當有人按贊其其中一篇貼文時，通知使用者。 可以立即、經常或永遠不能。 |
| **[!UICONTROL livefyre_replies]** | 字串 | 當有人回覆其貼文時通知使用者。可以立即、經常或永遠不可以。 |
| **[!UICONTROL livefyre_moderator_comments]** | 字串 | 當某人對對對話留言時通知協調者他們正在協調。可以立即、經常或永遠不要。 |
| **[!UICONTROL livefyre_moderator_flags]** | 字串 | 當某人標籤對話中的貼文時，通知協調者他們正在協調。可以立即、經常或永遠不會。 |
| **[!UICONTROL livefyre_autofollow_conversations]** | 布林值 | 讓使用者在離開貼文時自動追蹤對話。 可以是true或false。 |

## 步驟3:建立Janrain整合的AuthDelegate物件 {#section_asv_vyt_bbb}

Livefyre.require提供外掛程式，可讓驗證人員監聽Janrain Backplane匯流排。

### 登入 {#login}

當在底板頻道上廣播身分／登入訊息時，將會使用使用者的Livefyre驗證Token來呼叫auth.authenticate()。 您仍必須實作AuthDelegate。

```
Livefyre.require(['auth', 'backplane-auth-plugin#0'], function(auth, backplanePluginFactory) { 
   auth.plugin(backplanePluginFactory('network.fyre.co')); 
   auth.delegate({ 
      login: function (finishLogin) { 
         loginWithCapture(finishLogin); 
      } 
   }); 
});
```

>[!NOTE]
>
>在使用Livefyre Backplane外掛程式呼叫auth.plugin之前，必須先在您的頁面上定義window.Backplane物件。 若要確定Backplane物件可用，請從onReady回呼呼叫Livefyre實例化程式碼。 請洽詢您的Janrain聯繫人，以確定其他應用程式何時可以使用底板對象。



>[!NOTE]
>
>您的驗證委派會視您的Janrain例項而有所不同。

以下是驗證委派如何尋找Janrain Capture整合的一些範例。

* `errback`:傳遞給驗證委派登入方法的回呼
* `janrain`:Janrain捕獲變數的引用。
* `window.Backplane`:對底板對象的引用。

```
/** 
* Login function 
* In this case, opens a login modal and triggers Backplane to start listening 
* for login messages 
*/ 
authDelegate.login = function(finishLogin) { 
   var successCallback = function() { 
      // These need to be replaced with the actions that correspond to successful login  
      // and when the Janrain modal is closed. 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      finishLogin(); 
   }; 
  
   var failureCallback = function(e) { 
      janrain.events.onModalClose.removeHandler(failureCallback); 
      janrain.events.onCaptureLoginSuccess.removeHandler(successCallback); 
      finishLogin(e || new Error("Error logging in with Janrain Capture")); 
   }; 
  
   // Open the modal to log a user in 
   janrain.capture.ui.renderScreen('signIn'); 
   // Send a backplane message 
   window.Backplane.expectMessages('identity/login'); 
   // Add handlers to specific janrain events 
   janrain.events.onCaptureLoginSuccess.addHandler(successCallback); 
   janrain.events.onModalClose.addHandler(failureCallback); 
};
```

### 登出 {#logout}

* `finishLogout`:傳遞給驗證委派登入方法的回呼。

* `window.Backplane`:對底板對象的引用。

```
/** 
* Logout function 
* In this case, invalidates the session and removes the cookie. 
* Also reloads the page to change state. In order to do this without a reload, 
* it would be necessary to also update the UI. 
*/ 
authDelegate.logout = function(finishLogout) { 
   Backplane.resetCookieChannel(); 
   janrain.capture.ui.endCaptureSession(); 
   finishLogout(); 
}; 
```

### 編輯個人資料 {#editprofile}

這可以連結至您希望使用者瀏覽網站的任何部分，以檢視其個人檔案頁面。 此範例僅列印傳入的作者物件。

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

### 檢視設定檔 {#viewprofile}

如同「編輯設定檔」，這應該會連結至與目前登入使用者不同的使用者頁面。 不論您認為適合，都可實作此項目。 此範例只會將作者參數記錄至主控台。

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

## 步驟4:與Ping for Pull for Janrain整合同步至Livefyre {#section_ilv_bzt_bbb}

讓Livefyre遠端設定檔與您的Capture使用者管理系統同步，需要執行一系列步驟，稱為Ping for Pull。 此程式要求您從Janrain取得有效的存取Token，然後將該Token傳遞至以下步驟3中指定的端點。

1. 從Janrain取得存取程式碼。

   若要取得存取程式碼，請提供必要的憑證、將user_type指定為"user"，以及uuid指定為目前使用者的uuid以進行更新。 如需詳細資訊，請參 [閱https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/)。

1. 將存取程式碼換成存取Token。 提供必要的憑證、從步驟1接收的存取碼，並將grant_type指定為"authorization_code"。

   如需詳細資訊，請參 [閱https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/)。

1. 按一下Livefyre的「Ping to Pull Capture」端點。

   端點URL:其 [!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] 中{ ***networkName}*** }是Livefyre提供給您的網路名稱，而jrtoken是在步驟2中從Janrain接收的代號。

   一旦您到達此端點，就會收到202回應，Livefyre就會開始非同步程式。

## How It All Works {#concept_mty_f31_2cb}

若要受益於此內建的Capture/Backplane整合，您必須對Capture應用程式和Livefyre.js整合進行一些設定變更。

Janrain會透過底板匯流排傳送成功的登入／登出訊息，當Livefyre應用程式正確設定時，會在底板匯流排上監聽。 這些訊息包含顯示應用程式使用者已登入或已登出時所需的所有資訊。 開發人員可在瀏覽器的開發人員主控台中檢查「網路」標籤，以檢視底板匯流排訊息。

## 登入代碼範例 {#section_ftt_tvp_mz}

請求:

```
https://backplane1.janrainbackplane.com//bus/{CUSTOMER_NAME}/channel/{CHANNEL}?callback=Backplane.response&rnd=0.15930617856793106
```

回應:

```
Backplane.response([{ 
  "id": "2014-05-06T22:51:55.406Z-eZp1HB1F7B", 
  "channel_name": "{CHANNEL_NAME}", 
  "message": { 
    "source": "https://{CUSTOMER_DOMAIN}", 
    "type": "identity/login", 
    "sticky": true, 
    "payload": { 
      "context": "https://{CUSTOMER_DOMAIN}", 
      "identities": { 
        "startIndex": 0, 
        "itemsPerPage": 1, 
        "totalResults": 1, 
        "entry": { 
          "id": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
          "displayName": "{USER_DISPLAY_NAME}", 
          "accounts": [ 
            { 
              "username": "{USER_DISPLAY_NAME}", 
              "identityUrl": "https://{CUSTOMER}.janraincapture.com/oauth/public_profile?uuid={UNIQUE_USER_ID}", 
              "photos": [ 
                { 
                  "id": 48570146, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "other" 
                }, 
                { 
                  "id": 48570147, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "original" 
                }, 
                { 
                  "id": 48570148, 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "large" 
                }, 
                { 
                  "value": "https://lh3.googleusercontent.com/-h8poqH8hlgw/AAA/AAA1/QuHtbeHMJzc/photo.jpg?sz=50", 
                  "type": "avatar" 
                } 
              ] 
            }, 
            { 
              "identityUrl": "{USER_PROFILE_LINK}" 
            } 
          ] 
        } 
      } 
    } 
  } 
} 
]);
```

空回應：

```
Backplane.response([]);
```

## 註銷代碼示例 {#section_t52_svp_mz}

請求:

```
https://backplane1.janrainbackplane.com/v1.2/bus/{CUSTOMER}/channel/new?callback=Backplane.finishInit&amp;rnd=0.1057701709214598
```

回應:

```
Backplane.finishInit("{CHANNEL}");
```

如果這些訊息未出現在您的網路要求中，Livefyre將不會察覺登入／登出嘗試，因此Livefyre將無法將使用者整合至應用程式。
