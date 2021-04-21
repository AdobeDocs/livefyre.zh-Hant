---
description: 使用Livefyre.js為您的Livefyre應用程式新增全頁驗證。
title: 使用Livefyre.js將驗證新增至應用程式
exl-id: 6246a2bc-e7ff-4f86-a63a-36261c71d460
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# 使用Livefyre.js{#add-authetication-to-an-app-using-livefyre-js}將驗證新增至應用程式

使用Livefyre.js為您的Livefyre應用程式新增全頁驗證。

`Livefyre.js Aut`h是由Livefyre開發的JavaScript套件，可讓您網站上的所有應用程式共用單一驗證整合。Auth可讓您將這些流委派給您定義的AuthDelegate物件，以定義使用者應如何註冊、登入和登出。

## 步驟1:啟用頁面{#section_pgp_jtt_bbb}的驗證

使用`Livefyre.js`啟用頁面驗證，讓使用者使用您現有的驗證系統登入應用程式並與之互動。

1. 若要啟用頁面上的驗證，請將`Livefyre.js`新增至您網頁或網站範本的&#x200B;*&lt;head>*&#x200B;元素。

   ```
   <script src="//cdn.livefyre.com/Livefyre.js"></script>
   ```

1. 使用`Livefyre.require`啟用驗證。 使用`Livefyre.require`與使用要求呼叫其他軟體包類似。 需要驗證的整合程式碼如下所示：

   ```
   Livefyre.require(['auth'], function (auth) { // Do authy things...});
   ```

## 步驟2:註冊AuthDelegate {#section_oqm_15t_bbb}

要啟用身份驗證，請建立`AuthDelegate`並將其傳遞至`Livefyre.js`身份驗證。

`AuthDelegate`是您定義的物件，可決定使用者登入、登出和檢視描述檔的方式。

1. 建立 `AuthDelegate`. 建構`AuthDelegate`的方式取決於您的身分提供者。 如需詳細指示，請參閱身分整合。

1. 將`AuthDelegate`傳遞至`Livefyre.js`驗證。 最簡單的`AuthDelegate`會在每次使用者從應用程式觸發委派登入方法時記錄相同的使用者：

   ```
   Livefyre.require(['auth'], function (auth) { 
      auth.delegate({ 
         login: function (errback) { 
            errback(null, { livefyre: '<userAuthToken>' }); 
         }    
      });  
   });
   ```

## 步驟3:同步用戶資料{#section_u4m_j5t_bbb}

同步Livefyre和您的身分提供者之間的使用者個人檔案資訊。

您必須在Livefyre和身分提供者之間同步您的使用者個人檔案資訊。 如需詳細資訊，請參閱[Janrain Capture整合](/help/implementation/c-livefyre-identity-comp/c-janrain-capture-backplane-comp.md)。
