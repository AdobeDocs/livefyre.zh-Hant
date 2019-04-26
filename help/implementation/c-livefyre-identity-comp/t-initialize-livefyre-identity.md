---
description: Livefyre. js Ath套件可確保頁面上的所有社交元件都能發現單一驗證整合。
seo-description: Livefyre. js Ath套件可確保頁面上的所有社交元件都能發現單一驗證整合。
seo-title: 初始化Livefyre身分識別
title: 初始化Livefyre身分識別
uuid: 9365d827-273-4a84-bfe7-9be373 b2 b03 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 初始化Livefyre身分識別{#initialize-livefyre-identity}

Livefyre. js Ath套件可確保頁面上的所有社交元件都能發現單一驗證整合。

Livefyre提供 `lfep-auth-delegate` 一個套件，可為您建立適當的委派委派。必須提供AuthDelegate物件，它知道如何執行驗證動作，例如登入和登出。

1. 將Livefyre. js新增至您的網頁。
1. 若要告訴Ah將這些動作委派至Livefyre Identity，請新增下列項目：

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
