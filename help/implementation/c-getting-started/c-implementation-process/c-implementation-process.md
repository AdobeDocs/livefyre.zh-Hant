---
description: 實作Livefyre Studio的期待。
seo-description: 實作Livefyre Studio的期待。
seo-title: 實施程序
solution: Experience Manager
title: 實施程序
uuid: 9a0f394e-3467-47d1-9816-45e2130db440
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 3%

---


# 實施程序{#implementation-process}

實作Livefyre的時間長度視您的實作和工作範圍而定。

## Livefyre網路架構概觀{#section_dgj_l32_rbb}

Livefyre在討論網路架構時使用下列術語：

* 網路. 您計畫使用Livefyre的最高層級網域。
* 網站. 屬於網路一部分的子域或站點部分。
* 應用程式. 轉換您網站上的內容。 內容是使用視覺化應用程式（Mosaic、Carousel、功能卡等）以視覺化方式顯示在應用程式中 或文字格式，使用對話應用程式（注釋、評論、聊天等）。 您可以在網站上放置一或多個應用程式。
* 串流。 串流是搜尋社交媒體和其他網站的篩選器，可自動收集內容，以便在應用程式中協調或直接發佈。
* 內容（例如UGC、注釋）。 顯示在「應用程式」中的項目。 內容可以是視覺化（例如像片或視訊）、僅限音訊或文字。

下圖顯示網路、網站、應用程式和內容之間的關係。

![](assets/network_site_architecture.png)

您有自己的Livefyre例項，它是您用來協調內容、管理使用者等的中央儀表板。 請連絡您的CSM以取得Livefyre實例的存取權。

## 整合步驟 {#section_s2j_d2x_tz}

整合Livefyre有三個主要步驟：

* 應用程式整合

   當您實作Livefyre時，實作的樣式會視您的使用案例而定。 對於[更多關於每種實作類型](/help/implementation/c-getting-started/c-implementation-process/c-app-integration-types.md#c_app_integration_types)。

* 驗證整合

   您必須將現有的使用者管理系統與Livefyre整合，才能在您的網站上取得對話應用程式和任何其他需要使用者驗證的應用程式。 如果您目前未使用使用者管理工具，則可使用Livefyre Identity。 如需[更多有關Livefyre Identity的資訊、它是什麼以及如何設定它](/help/implementation/c-livefyre-identity-comp/c-livefyre-identity-comp.md#c_livefyre_identity)。

* 自訂

   自訂是可選的，但大部分客戶都會自訂應用程式以符合其品牌。

