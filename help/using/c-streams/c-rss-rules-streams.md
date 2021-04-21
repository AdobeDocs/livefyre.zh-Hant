---
description: 您可以建立從RSS饋送提取內容的串流規則。
title: RSS規則
exl-id: bfb3bbad-ab26-451e-b540-d6c41f54dc31
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# RSS規則{#rss-rules}

您可以建立從RSS饋送提取內容的串流規則。

RSS串流每5分鐘更新一次，從動態消息的前50個項目尋找Livefyre中不存在的內容。 Livefyre會忽略動態消息中前50個項目的所有項目。

若要建立RSS規則以從RSS饋送提取內容至您的應用程式或資料夾，您可以依下列方式進行篩選：

* **[!UICONTROL URL]** RSS饋送。
* **[!UICONTROL Include recent items.]** 如果此值設定為：

   * **[!UICONTROL Enabled]**,Livefyre會將動態消息中的前50個內容項目新增至串流，不論發佈日期為何。
   * **[!UICONTROL Disabled]**,Livefyre會將動態消息中的前50個內容項目新增至串流，其發佈日期與串流規則建立日期或更新版本相同。

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** 從項目連結或XML擷取資訊。

**RSS規則**

Livefyre會根據下列RSS規格剖析RSS饋送：

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [媒體RSS](https://en.wikipedia.org/wiki/Media_RSS)
* [原子饋送](https://validator.w3.org/feed/docs/atom.html)

Livefyre不會閱讀不符合這些規格的動態消息，而且其內容不會提取到您的串流中。 使用WC3饋送驗證服務來檢查RSS饋送的語法，並確定其有效。

如需所有串流規則的其他串流規則選項，請參閱[所有串流規則的串流規則選項](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
