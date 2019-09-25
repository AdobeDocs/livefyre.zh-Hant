---
description: 您可以建立可從Tumblr提取內容的串流規則。
seo-description: 您可以建立可從Tumblr提取內容的串流規則。
seo-title: Tumblr規則
solution: Experience Manager
title: Tumblr規則
uuid: fe9601ab-aa5e-48c6-a5bf-5543c179cb90
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Tumblr規則{#tumblr-rules}

您可以建立可從Tumblr提取內容的串流規則。

根據Tumblr部落格建立Tumblr規則，並依標籤篩選。 Tumblr串流每5分鐘更新一次，從動態消息的前20個項目尋找Livefyre中不存在的內容。 Livefyre會忽略動態消息中前20個項目的所有項目。

若要建立Tumblr規則以從Tumblr將內容拉入您的應用程式或資料夾，您可以依下列方式進行篩選：

* **[!UICONTROL Blog]**

   * 輸入 **[!UICONTROL Blog Name]** Tumblr部落格的。 輸入URL(*staff.tumblr.com*)或部落格(*staff*)的名稱。

   * 最多可包含一 **[!UICONTROL Tag]** 個，以依包含指定標籤的貼文篩選結果。

* **[!UICONTROL Include recent items.]** 如果此值設定為：

   * **[!UICONTROL Enabled]**,Livefyre會將動態消息中的前20個內容項目新增至串流，不論發佈日期為何。
   * **[!UICONTROL Disabled]**,Livefyre會將動態消息中的前20個內容項目新增至串流，其發佈日期與串流規則建立日期或更新版本相同。

如需所有串流規則的其他串流規則選項，請參 [閱所有串流規則的串流規則選項](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
