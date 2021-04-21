---
description: 您可以建立可從Tumblr提取內容的串流規則。
title: Tumblr規則
exl-id: 5d49b266-6d1f-4ec2-8891-5e98fcab14a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Tumblr規則{#tumblr-rules}

您可以建立可從Tumblr提取內容的串流規則。

根據Tumblr部落格建立Tumblr規則，並依標籤篩選。 Tumblr串流每5分鐘更新一次，從動態消息的前20個項目尋找Livefyre中不存在的內容。 Livefyre會忽略動態消息中前20個項目的所有項目。

若要建立Tumblr規則以從Tumblr將內容拉入您的應用程式或資料夾，您可以依下列方式進行篩選：

* **[!UICONTROL Blog]**

   * 輸入Tumblr部落格的&#x200B;**[!UICONTROL Blog Name]**。 輸入URL(*staff.tumblr.com*)或部落格名稱(*staff*)。

   * 包含最多一個&#x200B;**[!UICONTROL Tag]**，可依包含指定標籤的貼文篩選結果。

* **[!UICONTROL Include recent items.]** 如果此值設定為：

   * **[!UICONTROL Enabled]**,Livefyre會將動態消息中的前20個內容項目新增至串流，不論發佈日期為何。
   * **[!UICONTROL Disabled]**,Livefyre會將動態消息中的前20個內容項目新增至串流，其發佈日期與串流規則建立日期或更新版本相同。

如需所有串流規則的其他串流規則選項，請參閱[所有串流規則的串流規則選項](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
