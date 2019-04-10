---
description: 定義請求Instagram和Twitter貼文權限的設定。
seo-description: 定義請求Instagram和Twitter貼文權限的設定。
seo-title: 設定Rights Management
solution: Experience Manager
title: 設定Rights Management
uuid: 3ffcbc95-484f-4eba-b817-658c1 d658 fb8
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 設定Rights Management{#set-up-rights-management}

定義請求Instagram和Twitter貼文權限的設定。

在定義Rights Request Settings之前，您必須為Instagram或Twitter設定一或多個社交帳戶。如需如何設定社交帳戶的詳細資訊，請參閱 [新增社交帳戶](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram)。

>[!NOTE]
>
>您只能在「網路」層級設定權限管理。您無法設定網站特定的權限管理。

1. 在Livefyre Studio中，瀏覽至 **[!UICONTROL Network]****[!UICONTROL Settings > Rights Management]**。

   >[!NOTE]
   >
   >您需要協調者或管理員網路層級權限才能設定Rights Management帳戶。

1. 如果 **[!UICONTROL +Add New Account]** 您未設定任何Rights Management帳戶，請選取此選項。
1. 按一下 **[!UICONTROL Create New Setting]** 您要用於Rights Management的社交網路。

   >[!NOTE]
   >
   >對於Instagram帳戶，您必須擁有Instagram商業帳戶才能使用部分自動化。如需各種Instagram帳戶以及如何使用的詳細資訊，請參閱 [關於Instagram帳戶](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。

1. 填寫顯示的欄位。所有欄位都是必要欄位。

   * **[!UICONTROL Display name:]** 輸入顯示名稱，以識別用於您的Rights Request帳戶的Twitter或Instagram帳戶。此名稱僅為內部。
   * ****[!UICONTROL Enabled:]預設為開啓。啓用帳戶的權限管理。
   * **[!UICONTROL Approval hashtag:]** 內容擁有者用來表示他們同意使用其內容的主題標籤。
   * **[!UICONTROL Terms and conditions:]** 您網路「條款與條件」的連結，用於重復使用內容。此欄位區分大小寫。
   * **[!UICONTROL Network and sites:]** 此帳戶可要求內容重復使用權的網路或網站。若要在整個網路上提供此帳戶，請選取清單中的第一個項目，或使用Command/CTRL金鑰限制特定網站的限制。
   * **[!UICONTROL Default message:]** 與您的權利請求一起顯示的訊息。您可以在請求權限時覆寫此訊息。

      * 當協調者向內容作者發出請求時，Livefyre會向協調者展示其中一個預設訊息。協調者可產生另一個預設訊息，或在傳送前編輯訊息。訊息必須包含作者的Twitter或Instagram控制代碼({handle})、您的核准主題標籤({GrantTag})，以及您的「條款與條件」({termLink})的連結。

         **[!UICONTROL Note:]** {handle}、{GrantTag}和{termsLink}全都區分大小寫。

         **[!UICONTROL Note:]** 為防止惡意使用，Twitter會將任何包含 [t. co](https://t.co/) 格式的URL包裝在一起。為防止預設訊息超過140個字元，Livefyre建議您不要在預設訊息中加入URL。

      * 撰寫權限要求訊息的最佳做法：

         * 建立多個預設訊息，讓您聽起來不像機器人。在建立下一個預設訊息之前，先儲存每個預設訊息。
         * 鼓勵協調者在傳送前先個人化此附註，以防止您網路的要求遭到偽造。

1. 按一下 **[!UICONTROL Save Settings]** 以新增您的Rights Request帳戶。
從資產庫傳送權限請求。如需如何從資產庫傳送權限請求的詳細資訊，請參閱 [傳送權限請求](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset) 。