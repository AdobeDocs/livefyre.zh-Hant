---
description: 建立ping，如此當使用者更新其描述檔時，您的頁面就會掃描Livefyre。
seo-description: 建立ping，如此當使用者更新其描述檔時，您的頁面就會掃描Livefyre。
seo-title: 建立Ping
solution: Experience Manager
title: 建立Ping
uuid: cb8cc043-9ea5-407c-b70 f-3f1 e37 acco
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 建立Ping{#build-the-ping}

建立ping，如此當使用者更新其描述檔時，您的頁面就會掃描Livefyre。

當Livefyre收到更新通知時，系統會傳送「提取」請求至您的「提取URL」的「Ping `networkName``user_id`URL」。

>[!NOTE]
>
>403/未授權回應您的Ping表示Ping請求附加無效 `lftoken` 的附加。請確定適用於 `lftoken` 網路 `user_id` 擁有者權限或系統使用者。如果您使用Livefyre程式庫，請使用 `buildLivefyreToken` 方法為請求產生有效的系統Token。

1. 在使用者更新其描述檔時，將程式碼新增至您的頁面，以進行Livefyre。以此方式建構URL：

```
 POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
```

* **[!UICONTROL networkName:]** 您的Livefyre提供的網路名稱。
* **[!UICONTROL user_id:]** 使用者的ID。
* **[!UICONTROL token:]** 有效的系統代號。

1. 提取請求結構。
