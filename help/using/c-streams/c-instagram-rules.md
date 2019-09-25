---
description: 您可以建立從Instagram提取內容的串流規則。
seo-description: 您可以建立從Instagram提取內容的串流規則。
seo-title: Instagram規則
title: Instagram規則
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Instagram規則{#instagram-rules}

您可以建立從Instagram提取內容的串流規則。

>[!NOTE]
>
>在建立Instagram串流之前，您必須至少將一個Instagram商業帳戶新增至中的 **[!UICONTROL Social Accounts]** 區段 **[!UICONTROL Network Settings]**。 如需如何設定Instagram帳戶的詳細資訊，請參閱關於 [Instagram帳戶](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。

根據@mentions或主題標籤建立Instagram規則。

>[!NOTE]
>
>所有Instagram規則都至少需要一個主題標籤。 新增規則的關鍵字和使用者名稱將會傳回包含兩個項目的內容。

若要建立Instagram規則，將Instagram動態消息的內容提取到您的應用程式或資料夾，請依下列方式篩選：

* **[!UICONTROL Words]**

   * 輸入 **[!UICONTROL hashtags]** 要包含在Instagram串流中或排除在Instagram串流中。 指定和欄位的 **[!UICONTROL Contains]** 值 **[!UICONTROL Does not contain]** 將會傳回包含第一個影像，而不包含第二個影像。

   * 例如，輸入關 **[!UICONTROL Contains]** 鍵字Giants、Posey和 **[!UICONTROL Does not contain]** keyword Dodger，會傳回包含單字Giants或Posey的所有貼文，而不包含單字Dodger。

      >[!NOTE]
      >
      >Instagram規則會傳回貼文，其中包含作者留言中所列的主題標籤，但該標籤可能不會出現在串流中。

* **[!UICONTROL Mentions]**

   * 輸入 **[!UICONTROL @mentions]** 以拉入流，或從流中排除。

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >您必須在Livefyre中設定Instagram商業帳戶，才能在Instagram串流規則中使用「作者」搜尋。 如需在Livefyre中設定Instagram商業帳戶的詳細資訊，請參閱關於 [Instagram帳戶](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。

   * 輸入 **[!UICONTROL @usernames]** 以拉入流。 與@username關聯的帳 **戶必須是** Instagram商業帳戶。

   * 輸入要 **從流中排除的** @usernames。

* **[!UICONTROL Additional Filters]**

   * 選擇您要在串流中 **[!UICONTROL All Content]**&#x200B;包 **[!UICONTROL Videos Only]**&#x200B;含、 **[!UICONTROL Photos Only]** 或。

如需所有串流規則的其他串流規則選項，請參 [閱所有串流規則的串流規則選項](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
