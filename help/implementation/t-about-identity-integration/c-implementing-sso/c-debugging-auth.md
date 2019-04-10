---
description: 您可以在整合和測試期間透過主控台登入，進行除錯授權。
seo-description: 您可以在整合和測試期間透過主控台登入，進行除錯授權。
seo-title: 除錯Auth委派
solution: Experience Manager
title: 除錯Auth委派
uuid: fb0c7396-190e-4dc9-bc26-23dde9 efd45 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 除錯Auth委派{#debugging-auth-delegate}

您可以在整合和測試期間透過主控台登入，進行除錯授權。

使用下列(Token)，透過主控台登入使用者 `auth.authenticate` ，並傳遞Livefyre使用者Token以驗證頁面上的使用者。

您也可以修改上述範例，並在JavaScript中加入下列程式碼片段，以快速將使用者記錄至Livefyre(需要對驗證的參考)。

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```

