---
description: 從頭開始建立Livefyre應用程式，以建立自訂的體驗和資料視覺化。
seo-description: 從頭開始建立Livefyre應用程式，以建立自訂的體驗和資料視覺化。
seo-title: 將Livefyre與協力廠商整合
solution: Experience Manager
title: 將Livefyre整合至CMS
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 2436c389cbe14c7d64dd8c0392a3e0f031468836
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# 透過協力廠商整合實作Livefyre

從頭開始建立Livefyre應用程式，以建立自訂的體驗和資料視覺化。

您可以使用引導和串流API來使用Livefyre和社交資料，從頭開始建立Livefyre應用程式。

如需需驗證的Livefyre應用程式，請參閱身分整合以取得支援協力廠商驗證平台的相關資訊。

若要實作對話應用程式（註解、聊天、即時部落格、Sides）:

1. 執行應用程式整合。
a.使用CollectionMeta Token建立系列。
b.使用Livefyre.js內嵌程式碼結構，將Livefyre應用程式整合至網站。

   * 如需如何使用Livefyre.js內嵌程式碼結構的詳細資訊，請參閱 [內嵌應用程式](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)。

   * 如需如何整合「注釋應用程式」的詳細資訊，請參 [閱注釋](/help/using/c-about-apps/c-comments/c-comments.md)。

   * 如需如何整合聊天應用程式的詳細資訊，請參閱 [聊天](/help/using/c-about-apps/c-chat-app/c-chat-app.md)。

   * 如需如何整合即時部落格應用程式的詳細資訊，請參 [閱即時部落格](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md)。

   * 如需如何整合Siestroms應用程式的詳細資訊，請參閱 [Siestroms](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md)。

1. 執行驗證整合。
a.建立使用者驗證Token，以在Livefyre中傳遞和儲存使用者資料。
b.整合協力廠商使用者和驗證平台。 如需支援平台的清單，請參閱 [Identity Integration](/help/implementation/t-about-identity-integration/t-about-identity-integration.md)。

1. 執行應用程式自訂。 「應用程式自訂」選項，以符合您的品牌和樣式，並新增自訂功能。

若要建立視覺化應用程式（地圖、媒體塗鴉牆、趨勢、轉盤、幻燈片、景物、功能卡、馬賽克、民調問答）:

1. 執行應用程式整合。
a.使用CollectionMeta Token建立系列。
b.使用Livefyre.js內嵌程式碼結構，將Livefyre應用程式整合至網站。 如需如何使用Livefyre.js內嵌程式碼結構的詳細資訊，請參閱 [內嵌應用程式](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)。

   * 如需如何整合地圖應用程式的詳細資訊，請參 [閱地圖](/help/using/c-about-apps/c-map-app/c-map-app.md)。

   * 如需如何整合媒體塗鴉牆應用程式的詳細資訊，請參閱 [媒體塗鴉牆](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md)。

   * 如需如何整合趨勢應用程式的詳細資訊，請參閱趨勢 [分析](/help/using/c-about-apps/c-trending-app/c-trending-app.md)。

1. 執行驗證整合。
a.建立使用者驗證Token，將使用者資料傳遞並儲存至Livefyre。
b.整合協力廠商使用者和驗證平台。 如需支援平台的清單，請參閱 [Identity Integration](/help/implementation/t-about-identity-integration/t-about-identity-integration.md)。

>[!NOTE]
>
>Livefyre不支援使用Livefyre.js的Carousel、Filmstrip、Storify、Feature Card、Mosaic和Pols Apps。

使用「建立應用程式」 [程式整合這些應用程式](/help/using/c-about-apps/c-create-an-app.md) 。