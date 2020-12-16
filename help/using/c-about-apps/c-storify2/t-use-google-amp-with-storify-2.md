---
description: 使用Livefyre API將Google AMP功能新增至Storify 2頁面，讓內容保持互動式和SEO友好。
seo-description: 使用Livefyre API將Google AMP功能新增至Storify 2頁面，讓內容保持互動式和SEO友好。
seo-title: 搭配Storify 2使用Google AMP
solution: Experience Manager
title: 搭配Storify 2使用Google AMP
uuid: 40c9f083-7284-43ba-ae27-53b1ff9e3954
translation-type: tm+mt
source-git-commit: 65d931e5bd04964db44f8e3a0e000ecec2652893
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# 將Google AMP與Storify 2搭配使用{#use-google-amp-with-storify}

使用Livefyre API將Google AMP功能新增至Storify 2頁面，讓內容保持互動式和SEO友好。

若要搭配Storify 2使用Google AMP，您必須為Storify 2應用程式搭配Google AMP標籤建立頁面。

應用程式請求的AMP版本會從原始頁面更新（使用&#x200B;**amp-live-list** API中的&#x200B;**pollInterval**&#x200B;參數來設定更新請求的間隔）。 為確保AMP頁面上的訪客能快速取得最新內容，請在Storify 2 AMP頁面上保留低快取TTL。

包含在Storify 2應用程式中的貼文的非影像資產（例如視訊）必須使用HTTPS，如AMP規格所指定。 使用Google Cloud內容傳送網路(CDN)的AMP URL使用HTTPS。

若要搭配Storify 2使用Google AMP:

1. 在您的網站上建立經AMP驗證的範本。
1. 使用下列一或多個Google AMP API來自訂您的Google AMP頁面：
   1. [amp-](https://www.ampproject.org/docs/reference/components/amp-iframe) iframeto自訂Storify 2顯示
   1. [amp-live-](https://www.ampproject.org/docs/reference/components/amp-live-list) list以自訂更新的時間間隔
   1. [amp-social-](https://www.ampproject.org/docs/reference/components/amp-social-share) share以新增社交共用按鈕
1. 在`<style amp-custom>`標籤中，將下列Storify 2 AMP頁面的內容加入Storify 2頁面的CSS中：[https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. 將下列Storify 2 AMP標籤API的內容加入您的Google AMP範本：`https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp`其中{{APP_ID}}是Livefyre Studio中Storify 2應用程式的應用程式ID。
   1. 唯一的查詢參數是&#x200B;**pollInterval**，這是應用程式檢查更新的間隔（以毫秒為單位）。
   1. URL包含來自最新貼文的內容（包括推文、影片等）
   1. 發佈者頁面需要從此URL取得內容的頻度，就像您想要更新Google AMP頁面的頻度一樣。
