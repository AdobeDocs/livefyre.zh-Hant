---
description: 2018年月23日發行的發行說明。
seo-description: 2018年月23日發行的發行說明。
seo-title: 2018 年 3 月 23 日
solution: Experience Manager
title: 2018 年 3 月 23 日
uuid: b69b8715-ace4-48e0-8f54-ce4 e12170 ef3
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 2018年月23日{#march}

2018年月23日發行的發行說明。

## 新特性 {#section_syx_mdt_wcb}

此發行版本的生產版本包含下列功能：

* **生產新功能：** Facebook建立了Facebook登入安全性更新，會導致客戶的Facebook登入無法正確運作。若要修正此問題，您必須：

   1. 在Client OAuth設定中新增下列URL至 **[!UICONTROL Valid OAuth redirect URIs]** 欄位。以 `<networkname>` 正確的網路名稱取代：
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. 切換 **[!UICONTROL Use Strict Mode for Redirect URI]** 至 **[!UICONTROL Yes]**。

* **UAT的新功能：** 您現在可以在串流中選擇智慧標記的信賴臨界值。設定標籤的精確度分數(0-100)可讓您控制正在擷取之資產的準確性。

## 問題 {#section_ehw_ndt_wcb}

下列表格中的問題已解決。

## 生產版本

| **問題類型** | **元件** | **發行說明** |
|---|---|---|
| Bug | Media Wall | 修正媒體塗鴉牆中，從串流規則新增Instagram貼文時，無法點按標記的問題。 |
| Bug | ModQ | 修正ModQ無法正確載入的問題。 |
| Bug | ModQ | 修正內嵌音效造成ModQ停止運作的問題。 |

## UAT版本

| **問題類型** | **元件** | **發行說明** |
|---|---|---|
| 增強功能 | 幻燈片幻燈片 | 修正某些問題，使檔案更易於存取。 |
| 增強功能 | Studio | 您現在可以使用IMS登入登入Livefyre。 |

