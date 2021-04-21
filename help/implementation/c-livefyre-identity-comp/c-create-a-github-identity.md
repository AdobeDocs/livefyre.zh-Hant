---
description: 您可以搭配使用Livefyre Identity與GitHub Identity，讓使用者使用其GitHub登入來在您的網站上互動應用程式。
title: 建立GitHub身分識別應用程式，以便與Livefyre身分識別搭配使用
exl-id: f25ffd0e-ea4f-42ac-abfc-c02018421b85
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '182'
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
