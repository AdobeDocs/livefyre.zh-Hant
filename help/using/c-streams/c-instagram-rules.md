---
description: 您可以建立從Instagram提取內容的串流規則。
title: Instagram規則
exl-id: ac00a12c-94b1-4464-ad3f-991382759d71
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Instagram規則{#instagram-rules}

您可以建立從Instagram提取內容的串流規則。

>[!NOTE]
>
>在建立Instagram流之前，您至少必須向&#x200B;**[!UICONTROL Network Settings]**&#x200B;中的&#x200B;**[!UICONTROL Social Accounts]**&#x200B;部分添加一個Instagram業務帳戶。 有關如何配置Instagram帳戶的詳細資訊，請參閱[關於Instagram帳戶](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。

根據@mentions或主題標籤建立Instagram規則。

>[!NOTE]
>
>所有Instagram規則都至少需要一個主題標籤。 新增規則的關鍵字和使用者名稱將會傳回包含兩個項目的內容。

若要建立Instagram規則以從Instagram動態消息提取內容至您的應用程式或資料夾，請依下列方式篩選：

* **[!UICONTROL Words]**

   * 輸入&#x200B;**[!UICONTROL hashtags]**&#x200B;以包含在您的Instagram流中或從中排除。 為&#x200B;**[!UICONTROL Contains]**&#x200B;和&#x200B;**[!UICONTROL Does not contain]**&#x200B;欄位指定值時，會傳回包含第一個欄位的影像，但不包含第二個欄位。

   * 例如，輸入&#x200B;**[!UICONTROL Contains]**&#x200B;關鍵字Giants、Posey和&#x200B;**[!UICONTROL Does not contain]**&#x200B;關鍵字Dodger，將會傳回所有包含單字Giants或Posey的貼文，而不包含單字Dodger。

      >[!NOTE]
      >
      >Instagram規則會傳回貼文，其中包含作者留言中所列的主題標籤，這些主題標籤可能不會出現在串流中。

* **[!UICONTROL Mentions]**

   * 輸入&#x200B;**[!UICONTROL @mentions]**&#x200B;以拉入串流，或從串流中排除。

* **[!UICONTROL Authors]**

   >[!NOTE]
   >
   >您必須在Livefyre中設定Instagram商業帳戶，才能在Instagram串流規則中使用「作者」搜尋。 有關在Livefyre中設定Instagram企業帳戶的詳細資訊，請參閱[關於Instagram帳戶](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。

   * 輸入&#x200B;**[!UICONTROL @usernames]**&#x200B;以拉入流。 與&#x200B;**@username**&#x200B;關聯的帳戶必須是Instagram商業帳戶。

   * 輸入&#x200B;**@usernames**&#x200B;以排除在串流中。

* **[!UICONTROL Additional Filters]**

   * 選擇要在流中包含&#x200B;**[!UICONTROL All Content]**、**[!UICONTROL Videos Only]**&#x200B;或&#x200B;**[!UICONTROL Photos Only]**。

如需所有串流規則的其他串流規則選項，請參閱[所有串流規則的串流規則選項](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
