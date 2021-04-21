---
description: 您可將Livefyre Identity與Microsoft Live Identity搭配使用，讓使用者使用其Facebook登入來與您網站上的應用程式互動。
title: 建立Microsoft Live Identity應用程式以搭配Livefyre Identity使用
exl-id: 7702c956-ecb5-424a-9866-d6f73d4d4bc9
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# 建立Microsoft Live Identity應用程式以搭配Livefyre Identity使用{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

您可將Livefyre Identity與Microsoft Live Identity搭配使用，讓使用者使用其Facebook登入來與您網站上的應用程式互動。

若要允許使用者使用其Microsoft Live Identity認證登入，Livefyre需要下列Microsoft Live Identity資訊：

* 用戶端ID（私密金鑰）
* 用戶端密碼（密碼）

若要建立Microsoft Live Identity應用程式以搭配Livefyre Identity使用：

1. 在[https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)建立或登入Microsoft Live帳戶
1. 建立新應用程式或選取現有應用程式，以便與Livefyre Identity搭配使用。
1. 按一下&#x200B;**[!UICONTROL Add Platform]** ，然後選擇Web作為平台類型。
1. 請確定已勾選&#x200B;**[!UICONTROL Allow Implicit Flow]**&#x200B;選項，並使用您的網路名稱（而非{network-name}）輸入「重新導向URL」:`https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`。
1. 產生新密碼／金鑰對以取得私密金鑰。
1. 在&#x200B;**[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**&#x200B;中，將&#x200B;**[!UICONTROL Enable Microsoft Live Login]**&#x200B;切換為&#x200B;**[!UICONTROL On]**。
1. 輸入Microsoft Live Client ID和Microsoft Live Client Secret。
1. 按一下 **[!UICONTROL Save Settings]**.

完成後，Microsoft Live Identity的應用程式詳細資訊頁面將會列出應用程式的用戶端ID（消費者金鑰）和用戶端密碼（消費者密碼），以用於Studio的「整合設定」頁面。
