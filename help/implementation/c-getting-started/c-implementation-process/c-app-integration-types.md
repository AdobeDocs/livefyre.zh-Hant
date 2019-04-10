---
description: 實施Livefyre應用程式時，實作樣式視您的使用案例而定。此頁面說明您可以建立應用程式的三種方式的功能。
seo-description: 實施Livefyre應用程式時，實作樣式視您的使用案例而定。此頁面說明您可以建立應用程式的三種方式的功能。
seo-title: CMS應用程式整合
solution: Experience Manager
title: CMS應用程式整合
uuid: 14fd7e36-0e50-4ae3-97f0-2de731c184f
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# CMS應用程式整合{#cms-app-integrations}

實施Livefyre應用程式時，實作樣式視您的使用案例而定。此頁面說明您可以建立應用程式的三種方式的功能。

Livefyre整合與任何CMS和User Profile和Auth平台密不可分。根據您的使用案例和需求，以一或多個方式實施Livefyre。

您可以使用傳統整合來建立自訂的AEM元件。

## CMS應用程式整合類型概觀

| Type | 開發需求 | 功能 | Pros | 限制 |
|--- |--- |--- |--- |--- |
| App Designer | 非常低 | 在Studio中建立JS內嵌功能，以新增至頁面，而不需有開發人員 <br>有限樣式和設定可用 </br>的設定：單一使用頁面(事件涵蓋範圍、促銷活動、ub) | 可在短時間內啓動應用程式並執行。<br>設定可由非技術成員進行。<br>輕鬆即時變更組態 | 必須使用Livefyre Studio建立應用程式 <br>，而非自動化 |
| Livefyre. js | medium | 將應用程式整合至頁面的JavaScript <br>使用案例：可重復使用的範本(編輯內容、產品評論) | 使用完整的應用程式自訂和組態 <br>套件自動化從CMS動態實例化應用程式到頁面的程序 | 需要開發人員。 |
| SDK API | 進階 | 從Livefyre擷取您的內容以用於自訂應用程式 <br>自訂前端超越支援的方案 <br>使用案例：資料/分析整合與自訂前端應用程式 | 完全掌控應用程式的外觀和感覺 | 需要前期開發。<br>更高層級的開發工作。 |
