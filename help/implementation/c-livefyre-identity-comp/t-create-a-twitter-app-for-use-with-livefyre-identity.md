---
description: 您可將Livefyre Identity與Twitter搭配使用，讓使用者使用其Twitter登入，在您的網站上與應用程式互動。
seo-description: 您可將Livefyre Identity與Twitter搭配使用，讓使用者使用其Twitter登入，在您的網站上與應用程式互動。
seo-title: 建立Twitter應用程式以搭配Livefyre身分識別使用
solution: Experience Manager
title: 建立Twitter應用程式以搭配Livefyre身分識別使用
uuid: 841cce7c-618d-4154-85a3-1de96d04bb69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 建立Twitter應用程式以搭配Livefyre身分識別使用{#create-a-twitter-app-for-use-with-livefyre-identity}

您可將Livefyre Identity與Twitter搭配使用，讓使用者使用其Twitter登入，在您的網站上與應用程式互動。

若要啟用Twitter登入，Livefyre需要下列Twitter應用程式資訊：

* 消費者金鑰（API金鑰）
* 消費者密碼（API密碼）

若要建立Twitter應用程式以搭配Livefyre身分識別使用：

1. 前往https://apps.twitter.com/ [](https://apps.twitter.com/)，並登入您的Twitter帳戶以建立新的應用程式，或選取現有的應用程式以搭配Livefyre Identity使用。
1. 從應用程式的「設定」頁面：

   * 輸 **[!UICONTROL Callback URL:]** 入( `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` 其中 **{networkName}** 是Livefyre提供的網路名稱。 For example:** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * 取消選 **[!UICONTROL Enable Callback Locking]**&#x200B;擇。
   * Select **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. 從頁籤 **[!UICONTROL Permissions]** 中，選擇 **[!UICONTROL Access: Read only]**。

完成時，Twitter的「應用程式管理&gt;金鑰和存取Token」頁面會列出應用程式的「消費者金鑰」（API金鑰）和「消費者密碼」（API密碼），以用於Studio的「整合設定」頁面。
