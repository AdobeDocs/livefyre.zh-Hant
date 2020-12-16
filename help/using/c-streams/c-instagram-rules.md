---
description: 您可以建立從Instagram提取內容的串流規則。
seo-description: 您可以建立從Instagram提取內容的串流規則。
seo-title: Instagram規則
title: Instagram規則
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---


# Instagram規則{#instagram-rules}

您可以建立從Instagram提取內容的串流規則。

>[!NOTE]
>
>在建立Instagram串流之前，您至少必須在&#x200B;**[!UICONTROL Network Settings]**&#x200B;的&#x200B;**[!UICONTROL Social Accounts]**&#x200B;區段中新增一個Instagram商業帳戶。 如需如何設定Instagram帳戶的詳細資訊，請參閱[關於Instagram帳戶](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。

根據@mentions或主題標籤建立Instagram規則。

>[!NOTE]
>
>所有Instagram規則都至少需要一個主題標籤。 新增規則的關鍵字和使用者名稱將會傳回包含兩個項目的內容。

若要建立Instagram規則，將Instagram動態消息的內容提取到您的應用程式或資料夾，請依下列方式篩選：

* **[!UICONTROL Words]**

   * 輸入&#x200B;**[!UICONTROL hashtags]**&#x200B;以加入或排除在Instagram串流中。 為&#x200B;**[!UICONTROL Contains]**&#x200B;和&#x200B;**[!UICONTROL Does not contain]**&#x200B;欄位指定值時，會傳回包含第一個欄位的影像，但不包含第二個欄位。

   * 例如，輸入&#x200B;**[!UICONTROL Contains]**&#x200B;關鍵字Giants、Posey和&#x200B;**[!UICONTROL Does not contain]**&#x200B;關鍵字Dodger，將會傳回所有包含單字Giants或Posey的貼文，而不包含單字Dodger。

      >[!NOTE]
      >
      >Instagram規則會傳回貼文，其中包含作者留言中所列的主題標籤，但該標籤可能不會出現在串流中。

* **[!UICONTROL Mentions]**

   * 輸入&#x200B;**[!UICONTROL @mentions]**&#x200B;以拉入串流，或從串流中排除。

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >您必須在Livefyre中設定Instagram商業帳戶，才能在Instagram串流規則中使用「作者」搜尋。 如需在Livefyre中設定Instagram商業帳戶的詳細資訊，請參閱[關於Instagram帳戶](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。

   * 輸入&#x200B;**[!UICONTROL @usernames]**&#x200B;以拉入流。 與&#x200B;**@username**&#x200B;關聯的帳戶必須是Instagram商業帳戶。

   * 輸入&#x200B;**@usernames**&#x200B;以排除在串流中。

* **[!UICONTROL Additional Filters]**

   * 選擇要在流中包含&#x200B;**[!UICONTROL All Content]**、**[!UICONTROL Videos Only]**&#x200B;或&#x200B;**[!UICONTROL Photos Only]**。

如需所有串流規則的其他串流規則選項，請參閱[所有串流規則的串流規則選項](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
