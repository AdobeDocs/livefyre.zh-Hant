---
description: 您可以將Livefyre Identity與Facebook搭配使用，讓使用者使用其Facebook登入來與您網站上的應用程式互動。
seo-description: 您可以將Livefyre Identity與Facebook搭配使用，讓使用者使用其Facebook登入來與您網站上的應用程式互動。
seo-title: 建立Facebook應用程式以搭配Livefyre身分識別使用
solution: Experience Manager
title: 建立Facebook應用程式以搭配Livefyre身分識別使用
uuid: a7f7be4e-8986-4e79-831a-0bb0ae555599
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 建立Facebook應用程式以搭配Livefyre身分識別使用{#create-a-facebook-app-for-use-with-livefyre-identity}

您可以將Livefyre Identity與Facebook搭配使用，讓使用者使用其Facebook登入來與您網站上的應用程式互動。

若要允許您的使用者使用其Facebook認證登入，Livefyre需要下列Facebook應用程式資訊：

* 應用程式 ID
* 應用程式密碼

若要建立Facebook應用程式以搭配Livefyre Identity使用：

1. 請至 [https://developers.facebook.com/apps](https://developers.facebook.com/apps)。
1. 登入您的Facebook開發人員帳戶。
1. 按一 **[!UICONTROL Add New App]** 下或選取現有的應用程式，以便與Livefyre Identity搭配使用。
1. 按一 **[!UICONTROL Settings]**&#x200B;下，然後 **[!UICONTROL Basic]**。 輸入地 **[!UICONTROL Contact Email]** 址、 **[!UICONTROL Display Name]**、 **[!UICONTROL Privacy Policy URL]**&#x200B;和 **[!UICONTROL Terms of Service URL]**。
1. 按一下旁邊的加 **[!UICONTROL +]**&#x200B;號() **[!UICONTROL Products]**。
1. 按一下下 **[!UICONTROL Set Up]** 面的 **[!UICONTROL Facebook Login]**。
1. 按一 **[!UICONTROL Settings]** 下並設定下列項目：

   * Set **[!UICONTROL Client OAuth Login]** to **[!UICONTROL Yes]**.
   * Set **[!UICONTROL Web OAuth Login]** to **[!UICONTROL Yes]**.
   * Set **[!UICONTROL Use Strict Mode for Redirect URIs]** to **[!UICONTROL Yes]**.
   * Set **[!UICONTROL Enforce HTTPS for Web OAuth Login]** to **[!UICONTROL Yes]**.
   * 在下 **[!UICONTROL Valid OAuth redirect URLs]**&#x200B;方新增URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (其中 `{networkName}` 是您提供的Livefyre網路名稱)。

1. Under **[!UICONTROL App Review]**:

   * 讓應用程式公開。
   * 請確定 **[!UICONTROL Approved Items]** 包含 **[!UICONTROL Login Permissions]** 、 `email`和 `public_profile``user_friends`。

完成後，Facebook開發人員的「儀表板」頁面會列出您的應用程式ID和應用程式密碼，以便用於Studio的「整合設定」中。
