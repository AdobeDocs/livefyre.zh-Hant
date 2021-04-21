---
description: 建立ping，讓您的頁面在使用者更新其描述檔時ping Livefyre。
title: 建立Ping
exl-id: 626c200b-eaff-483f-b1eb-7d8993fe5e7c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# 生成Ping{#build-the-ping}

建立ping，讓您的頁面在使用者更新其描述檔時ping Livefyre。

當Livefyre收到`networkName`和`user_id`的更新通知時，系統會傳送Pull要求給您的Ping for Pull URL。

>[!NOTE]
>
>403/Not Authorized for your Ping（響應您的Ping）表示Ping請求後附加了無效的`lftoken`。 請確保`lftoken`適用於具有網路所有者權限的`user_id`或系統用戶。 如果您使用Livefyre程式庫，請使用`buildLivefyreToken`方法為請求產生有效的系統Token。

1. 將程式碼新增至您的頁面，讓使用者在更新其描述檔時ping Livefyre。 以此方式建構URL:

   ```
   POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
   ```

   * **[!UICONTROL networkName:]** 您的Livefyre提供的網路名稱。
   * **[!UICONTROL user_id:]** 您的使用者ID。
   * **[!UICONTROL token:]** 有效的系統Token。

1. 提取請求結構。
