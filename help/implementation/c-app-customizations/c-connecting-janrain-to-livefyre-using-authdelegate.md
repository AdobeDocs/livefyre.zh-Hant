---
description: Livefyre.require提供外掛程式，可讓驗證人員監聽Janrain Backplane匯流排。
seo-description: Livefyre.require提供外掛程式，可讓驗證人員監聽Janrain Backplane匯流排。
seo-title: 使用AuthDelegate將Janrain連線至Livefyre
title: 使用AuthDelegate將Janrain連線至Livefyre
uuid: 9d56e3f4-960a-4108-aab5-2795b0e71c88
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 使用AuthDelegate將Janrain連線至Livefyre{#connecting-janrain-to-livefyre-using-authdelegate}

Livefyre.require提供外掛程式，可讓驗證人員監聽Janrain Backplane匯流排。

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

以下是驗證委派如何尋找Janrain Capture整合的一些範例。

>[!NOTE]
>
>您的驗證委派會視您的Janrain例項而有所不同。

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* 傳遞給驗證委派登入方法的回呼
* Janrain捕獲變數的引用。
* :對底板對象的引用。

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

登出

* **** finishLogout:傳遞給驗證委派登入方法的回呼。

* **** window.底板：對底板對象的引用。

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

編輯個人資料

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

檢視設定檔

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

