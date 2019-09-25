---
description: AuthDelegate物件會針對如何執行驗證動作和事件實施您想要的行為，讓您可以自訂與網站現有驗證系統的整合。
seo-description: AuthDelegate物件會針對如何執行驗證動作和事件實施您想要的行為，讓您可以自訂與網站現有驗證系統的整合。
seo-title: AuthDelegate物件
solution: Experience Manager
title: AuthDelegate物件
uuid: a6acc4ef-d442-4782-9bfa-bbe494547c2e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# AuthDelegate物件{#authdelegate-object}

AuthDelegate物件會針對如何執行驗證動作和事件實施您想要的行為，讓您可以自訂與網站現有驗證系統的整合。

## 建立驗證委派 {#section_wmn_tv2_gz}

驗證套件必須先隨驗證委派提供，才能執行動作。 驗證委派是實施本主題中其中一個方法的任何JavaScript物件。

## .login(finishLogin) {#section_mpk_lv2_gz}

登入有效的使用者，並在發生錯誤時使用Error物件叫用finishLogin函式，或是使用者的Livefyre憑證。 此方法的常見實作會將使用者重新導向至登入頁面，或開啟新視窗或模式。

此範例會自動通知具有驗證Token(Token)的Livefyre使用者驗證：

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

最簡單的登入委派可能會要求使用者取得其Livefyre驗證Token。

```
authDelegate.login = function contrivedLogin(finishLogin) { 
  var lfToken = prompt("Please type your Livefyre Token");  
  if (lfToken.length === 0) { 
   return finishLogin(new Error("User failed to type their lftoken")); 
  }  
 finishLogin(null, { 
   livefyre: lfToken 
 }); 
};
```

## .logout(finishLogout) {#section_uqz_2v2_gz}

註銷用戶並調用finishLogout函式（如果出現錯誤，則使用Error對象），或者使用null通知auth註銷成功。

例如:

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## .viewProfile(user) {#section_kkv_dv2_gz}

採取行動來檢視使用者的個人檔案。

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## .editProfile(user) {#section_bkx_pq2_gz}

採取行動來編輯使用者的設定檔。

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

透過實施上述所有方法，驗證可以使用自訂驗證委派來設定。 一旦建立委派後，就可以使用委派方法來提供它以進行驗證。

```
var authDelegate = { 
 login: function(cb) { 
  ... 
  cb(null); 
 }, 
 ... 
} 
  
auth.delegate(authDelegate);
```

