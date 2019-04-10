---
description: 使用Livefyre API將Google AMP功能新增至您的Storify頁面，以維持內容互動與SEO友好。
seo-description: 使用Livefyre API將Google AMP功能新增至您的Storify頁面，以維持內容互動與SEO友好。
seo-title: 搭配使用Google AMP與Storify2
solution: Experience Manager
title: 搭配使用Google AMP與Storify2
uuid: 40c9f083-7284-43ba-ae27-53b1 ff9 e3954
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 搭配使用Google AMP與Storify2{#use-google-amp-with-storify}

使用Livefyre API將Google AMP功能新增至您的Storify頁面，以維持內容互動與SEO友好。

若要搭配使用Google AMP與Storify2，您必須使用Google AMP標記為您的Storify App建立一個頁面。

AMP版本的應用程式會從原始頁面更新(使用 ******amp-live-list** API中的pollInterval參數來設定更新請求的間隔)。為確保AMP頁面上的訪客快速獲得最新的內容，請在您的Storify AMP頁面上保留低快快TTL。

隨附於Storify應用程式中的非影像資產(例如視訊)必須使用AMP規格指定的HTTPS。使用Google Cloud內容放送網路(CDN)的AMP URL使用HTTPS。

若要搭配Storify使用Google AMP2：

1. 在您的網站上建立AMP驗證的範本。
1. 使用下列一或多個Google AMP API來自訂您的Google AMP頁面：
   1. [amp-iframe](https://www.ampproject.org/docs/reference/components/amp-iframe) to customize the Storify2 display
   1. [amp-live-list](https://www.ampproject.org/docs/reference/components/amp-live-list) 可自訂更新的時間間隔
   1. [amp-social-share](https://www.ampproject.org/docs/reference/components/amp-social-share) to add a social sharing button
1. 將下列Storify AMP頁面的內容加入至 <style amp-custom> tag： [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. 將下列Storify AMP標記API的內容納入您的Google AMP範本中： `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` 其中{{App_ ID}}是Livefyre Studio中Storify2App的應用程式ID。
   1. 唯一的查詢參數是 **PollInterval**，這是應用程式檢查更新的間隔(以毫秒為單位)。
   1. URL包含來自最新貼文的內容(包括推文、影片等)
   1. 發行者頁面需要盡可能地從此URL取得內容，如您想要更新Google AMP頁面。
