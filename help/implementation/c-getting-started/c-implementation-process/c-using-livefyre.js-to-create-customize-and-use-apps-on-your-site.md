---
title: 內嵌應用程式
description: 內嵌應用程式
exl-id: 12f75093-1b4d-4cf1-8593-dbd17ff33872
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# 內嵌應用程式{#embed-an-app}

使用Livefyre.js內嵌程式碼結構，將Livefyre應用程式新增至您的網頁。

本檔案適用於技術觀眾。 有關[應用程式的非技術資訊](/help/using/c-about-apps/c-about-apps.md)。

本節說明您在網站上內嵌Livefyre應用程式時，在頁面範本中必須包含的程式碼結構。

1. 使用Livefyre預留位置建立。html檔案。

   在您選擇的文字編輯器中建立新的。html檔案。 建立預留位置Livefyre `<div>`元素，應用程式將嵌入其中。

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. 包含Livefyre.js程式庫。

   然後，加入Livefyre JS程式庫。 在`<head>`元素的`<script>`元素中放置以下引用。 然後，在瀏覽器中開啟您的頁面，並使用瀏覽器的網頁偵測器確認Livefyre已載入。

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. 建構Livefyre應用程式。

   使用`Livefyre.require`傳入您計畫使用的Livefyre套件，以建立核心和SDK應用程式。

   1. 建立核心應用程式。

      若要建立核心應用程式（注釋、即時部落格或聊天），請使用下列結構：

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. 建立SDK應用程式。

      若要建立SDK應用程式，例如「媒體塗鴉牆」或「動態消息」，請使用下列結構：

      ```
             Livefyre.require(['app#{version_number}'], 
         function (App, SDK) { 
            var app = new App({ 
            el: document.getElementById('app'), 
         }); 
         var collection = new SDK.Collection({ 
            network: "`labs.fyre.co`", 
            environment: "livefyre.com", 
            siteId: "315833", 
            articleId: 'livefyre-tweets' 
         }); 
         collection.pipe(feed); 
      }); 
      ```

      請參閱[有關特定應用程式的詳細資訊](/help/using/c-about-apps/c-about-apps.md)。 建議您釘選至最新的主要套件版本（可透過[Livefyre.require](https://cdn.livefyre.com/packages.html)找到），以避免意外的整合中斷。

下一步：將驗證新增至您的網站，讓您的使用者張貼意見。
