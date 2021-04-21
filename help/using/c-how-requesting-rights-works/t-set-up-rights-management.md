---
description: 定義請求Instagram和Twitter貼文權限的設定。
title: 設定Rights Management
exl-id: d3d3e837-0ed0-47a8-ac5c-7b9da431d149
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# 設定Rights Management{#set-up-rights-management}

定義請求Instagram和Twitter貼文權限的設定。

您必須先為Instagram或Twitter設定一或多個社交帳戶，才能定義「權限請求設定」。 如需如何設定社交帳戶的詳細資訊，請參閱[新增社交帳戶](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram)。

>[!NOTE]
>
>您只能在網路層級設定權限管理。 您無法設定網站特定的權限管理。

1. 在Livefyre Studio中，導覽至&#x200B;**[!UICONTROL Network]** **[!UICONTROL Settings > Rights Management]**。

   >[!NOTE]
   >
   >您需要協調者或管理員網路層級權限才能設定Rights Management帳戶。

1. 如果您未設定任何Rights Management帳戶，請選擇&#x200B;**[!UICONTROL +Add New Account]**。
1. 按一下您要用於Rights Management的社交網路下方的&#x200B;**[!UICONTROL Create New Setting]**。

   >[!NOTE]
   >
   >對於Instagram帳戶，您必須擁有Instagram商業帳戶，才能申請部分自動化的權限。 有關Instagram帳戶的不同種類及如何使用它們的詳細資訊，請參閱[關於Instagram帳戶](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。

1. 填寫顯示的欄位。 所有欄位都是必要欄位。

   * **[!UICONTROL Display name:]** 輸入顯示名稱，以識別要用於您的「權利請求」帳戶的Twitter或Instagram帳戶。此名稱僅為內部。
   * **[!UICONTROL Enabled:]**預設為on。 啟用帳戶的權限管理。
   * **[!UICONTROL Approval hashtag:]** 內容擁有者將用來指出他們同意使用其內容的主題標籤。
   * **[!UICONTROL Terms and conditions:]** 網路條款與條件的連結，以供內容重複使用。此欄位區分大小寫。
   * **[!UICONTROL Network and sites:]** 此帳戶可要求內容重複使用權限的網路或網站。若要讓此帳戶在整個網路上都可使用，請選取清單中的第一個項目，或使用Command/CTRL鍵限制到特定網站。
   * **[!UICONTROL Default message:]** 要與您的「權限請求」一起顯示的訊息。您可以在請求權限時覆寫此訊息。

      * 當協調者向內容作者發出請求時，Livefyre會向協調者顯示其中一個預設訊息。 協調者可以產生其他預設訊息，或在傳送前編輯訊息。 訊息必須包含作者的Twitter或Instagram句柄({handle})、您的核准主題標籤({grantTag})，以及您的「條款與條件」連結({termsLink})。

         **[!UICONTROL Note:]** {handle}、{grantTag}和{termsLink}都區分大小寫。

         **[!UICONTROL Note:]** 為防止惡意使用，Twitter會以 [t.](https://t.co/) coformatting包裝任何內含的URL。為避免預設訊息超過140個字元，Livefyre建議您不要在預設訊息中加入URL。

      * 編寫權限要求訊息的最佳實務：

         * 建立多個預設訊息，讓您聽起來不像機器人。 在建立下一個預設訊息之前，先儲存每個預設訊息。
         * 鼓勵您的協調者在傳送前個人化此附註，以防止網路的要求被標籤為垃圾訊息。

1. 按一下&#x200B;**[!UICONTROL Save Settings]**以新增您的Rights Request帳戶。
從資產庫傳送權限要求。 如需如何從資產庫傳送權限要求的詳細資訊，請參閱[傳送權限要求](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset)。
