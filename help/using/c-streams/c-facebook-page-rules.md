---
description: 您可以建立從Facebook頁面提取內容的串流規則。
seo-description: 您可以建立從Facebook頁面提取內容的串流規則。
seo-title: Facebook頁面規則
solution: Experience Manager
title: Facebook頁面規則
uuid: 2be63476-1a92-409d-a22f-e1ec66b6dcc8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Facebook頁面規則{#facebook-page-rules}

您可以建立從Facebook頁面提取內容的串流規則。

您可以使用「Facebook頁面規則」，從「Facebook頁面」串流公開張貼的內容。 內容會以與SocialSync相同的頻率提取到應用程式或資料夾中，SocialSync會根據Facebook頁面和貼文流量模式進行變更。 Facebook頁面內的連結也受支援，並會顯示在串流中。

若要建立「Facebook頁面規則」以從Facebook頁面將內容提取至您的應用程式或資料夾，您可以依下列方式進行篩選：

* **[!UICONTROL Facebook Page]**

   * 輸入頁 **[!UICONTROL Name]** 面的。 僅輸入URL的尾隨文字。 **** 例如：若要從新增 `https://facebook.com/KellysSuperFunFanPage`內容，請 *在欄位中輸入***[!UICONTROL Name]** KellysSuperFunFanPage。

   * 如果 **[!UICONTROL Include Facebook Comments for each post]** 您想要將使用者留言加入「頁面」貼文，請開啟。
   * 如果 **[!UICONTROL Only Show Author Posts]** 您想要排除其他使用者的貼文，請開啟。

如需所有串流規則的其他串流規則選項，請參 [閱所有串流規則的串流規則選項](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。

>[!NOTE]
>
>Livefyre僅限於從Facebook收到的內容，因此無法保證Facebook頁面上的每個貼文都會包含在您的串流中。

>[!NOTE]
>
>如果Facebook SocialSync和Facebook頁面規則都針對特定Facebook頁面啟用，且使用者留言已針對Facebook頁面規則啟用，則「串流規則」將覆寫SocialSync。 內容將僅會根據「Facebook頁面組織規則」串流至應用程式，而不會使用SocialSync。

Facebook頁面組織支援的內容類型包括：

* 頁面擁有者或管理員

   * 狀態
   * 相片
   * 視訊做為連結

* 標準Facebook使用者

   * 狀態
   * 相片
   * 視訊做為連結

* 第三方

   * 狀態

