---
description: 您可以建立串流規則，從YouTube規則提取內容。
title: YouTube規則
exl-id: 720a6fc6-d5de-4c78-a14e-51bced6e8dda
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---

# YouTube規則{#youtube-rules}

您可以建立串流規則，從YouTube規則提取內容。

根據使用者、頻道或播放清單建立YouTube規則。

若要建立「YouTube規則」以將內容從YouTube拉入您的應用程式或資料夾，您可以依下列方式進行篩選：

* **[!UICONTROL User]**
   * 輸入&#x200B;**[!UICONTROL User]**&#x200B;的虛名字串，將「使用者」的影片包含在串流中。
   * 例如，如果您要輸入的使用者動態消息的URL是`https://www.youtube.com/user/livefyresupport`，只需輸入`livefyresupport`。

* **[!UICONTROL Channel]**
   * 輸入&#x200B;**[!UICONTROL Channel]**&#x200B;的虛名字串，以在串流中包含來自頻道的影片。
   * 例如，如果您要輸入的渠道饋送的URL是`https://www.youtube.com/channel/UCeNZlh03MyUkjRlLFpVQxsg`，只需輸入`UCeNZlh03MyUkjRlLFpVQxsg`。

* **[!UICONTROL Playlist]**
   * 輸入&#x200B;**[!UICONTROL Playlist]**&#x200B;的虛名字串，以在串流中包含來自播放清單的視訊。
   * 例如，如果您要輸入的播放清單饋送的URL是`https://www.youtube.com/playlist?list=PLFE5670C92BDAC201`，只需輸入`PLFE5670C92BDAC201`

* **[!UICONTROL Include recent items.]** 如果此值設定為：
   * **[!UICONTROL Enabled]**,Livefyre會將動態消息中的前15個內容項目新增至串流，不論發佈日期為何。
   * **[!UICONTROL Disabled]**,Livefyre會將動態消息中的前15個內容項目新增至串流，其發佈日期與串流規則建立日期或更新版本相同。

如需所有串流規則的其他串流規則選項，請參閱[所有串流規則的串流規則選項](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
