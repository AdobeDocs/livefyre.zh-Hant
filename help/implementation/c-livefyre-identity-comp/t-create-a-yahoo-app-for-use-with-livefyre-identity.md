---
description: 您可以使用Livefyre Identity與Yahoo！讓使用者使用其Yahoo！登入以與您網站上的應用程式互動。
seo-description: 您可以使用Livefyre Identity與Yahoo！讓使用者使用其Yahoo！登入以與您網站上的應用程式互動。
seo-title: 建立Yahoo！應用程式搭配Livefyre身分識別
solution: Experience Manager
title: 建立Yahoo！應用程式搭配Livefyre身分識別
uuid: 6863cd2e-eb0 d-465b-b706-88eaccf41 bc
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 建立Yahoo！應用程式搭配Livefyre身分識別{#create-a-yahoo-app-for-use-with-livefyre-identity}

您可以使用Livefyre Identity與Yahoo！讓使用者使用其Yahoo！登入以與您網站上的應用程式互動。

為了讓您的使用者使用其Yahoo認證登入，Livefyre需要下列Yahoo App資訊：

* 用戶端ID(消費者金鑰)
* 用戶端密碼(消費者機密)

若要建立Yahoo！應用程式，以搭配Livefyre身分識別使用：

1. 前往 [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/)，然後登入您的Yahoo！account to create a new or selected a existing app for use with Livefyre Identity.
1. 選取 **[!UICONTROL Application Type: Web Application]**。
1. Enter **[!UICONTROL Callback Domain:]**`https://identity.livefyre.com`
1. 選擇 **[!UICONTROL API Permissions: Profiles (Social Directory)]** 和 **[!UICONTROL Read Public]**。

   完成後，Yahoo的應用程式詳細資訊頁面將列出應用程式的用戶端ID(消費者金鑰)和用戶端密碼(消費者密碼)，以便用於Studio的「整合設定」頁面。

   >[!NOTE]
   >
   >如果您啓用Yahoo！登入而不建立Yahoo！應用程式，如果您將Studio中的用戶端ID和Client Secret欄位保留為空白，Livefyre將會使用OpenID將這些使用者記錄到您的Livefyre應用程式中。在此情況下，無法使用OAuth和自訂品牌。