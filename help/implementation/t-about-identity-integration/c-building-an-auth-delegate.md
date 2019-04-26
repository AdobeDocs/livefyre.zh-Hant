---
description: authDelegate物件會實作您要如何執行驗證動作和事件的行為，以便您自訂與您網站現有驗證系統的整合。
seo-description: authDelegate物件會實作您要如何執行驗證動作和事件的行為，以便您自訂與您網站現有驗證系統的整合。
seo-title: authDelegate物件
solution: Experience Manager
title: authDelegate物件
uuid: a6acc4ef-d442-4782-9bfa-bbe494547 c2 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# authDelegate物件{#authdelegate-object}

authDelegate物件會實作您要如何執行驗證動作和事件的行為，以便您自訂與您網站現有驗證系統的整合。

## 建立Auth委派 {#section_wmn_tv2_gz}

驗證套件必須提供給auth委派，才能執行動作。auth委派是任何實施本主題其中一種方法的JavaScript物件。

## . login(FinishLogin) {#section_mpk_lv2_gz}

登入有效的使用者，並叫用FindisLogin函數(如果發生錯誤，或使用者的Livefyre認證)。此方法的常見實作會將使用者重新導向至登入頁面，或開啓新視窗或模式。

此範例會自動通知Livefyre使用者with the authentication Token，Token：

```
authDelegate.login = function (finishLogin) { 
 finishLogin(null, { 
   livefyre: 'token' 
 }); 
};
```

最簡單的登入委派可能會詢問使用者其Livefyre驗證Token。

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

## . logout(FinishLogout) {#section_uqz_2v2_gz}

登出使用者並叫用FinishLogout函數(如果發生錯誤)，或null null通知驗證已成功登出。

例如：

```
authDelegate.logout = function (finishLogout) { 
 clearUserSession(); //logic to clear a user session  
 finishLogout(null); 
}
```

## . ViewProfile(使用者) {#section_kkv_dv2_gz}

採取行動檢視使用者的個人檔案。

```
authDelegate.viewProfile = function (user) { 
 window.open(user.get('profileUrl')); 
}
```

## . editProfile(user) {#section_bkx_pq2_gz}

採取行動編輯使用者的個人檔案。

```
authDelegate.editProfile = function (user) { 
 window.open(user.get('profileUrl') + '/edit/'); 
}
```

透過實施上述所有方法，Auth可使用自訂的auth委派設定。建立委派後，即可使用委派方法提供給驗證。

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

