---
description: 您可以建立可從Twitter提取內容的串流規則。
seo-description: 您可以建立可從Twitter提取內容的串流規則。
seo-title: Twitter規則
solution: Experience Manager
title: Twitter規則
uuid: a7fd2398-fd6b-4c24-92b2-7471176d7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Twitter規則{#twitter-rules}

您可以建立可從Twitter提取內容的串流規則。

根據主題標籤、關鍵字、@mentions或作者建立Twitter規則。

新增 **[!UICONTROL Words]** 和規 **[!UICONTROL Username]** 則會傳回包含兩個項目的內容。

>[!NOTE]
>
>Livefyre遵守Twitter展示方針，客戶也有責任遵守這些方針。 如需詳細資訊，請參閱Twitter的顯示需求 [檔案](https://dev.twitter.com/terms/display-requirements)。

若要建立Twitter規則以從Twitter動態消息提取內容至您的應用程式或資料夾，您可以依下列方式進行篩選：

* **[!UICONTROL Keywords]**
   * 輸入 **[!UICONTROL Keywords]** 要包含在Twitter串流中或排除在Twitter串流中。 指定和欄位的值 **[!UICONTROL Contains any of these words]** 時， **[!UICONTROL Does not contain any of these words]** 會傳回包含第一個、不包含第二個的推文。 可輸入單一欄位的多個值，並傳回包含任何值的結果。 若要使用布林運算子AND來搜尋包含兩個或多個字詞的推文，請使用兩個&amp;符號(*&amp;*)來分隔這兩個字詞。
   * 例如，輸入關 **[!UICONTROL Contains any of these words]** 鍵字Giants、Posey和 **[!UICONTROL Does not contain any of these words]** Dodger時，會傳回所有包含單字 *Giants* 或Posey的推文，而不包含 ****Dodger的單字。
若要搜尋同時包含 *Giants* 和 *Posey的推文*，請輸入「Giants &amp; &amp; Posey」。 此功能僅支援Twitter規則 **[!UICONTROL Contains any of these words]** 中 **[!UICONTROL Does not contain any of these words]** 的和欄位。

* **[!UICONTROL Hashtags]**.
   * 輸入 **[!UICONTROL Hashtags]** 要包含在Twitter串流中或排除在Twitter串流中。 指定和欄位的值 **[!UICONTROL Contains any of these words]** 時， **[!UICONTROL Does not contain any of these words]** 會傳回在第一個欄位中包含主題標籤的推文，而在第二個欄位中不包含主題標籤的推文。 您可以為單一欄位輸入多個值。 串流會傳回包含任何值的結果。

* **[!UICONTROL Usernames]**
   * 輸入 **[!UICONTROL @mentions]** 或 **[!UICONTROL authors]** 以拉入串流，或從串流中排除。 使用核取方塊來定義 **[!UICONTROL Retweets]** 是否 **[!UICONTROL replies]** 也應包含選取的作者。
   >[!NOTE]
   >
   >您可以包含或排除作者；您無法將這兩個欄位結合為單一Twitter規則。

* **[!UICONTROL Minimum number of followers.]** 選取使用者必須從其貼文提取資訊的追隨者人數下限。
* **[!UICONTROL Location]**

   * 輸入位置(城市、zipcode、地址或地理代碼，使用通用的經緯度格式(+/- 90, +/- 180))。 開始輸入位置以顯示含建議的下拉式選單。 從下拉式清單中選取位置。 地圖會顯示該位置的管腳。 調整滑桿，為每個位置選取1英里至25英里半徑。 如果您未選擇半徑，Livefyre會自動選擇預設的8英里。
   >[!NOTE]
   >
   >對於這兩個欄位，將從輸入位置的中心計算距離。

   * 您可以新增多個位置和半徑。 通過按一下框中位置名稱旁的X，可以刪除位置。
   * 結合欄 **[!UICONTROL Is near this location]** 位和欄 **[!UICONTROL Is not near this location]** 位，以提取欄位中位置內的內容，但 **[!UICONTROL Is near this location]** 不是位於欄位中位置附 **[!UICONTROL Is not near this location]** 近。


* **[!UICONTROL Additional Filters]**
   * 使用其他篩選器進一步調整您的Twitter規則。 定義您是否要：
      * 包含 **[!UICONTROL Replies]** 至目標推文（如果串流變成高速度，此功能會自動停用）。
      * 包含來自 **[!UICONTROL Verified Twitter accounts only.]**
      * 包 **[!UICONTROL All Content]**&#x200B;含、 **[!UICONTROL Vines Only]**&#x200B;或 **[!UICONTROL Images Only.]**
      * 僅包含源自所選帳戶( **[!UICONTROL Minimum number of followers]** any、100、500、1000、10,000或100,000)之帳戶的推文。

如需所有串流規則的其他串流規則選項，請參 [閱所有串流規則的串流規則選項](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
