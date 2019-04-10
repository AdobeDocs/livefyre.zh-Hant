---
description: 這些選項適用於所有社交網路或發佈方法中的任何串流規則。
seo-description: 這些選項適用於所有社交網路或發佈方法中的任何串流規則。
seo-title: 所有串流規則的串流規則選項
solution: Experience Manager
title: 所有串流規則的串流規則選項
uuid: 4072ee83-31e7-4de6-918c-134b8b8032e1
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 所有串流規則的串流規則選項{#stream-rule-options-for-all-stream-rules}

這些選項適用於所有社交網路或發佈方法中的任何串流規則。

文字和關鍵字欄位的搜尋功能：

* 當您輸入關鍵字時，Livefyre會自動使用布林運算子 **或** 個別字詞。例如，若要使用單字蛋糕 ** 或 *配方搜尋貼文*，請輸入 *蛋糕*，然後在欄位中輸入 *配方***[!UICONTROL keyword]** 。

* 您可以用引號括住精確的片語文字，搜尋精確片語。例如，若要搜尋精確片語 *食譜，*請在欄位中輸入 *「蛋糕配方」***[!UICONTROL keyword]** 。

* 您可以將布林和精確字句搜尋結合在一個串流規則中。例如，您可以逐一輸入每一個片語，搜尋 *蛋糕*、 *配方*和 *「蛋糕配方」* 。

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. 選取下列其中一項：

   * **[!UICONTROL All Content.]** 允許任何內容。
   * **[!UICONTROL Media Required.]** 只允許包含影像和視訊的內容。(對於Instagram和Facebook內容，您可以指定 **[!UICONTROL Photos]** 或 **[!UICONTROL Videos]** 僅限)。

* **[!UICONTROL Language]**. 選擇要搜尋的語言。英文是預設語言。
* **[!UICONTROL Smart Tags]**. 選擇要用來識別內容的標籤。Livefyre使用電腦視覺化技術來識別像片和視訊，並使用特定智慧標記來提高搜尋精確度。使用 **[!UICONTROL ANY]** 修飾詞，使用任何標記或 **[!UICONTROL ALL]** 修飾詞將內容篩選成串流，以便將內容篩選成使用所有標記的串流。使用 **[!UICONTROL Image contains none of these smart tags]** 欄位，在包含您不想要的內容的像片中輸入標記。這個選項無法用於文字內容。

* **[!UICONTROL Products]**. 新增產品標記，以便與產品目錄中的產品搭配使用串流規則。
* **[!UICONTROL Premoderate]**. 選取下列其中一項：

   * **[!UICONTROL On]**. 預覽所有傳入的規則內容。您可以從ModQ的「串流」區段檢視預先控管的內容。**[!UICONTROL On]** 會覆寫App Settings中的設定。
   * **[!UICONTROL Off]**. 請勿預先調節傳入的規則內容。**[!UICONTROL Off]** 會覆寫App Settings中的設定。
   * **[!UICONTROL Inherited (Off)]**. 使用網站上的預備設定(位於) **[!UICONTROL Site Settings]**。

* **[!UICONTROL SAFE Rules]**. 選取下列其中一項：
   * **[!UICONTROL Apply SAFE Rules]**. 將所有SAFE規則套用至此串流。
   * **[!UICONTROL Apply SAFE Rules for:]** 選取一或多個可套用此串流規則之SAFE規則的選項。
   * **[!UICONTROL Disable SAFE Rules]**. 請勿將任何SAFE規則套用至此串流。

針對社交網路或內容類型專用的串流規則選項，請參閱下列社交網路或內容類型的說明文件：

* [Facebook頁面](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [電子郵件](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
