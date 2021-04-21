---
description: 若要透過Livefyre應用程式未觸發的流程，向Livefyre驗證使用者，Livefyre建議您在AuthDelegate物件上實作forEachAuthentication方法。
title: 實作SSO
exl-id: 9af75b8a-9d2a-446e-8cce-2de8645038f2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# 實作SSO{#implementing-sso}

若要透過Livefyre應用程式未觸發的流程，向Livefyre驗證使用者，Livefyre建議您在AuthDelegate物件上實作forEachAuthentication方法。

當`authDelegate`傳遞至`auth.delegate`時，會呼叫此功能，並傳遞可多次傳遞的驗證函式。 此方法提供驗證事件的控制反轉，以便您的`AuthDelegateobject`可自我包含，而不需要驗證的全域參考。

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
>成功登入後，驗證會為使用者建立工作階段，並會嘗試在重新整理頁面並重新載入使用者的工作階段。 `auth.logout()` 將清除此會話。這表示您不需要獨立於授權管理使用者的作業。
