---
description: 若要啓用社交登入，請使用Studio將您的社交應用程式認證新增至Livefyre整合，並自訂登入模型。
seo-description: 若要啓用社交登入，請使用Studio將您的社交應用程式認證新增至Livefyre整合，並自訂登入模型。
seo-title: 使用Studio將您的社交應用程式連接到您的Livefyre實作
title: 使用Studio將您的社交應用程式連接到您的Livefyre實作
uuid: 是14869c-e0 df-48cd-a1 f3-99eb953 dd9 ce
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 使用Studio將您的社交應用程式連接到您的Livefyre實作{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

若要啓用社交登入，請使用Studio將您的社交應用程式認證新增至Livefyre整合，並自訂登入模型。

## 自訂登入模型 {#section_v4c_hv2_3z}

「登入模式」可讓您自訂使用者登入應用程式時所看到的資訊。您可以自訂模型視窗。

* **標誌：** 上傳標誌以用於登入模式中。
* **字型系列：** 選取字體以符合您的品牌。
* **品牌色彩：** 輸入要用於模式中特定文字的十六進位色彩。
* **詞語與條件URL：** 輸入公司的「條款與條件」頁面的URL。必須使用此欄位，才能搭配Livefyre Identity使用。

## 翻譯Livefyre身份 {#section_xxt_z52_3z}

您可以為Livefyre Identity中的文字字串建立和修改翻譯集。

請參閱翻譯集，瞭解如何搭配Livefyre Identity使用翻譯集。

如需Livefyre身分識別的自訂字串，請參閱Livefyre身份識別。

## 啓用使用電子郵件登入 {#section_dlv_wzt_bbb}

允許使用者使用其電子郵件地址登入您的網站上的應用程式並與之互動。

若要使用Livefyre原生帳戶啓用登入：

1. 在Livefyre Studio中導覽至 **[!UICONTROL Integration Settings]** 。
1. 切換 **[!UICONTROL Enable Login with Email]** 切換至 **[!UICONTROL On]**。

## 使用Facebook帳戶啓用登入 {#section_ph3_515_bbb}

將您的Facebook帳戶連接至Livefyre，允許使用者使用其Facebook登入功能與您網站上的應用程式互動。

若要使用Facebook帳戶啓用登入：

1. 切換 **[!UICONTROL Enable Login with Facebook]** 切換至 **[!UICONTROL ON]**。

1. Add your Facebook app’s **[!UICONTROL App ID]** and **[!UICONTROL App Secret]**.

   這些值會列在您的Facebook開發人員控制面板中，可從 [https://developers.facebook.com/apps/](https://developers.facebook.com/apps/675503539257343/dashboard/)取得。

## 啓用使用Google登入 {#section_fq3_kb5_bbb}

將您的Google+帳戶連接至Livefyre，允許使用者使用其Google+登入功能與您網站上的應用程式互動。

若要使用Google+帳戶啓用登入：

1. 切換 **[!UICONTROL Enable Login with Google]** 切換至 **[!UICONTROL ON]**。

1. Add your Google app’s **[!UICONTROL Client ID]** and **[!UICONTROL Client secret]**.

   這些值會列在您的Google Cloud Platform專案介面中，可從 [https://console.cloud.google.com/取得](https://console.cloud.google.com/apis/library)。若要擷取此資訊，請前往 **[!UICONTROL API Manager > Credentials]**，然後按一下專案名稱。

## 使用Twitter帳戶啓用登入 {#section_iyz_wb5_bbb}

將您的Twitter帳戶連接至Livefyre，允許使用者使用其Twitter登入功能與您網站上的應用程式互動。

若要使用Twitter帳戶啓用登入：

1. 切換 **[!UICONTROL Enable Login with Twitter]** 切換至 **[!UICONTROL ON]**。

1. Add your Twitter app’s **[!UICONTROL Consumer Key (API Key)]** and **[!UICONTROL Consumer Secret (API Secret)]**.

   這些值會列在您的Twitter應用程式 **[!UICONTROL Keys and Access Tokens]** 頁面中，可從 [https://apps.twitter.com/取得](https://apps.twitter.com/)。

## 啓用使用Yahoo！帳戶 {#section_s1q_3c5_bbb}

連接您的Yahoo！帳戶，以允許使用者使用其Yahoo！登入以與您網站上的應用程式互動。

若要使用Yahoo！帳戶：

1. 切換 **[!UICONTROL Enable Login with Yahoo!]** 切換至 **[!UICONTROL ON]**。

1. 新增Yahoo！應用程式 **[!UICONTROL Client ID]** 和 **[!UICONTROL Client Secret]**。

   這些值會列在Yahoo！應用程式詳細資訊頁面，可從 [developer.yahoo.com/apps取得](https://developer.yahoo.com/apps)。

## 使用Microsoft Live帳戶啓用登入 {#section_z42_4c5_bbb}

將您的Microsoft Live ID帳戶連接至Livefyre，允許使用者使用其Microsoft Live ID登入功能與您網站上的應用程式互動。

若要使用Microsoft Live ID帳戶啓用登入：

1. In **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]**，switching the **[!UICONTROL Enable Microsoft Live Login]** socialto **[!UICONTROL On]**.

1. 輸入 **[!UICONTROL Microsoft Live Client ID (Private Key)]** 和 **[!UICONTROL Microsoft Live Client Secret (Password)]**。

1. 按一 **[!UICONTROL Save Settings]**下。

   這些 **[!UICONTROL Microsoft Live Client ID (Private Key)]****[!UICONTROL Microsoft Live Client Secret (Password)]** 值會列在Microsoft Live ID應用程式詳細資訊頁面中。

## 將您的社交應用程式連接至Livefyre身份識別 {#section_on2_vc5_bbb}

讓您的使用者可以在您的網站上使用Livefyre身分識別實施。

1. 建立應用程式。
1. 導覽至 **[!UICONTROL Studio]** > **[!UICONTROL Settings]** > **[!UICONTROL Integration Settings]**> **[!UICONTROL Livefyre Identity]**。

1. 輸入您所建立應用程式的必要應用程式憑證。