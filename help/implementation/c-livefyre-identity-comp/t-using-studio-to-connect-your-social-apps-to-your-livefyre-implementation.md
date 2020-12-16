---
description: 若要啟用社交登入，請使用Studio將您的社交應用程式認證新增至您的Livefyre整合，並自訂登入模式。
seo-description: 若要啟用社交登入，請使用Studio將您的社交應用程式認證新增至您的Livefyre整合，並自訂登入模式。
seo-title: 使用Studio將您的社交應用程式連接至Livefyre實作
title: 使用Studio將您的社交應用程式連接至Livefyre實作
uuid: be14869c-e0df-48cd-a1f3-99eb953dd9ce
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 0%

---


# 使用Studio將您的社交應用程式連接至您的Livefyre實作{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

若要啟用社交登入，請使用Studio將您的社交應用程式認證新增至您的Livefyre整合，並自訂登入模式。

## 自訂登入模式{#section_v4c_hv2_3z}

登入模式可讓您自訂使用者登入應用程式時將看到的資訊。 可定製模式窗口。

* **標誌：** 上傳標誌以用於您的登入模式。
* **字型系列：** 選取符合您品牌的字型。
* **品牌色彩：** 輸入十六進位色彩，以用於模型中的特定文字。
* **條款與條件URL:** 輸入您公司「條款與條件」頁面的URL。此欄位是與Livefyre Identity搭配使用的必要欄位。

## 轉換Livefyre身分{#section_xxt_z52_3z}

您可以在Livefyre Identity中建立和修改文字字串的轉譯集。

有關使用具有Livefyre身份的翻譯集的詳細資訊，請參閱翻譯集。

如需您可針對Livefyre身分自訂之特定字串的詳細資訊，請參閱Livefyre身分識別。

## 啟用電子郵件{#section_dlv_wzt_bbb}登入

允許使用者使用其電子郵件地址登入您網站上的應用程式，並與之互動。

若要使用Livefyre原生帳戶啟用登入：

1. 導覽至Livefyre Studio中的&#x200B;**[!UICONTROL Integration Settings]**。
1. 切換&#x200B;**[!UICONTROL Enable Login with Email]**&#x200B;切換為&#x200B;**[!UICONTROL On]**。

## 啟用使用Facebook帳戶{#section_ph3_515_bbb}登入

將您的Facebook帳戶連線至Livefyre，讓使用者使用其Facebook登入來與您網站上的應用程式互動。

若要啟用使用Facebook帳戶的登入：

1. 切換&#x200B;**[!UICONTROL Enable Login with Facebook]**&#x200B;切換為&#x200B;**[!UICONTROL ON]**。

1. 新增您的Facebook應用程式的&#x200B;**[!UICONTROL App ID]**&#x200B;和&#x200B;**[!UICONTROL App Secret]**。

   這些值會列在您應用程式的Facebook開發人員儀表板中，可從[https://developers.facebook.com/apps/](https://developers.facebook.com/apps/675503539257343/dashboard/)取得。

## 啟用Google {#section_fq3_kb5_bbb}登入

將您的Google+帳戶連線至Livefyre，讓使用者使用其Google+登入來與您網站上的應用程式互動。

若要使用Google+帳戶啟用登入：

1. 切換&#x200B;**[!UICONTROL Enable Login with Google]**&#x200B;切換為&#x200B;**[!UICONTROL ON]**。

1. 新增您的Google應用程式的&#x200B;**[!UICONTROL Client ID]**&#x200B;和&#x200B;**[!UICONTROL Client secret]**。

   這些值會列在您的Google Cloud Platform專案介面中，可從[https://console.cloud.google.com/](https://console.cloud.google.com/apis/library)取得。 要檢索此資訊，請轉至&#x200B;**[!UICONTROL API Manager > Credentials]** ，然後按一下項目名稱。

## 使用Twitter帳戶{#section_iyz_wb5_bbb}啟用登入

將您的Twitter帳戶連線至Livefyre，讓使用者使用其Twitter登入，與您網站上的應用程式互動。

若要使用Twitter帳戶啟用登入：

1. 切換&#x200B;**[!UICONTROL Enable Login with Twitter]**&#x200B;切換為&#x200B;**[!UICONTROL ON]**。

1. 新增您的Twitter應用程式的&#x200B;**[!UICONTROL Consumer Key (API Key)]**&#x200B;和&#x200B;**[!UICONTROL Consumer Secret (API Secret)]**。

   這些值會列在您Twitter應用程式的&#x200B;**[!UICONTROL Keys and Access Tokens]**&#x200B;頁面中，可從[https://apps.twitter.com/](https://apps.twitter.com/)取得。

## 啟用使用Yahoo！登入 帳戶 {#section_s1q_3c5_bbb}

連線您的Yahoo! 帳戶，以允許使用者使用其Yahoo! 登入以與您網站上的應用程式互動。

若要啟用使用Yahoo! account:

1. 切換&#x200B;**[!UICONTROL Enable Login with Yahoo!]**&#x200B;切換為&#x200B;**[!UICONTROL ON]**。

1. 新增您的Yahoo! app的&#x200B;**[!UICONTROL Client ID]**&#x200B;和&#x200B;**[!UICONTROL Client Secret]**。

   這些值會列在Yahoo! 應用程式詳細資訊頁面，可從[developer.yahoo.com/apps](https://developer.yahoo.com/apps)取得。

## 啟用使用Microsoft Live帳戶{#section_z42_4c5_bbb}登入

將您的Microsoft Live ID帳戶連接至Livefyre，讓使用者使用其Microsoft Live ID登入來與您網站上的應用程式互動。

若要使用Microsoft Live ID帳戶啟用登入：

1. 在&#x200B;**[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]**&#x200B;中，將&#x200B;**[!UICONTROL Enable Microsoft Live Login]**&#x200B;切換為&#x200B;**[!UICONTROL On]**。

1. 輸入&#x200B;**[!UICONTROL Microsoft Live Client ID (Private Key)]**&#x200B;和&#x200B;**[!UICONTROL Microsoft Live Client Secret (Password)]**。

1. 按一下 **[!UICONTROL Save Settings]**.

   **[!UICONTROL Microsoft Live Client ID (Private Key)]**&#x200B;和&#x200B;**[!UICONTROL Microsoft Live Client Secret (Password)]**&#x200B;值會列在Microsoft Live ID應用程式詳細資訊頁面中。

## 將您的社交應用程式連線至Livefyre身分識別{#section_on2_vc5_bbb}

讓您的使用者可針對網站上的應用程式使用Livefyre Identity實作。

1. 建立應用程式.
1. 導覽至&#x200B;**[!UICONTROL Studio]** > **[!UICONTROL Settings]** > **[!UICONTROL Integration Settings]** > **[!UICONTROL Livefyre Identity]**。

1. 輸入您所建立之應用程式的必要應用程式認證。