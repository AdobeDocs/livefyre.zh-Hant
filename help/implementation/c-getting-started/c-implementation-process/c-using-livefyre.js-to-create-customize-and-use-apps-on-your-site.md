---
seo-title: 內嵌應用程式
solution: Experience Manager
title: 內嵌應用程式
uuid: e75caf0e-04ea-4b04-89ed-fea1183 ef63
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 內嵌應用程式{#embed-an-app}

使用Livefyre. js內嵌代碼結構，將Livefyre應用程式新增至您的網頁。

本文件適用於技術對象。有關 [應用程式](/help/using/c-about-apps/c-about-apps.md)的非技術資訊。

本節說明您需要包含在頁面範本中的程式碼結構，以便將Livefyre應用程式內嵌在您的網站上。

1. 使用Livefyre預留位置建立.html檔案。

   在您選擇的文字編輯器中建立新的.html檔案。建立要內嵌應用程式的預留位置Livefyre `<div>` 元素。

   ```
   <html> 
      <head> </head> 
      <body> 
         <div id='livefyre'> </div> 
      </body> 
   </html>
   ```

1. 納入Livefyre. js Library。

   然後，加入Livefyre JS Library。將下列參考放入元素中的 `<script>` 元素 `<head>` 中。然後，在瀏覽器中開啓您的頁面，並使用瀏覽器的網頁偵測器確認Livefyre已載入。

   ```
   <head> 
      <script src='@{livefyre_js}'></script> 
   </head> 
   ```

1. 建構Livefyre應用程式。

   使用 `Livefyre.require` 您打算使用的Livefyre套件來建構核心和SDK應用程式。

   1. 建立核心應用程式。

      若要建立核心應用程式(評論、即時部落格或聊天)，請使用下列結構：

      ```
      Livefyre.require(['fyre.conv#@{fyre_conv_version_prod}'], function(Conv) { 
           new Conv(networkConfig, [convConfig], function(widget) {});  
      });  
      ```

   1. 建立SDK應用程式。

      若要建立「媒體牆」或「動態消息」等SDK應用程式，請使用下列結構：

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

      請參閱 [特定應用程式](/help/using/c-about-apps/c-about-apps.md)的詳細資訊。建議您釘選至最新的主要套件版本(透過 [Livefyre. require](https://cdn.livefyre.com/packages.html))，以避免意外中斷的整合。

下一步：新增驗證至您的網站，讓使用者能夠張貼意見。
