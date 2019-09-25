---
description: 註冊URL端點，讓Livefyre可以使用URL來提取更新的描述檔資訊。
seo-description: 註冊URL端點，讓Livefyre可以使用URL來提取更新的描述檔資訊。
seo-title: 向Studio註冊端點
solution: Experience Manager
title: 向Studio註冊端點
uuid: 4eb816ee-d743-43bf-bfee-d9b9fd98b482
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 向Studio註冊端點{#register-the-endpoint-with-studio}

註冊URL端點，讓Livefyre可以使用URL來提取更新的描述檔資訊。

每個網路僅註冊一次Ping以取得URL。 設定後，除非從使用者管理系統擷取使用者描述檔資料的端點變更，否則此值不應變更。

1. 使用Studio將此URL端點註冊至Livefyre。
1. 註冊Livefyre將從中擷取更新的使用者個人檔案資訊的URL, **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]**&#x200B;前往並在欄位中輸 **[!UICONTROL Ping for Pull URL]** 入。

   例如，URL可以是： `https://example.yoursite.com/some_path/?id={id}`

