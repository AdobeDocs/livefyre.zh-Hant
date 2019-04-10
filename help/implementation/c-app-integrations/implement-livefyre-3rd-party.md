---
description: 從頭開始建立Livefyre應用程式，建立自訂體驗和資料視覺化。
seo-description: 從頭開始建立Livefyre應用程式，建立自訂體驗和資料視覺化。
seo-title: 整合Livefyre與協力廠商整合
solution: Experience Manager
title: 將Livefyre整合至CMS
uuid: 5e18e8-8568-45bb-9070-d0 fa43 dd819 b
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 使用協力廠商整合實施Livefyre

從頭開始建立Livefyre應用程式，建立自訂體驗和資料視覺化。

您可以使用Bootstrap和Stream API使用Livefyre和社交資料，從頭開始建立Livefyre應用程式。

對於需要驗證的Livefyre應用程式，請參閱身份整合，以取得有關支援第三方驗證平台的資訊。

實作對話應用程式(留言、聊天、即時部落格、SitenNotes)：

1. 執行應用程式整合。
a. 使用CollectionMeta Token建立系列。
b. 使用Livefyre. js內嵌程式碼結構將Livefyre應用程式整合至網站。

   * 如需如何使用Livefyre. js內嵌代碼結構的詳細資訊，請參閱 [內嵌應用程式](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)。

   * 如需如何整合「注釋應用程式」的詳細資訊，請參閱 [「注釋](/help/using/c-about-apps/c-comments/c-comments.md)」。

   * 如需如何整合聊天應用程式的詳細資訊，請參閱 [聊天](/help/using/c-about-apps/c-chat-app/c-chat-app.md)。

   * 如需如何整合即時部落格應用程式的詳細資訊，請參閱 [即時部落格](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md)。

   * 如需如何整合Sitdemes應用程式的詳細資訊，請參閱 [Sitenets](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md)。

1. 執行驗證整合。
a. 建立使用者驗證Token，在Livefyre中傳遞和儲存使用者資料。
b. 整合協力廠商使用者和驗證平台。如需支援的平台清單，請參閱 [「身分整合](/help/implementation/t-about-identity-integration/t-about-identity-integration.md)」。

1. 執行應用程式自訂。應用程式自訂選項可符合品牌和樣式，並新增自訂功能。

建立視覺效果應用程式(地圖、媒體塗鴉牆、趨勢、轉盤、幻燈片、Storify、Feature Card、Mosaic、民調問答)：

1. 執行應用程式整合。
a. 使用CollectionMeta Token建立系列。
b. 使用Livefyre. js內嵌程式碼結構將Livefyre應用程式整合至網站。如需如何使用Livefyre. js內嵌代碼結構的詳細資訊，請參閱 [內嵌應用程式](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)。

   * 如需如何整合地圖應用程式的詳細資訊，請參閱 [地圖](/help/using/c-about-apps/c-map-app/c-map-app.md)。

   * 如需如何整合Media塗鴉牆應用程式的詳細資訊，請參閱 [媒體牆](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md)。

   * 如需如何整合趨勢應用程式的詳細資訊，請參閱 [趨勢](/help/using/c-about-apps/c-trending-app/c-trending-app.md)。

1. 執行驗證整合。
a. 建立使用者驗證Token，將使用者資料傳送並儲存至Livefyre。
b. 整合協力廠商使用者和驗證平台。如需支援的平台清單，請參閱 [「身分整合](/help/implementation/t-about-identity-integration/t-about-identity-integration.md)」。

>[!NOTE]
>
>Livefyre不支援使用Livefyre. js的轉盤、幻燈片、Storify、Feature Card、Mosaic和民調問答應用程式。
使用 [建立應用程式](/help/using/c-about-apps/c-create-an-app.md) 程序整合這些應用程式。