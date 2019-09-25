---
description: 您可在整合和測試期間，透過主控台登入使用者，以除錯授權。
seo-description: 在整合和測試以除錯授權期間，您可透過主控台登入使用者。
seo-title: 除錯驗證委派
solution: Experience Manager
title: 除錯驗證委派
uuid: fb0c7396-190e-4dc9-bf26-23dde9efd45d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 除錯驗證委派{#debugging-auth-delegate}

在整合和測試以除錯授權期間，您可透過主控台登入使用者。

使用下列(Token)透過主控台登入使 `auth.authenticate` 用者，並傳遞Livefyre使用者Token，以驗證頁面上的使用者。

您也可以修改上述範例，並在JavaScript中加入下列程式碼片段，以快速將使用者登入Livefyre（需要參考驗證）。

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

