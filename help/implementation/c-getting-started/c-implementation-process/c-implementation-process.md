---
description: 實作Livefyre Studio的期望。
seo-description: 實作Livefyre Studio的期望。
seo-title: 實作程序
solution: Experience Manager
title: 實作程序
uuid: 9a0f394e-3467-47d1-9816-45e2130db440
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 實作程序{#implementation-process}

實施Livefyre的時間長度取決於您的實施和工作範圍。

## Livefyre網路架構概觀 {#section_dgj_l32_rbb}

Livefyre在討論網路架構時使用下列詞彙：

* 網路。您打算使用Livefyre的最高層網域。
* 網站。屬於網路的子網域或網站區域。
* 應用程式。在您的網站上呈現內容。內容會以視覺化方式顯示在應用程式中，使用Visualization Apps(Mosic、Carousel、Feature Card等)或文字格式，使用對話應用程式(留言、評論、聊天等)。您可以將一或多個應用程式放在您的網站上。
* 串流。串流是搜尋社交媒體和其他網站的篩選器，可自動收集內容以進行協調或直接在應用程式中發佈。
* 內容(例如UGC、留言)。應用程式中顯示的項目。內容可以是視覺內容(例如像片或影片)、純音訊或文字。

下圖顯示網路、網站、應用程式和內容之間的關係。

![](assets/network_site_architecture.png)

您有自己的Livefyre例項，此例項是您的中央控制面板，用於協調內容、管理使用者等。請連絡您的CSM以存取您的Livefyre例項。

## 整合步驟 {#section_s2j_d2x_tz}

整合Livefyre的主要步驟有三個：

* 應用程式整合

   實施Livefyre時，實作樣式視您的使用案例而定。如 [需各實施類型](/help/implementation/c-getting-started/c-implementation-process/c-app-integration-types.md#c_app_integration_types)的詳細資訊，請參閱。

* 驗證整合

   您必須將現有的使用者管理系統與Livefyre整合，以便用於對話應用程式和任何需要網站使用者驗證的應用程式。如果您目前未使用使用者管理工具，則可使用Livefyre Identity。如需 [Livefyre身分識別的詳細資訊，以及如何設定](/help/implementation/c-livefyre-identity-comp/c-livefyre-identity-comp.md#c_livefyre_identity)，請參閱。

* 自訂

   自訂是選擇性的，但大部分的客戶自訂應用程式以符合其品牌。

