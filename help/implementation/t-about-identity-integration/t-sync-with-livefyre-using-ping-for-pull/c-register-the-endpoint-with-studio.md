---
description: 註冊URL端點，讓Livefyre可以使用URL來提取更新的描述檔資訊。
title: 向Studio註冊端點
exl-id: 2910a13a-ae88-41d7-ba7c-88d7a1dbe445
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# 使用Studio{#register-the-endpoint-with-studio}註冊端點

註冊URL端點，讓Livefyre可以使用URL來提取更新的描述檔資訊。

每個網路僅註冊一次Ping以取得URL。 設定後，除非從使用者管理系統擷取使用者描述檔資料的端點變更，否則此值不應變更。

1. 使用Studio將此URL端點註冊至Livefyre。
1. 註冊Livefyre將從中擷取更新的使用者設定檔資訊的URL，前往&#x200B;**[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]**，然後在&#x200B;**[!UICONTROL Ping for Pull URL]**&#x200B;欄位中輸入。

   例如，URL可以是：`https://example.yoursite.com/some_path/?id={id}`
