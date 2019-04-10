---
description: 安裝「驗證套件」以啓用使用者驗證，讓使用者可與您的應用程式互動。
seo-description: 安裝「驗證套件」以啓用使用者驗證，讓使用者可與您的應用程式互動。
seo-title: 驗證套件
solution: Experience Manager
title: 驗證套件
uuid: 4eec30cf-66b6-408d-985d-3e23b8b70d01
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 驗證套件{#authentication-package}

安裝「驗證套件」以啓用使用者驗證，讓使用者可與您的應用程式互動。

Livefyre應用程式使用全球驗證套件，將使用者與應用程式動作產生關聯。驗證套件 `Livefyre.require`可供使用。

若要啓用頁面上的驗證，請先新增 `Livefyre.js` 至網頁或網站範本 `<head>` 的元素。

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

使用Livefyre的要求啓用驗證類似於呼叫其他套件。要求驗證的整合程式碼如下：

```
Livefyre.require(['auth'], function (auth) {  
// Perform action... 
});
```

## 方法 {#section_ojx_1lz_fz}

在使用上述項目後 `Livefyre.require`，Auth模組會公開下列方法，以通知頁面上的其他應用程式關於驗證相關事件。

| 方法 | 說明 |
|--- |--- |
| `.login(callback)` | 觸發由已註冊的AuthDelegate實施的登入流程。通常只有啓用驗證的應用程式才會呼叫此項目，而非主機頁面本身。 |
| `.logout(callback)` | 通知使用者已由某些外部方法登出，且所有依賴的應用程式都應清除其驗證狀態，直到下次登入為止。這將清除Auth維護的內部作業。 |
| `.authenticate(credentials)` | 通知Ath使用者已透過某些外部方式驗證，並為使用者取得Livefyre驗證Token。如果您使用Livefyre Token設定Cookie，或想要明確地將使用者登入，請使用此選項。例如： <br>`auth.authenticate({&nbsp;livefyre:&nbsp;`<br>`'<insert&nbsp;lftoken&nbsp;string&nbsp;for&nbsp;newly&nbsp;logged-in&nbsp;user>'&nbsp;});` |
| `.delegate(authDelegate)` | 將驗證的實施詳細資訊(例如您的自訂驗證流程)委派給您定義的物件。主機頁面必須呼叫此項目，才能啓用Livefyre應用程式的互動功能。 |

