---
description: 您可以使用Livefyre Identity與Facebook搭配使用Facebook登入，以便在您的網站上與應用程式互動。
seo-description: 您可以使用Livefyre Identity與Facebook搭配使用Facebook登入，以便在您的網站上與應用程式互動。
seo-title: 建立Facebook應用程式以搭配Livefyre身分識別
solution: Experience Manager
title: 建立Facebook應用程式以搭配Livefyre身分識別
uuid: a7f7e-89866e79-831a-0bb0ae555599
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 建立Facebook應用程式以搭配Livefyre身分識別{#create-a-facebook-app-for-use-with-livefyre-identity}

您可以使用Livefyre Identity與Facebook搭配使用Facebook登入，以便在您的網站上與應用程式互動。

為了讓您的使用者使用其Facebook認證登入，Livefyre需要下列Facebook應用程式資訊：

* 應用程式ID
* 應用程式密碼

若要建立用於搭配Livefyre身分識別的Facebook應用程式：

1. 前往 [https://developers.facebook.com/apps](https://developers.facebook.com/apps)。
1. 登入您的Facebook開發人員帳戶。
1. 按一下 **[!UICONTROL Add New App]** 或選取現有應用程式，以便搭配Livefyre Identity使用。
1. 然後按一下 **[!UICONTROL Settings]****[!UICONTROL Basic]**。輸入 **[!UICONTROL Contact Email]** 地址、 **[!UICONTROL Display Name]**和 **[!UICONTROL Privacy Policy URL]****[!UICONTROL Terms of Service URL]**。
1. 按一下旁邊的加號( **[!UICONTROL +]**) **[!UICONTROL Products]**。
1. 按一下 **[!UICONTROL Set Up]** 下方 **[!UICONTROL Facebook Login]**。
1. 按一下並 **[!UICONTROL Settings]** 設定下列項目：

   * 設 **[!UICONTROL Client OAuth Login]****[!UICONTROL Yes]**為。
   * 設 **[!UICONTROL Web OAuth Login]****[!UICONTROL Yes]**為。
   * 設 **[!UICONTROL Use Strict Mode for Redirect URIs]****[!UICONTROL Yes]**為。
   * 設 **[!UICONTROL Enforce HTTPS for Web OAuth Login]****[!UICONTROL Yes]**為。
   * 在下方 **[!UICONTROL Valid OAuth redirect URLs]**，新增URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (您 `{networkName}` 的Livefyre提供的網路名稱)。

1. **[!UICONTROL App Review]**下方：

   * 讓應用程式公開。
   * 確定 **[!UICONTROL Approved Items]****[!UICONTROL Login Permissions]** 包含 `email`、 `public_profile`和 `user_friends`。

完成後，Facebook開發人員的控制面板頁面將列出您的應用程式ID和應用程式密碼，以便用於Studio的「整合設定」中。
