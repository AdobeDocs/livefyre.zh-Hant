---
description: 您可以使用Livefyre Identity搭配Microsoft Live Identity，讓使用者使用其Facebook登入功能在您的網站上互動應用程式。
seo-description: 您可以使用Livefyre Identity搭配Microsoft Live Identity，讓使用者使用其Facebook登入功能在您的網站上互動應用程式。
seo-title: 建立Microsoft Live Identity App以搭配Livefyre身分識別使用
solution: Experience Manager
title: 建立Microsoft Live Identity App以搭配Livefyre身分識別使用
uuid: 0c13e1bc-817f-43ed-85d5-09c9e95b6234
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 建立Microsoft Live Identity App以搭配Livefyre身分識別使用{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

您可以使用Livefyre Identity搭配Microsoft Live Identity，讓使用者使用其Facebook登入功能在您的網站上互動應用程式。

若要讓使用者使用其Microsoft Live Identity認證登入，Livefyre需要下列Microsoft Live身分識別資訊：

* 用戶端ID(私密金鑰)
* 用戶端密碼(密碼)

若要建立Microsoft Live Identity應用程式，以便搭配Livefyre Identity使用：

1. 在 [https://apps.dev.microsoft.com中建立或登入Microsoft Live帳戶](https://apps.dev.microsoft.com/)
1. 建立新的應用程式或選取現有應用程式，以便搭配Livefyre Identity使用。
1. 按一下 **[!UICONTROL Add Platform]**，然後選擇「網頁」作為平台類型。
1. 請確定已勾選 **[!UICONTROL Allow Implicit Flow]** 此選項，並使用您的網路名稱(而非{network-name})輸入「重新導向URL」： `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`。
1. 產生新密碼/金鑰配對以取得私密金鑰。
1. In **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**，switching the **[!UICONTROL Enable Microsoft Live Login]** socialto **[!UICONTROL On]**.
1. 輸入Microsoft Live Client ID和Microsoft Live Client密碼。
1. 按一 **[!UICONTROL Save Settings]**下。

完成後，Microsoft Live Identity的應用程式詳細資訊頁面將列出應用程式的用戶端ID(消費者金鑰)和用戶端密碼(消費者密碼)，以便用於Studio的「整合設定」頁面。
