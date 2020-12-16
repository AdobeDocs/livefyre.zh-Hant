---
description: 您可以搭配使用Livefyre Identity與GitHub Identity，讓使用者使用其GitHub登入來在您的網站上互動應用程式。
seo-description: 您可以搭配使用Livefyre Identity與GitHub Identity，讓使用者使用其GitHub登入來在您的網站上互動應用程式。
seo-title: 建立GitHub身分識別應用程式，以便與Livefyre身分識別搭配使用
title: 建立GitHub身分識別應用程式，以便與Livefyre身分識別搭配使用
uuid: cf56164c-1521-4a42-89cb-39483764807e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# 建立GitHub身分識別應用程式以搭配Livefyre Identity使用{#create-a-github-identity-app-for-use-with-livefyre-identity}

您可以搭配使用Livefyre Identity與GitHub Identity，讓使用者使用其GitHub登入來在您的網站上互動應用程式。

若要允許使用者使用其GitHub身分認證登入，Livefyre需要下列GitHub身分資訊：

* 用戶端ID（私密金鑰）
* 用戶端密碼（密碼）

若要建立GitHub Identity App以搭配Livefyre Identity使用：

1. 在[](https://github.com/settings/developers)建立或登入GitHub帳戶。
1. 註冊新的應用程式或選取現有的應用程式，以便與Livefyre Identity搭配使用。
1. 在表單上輸入所有資訊。 輸入&#x200B;**[!UICONTROL Authorization callback URL]**，使用您的網路名稱，而不是`{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`。

1. 在&#x200B;**[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**&#x200B;中，將&#x200B;**[!UICONTROL Enable GitHub Login]**&#x200B;切換為&#x200B;**[!UICONTROL On]**。

1. 輸入GitHub用戶端ID和GitHub用戶端密碼。
1. 按一下 **[!UICONTROL Save Settings]**.

完成後，GitHub Identity的應用程式詳細資訊頁面會列出應用程式的用戶端ID（消費者金鑰）和用戶端密碼（消費者密碼），以用於Studio的「整合設定」頁面。
