---
description: 安裝驗證套件以啟用使用者驗證，讓使用者可以與您的應用程式互動。
title: 驗證套件
exl-id: 639032ee-ed7d-4cb0-83ba-f11d3dc607b6
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---

# 驗證包{#authentication-package}

安裝驗證套件以啟用使用者驗證，讓使用者可以與您的應用程式互動。

Livefyre應用程式使用全域驗證套件，將使用者與應用程式動作產生關聯。 驗證軟體包可通過`Livefyre.require`使用。

若要啟用頁面上的驗證，請先將`Livefyre.js`新增至網頁或網站範本的`<head>`元素。

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

使用Livefyre.require啟用驗證類似於使用要求呼叫其他套件。 需要驗證的整合程式碼如下所示：

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## 方法 {#section_ojx_1lz_fz}

在使用`Livefyre.require`加入上述功能後，驗證模組會公開下列您可呼叫的方法，以通知頁面上其他應用程式有關驗證相關事件的資訊。

| 方法 | 說明 |
|--- |--- |
| `.login(callback)` | 觸發由註冊的AuthDelegate實施的登入流程。 通常只有啟用驗證的應用程式才會呼叫此項，而不是主機頁面本身。 |
| `.logout(callback)` | 通知驗證使用者已透過某些外部方式登出，且所有依賴應用程式應清除其驗證狀態，直到下次登入為止。 這將清除由Auth維護的內部作業。 |
| `.authenticate(credentials)` | 通知驗證使用者已透過某些外部方式進行驗證，且已為使用者購買Livefyre驗證Token。 如果您使用Livefyre Token設定Cookie，或是有使用者的Token，並想要明確登入使用者，請使用此功能。 例如︰<br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | 將驗證的實作詳細資訊（例如，您的自訂驗證流程）委派給您定義的物件。 主機頁面必須呼叫此項，才能啟用Livefyre應用程式的互動功能。 |
