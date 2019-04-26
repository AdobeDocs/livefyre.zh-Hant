---
description: 使用Janrain Capture和Backflight的客戶可使用Livefyre Auth for Single登入(SSO)，讓使用者在登入您的網站時立即與您的Livefyre應用程式互動。
seo-description: 使用Janrain Capture和Backflight的客戶可使用Livefyre Auth for Single登入(SSO)，讓使用者在登入您的網站時立即與您的Livefyre應用程式互動。
seo-title: Janrain Capture/Backflight
solution: Experience Manager
title: Janrain Capture/Backflight
uuid: 776e9626-db04-4c34-adfe-681a71 b552 c
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Janrain Capture/Backflight{#janrain-capture-backplane}

使用Janrain Capture和Backflight的客戶可使用Livefyre Auth for Single登入(SSO)，讓使用者在登入您的網站時立即與您的Livefyre應用程式互動。

若要從內建Capture/Backflane整合中獲益，您必須對Capture應用程式和Livefyre. js整合進行組態變更。

>[!NOTE]
>
>如果您未使用Janrain Capture，請跳過此章節。

如需詳細資訊，請參閱 [Janrain的Backflane文件](https://developers.janrain.com/how-to/integrations/self-serve-integrations-and-tools/backplane-1-2/)。

1. [設定Capture。](#c_janrain_capture_backplane/section_r2f_kxt_bbb)
1. (選擇性) [將Livefyre預設新增至您的Capture App](#c_janrain_capture_backplane/section_z2s_txt_bbb)。
1. [建立authDelegate物件。](#c_janrain_capture_backplane/section_asv_vyt_bbb)
1. [同步至Livefyre，並使用Ping for Draw。](#c_janrain_capture_backplane/section_ilv_bzt_bbb)

## 步驟1：設定擷取 {#section_r2f_kxt_bbb}

Livefyre需要您的Janrain Capture應用程式的特定認證。

1. 設定Janrain Capture應用程式。
1. 收集Livefyre的下列資訊：

   * 存取您的Janrain Capture實例。
   * 存取您的Janrain Engagement儀表板。
   * 您的Capture設定和認證。
   * 您的參與認證。
   * 您的身分URL。

>[!NOTE]
>
>Livefyre直接從CNAME接收資料；因此，此識別URL無法為可解析Janrain Capture實際CNAME的CNAME記錄(虛名URL CNAME)。

## 步驟2：(選擇性)將Livefyre預設新增至您的Capture App {#section_z2s_txt_bbb}

將Livefyre預設為儲存在Capture應用程式中的使用者，讓您可以傳送使用者電子郵件通知，或允許他們自動遵循使用者評論的對話。

1. 完成 [步驟1：設定Capture](#c_janrain_capture_backplane/section_r2f_kxt_bbb)。
1. 新增下列Livefyre預設欄位。所有欄位皆為選用欄位。

| 參數 | Type | 說明 |
|---|---|---|
| **[!UICONTROL livefyre_comments]** | 字串 | 當使用者在文章上留言時通知使用者。可以立即、經常或永不完成。 |
| **[!UICONTROL livefyre_likes]** | 字串 | 當某人喜歡其中一個貼文時通知使用者。可以立即、經常或永不完成。 |
| **[!UICONTROL livefyre_replies]** | 字串 | 當某人回覆其中一個貼文時通知使用者。可以立即、頻繁或永不通知使用者。 |
| **[!UICONTROL livefyre_moderator_comments]** | 字串 | 通知協調者有關他們正在協調的對話的對話者。可以立即、經常或永不。 |
| **[!UICONTROL livefyre_moderator_flags]** | 字串 | 當有人在他們協調的對話中標幟貼文時通知協調者。可以立即、頻繁或永不。 |
| **[!UICONTROL livefyre_autofollow_conversations]** | 布林值 | 讓使用者在離開貼文時自動進行對話。可以是true或false。 |

## 步驟3：建立適用於Janrain整合的AuthDelegate物件 {#section_asv_vyt_bbb}

Livefyre需要提供增效模組，可讓驗證Janrain Backflane巴士。

### 登入 {#login}

在Backflight頻道上廣播身分/登入訊息時，將會呼叫使用者的Livefyre驗證Token。您仍必須實作AuthDelegate。

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
>您必須先在頁面上定義windows. backflight物件，再使用Livefyre Backflane外掛程式呼叫auth. plugin。若要確保Backflight物件可供使用，請從onReady回呼呼叫Livefyre重新整理代碼。請洽詢您的Janlin聯絡人以判斷其他應用程式何時可能使用Backflane物件。



>[!NOTE]
>
>您的驗證委派將視您的Janrain例項而有所不同。

以下舉例說明Auth委派如何尋找Janrain Capture整合。

* `errback`：傳遞回您的驗證委派的回呼方法
* `janrain`：您的Janrain擷取變數參考。
* `window.Backplane`：反向平面物件的參考。

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

* `finishLogout`：傳遞回您的驗證委派的回呼方法。

* `window.Backplane`：反向平面物件的參考。

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

### 編輯描述檔 {#editprofile}

這可以連結至您希望使用者瀏覽的網站部分，以檢視其個人資料頁面。此範例只會列印傳入的作者物件。

```
/** 
* Edit profile function 
* @param user - User who would like to edit their profile 
*/ 
authDelegate.editProfile = function(user) { 
   console.log(user); 
}; 
```

### 檢視描述檔 {#viewprofile}

如同編輯設定檔，這應該連結至與目前登入使用者不同的使用者頁面。您可以視需要實作此項目。此範例只會將作者參數記錄至主控台。

```
/** 
* View profile function 
* @param user - User or userId whose profile should be displayed 
*/ 
authDelegate.viewProfile = function(user) { 
   console.log(author); 
};
```

## 步驟4：同步至Livefyre與Ping for Janrain整合 {#section_ilv_bzt_bbb}

與Capture使用者管理系統同步的Livefyre遠端描述檔包含一系列稱為「Ping for Draw」的步驟。此程序要求您從Janrain取得有效的存取Token，然後將該代號傳遞至以下步驟中所指定的端點。

1. 從Janrain取得存取程式碼。

   若要取得存取代碼，請提供必要的認證、指定user_ type作為「user」，以及uuid作為目前使用者的uuid進行更新。如需詳細資訊，請參閱 [https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/](https://developers.janrain.com/rest-api/methods/authentication/access-codes-and-tokens/getauthorizationcode/)。

1. 交易存取代碼以取得存取Token。提供必要的認證、從步驟接收的存取代碼，並將rangrant_ type指定為「authorization_ code」。

   如需詳細資訊，請參閱 [https://developers.janrain.com/rest-api/methods/authentication/oauth/token/](https://developers.janrain.com/rest-api/methods/authentication/oauth/token/)。

1. 按一下Livefyre「Ping to Rull Capture」端點。

   端點URL： [!DNL https://{networkName}/api/v1.1/private/capture/profile_updated/?jrtoken={token}] 其中 ***{publishName}*** 是Livefyre提供給您的網路名稱，而jrten是在步驟中從Janrain收到的Token。

   當您點擊此端點後，就會收到202回應，Livefyre會開始非同步程序。

## 所有運作方式 {#concept_mty_f31_2cb}

為了從內建Capture/Backflane整合中獲益，您必須對Capture應用程式和Livefyre. js整合進行一些組態變更。

Janrain會透過「Backflight」(背景)匯出程式，傳送成功的登入/登出訊息，在適當設定時，Livefyre應用程式會偵聽。這些訊息包含顯示應用程式使用者登入或登出所需的所有資訊。開發人員可檢視瀏覽器開發人員主控台中的「網路」索引標籤，以檢視「回溯」巴士訊息。

## 登入代碼範例 {#section_ftt_tvp_mz}

要求：

```
https://backplane1.janrainbackplane.com//bus/{CUSTOMER_NAME}/channel/{CHANNEL}?callback=Backplane.response&rnd=0.15930617856793106
```

回應：

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

空白回應：

```
Backplane.response([]);
```

## 登出代碼範例 {#section_t52_svp_mz}

要求：

```
https://backplane1.janrainbackplane.com/v1.2/bus/{CUSTOMER}/channel/new?callback=Backplane.finishInit&amp;rnd=0.1057701709214598
```

回應：

```
Backplane.finishInit("{CHANNEL}");
```

如果這些訊息未出現在您的網路要求中，Livefyre將不會察覺登入/登出嘗試，因此Livefyre將無法將使用者整合至應用程式。
