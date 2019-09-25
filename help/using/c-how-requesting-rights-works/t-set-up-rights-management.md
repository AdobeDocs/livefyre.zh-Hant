---
description: 定義Instagram和Twitter貼文的請求權限設定。
seo-description: 定義Instagram和Twitter貼文的請求權限設定。
seo-title: 設定Rights Management
solution: Experience Manager
title: 設定Rights Management
uuid: 3ffcbc95-484f-4eba-b817-658c1d658bf8
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# 設定Rights Management{#set-up-rights-management}

定義Instagram和Twitter貼文的請求權限設定。

您必須先為Instagram或Twitter設定一或多個社交帳戶，才能定義「權限請求設定」。 如需如何設定社交帳戶的詳細資訊，請參 [閱新增Social帳戶](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram)。

>[!NOTE]
>
>您只能在網路層級設定權限管理。 您無法設定網站特定的權限管理。

1. 在Livefyre studio中，導覽至 **[!UICONTROL Network]****[!UICONTROL Settings > Rights Management]**。

   >[!NOTE]
   >
   >您需要協調者或管理員網路層級權限，才能設定Rights Management帳戶。

1. 如果 **[!UICONTROL +Add New Account]** 您沒有設定任何Rights Management帳戶，請選取。
1. 按一 **[!UICONTROL Create New Setting]** 下您要用於「Rights Management」的社交網路下方。

   >[!NOTE]
   >
   >若是Instagram帳戶，您必須有Instagram商業帳戶，才能透過部分自動功能要求權限。 如需不同Instagram帳戶類型及其使用方式的詳細資訊，請參閱關於 [Instagram帳戶](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。

1. 填寫顯示的欄位。 所有欄位都是必要欄位。

   * **[!UICONTROL Display name:]** 輸入顯示名稱，以識別要用於您「權限請求」帳戶的Twitter或Instagram帳戶。 此名稱僅為內部。
   * **[!UICONTROL Enabled:]**預設設為on。 啟用帳戶的權限管理。
   * **[!UICONTROL Approval hashtag:]** 內容擁有者將用來指出他們同意使用其內容的主題標籤。
   * **[!UICONTROL Terms and conditions:]** 網路條款與條件的連結，以供內容重複使用。 此欄位區分大小寫。
   * **[!UICONTROL Network and sites:]** 此帳戶可要求內容重複使用權限的網路或網站。 若要讓此帳戶在整個網路上都可使用，請選取清單中的第一個項目，或使用Command/CTRL鍵限制到特定網站。
   * **[!UICONTROL Default message:]** 要與您的「權限請求」一起顯示的訊息。 您可以在請求權限時覆寫此訊息。

      * 當協調者向內容作者發出請求時，Livefyre會向協調者顯示其中一個預設訊息。 協調者可以產生其他預設訊息，或在傳送前編輯訊息。 訊息必須包含作者的Twitter或Instagram控制代碼({handle})、您的核准主題標籤({grantTag})，以及您的「條款」和「條件」連結({termsLink})。

         **[!UICONTROL Note:]** {handle}、{grantTag}和{termsLink}都區分大小寫。

         **[!UICONTROL Note:]** 為防止惡意使用，Twitter會以 [t.co格式包裝任何內含的URL](https://t.co/) 。 為避免預設訊息超過140個字元，Livefyre建議您不要在預設訊息中加入URL。

      * 編寫權限要求訊息的最佳實務：

         * 建立多個預設訊息，讓您聽起來不像機器人。 在建立下一個預設訊息之前，先儲存每個預設訊息。
         * 鼓勵您的協調者在傳送前個人化此附註，以防止網路的要求被標籤為垃圾訊息。

1. 按一 **[!UICONTROL Save Settings]** 下以新增您的Rights Request帳戶。
從資產庫傳送權限要求。 如需 [如何從資產庫傳送權限要求的詳細資訊](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset) ，請參閱傳送權限要求。