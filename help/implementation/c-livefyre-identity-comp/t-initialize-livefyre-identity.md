---
description: Livefyre.js Auth套件可確保頁面上的所有社交元件都能發現單一驗證整合。
seo-description: Livefyre.js Auth套件可確保頁面上的所有社交元件都能發現單一驗證整合。
seo-title: 初始化Livefyre身分
title: 初始化Livefyre身分
uuid: 9365d827-2734-4a84-bfe7-9be573b2b03e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 初始化Livefyre身分{#initialize-livefyre-identity}

Livefyre.js Auth套件可確保頁面上的所有社交元件都能發現單一驗證整合。

Livefyre提供可 `lfep-auth-delegate` 為您建立適當驗證委派的套件。 必須提供AuthDelegate物件，以瞭解如何執行驗證動作，例如登入和登出。

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
