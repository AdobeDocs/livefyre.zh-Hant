---
description: 在整合和測試以除錯授權期間，您可透過主控台登入使用者。
title: 除錯驗證委派
exl-id: fa1c17fa-5aba-4f4c-9217-5823af30af61
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# 調試驗證委派{#debugging-auth-delegate}

在整合和測試以除錯授權期間，您可透過主控台登入使用者。

使用下列`auth.authenticate`(Token)透過主控台登入使用者，並傳遞Livefyre使用者Token，以驗證頁面上的使用者。

您也可以修改上述範例，並在JavaScript中加入下列程式碼片段，以快速將使用者登入Livefyre（需要參考驗證）。

```
window.addEventListener('userAuthenticated', function(data) { 
 Livefyre.require(['auth'], function (auth) { 
  auth.authenticate({livefyre: data.token}); 
 }); 
});
```
