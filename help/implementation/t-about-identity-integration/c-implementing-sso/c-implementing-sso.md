---
description: 若要透過Livefyre應用程式未觸發的流程，向Livefyre驗證使用者，Livefyre建議您在AuthDelegate物件上實作forEachAuthentication方法。
seo-description: 若要透過Livefyre應用程式未觸發的流程，向Livefyre驗證使用者，Livefyre建議您在AuthDelegate物件上實作forEachAuthentication方法。
seo-title: 實作SSO
solution: Experience Manager
title: 實作SSO
uuid: c96d456c-b1ac-40e0-8d18-224652b9697f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 實作SSO{#implementing-sso}

若要透過Livefyre應用程式未觸發的流程，向Livefyre驗證使用者，Livefyre建議您在AuthDelegate物件上實作forEachAuthentication方法。

這將在傳遞至 `authDelegate` 時被叫 `auth.delegate`用，並傳遞可多次傳遞的驗證函式。 此方法提供驗證事件的控制反轉，以便您 `AuthDelegateobject` 可以獨立控制，而不需要驗證的全域參考。

```
authDelegate.forEachAuthentication = function (authenticate) { 
 window.addEventListener('userAuthenticated', function(data) { 
  authenticate({livefyre: data.token}); 
 }); 
}
```

Livefyre依賴使用者Token來協調驗證。 因此，您的身分服務必須傳回此Token，才能使用Livefyre驗證使用者。 若要瞭解如何建立Livefyre使用者Token，請參閱「建立使用者驗證Token」。

>[!NOTE]
>
>成功登入後，驗證會為使用者建立工作階段，並會嘗試在重新整理頁面並重新載入使用者的工作階段。 `auth.logout()` 將清除此會話。 這表示您不需要獨立於授權管理使用者的作業。

