---
description: 您可將Livefyre Identity與Twitter搭配使用，讓使用者使用其Twitter登入，在您的網站上與應用程式互動。
title: 建立Twitter應用程式以搭配Livefyre Identity使用
exl-id: 4f2b919f-fe5d-49a3-8432-04ffb3d68ce4
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# 建立Twitter應用程式以搭配Livefyre Identity使用{#create-a-twitter-app-for-use-with-livefyre-identity}

您可將Livefyre Identity與Twitter搭配使用，讓使用者使用其Twitter登入，在您的網站上與應用程式互動。

若要啟用Twitter登入，Livefyre需要下列Twitter應用程式資訊：

* 消費者金鑰（API金鑰）
* 消費者密碼（API密碼）

若要建立與Livefyre Identity搭配使用的Twitter應用程式：

1. 前往[https://apps.twitter.com/](https://apps.twitter.com/)，並登入您的Twitter帳戶以建立新應用程式或選取現有應用程式以搭配Livefyre Identity使用。
1. 從應用程式的「設定」頁面：

   * 輸入&#x200B;**[!UICONTROL Callback URL:]** `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre`(其中&#x200B;**{networkName}**&#x200B;是您Livefyre提供的網路名稱。 例如：** [!UICONTROL labs]**（**[!UICONTROL `labs.fyre.co`]**&#x200B;中）。
   * 取消選擇&#x200B;**[!UICONTROL Enable Callback Locking]**。
   * 選擇 **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. 從&#x200B;**[!UICONTROL Permissions]**&#x200B;標籤中，選擇&#x200B;**[!UICONTROL Access: Read only]**。

完成後，Twitter的「應用程式管理>金鑰和存取Token」頁面會列出應用程式的消費者金鑰（API金鑰）和消費者機密（API密碼），以用於Studio的「整合設定」頁面。
