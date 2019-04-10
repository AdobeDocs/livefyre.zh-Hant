---
description: 您可以使用Twitter的Livefyre Identity，讓使用者使用其Twitter登入功能在您的網站上互動應用程式。
seo-description: 您可以使用Twitter的Livefyre Identity，讓使用者使用其Twitter登入功能在您的網站上互動應用程式。
seo-title: 建立Twitter應用程式以搭配Livefyre身分識別
solution: Experience Manager
title: 建立Twitter應用程式以搭配Livefyre身分識別
uuid: 841cce7c-618d-4154-85a3-1d96d04bb69
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 建立Twitter應用程式以搭配Livefyre身分識別{#create-a-twitter-app-for-use-with-livefyre-identity}

您可以使用Twitter的Livefyre Identity，讓使用者使用其Twitter登入功能在您的網站上互動應用程式。

若要啓用Twitter登入，Livefyre需要下列Twitter應用程式資訊：

* 消費者金鑰(API金鑰)
* 消費者機密(API密碼)

若要建立Twitter應用程式以搭配Livefyre身分識別使用：

1. 前往 [https://apps.twitter.com/](https://apps.twitter.com/)，然後登入您的Twitter帳戶以建立新的應用程式，或選取現有應用程式以搭配Livefyre Identity使用。
1. 從應用程式的「設定」頁面：

   * 輸入 **[!UICONTROL Callback URL:]**`https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` (其中 **{socialName}** 是您的Livefyre提供的網路名稱。例如：** [!UICONTROL labs]** **[!UICONTROL `labs.fyre.co`]**in
   * 取消選取 **[!UICONTROL Enable Callback Locking]**。
   * 選取 **[!UICONTROL Allow this application to be used to Sign in with Twitter]**。

1. 從 **[!UICONTROL Permissions]** 標籤中選取 **[!UICONTROL Access: Read only]**。

完成後，Twitter的「應用程式管理>按鍵和存取Token」頁面將列出應用程式的消費者金鑰(API金鑰)和消費者密碼(API密碼)，以便用於Studio的「整合設定」頁面。
