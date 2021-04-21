---
description: 您可以建立可從「Facebook頁面」提取內容的串流規則。
title: Facebook頁面規則
exl-id: 1dc728c6-81fa-4c6c-acba-d9a4aea71ed2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# Facebook頁面規則{#facebook-page-rules}

您可以建立可從「Facebook頁面」提取內容的串流規則。

您可以使用「Facebook頁面規則」，從「Facebook頁面」串流公開張貼的內容。 內容會以與SocialSync相同的頻率提取至「應用程式」或「資料夾」中，SocialSync會根據「Facebook頁面」和貼文流量模式進行變更。 也支援「Facebook頁面」內的連結，並會顯示在串流中。

若要建立「Facebook頁面規則」以將Facebook頁面的內容提取到您的應用程式或資料夾中，您可以依下列方式進行篩選：

* **[!UICONTROL Facebook Page]**

   * 為頁面輸入&#x200B;**[!UICONTROL Name]**。 僅輸入URL的尾隨文字。 **例如：若要** 從新增內容， `https://facebook.com/KellysSuperFunFanPage`請在欄位中 ** 輸入KellysSuperFunFanPage **[!UICONTROL Name]** 。

   * 如果您想要將使用者留言加入「頁面」貼文，請切換&#x200B;**[!UICONTROL Include Facebook Comments for each post]**。
   * 如果您想要從其他使用者排除貼文，請將&#x200B;**[!UICONTROL Only Show Author Posts]**&#x200B;切換為開。

如需所有串流規則的其他串流規則選項，請參閱[所有串流規則的串流規則選項](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。

>[!NOTE]
>
>Livefyre僅能接收自Facebook的內容，因此無法保證Facebook頁面上的每個貼文都會包含在您的串流中。

>[!NOTE]
>
>如果FacebookSocialSync和Facebook頁面規則都針對特定Facebook頁面啟用，而使用者注釋則針對Facebook頁面規則啟用，則串流規則會覆寫SocialSync。 內容僅會根據「Facebook頁面組織規則」串流至應用程式，而不會使用SocialSync。

facebook網頁組織支援的內容類型包括：

* 頁面擁有者或管理員

   * 狀態
   * 相片
   * 視訊做為連結

* 標準Facebook用戶

   * 狀態
   * 相片
   * 視訊做為連結

* 第三方

   * 狀態
