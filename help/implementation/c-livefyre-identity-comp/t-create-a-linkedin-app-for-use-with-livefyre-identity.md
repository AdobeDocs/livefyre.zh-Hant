---
description: 您可將Livefyre Identity與LinkedIn搭配使用，讓使用者使用其LinkedIn登入，在您的網站上互動應用程式。
seo-description: 您可將Livefyre Identity與LinkedIn搭配使用，讓使用者使用其LinkedIn登入，在您的網站上互動應用程式。
seo-title: 建立Livefyre身分識別的LinkedIn應用程式
solution: Experience Manager
title: 建立Livefyre身分識別的LinkedIn應用程式
uuid: c5112f24-a4e0-4526-afe8-b8f27a3b2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 建立Livefyre身分識別的LinkedIn應用程式{#create-a-linkedin-app-for-use-with-livefyre-identity}

您可將Livefyre Identity與LinkedIn搭配使用，讓使用者使用其LinkedIn登入，在您的網站上互動應用程式。

若要啟用LinkedIn登入，Livefyre需要下列LinkedIn應用程式資訊：

* 消費者金鑰（API金鑰）
* 消費者密碼（API密碼）

若要建立Livefyre身分識別的LinkedIn應用程式：

1. 前往https://www.linkedin.com/secure/developer，並登入您的LinkedIn帳戶以建立新的應用程式，或選取現有應用程式以搭配Livefyre Identity使用。
1. Click **[!UICONTROL Create Application]**.
1. 填寫表單以建立應用程式。
1. 在中， **[!UICONTROL Default Application Permissions]**&#x200B;啟用和 **[!UICONTROL r_basicprofile]** 應用 **[!UICONTROL r_emailaddress]** 程式權限。
1. 輸入 **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** 為 `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`。
1. 儲存應用程式。
1. 在中 **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**，將切換 **[!UICONTROL Enable LinkedIn Login]** 切換為 **[!UICONTROL On]**。
1. 輸入LinkedIn用戶端ID和LinkedIn用戶端密碼。
1. Click **[!UICONTROL Save Settings]**.

完成後，LinkedIn的應用程式詳細資訊頁面將會列出應用程式的API金鑰（消費者金鑰）和API密碼（消費者密碼），以便用於Studio的「整合設定」頁面。
