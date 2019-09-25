---
description: 您可將Livefyre Identity與Microsoft Live Identity搭配使用，讓使用者使用其Facebook登入，在您的網站上與應用程式互動。
seo-description: 您可將Livefyre Identity與Microsoft Live Identity搭配使用，讓使用者使用其Facebook登入，在您的網站上與應用程式互動。
seo-title: 建立Microsoft Live Identity應用程式以搭配Livefyre Identity使用
solution: Experience Manager
title: 建立Microsoft Live Identity應用程式以搭配Livefyre Identity使用
uuid: 0c13e1bc-817f-43ed-85d5-09c9e95b6234
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 建立Microsoft Live Identity應用程式以搭配Livefyre Identity使用{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

您可將Livefyre Identity與Microsoft Live Identity搭配使用，讓使用者使用其Facebook登入，在您的網站上與應用程式互動。

若要允許使用者使用其Microsoft Live Identity認證登入，Livefyre需要下列Microsoft Live Identity資訊：

* 用戶端ID（私密金鑰）
* 用戶端密碼（密碼）

若要建立Microsoft Live Identity應用程式以搭配Livefyre Identity使用：

1. 建立或登入Microsoft Live帳戶，網址為 [https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)
1. 建立新應用程式或選取現有應用程式，以便與Livefyre Identity搭配使用。
1. 按一 **[!UICONTROL Add Platform]**&#x200B;下，然後選擇「網頁」作為平台類型。
1. 請確定已選 **[!UICONTROL Allow Implicit Flow]** 中此選項，並使用您的網路名稱（而非{network-name}）輸入「重新導向URL」: `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`。
1. 產生新密碼／金鑰對以取得私密金鑰。
1. 在中 **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**，將切換 **[!UICONTROL Enable Microsoft Live Login]** 切換為 **[!UICONTROL On]**。
1. 輸入Microsoft Live Client ID和Microsoft Live Client Secret。
1. Click **[!UICONTROL Save Settings]**.

完成後，Microsoft Live Identity的應用程式詳細資訊頁面將會列出應用程式的用戶端ID（消費者金鑰）和用戶端密碼（消費者密碼），以用於Studio的「整合設定」頁面。
