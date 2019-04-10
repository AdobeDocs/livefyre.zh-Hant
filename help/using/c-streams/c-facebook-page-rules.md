---
description: 您可以建立從Facebook頁面提取內容的串流規則。
seo-description: 您可以建立從Facebook頁面提取內容的串流規則。
seo-title: Facebook頁面規則
solution: Experience Manager
title: Facebook頁面規則
uuid: 2be63476-1a92-409d-a22 f-e1 ec66 b6 dcc8
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Facebook頁面規則{#facebook-page-rules}

您可以建立從Facebook頁面提取內容的串流規則。

您可以使用Facebook頁面規則，從Facebook頁面公開發佈內容。內容會以與Social相同的頻率提取至應用程式或資料夾，而這會根據Facebook頁面和貼文流量模式而變更。也支援Facebook頁面內的連結，並將顯示在串流中。

若要建立Facebook頁面規則，將內容從Facebook頁面提取至您的應用程式或資料夾，您可以依下列方式進行篩選：

* **[!UICONTROL Facebook Page]**

   * 輸入 **[!UICONTROL Name]** 頁面。只輸入URL的尾端文字。**For example:** To add content from `https://facebook.com/KellysSuperFunFanPage`, type *KellysSuperFunFanPage* in the **[!UICONTROL Name]** field.

   * 如果 **[!UICONTROL Include Facebook Comments for each post]** 您要將使用者注釋包含在頁面貼文中，請改用「切換」。
   * 如果 **[!UICONTROL Only Show Author Posts]** 您要排除其他使用者的貼文，請改用切換。

如需所有串流規則的其他串流規則選項，請參閱 [所有串流規則的串流規則選項](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。

>[!NOTE]
>
>Livefyre僅限於從Facebook收到的內容，因此無法保證Facebook頁面上的每個貼文都將包含在您的串流中。

>[!NOTE]
>
>如果Facebook SocialSync和Facebook頁面規則已針對Facebook頁面規則啓用，且使用者留言已啓用Facebook頁面規則，則串流規則會覆寫SocialSync。內容會根據僅限Facebook頁面組織規則，而不是使用SocialSync串流至應用程式。

Facebook頁面組織支援的內容類型包括：

* 頁面擁有者或管理員

   * 狀態
   * 像片
   * 視訊為連結

* 標準Facebook使用者

   * 狀態
   * 像片
   * 視訊為連結

* 第三方

   * 狀態

