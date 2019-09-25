---
description: 這些選項適用於所有社交網路或張貼方法的任何串流規則。
seo-description: 這些選項適用於所有社交網路或張貼方法的任何串流規則。
seo-title: 所有串流規則的串流規則選項
solution: Experience Manager
title: 所有串流規則的串流規則選項
uuid: 4072ee83-31e7-4de6-918c-134b8b8032e1
translation-type: tm+mt
source-git-commit: 8bdb537b38d78dba033d6671b710c2a61934d6b2

---


# 所有串流規則的串流規則選項{#stream-rule-options-for-all-stream-rules}

這些選項適用於所有社交網路或張貼方法的任何串流規則。

文字和關鍵字欄位的搜尋功能：

* 當您輸入關鍵字時，Livefyre會自動使用布林運算 **元** OR，以用於個別字詞。 例如，要查找包含單詞 *cake* 或recipe *的貼文*，請輸入cake *，然後在* recipe *cake欄位中輸入recipe***[!UICONTROL keyword]** cake。

* 您可以以引號包住確切的片語文字，以搜尋精確的片語。 例如，要搜索準確的片語 *蛋糕配方*，請在欄位 *中輸入* 「蛋糕配方」 **[!UICONTROL keyword]** 。

* 您可以將布林值和精確的片語搜尋結合為一個串流規則。 例如，您可以逐一輸 *入每個片語*，以搜尋 *蛋糕*** 、食譜和「蛋糕食譜」。

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. 選擇以下選項之一：

   * **[!UICONTROL All Content.]** 允許任何內容。
   * **[!UICONTROL Media Required.]** 僅允許包含影像和視訊的內容。 (若是Instagram和Facebook內容，您可以指定 **[!UICONTROL Photos]** 或僅 **[!UICONTROL Videos]** 指定)。

* **[!UICONTROL Language]**. 選擇要搜尋的語言。 英文是預設語言。
* **[!UICONTROL Smart Tags]**. 選擇用來識別內容的標籤。 Livefyre運用電腦視覺技術，透過特定智慧型標籤來識別像片和視訊，讓搜尋更精確。 使用修 **[!UICONTROL ANY]** 飾詞可使用任何標籤將內容篩選到串流中，或 **[!UICONTROL ALL]** 使用修飾詞將內容篩選到使用所有標籤的串流中。 使用欄 **[!UICONTROL Image contains none of these smart tags]** 位輸入像片的標籤，這些像片包含您不想要的串流內容。 此選項不適用於文字內容。

* **[!UICONTROL Products]**. 新增產品標籤，以符合串流規則與產品目錄中的產品。
* **[!UICONTROL Premoderate]**. 選擇以下選項之一：

   * **[!UICONTROL On]**. 預先協調所有傳入規則內容。 您可以從ModQ的「串流」區段檢視預先協調的內容。 **[!UICONTROL On]** 覆寫「應用程式設定」中的設定。
   * **[!UICONTROL Off]**. 請勿預先協調任何傳入的規則內容。 **[!UICONTROL Off]** 覆寫「應用程式設定」中的設定。
   * **[!UICONTROL Inherited (Off)]**. 使用網站（下方）的預協調設定 **[!UICONTROL Site Settings]**。

* **[!UICONTROL SAFE Rules]**. 選擇以下選項之一：
   * **[!UICONTROL Apply SAFE Rules]**. 將所有SAFE規則套用至此串流。
   * **[!UICONTROL Apply SAFE Rules for:]** 選擇一個或多個選項以應用此流規則的SAFE規則。
   * **[!UICONTROL Disable SAFE Rules]**. 請勿將任何SAFE規則套用至此串流。

如需社交網路或內容類型專屬的串流規則選項，請參閱各社交網路或內容類型的下列檔案：

* [Facebook 頁面](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [電子郵件](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
