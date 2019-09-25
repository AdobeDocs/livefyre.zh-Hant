---
description: 建立ping，讓您的頁面在使用者更新其描述檔時ping Livefyre。
seo-description: 建立ping，讓您的頁面在使用者更新其描述檔時ping Livefyre。
seo-title: 建立Ping
solution: Experience Manager
title: 建立Ping
uuid: cb8cc043-9ea5-407c-b70f-3f1e37accdae
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# 建立Ping{#build-the-ping}

建立ping，讓您的頁面在使用者更新其描述檔時ping Livefyre。

當Livefyre收到更新通知時， `networkName` 與 `user_id`一起使用時，系統會傳送Pull要求至您的Ping for Pull URL。

>[!NOTE]
>
>403/Not Authorized for your Ping表示Ping請求附加 `lftoken` 了無效。 請確定是針對 `lftoken` 具有網路擁 `user_id` 有者權限或系統用戶。 如果您使用Livefyre程式庫，請使 `buildLivefyreToken` 用方法為請求產生有效的系統Token。

1. 將程式碼新增至您的頁面，讓使用者在更新其描述檔時ping Livefyre。 以此方式建構URL:

```
 POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
```

* **[!UICONTROL networkName:]** 您的Livefyre提供的網路名稱。
* **[!UICONTROL user_id:]** 您的使用者ID。
* **[!UICONTROL token:]** 有效的系統Token。

1. 提取請求結構。
