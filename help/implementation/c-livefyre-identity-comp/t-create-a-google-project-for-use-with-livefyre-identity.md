---
description: 您可以使用Livefyre Identity與Google，讓使用者使用Google登入功能與網站上的應用程式互動。
seo-description: 您可以使用Livefyre Identity與Google，讓使用者使用Google登入功能與網站上的應用程式互動。
seo-title: 建立Google Project以搭配Livefyre身分識別
solution: Experience Manager
title: 建立Google Project以搭配Livefyre身分識別
uuid: b0a6bb8a-abea-4f5 c-92ed-026e60183 e1 d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 建立Google Project以搭配Livefyre身分識別{#create-a-google-project-for-use-with-livefyre-identity}

您可以使用Livefyre Identity與Google，讓使用者使用Google登入功能與網站上的應用程式互動。

若要讓使用者使用其Google認證登入，Livefyre需要下列Google專案資訊：

* 用戶端ID
* 用戶端密碼

若要建立Google Project以搭配Livefyre身分識別使用：

1. 前往 [https://console.cloud.google.com/project](https://console.cloud.google.com/project) 並登入您的Google帳戶以建立新的應用程式，或選取現有應用程式以搭配Livefyre Identity使用。
1. 從應用程式的專案儀表板中，按一下 **[!UICONTROL Enable and Manage APIs]**。
1. 在「API概述」頁面的Social API下，按一下以啓用Google+ API。
1. 從「API認證」頁面中，選取 **[!UICONTROL Credentials > New credentials > OAuth]** 用戶端ID。在開啓的 **[!UICONTROL Create client ID]** 頁面中：

   * 選取應用程式類型：Web應用程式。
   * 輸入 **[!UICONTROL Name]****[!UICONTROL Client ID]**a.
   * 保留 **[!UICONTROL Authorized JavaScript origins]** 欄位空白。
   * 輸入 **[!UICONTROL Authorized redirect URIs]**： `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/google_fyre` (您的Livefyre提供的網路名稱) **[!UICONTROL {networkName}]** 。例如：** [!UICONTROL labs]** **[!UICONTROL `labs.fyre.co`]**in
   * 按一下 **[!UICONTROL Create]** 以儲存您的憑證。

完成後，Google的API管理員>認證頁面將列出專案的用戶端ID和用戶端密碼，以便用於Studio的「整合設定」頁面。
