---
description: 2018年3月23日發行說明。
seo-description: 2018年3月23日發行說明。
seo-title: 2018 年 3 月 23 日
solution: Experience Manager
title: 2018 年 3 月 23 日
uuid: b69b8715-ace4-48e0-8f54-ce4e12170ef3
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 7%

---


# 2018年3月23日{#march}

2018年3月23日發行說明。

## 新功能 {#section_syx_mdt_wcb}

以下是此版本生產版本的新功能：

* **Production的新功能：** Facebook已建立Facebook登入的安全性更新，導致客戶的Facebook登入無法正常運作。若要修正此問題，您必須：

   1. 將下列URL新增至「用戶端OAuth設定」的&#x200B;**[!UICONTROL Valid OAuth redirect URIs]**&#x200B;欄位。 將`<networkname>`替換為正確的網路名稱：
      `https://identity.livefyre.com/<networkname>/api/v1.0/public/profile/social/complete/facebook_fyre`

   1. 將&#x200B;**[!UICONTROL Use Strict Mode for Redirect URI]**&#x200B;切換為&#x200B;**[!UICONTROL Yes]**。

* **UAT的新功能：** 您現在可以選擇串流中智慧標籤的信賴臨界值。設定標籤的精確度分數(0-100)可讓您控制我們擷取的資產的精確度。

## 問題 {#section_ehw_ndt_wcb}

本版本已解決下清單格中的問題。

## 生產版本

| **問題類型** | **元件** | **發行說明** |
|---|---|---|
| 錯誤 | 媒體牆 | 修正媒體塗鴉牆中，從串流規則新增Instagram貼文時，無法點選標籤的問題。 |
| 錯誤 | ModQ | 修正ModQ無法正確載入的問題。 |
| 錯誤 | ModQ | 已修正內嵌音訊導致ModQ停止運作的問題。 |

## UAT發行

| **問題類型** | **元件** | **發行說明** |
|---|---|---|
| 增強功能 | 幻燈片 | 已修正某些問題，讓幻燈片更容易存取。 |
| 增強功能 | Studio | 您現在可以使用IMS登入來登入Livefyre。 |

