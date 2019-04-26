---
description: 您可以使用GitHub身分識別搭配使用Livefyre Identity，讓使用者使用GitHub登入在您的網站上互動應用程式。
seo-description: 您可以使用GitHub身分識別搭配使用Livefyre Identity，讓使用者使用GitHub登入在您的網站上互動應用程式。
seo-title: 建立GitHub身分應用程式以搭配Livefyre身分識別使用
title: 建立GitHub身分應用程式以搭配Livefyre身分識別使用
uuid: cf56164c-152-1a42-89cb-39483764807e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 建立GitHub身分應用程式以搭配Livefyre身分識別使用{#create-a-github-identity-app-for-use-with-livefyre-identity}

您可以使用GitHub身分識別搭配使用Livefyre Identity，讓使用者使用GitHub登入在您的網站上互動應用程式。

若要允許使用者使用其GitHub身分認證登入，Livefyre需要下列GitHub身分資訊：

* 用戶端ID(私密金鑰)
* 用戶端密碼(密碼)

若要建立GitHub身分應用程式，以便搭配Livefyre Identity使用：

1. 建立或登入GitHub [](https://github.com/settings/developers)帳戶。
1. 註冊新的應用程式，或選取現有應用程式以搭配Livefyre身分識別使用。
1. 輸入表格上的所有資訊。請使用 **[!UICONTROL Authorization callback URL]**您的網路名稱來輸入 `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`。

1. In **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**，switching the **[!UICONTROL Enable GitHub Login]** socialto **[!UICONTROL On]**.

1. 輸入GitHub用戶端ID和GitHub用戶端密碼。
1. 按一 **[!UICONTROL Save Settings]**下。

完成後，GitHub Identity的應用程式詳細資訊頁面將列出應用程式的用戶端ID(消費者金鑰)和用戶端密碼(消費者密碼)，以便用於Studio的「整合設定」頁面。
