---
description: 您可以建立從Twitter提取內容的串流規則。
seo-description: 您可以建立從Twitter提取內容的串流規則。
seo-title: Twitter規則
solution: Experience Manager
title: Twitter規則
uuid: a7fd2398-fd6 b-4c24-92b2-7471176d7648
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Twitter規則{#twitter-rules}

您可以建立從Twitter提取內容的串流規則。

根據主題標籤、關鍵字、@提及或作者建立Twitter規則。

新增 **[!UICONTROL Words]** 和規則 **[!UICONTROL Username]** 規則會傳回包含這兩項項目的內容。

>[!NOTE]
>
>Livefyre會遵守Twitter顯示准則，客戶也有責任遵守這些准則。如需詳細資訊，請參閱Twitter [的顯示需求說明文件](https://dev.twitter.com/terms/display-requirements)。

若要建立Twitter規則，將內容從Twitter動態消息提取至您的應用程式或資料夾，您可以依下列方式進行篩選：

* **[!UICONTROL Keywords]**
   * 輸入 **[!UICONTROL Keywords]** 在您的Twitter串流中，或排除在外。指定和 **[!UICONTROL Contains any of these words]****[!UICONTROL Does not contain any of these words]** 欄位的值會傳回包含第一個值且不包含第二個推文的推文。可輸入單一欄位的多個值，並傳回包含任何值的結果。若要使用布林運算元AND搜尋推文，請使用兩個以上的字詞，使用兩個&(&)**分隔這兩個字詞。
   * 例如，輸入 **[!UICONTROL Contains any of these words]** 關鍵字Giant、Posey和 **[!UICONTROL Does not contain any of these words]** 關鍵字Dodger時，會傳回所有包含字詞Giant ** 或 *Poise* 且不包含Dodger單字 **的推文。
若要搜尋 *包含Giant* 和 *Posey*單字的推文，請輸入「giants&& Posey」。只有Twitter規則中的 **[!UICONTROL Contains any of these words]****[!UICONTROL Does not contain any of these words]** 和欄位支援此功能。

* **[!UICONTROL Hashtags]**.
   * 輸入 **[!UICONTROL Hashtags]** 在您的Twitter串流中，或排除在外。指定 **[!UICONTROL Contains any of these words]** 和 **[!UICONTROL Does not contain any of these words]** 欄位的值會傳回包含第一個欄位中主題標籤的推文，且在第二個欄位中不包含主題標籤。您可以為單一欄位輸入多個值。串流會傳回包含任何值的結果。

* **[!UICONTROL Usernames]**
   * 輸入 **[!UICONTROL @mentions]** 或 **[!UICONTROL authors]** 提取串流，或從串流排除。您可以使用核取方塊 **[!UICONTROL Retweets]** 來定義 **[!UICONTROL replies]** 是否也應納入選取的作者。
   >[!NOTE]
   >
   >您可以包括或排除作者；您無法將這兩個欄位合併為單一Twitter規則。

* **[!UICONTROL Minimum number of followers.]** 選取使用者必須在貼文中提取資訊的人數下限。
* **[!UICONTROL Location]**

   * 以通用緯度/經度格式(+/-90、+/-180)輸入位置(城市、郵遞區號、地址或地理位置)。開始鍵入位置，以顯示下拉式選單和建議。從下拉式清單中選取位置。地圖會顯示該位置的釘選。調整滑桿，為每個位置選擇一英里到25英里的半徑。如果您不選擇半徑，Livefyre會自動選擇8英里的預設值。
   >[!NOTE]
   >
   >對於這兩個欄位，距離會從輸入位置的中心計算。

   * 您可以新增多個位置和半徑。您可以按一下方塊中位置名稱旁邊的X來刪除位置。
   * 結合和 **[!UICONTROL Is near this location]****[!UICONTROL Is not near this location]** 欄位，將內容提取到 **[!UICONTROL Is near this location]** 欄位中位置的位置，但不能提取 **[!UICONTROL Is not near this location]** 欄位中的位置。


* **[!UICONTROL Additional Filters]**
   * 使用其他篩選器進一步細化您的Twitter規則。定義您是否將：
      * 加入 **[!UICONTROL Replies]** 目標推文(如果串流變成高速，則此功能會自動停用)。
      * 包括推文(從 **[!UICONTROL Verified Twitter accounts only.]**
      * 包括 **[!UICONTROL All Content]**、 **[!UICONTROL Vines Only]**或或 **[!UICONTROL Images Only.]**
      * 只包含源自所選 **[!UICONTROL Minimum number of followers]** (任何、100、500、1000、10,000或100,000)之帳戶的推文。

如需所有串流規則的其他串流規則選項，請參閱 [所有串流規則的串流規則選項](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
