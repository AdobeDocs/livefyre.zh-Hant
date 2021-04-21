---
description: 您可將Livefyre Identity與LinkedIn搭配使用，讓使用者使用其LinkedIn登入，在您的網站上與應用程式互動。
title: 建立LinkedIn應用程式以搭配Livefyre Identity使用
exl-id: e77eca6a-1698-414e-994e-1189f780ada1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# 建立LinkedIn應用程式以搭配Livefyre Identity使用{#create-a-linkedin-app-for-use-with-livefyre-identity}

您可將Livefyre Identity與LinkedIn搭配使用，讓使用者使用其LinkedIn登入，在您的網站上與應用程式互動。

若要啟用LinkedIn登入，Livefyre需要下列LinkedIn應用程式資訊：

* 消費者金鑰（API金鑰）
* 消費者密碼（API密碼）

若要建立與Livefyre Identity搭配使用的LinkedIn應用程式：

1. 前往https://www.linkedin.com/secure/developer，並登入您的LinkedIn帳戶以建立新的應用程式，或選取現有應用程式以搭配Livefyre Identity使用。
1. 按一下 **[!UICONTROL Create Application]**.
1. 填寫表單以建立應用程式。
1. 在&#x200B;**[!UICONTROL Default Application Permissions]**&#x200B;中，啟用&#x200B;**[!UICONTROL r_basicprofile]**&#x200B;和&#x200B;**[!UICONTROL r_emailaddress]**&#x200B;應用程式權限。
1. 將&#x200B;**[!UICONTROL OAuth 2.0 Authorized Redirect URL]**&#x200B;輸入為`https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`。
1. 儲存應用程式。
1. 在&#x200B;**[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**&#x200B;中，將&#x200B;**[!UICONTROL Enable LinkedIn Login]**&#x200B;切換為&#x200B;**[!UICONTROL On]**。
1. 輸入「LinkedIn客戶ID」和「LinkedIn客戶機密碼」。
1. 按一下 **[!UICONTROL Save Settings]**.

完成後，LinkedIn的應用程式詳細資訊頁面將會列出應用程式的API金鑰（消費者金鑰）和API密碼（消費者密碼），以便用於Studio的「整合設定」頁面。
