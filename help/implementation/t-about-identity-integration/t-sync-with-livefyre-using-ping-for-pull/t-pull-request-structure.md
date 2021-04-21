---
description: 建立拉式要求結構，以接收並回應存取您使用者識別系統的要求。
title: 提取請求結構
exl-id: 70203b23-9d7c-4a22-94ba-2a763e200972
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# 提取請求結構{#pull-request-structure}

建立拉式要求結構，以接收並回應存取您使用者識別系統的要求。

Livefyre會向您的端點URL發出「提取」請求。

例如，如果您的Pull端點URL是：

```
https://example.yoursite.com/some_path/?id={id}
```

對此端點的Livefyre Pull請求將是：

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

其中`lftoken`是使用您的網路金鑰簽名的JSON Web Token，而&#x200B;**[!UICONTROL {userAuthToken}]**&#x200B;是Livefyre產生的使用者驗證Token。

1. 使用`lftoken`來驗證Livefyre（而非惡意代理）傳送給您的Ping for Pull URL的請求。
1. 對於所有傳入請求：

   * 請確定請求上存在`lftoken`查詢字串。
   * 使用Livefyre程式庫中的`validateLivefyreToken`方法，確保`lftoken`已與您的網路金鑰簽署。

   * 如果`lftoken`不存在或驗證失敗，請勿允許端點以描述檔資訊回應。 請改為使用403（禁止）狀態碼回覆，且無回覆主體。

1. `userAuthToken` 是由Livefyre方法為使 `buildUserAuthToken` 用者產生，使用者ID為&quot;system&quot;。此用戶是為每個新網路建立的第一個用戶。
