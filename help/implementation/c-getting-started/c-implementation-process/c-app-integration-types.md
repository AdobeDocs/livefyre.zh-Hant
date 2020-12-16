---
description: 當您實作Livefyre應用程式時，實作的樣式會視您的使用案例而定。 本頁說明建立應用程式的三種方式。
seo-description: 當您實作Livefyre應用程式時，實作的樣式會視您的使用案例而定。 本頁說明建立應用程式的三種方式。
seo-title: CMS應用程式整合
solution: Experience Manager
title: CMS應用程式整合
uuid: 14fd7e36-0e50-4ae3-97f0-2de731c184f5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 1%

---


# CMS應用程式整合{#cms-app-integrations}

當您實作Livefyre應用程式時，實作的樣式會視您的使用案例而定。 本頁說明建立應用程式的三種方式。

Livefyre整合不受任何CMS和使用者設定檔及驗證平台的限制。 根據您的使用案例和需求，以一或多種方式實作Livefyre。

您可以使用傳統整合來建立自訂的AEM元件。

## CMS應用程式整合類型概觀

| 類型 | 開發需求 | 功能 | 優點 | 限制 |
|--- |--- |--- |--- |--- |
| 應用程式設計人員 | 非常低 | 在Studio中建立JS內嵌，以新增至沒有<br>開發人員</br>有限樣式和設定的頁面使用案例：單次使用頁面（事件涵蓋範圍、促銷活動、集線器） | 可讓應用程式在短時間內啟動及執行。 <br>配置可由非技術性成員完成。<br>輕鬆即時變更配置 | 必須先使用Livefyre Studio建立應用程式<br>非自動化 |
| Livefyre.js | 媒體 | 將應用程式整合至您頁面的JavaScript <br>使用案例：可重複使用的範本（編輯內容、產品評論） | 使用完整的應用程式自訂和設定<br>自動化程式，從CMS內動態執行個體化應用程式至您的頁面 | 需要前台的開發人員。 |
| SDK API | 進階 | 從Livefyre擷取您的內容以用於自訂應用程式<br>自訂前端，超越支援的產品<br>使用案例：資料／分析整合與自訂前端應用程式 | 完全掌控應用程式的外觀和感覺 | 需要事先開發。 <br>提高實施的開發力。 |
