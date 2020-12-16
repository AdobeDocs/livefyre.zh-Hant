---
description: 您可以搭配Yahoo! 允許使用者使用其Yahoo! 登入以與您網站上的應用程式互動。
seo-description: 您可以搭配Yahoo! 允許使用者使用其Yahoo! 登入以與您網站上的應用程式互動。
seo-title: 建立Yahoo! 與Livefyre Identity搭配使用的應用程式
solution: Experience Manager
title: 建立Yahoo! 與Livefyre Identity搭配使用的應用程式
uuid: 6863cd2e-eb0d-465b-b706-88ecaccf41bc
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# 建立Yahoo! 與Livefyre Identity搭配使用的應用程式{#create-a-yahoo-app-for-use-with-livefyre-identity}

您可以搭配Yahoo! 允許使用者使用其Yahoo! 登入以與您網站上的應用程式互動。

若要允許您的使用者使用其Yahoo認證登入，Livefyre需要下列Yahoo應用程式資訊：

* 用戶端ID（使用者金鑰）
* 用戶端密碼（消費者密碼）

若要建立Yahoo! 與Livefyre Identity搭配使用的應用程式：

1. 前往[https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/)，並登入您的Yahoo! 帳戶建立新應用程式，或選取現有應用程式以搭配Livefyre Identity使用。
1. 選擇 **[!UICONTROL Application Type: Web Application]**.
1. Enter **[!UICONTROL Callback Domain:]** `https://identity.livefyre.com`
1. 選擇&#x200B;**[!UICONTROL API Permissions: Profiles (Social Directory)]**&#x200B;和&#x200B;**[!UICONTROL Read Public]**。

   完成後，Yahoo的應用程式詳細資訊頁面會列出應用程式的用戶端ID（消費者金鑰）和用戶端密碼（消費者密碼），以便用於Studio的「整合設定」頁面。

   >[!NOTE]
   >
   >如果您啟用Yahoo! 不建立Yahoo! 應用程式，而如果您將Studio中的「用戶端ID」和「用戶端密碼」欄位留空，Livefyre將會使用OpenID將這些使用者登入您的Livefyre應用程式。 在這種情況下，將無法使用OAuth和自訂品牌。