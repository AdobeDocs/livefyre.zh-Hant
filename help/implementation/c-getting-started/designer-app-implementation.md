---
description: 搭配使用Bootstrap和Stream API搭配Livefyre應用程式。
seo-description: 搭配使用Bootstrap和Stream API搭配Livefyre應用程式。
seo-title: 應用程式建置
solution: Experience Manager
title: 應用程式建置
uuid: null
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---

# 應用程式建置 {#appimplementation}

使用案例：身為客戶，我想要使用Livefyre. js方法將Livefyre整合至我的第三方CMS。

將Livefyre建置至自訂AEM元件或其他CMS(例如WordPress、SiteCatore或DemandWare)有三種方式：設計人員應用程式實作、API、實作和第三方驗證整合。

## 設計人員應用程式建置 {#designerapp}

內容：整合Livefyre應用程式最簡單快速的方式。您可以設計、設定和產生自訂的Javascript內嵌碼，在幾分鐘內將LiveFrue應用程式整合在頁面上。

如何： [建立、預覽、發佈和內嵌Livefyre應用程式](/help/using/c-about-apps/c-create-an-app.md)

範例： [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Livefyre. js實作 {#livefyrejsimp}

內容： [Livefyre. js](/help/implementation/c-livefyre.js.md) 是在網站上推動應用程式和驗證的核心程式庫。它定義了全域 `window.Livefyre` 物件和單一公開方法，Livefyre. require，可用來載入其他Livefyre JavaScript程式庫，以協助內嵌Livefyre應用程式並整合協力廠商使用者的平台。

How:

* [使用CollectionMeta Token建立系列](/help/implementation/t-create-a-collectionmeta-token.md)

* 使用應用程式整合將應用程式整合到第三方CMS

範例:

* 注釋應用程式： [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* 評論應用程式： [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* Media Wall： [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* 如需使用SDK的進階自訂，請參閱StreamHub SDK。

## API實作 {#apiimplementation}

若要建立自訂體驗和資料視覺化，您可以使用Bootstrap和Stream API使用Livefyre和社交資料來從頭建立Livefyre應用程式。

## 協力廠商驗證整合 {#thirdpartyauth}

如需需要驗證的Livefyre應用程式，請參閱 [第三方驗證平台的身分整合](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) 。

## 客戶實例 {#customerexamples}

下列客戶透過第三方CMS整合實施Livefyre：

* [PGA Tour Media塗鴉牆](https://www.pgatour.com/social-hub.html)

* [Timeout](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
