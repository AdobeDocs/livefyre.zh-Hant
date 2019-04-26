---
description: 您可以搭配LinkedIn使用Livefyre Identity，讓使用者使用其LinkedIn登入功能在您的網站上互動應用程式。
seo-description: 您可以搭配LinkedIn使用Livefyre Identity，讓使用者使用其LinkedIn登入功能在您的網站上互動應用程式。
seo-title: 建立LinkedIn應用程式以搭配Livefyre身分識別使用
solution: Experience Manager
title: 建立LinkedIn應用程式以搭配Livefyre身分識別使用
uuid: c5112f24-a4 e0-4526-afe8-b8 f27 a3 b2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 建立LinkedIn應用程式以搭配Livefyre身分識別使用{#create-a-linkedin-app-for-use-with-livefyre-identity}

您可以搭配LinkedIn使用Livefyre Identity，讓使用者使用其LinkedIn登入功能在您的網站上互動應用程式。

若要啓用LinkedIn登入，Livefyre需要下列LinkedIn應用程式資訊：

* 消費者金鑰(API金鑰)
* 消費者機密(API密碼)

若要建立LinkedIn應用程式以搭配Livefyre身分識別使用：

1. 前往https://www.linkedin.com/secure/developer，然後登入您的LinkedIn帳戶建立新的應用程式，或選取現有應用程式以搭配Livefyre Identity使用。
1. 按一 **[!UICONTROL Create Application]**下。
1. 填寫表格以建立應用程式。
1. 在此中 **[!UICONTROL Default Application Permissions]**啓用 **[!UICONTROL r_basicprofile]** 和 **[!UICONTROL r_emailaddress]** 應用程式權限。
1. 輸入 **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** as `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`.
1. 儲存應用程式。
1. In **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**，switching the **[!UICONTROL Enable LinkedIn Login]** socialto **[!UICONTROL On]**.
1. 輸入LinkedIn用戶端ID和LinkedIn用戶端密碼。
1. 按一 **[!UICONTROL Save Settings]**下。

完成後，LinkedIn的應用程式詳細資訊頁面將列出應用程式的API金鑰(消費者金鑰)和API密碼(消費者機密)，以便用於Studio的「整合設定」頁面。
