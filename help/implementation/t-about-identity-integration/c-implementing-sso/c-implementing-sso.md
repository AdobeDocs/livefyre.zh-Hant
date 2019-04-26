---
description: 若要透過Livefyre App未觸發的流程來驗證使用者，Livefyre建議您在authDelegate物件上實作PreforchautEntication方法。
seo-description: 若要透過Livefyre App未觸發的流程來驗證使用者，Livefyre建議您在authDelegate物件上實作PreforchautEntication方法。
seo-title: 實作SSO
solution: Experience Manager
title: 實作SSO
uuid: c96d456c-b1 ac-40e0-8d18-224652b9697 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 實作SSO{#implementing-sso}

若要透過Livefyre App未觸發的流程來驗證使用者，Livefyre建議您在authDelegate物件上實作PreforchautEntication方法。

This will be vicked when the `authDelegate` when then to `auth.delegate`，and will be傳遞a authenticate function that can be then ptime.此方法可反轉驗證事件的控制，讓您可以自行獨立處理， `AuthDelegateobject` 不需要對驗證的全域參考。

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre依賴使用者Token來協調驗證。因此，您的身分服務必須傳回此代號，以驗證使用Livefyre的使用者。若要瞭解如何建立Livefyre使用者Token，請參閱建立使用者驗證Token。

>[!NOTE]
>
>成功登入後，Auth會為使用者建立工作階段，並嘗試在重新整理頁面並重新載入時載入使用者作業。`auth.logout()` 將會清除此作業。這表示不需要管理使用者的工作階段獨立於授權。

