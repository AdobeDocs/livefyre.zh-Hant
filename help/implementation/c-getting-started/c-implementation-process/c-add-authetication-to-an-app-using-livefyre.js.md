---
description: 使用Livefyre. js為您的Livefyre應用程式新增整頁驗證。
seo-description: 使用Livefyre. js為您的Livefyre應用程式新增整頁驗證。
seo-title: 使用Livefyre. js新增驗證至應用程式
solution: Experience Manager
title: 使用Livefyre. js新增驗證至應用程式
uuid: b7c61e07-e341-45d7-9112-c50155 e38 f1 d
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 使用Livefyre. js新增驗證至應用程式{#add-authetication-to-an-app-using-livefyre-js}

使用Livefyre. js為您的Livefyre應用程式新增整頁驗證。

`Livefyre.js Aut`h是由Livefyre開發的JavaScript套件，可讓您的網站上所有應用程式共用單一驗證整合。Auth可讓您定義使用者應如何註冊、登入，並將這些流程委派給您定義的authDelegate物件來登出。

## 步驟1：啓用頁面驗證 {#section_pgp_jtt_bbb}

用於 `Livefyre.js` 啓用頁面驗證，允許使用者使用您現有的驗證系統登入並與應用程式互動。

1. 若要啓用頁面上的驗證，請新增 `Livefyre.js` 至網頁或網站範本 *的< head>* 元素。

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. 用於 `Livefyre.require` 啓用驗證。使用 `Livefyre.require` 類似於呼叫其他套件時使用。要求驗證的整合程式碼如下：

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## 步驟2：註冊AuthDelegate {#section_oqm_15t_bbb}

若要啓用驗證，請建立一個並 `AuthDelegate` 將它傳遞 `Livefyre.js` 至驗證。

是 `AuthDelegate` 您定義的物件，可決定使用者登入、登出及檢視描述檔的方式。

1. 建立 `AuthDelegate`一個。您建構的 `AuthDelegate` 方式取決於您的身分提供者。如需詳細指示，請參閱識別整合。

1. 傳遞 `AuthDelegate``Livefyre.js` 「驗證」。每當使用者從應用程式觸發委派登入方法時，最簡單 `AuthDelegate` 的使用者就會登入相同的使用者：

   ```
   Livefyre.require(['auth'], function (auth) { 
      auth.delegate({ 
         login: function (errback) { 
            errback(null, { livefyre: '<userAuthToken>' }); 
         }    
      });  
   });
   ```

## 步驟3：同步使用者資料 {#section_u4m_j5t_bbb}

同步Livefyre和您的身分提供者之間的使用者描述檔資訊。

您必須同步Livefyre和您的身分提供者之間的使用者描述檔資訊。如需詳細資訊，請參閱 [「Janrain Capture整合](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)」。
