---
description: Livefyre.js Auth套件可確保頁面上的所有社交元件都能發現單一驗證整合。
title: 初始化Livefyre身分
exl-id: 9990d284-a21e-49fb-932c-62906b41484a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# 初始化Livefyre Identity{#initialize-livefyre-identity}

Livefyre.js Auth套件可確保頁面上的所有社交元件都能發現單一驗證整合。

Livefyre提供`lfep-auth-delegate`套件，可為您建立適當的驗證委派。 必須提供AuthDelegate物件，以瞭解如何執行驗證動作，例如登入和登出。

1. 將Livefyre.js新增至您的網頁。
1. 若要告訴Auth將這些動作委派至Livefyre Identity，請新增下列項目：

   ```
   Livefyre.require([ 
     'livefyre-auth', 
     'identity' 
     ], function (auth, Identity) { 
       var identity = new Identity({ 
         app: "https://identity.livefyre.com/{networkName}.fyre.co" 
       }); 
    auth.delegate( identity ); 
    });
   ```
