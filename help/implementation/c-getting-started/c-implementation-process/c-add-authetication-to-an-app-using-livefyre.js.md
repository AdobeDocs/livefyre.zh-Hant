---
description: 使用Livefyre.js為您的Livefyre應用程式新增全頁驗證。
seo-description: 使用Livefyre.js為您的Livefyre應用程式新增全頁驗證。
seo-title: 使用Livefyre.js將驗證新增至應用程式
solution: Experience Manager
title: 使用Livefyre.js將驗證新增至應用程式
uuid: b7c61e07-e341-45d7-9112-c50155e38f1d
translation-type: tm+mt
source-git-commit: a6aebcc14325632cab0415e4aa4a24fda8a19bfc

---


# 使用Livefyre.js將驗證新增至應用程式{#add-authetication-to-an-app-using-livefyre-js}

使用Livefyre.js為您的Livefyre應用程式新增全頁驗證。

`Livefyre.js Aut`h是由Livefyre開發的JavaScript套件，可讓您網站上的所有應用程式共用單一驗證整合。 Auth可讓您將這些流委派給您定義的AuthDelegate物件，以定義使用者應如何註冊、登入和登出。

## 步驟1:啟用頁面驗證 {#section_pgp_jtt_bbb}

使用 `Livefyre.js` 為頁面啟用驗證，以允許使用者使用您現有的驗證系統登入應用程式並與之互動。

1. 若要啟用頁面上的驗證，請 `Livefyre.js` 新增至網 *頁或網站範本的* &lt;head&gt;元素。

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. 使用 `Livefyre.require` 啟用驗證。 使用 `Livefyre.require` 與使用要求呼叫其他包類似。 需要驗證的整合程式碼如下所示：

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## 步驟2:註冊AuthDelegate {#section_oqm_15t_bbb}

若要啟用驗證，請建 `AuthDelegate` 立並傳遞給驗 `Livefyre.js` 證。

A `AuthDelegate` 是您定義的物件，可決定使用者登入、登出和檢視描述檔的方式。

1. 建立 `AuthDelegate`. 建構方式取決於 `AuthDelegate` 您的身分提供者。 如需詳細指示，請參閱身分整合。

1. 將傳遞 `AuthDelegate` 至驗 `Livefyre.js` 證。 最簡單 `AuthDelegate` 的記錄方式是，每當使用者從應用程式觸發委派登入方法時：

   ```
   Livefyre.require(['auth'], function (auth) { 
      auth.delegate({ 
         login: function (errback) { 
            errback(null, { livefyre: '<userAuthToken>' }); 
         }    
      });  
   });
   ```

## 步驟3:同步使用者資料 {#section_u4m_j5t_bbb}

同步Livefyre和您的身分提供者之間的使用者個人檔案資訊。

您必須在Livefyre和身分提供者之間同步您的使用者個人檔案資訊。 如需詳細資訊，請參 [閱Janrain Capture整合](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)。
