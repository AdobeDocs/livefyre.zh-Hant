---
description: 搭配Livefyre應用程式使用引導和串流API。
seo-description: 搭配Livefyre應用程式使用引導和串流API。
seo-title: 應用程式實作
solution: Experience Manager
title: 應用程式實作
uuid: null
translation-type: tm+mt
source-git-commit: b737f2c6afb03d91041a317cc0afb790c3eadcb1

---

# 應用程式實作 {#appimplementation}

使用案例：身為客戶，我想使用Livefyre.js方法，將Livefyre整合至我的第三方CMS。

在自訂AEM元件或其他CMS（例如WordPress、Sitecore或DemandWare）中實作Livefyre有三種方式：設計人員應用程式實作、API、實作和協力廠商驗證整合。

## 設計人員應用程式實作 {#designerapp}

什麼：整合Livefyre應用程式的最簡單、最快速方式。 您可以設計、設定並產生自訂的Javascript內嵌代碼，在幾分鐘內將Liveyfre應用程式整合在頁面上。

方式：建 [立、預覽、發佈和內嵌Livefyre應用程式](/help/using/c-about-apps/c-create-an-app.md)

範例： [https://codepen.io/dharafyre/pen/bvGrLo](https://codepen.io/dharafyre/pen/bvGrLo)

### Livefyre.js實作 {#livefyrejsimp}

什麼：Livefyre [](/help/implementation/c-livefyre.js.md) .js是核心資料庫，可為網站上的「應用程式」和「驗證」提供支援。 它定義全域物 `window.Livefyre` 件和單一公用方法Livefyre.require，可用來載入其他Livefyre javaScript程式庫，以協助內嵌Livefyre應用程式並與協力廠商使用者驗證平台整合。

方式：

* [使用CollectionMeta Token建立系列](/help/implementation/t-create-a-collectionmeta-token.md)

* 使用應用程式整合將應用程式整合至協力廠商CMS

範例:

* 注釋應用程式： [https://codepen.io/dharafyre/pen/oYoJdP](https://codepen.io/dharafyre/pen/oYoJdP)

* 評論應用程式： [https://codepen.io/dharafyre/pen/GXgvvd](https://codepen.io/dharafyre/pen/GXgvvd)

* 媒體牆： [https://codepen.io/dharafyre/pen/dNMPvM](https://codepen.io/dharafyre/pen/dNMPvM)

* 如需使用SDK的進階自訂，請參閱StreamHub SDK。

## API實作 {#apiimplementation}

若要建立自訂的體驗和資料視覺化，您可使用引導和串流API，從頭開始使用Livefyre和社交資料來建立Livefyre應用程式。

## 協力廠商驗證整合 {#thirdpartyauth}

如需需要驗證的Livefyre應用程式，請參 [閱協力廠商驗證平台的Identity Integration](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) 。

## 客戶範例 {#customerexamples}

下列客戶透過協力廠商CMS整合實作Livefyre:

* [PGA巡迴賽媒體牆](https://www.pgatour.com/social-hub.html)

* [逾時](https://www.timeout.com/london/restaurants/forest-bar-kitchen#tab_panel_3)
