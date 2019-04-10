---
description: 建立提取請求結構，以接收並回應存取使用者身分系統的請求。
seo-description: 建立提取請求結構，以接收並回應存取使用者身分系統的請求。
seo-title: 提取請求結構
solution: Experience Manager
title: 提取請求結構
uuid: bc6b9e45-d08 a-48e6-acc6-e4 fa56428 d25
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 提取請求結構{#pull-request-structure}

建立提取請求結構，以接收並回應存取使用者身分系統的請求。

Livefyre會對您的端點URL發出提取請求。

例如，如果您的提取端點URL為：

```
https://example.yoursite.com/some_path/?id={id}
```

對此端點的Livefyre提取請求如下：

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

JSON `lftoken` Web Token是使用您的網路金鑰簽署的， **[!UICONTROL {userAuthToken}]** 且是Livefyre產生的使用者驗證Token。

1. 用 `lftoken` 以驗證對您的「提取URL」的要求是由Livefyre傳送，而非惡意代理。
1. 對於所有傳入的請求：

   * 確定請求中出現 `lftoken` 查詢字串。
   * 請在Livefyre程式庫中使用此 `validateLivefyreToken` 方法，以確保 `lftoken` 使用您的網路金鑰簽署。

   * `lftoken` 如果未存在或驗證失敗，請勿讓端點回應描述檔資訊。請改為以403(Forbidden)狀態碼回應，並無回應主體。

1. `userAuthToken` 由使用者的Livefyre `buildUserAuthToken` 方法產生，使用者id「system」。此使用者是為每個新網路建立的第一個使用者。
1. 若要測試您的頁面，請使用我們 [的Ping for Draw](https://livefyre-p4p-wizard.herokuapp.com/home) 測試程式確認所有內容如預期般運作。
