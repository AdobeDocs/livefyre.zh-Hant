---
description: 您可以將Livefyre Identity與Facebook搭配使用，讓使用者使用其Facebook登入來與您網站上的應用程式互動。
seo-description: 您可以將Livefyre Identity與Facebook搭配使用，讓使用者使用其Facebook登入來與您網站上的應用程式互動。
seo-title: 建立Facebook應用程式以搭配Livefyre身分識別使用
solution: Experience Manager
title: 建立Facebook應用程式以搭配Livefyre身分識別使用
uuid: a7f7be4e-8986-4e79-831a-0bb0ae555599
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---


# 建立Facebook應用程式以搭配Livefyre Identity使用{#create-a-facebook-app-for-use-with-livefyre-identity}

您可以將Livefyre Identity與Facebook搭配使用，讓使用者使用其Facebook登入來與您網站上的應用程式互動。

若要允許您的使用者使用其Facebook認證登入，Livefyre需要下列Facebook應用程式資訊：

* 應用程式 ID
* 應用程式密碼

若要建立Facebook應用程式以搭配Livefyre Identity使用：

1. 前往[https://developers.facebook.com/apps](https://developers.facebook.com/apps)。
1. 登入您的Facebook開發人員帳戶。
1. 按一下&#x200B;**[!UICONTROL Add New App]**&#x200B;或選取現有應用程式以搭配Livefyre Identity使用。
1. 按一下&#x200B;**[!UICONTROL Settings]** ，然後按一下&#x200B;**[!UICONTROL Basic]**。 輸入&#x200B;**[!UICONTROL Contact Email]**&#x200B;地址、**[!UICONTROL Display Name]**、**[!UICONTROL Privacy Policy URL]**&#x200B;和&#x200B;**[!UICONTROL Terms of Service URL]**。
1. 按一下&#x200B;**[!UICONTROL Products]**&#x200B;旁的加號(**[!UICONTROL +]**)。
1. 按一下&#x200B;**[!UICONTROL Facebook Login]**&#x200B;下的&#x200B;**[!UICONTROL Set Up]**。
1. 按一下&#x200B;**[!UICONTROL Settings]**&#x200B;並設定以下內容：

   * 將&#x200B;**[!UICONTROL Client OAuth Login]**&#x200B;設為&#x200B;**[!UICONTROL Yes]**。
   * 將&#x200B;**[!UICONTROL Web OAuth Login]**&#x200B;設為&#x200B;**[!UICONTROL Yes]**。
   * 將&#x200B;**[!UICONTROL Use Strict Mode for Redirect URIs]**&#x200B;設為&#x200B;**[!UICONTROL Yes]**。
   * 將&#x200B;**[!UICONTROL Enforce HTTPS for Web OAuth Login]**&#x200B;設為&#x200B;**[!UICONTROL Yes]**。
   * 在&#x200B;**[!UICONTROL Valid OAuth redirect URLs]**&#x200B;下，新增URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre`（其中`{networkName}`是您提供的Livefyre網路名稱）。

1. 在&#x200B;**[!UICONTROL App Review]**&#x200B;下：

   * 讓應用程式公開。
   * 確保&#x200B;**[!UICONTROL Login Permissions]**&#x200B;的&#x200B;**[!UICONTROL Approved Items]**&#x200B;包含`email`、`public_profile`和`user_friends`。

完成後，Facebook開發人員的「儀表板」頁面會列出您的應用程式ID和應用程式密碼，以便用於Studio的「整合設定」中。
