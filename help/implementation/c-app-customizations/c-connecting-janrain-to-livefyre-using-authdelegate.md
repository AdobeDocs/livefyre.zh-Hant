---
description: Livefyre需要提供增效模組，可讓驗證Janrain Backflane巴士。
seo-description: Livefyre需要提供增效模組，可讓驗證Janrain Backflane巴士。
seo-title: 使用AuthDelegate將Janrain與Livefyre連結
title: 使用AuthDelegate將Janrain與Livefyre連結
uuid: 9d56e3f4-960a-4108-aab5-2795b0 e71 c88
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 使用AuthDelegate將Janrain與Livefyre連結{#connecting-janrain-to-livefyre-using-authdelegate}

Livefyre需要提供增效模組，可讓驗證Janrain Backflane巴士。

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

以下舉例說明Auth委派如何尋找Janrain Capture整合。

>[!NOTE]
>
>您的驗證委派將視您的Janrain例項而有所不同。

<!--Hannah: Mystery stray bullet found here. Please check against source. -Bob -->

* 傳遞回您的驗證委派的回呼方法
* 您的Janrain擷取變數參考。
* ：反向平面物件的參考。

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

* **FinishLogout：** 傳遞回您的驗證委派的回呼方法。

* **window. backflight：** 反向平面物件的參考。

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

編輯描述檔

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

檢視描述檔

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

