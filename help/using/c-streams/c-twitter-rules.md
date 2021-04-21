---
description: 您可以建立從Twitter提取內容的串流規則。
title: Twitter規則
exl-id: 3a5081eb-048d-4dcf-80a2-366af2cb2c86
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Twitter規則{#twitter-rules}

您可以建立從Twitter提取內容的串流規則。

根據主題標籤、關鍵字、@mentions或作者建立Twitter規則。

為規則新增&#x200B;**[!UICONTROL Words]**&#x200B;和&#x200B;**[!UICONTROL Username]**&#x200B;將會傳回包含兩個項目的內容。

>[!NOTE]
>
>Livefyre遵守Twitter的展示方針，客戶也有責任遵守這些方針。 如需詳細資訊，請參閱Twitter的[顯示要求](https://dev.twitter.com/terms/display-requirements)檔案。

若要建立「Twitter規則」以從Twitter動態消息提取內容至您的應用程式或資料夾，您可以依下列方式進行篩選：

* **[!UICONTROL Keywords]**
   * 輸入&#x200B;**[!UICONTROL Keywords]**&#x200B;以包含在您的Twitter流中或從中排除。 為&#x200B;**[!UICONTROL Contains any of these words]**&#x200B;和&#x200B;**[!UICONTROL Does not contain any of these words]**&#x200B;欄位指定值時，會傳回包含第一個欄位且不包含第二個欄位的推文。 可輸入單一欄位的多個值，並傳回包含任何值的結果。 若要使用布林運算子AND來搜尋包含兩個或多個字詞的推文，請使用兩個&amp;符號(*&amp;&amp;*)來分隔這兩個字詞。
   * 例如，輸入&#x200B;**[!UICONTROL Contains any of these words]**&#x200B;關鍵字Giants、Posey和&#x200B;**[!UICONTROL Does not contain any of these words]**&#x200B;關鍵字Dodger，將傳回包含單字&#x200B;*Giants*&#x200B;或&#x200B;*Posey*&#x200B;的所有推文，且不包含單字&#x200B;*Dodger*。
若要搜尋同時包含*Giants*&#x200B;和&#x200B;*Posey*&#x200B;字詞的推文，請輸入&quot;Giants &amp; &amp; Posey&quot;。 此功能僅受Twitter規則中&#x200B;**[!UICONTROL Contains any of these words]**&#x200B;和&#x200B;**[!UICONTROL Does not contain any of these words]**&#x200B;欄位支援。

* **[!UICONTROL Hashtags]**。
   * 輸入&#x200B;**[!UICONTROL Hashtags]**&#x200B;以包含在您的Twitter流中或從中排除。 為&#x200B;**[!UICONTROL Contains any of these words]**&#x200B;和&#x200B;**[!UICONTROL Does not contain any of these words]**&#x200B;欄位指定值時，會傳回在第一個欄位中包含主題標籤的推文，而在第二個欄位中不包含主題標籤。 您可以為單一欄位輸入多個值。 串流會傳回包含任何值的結果。

* **[!UICONTROL Usernames]**
   * 輸入&#x200B;**[!UICONTROL @mentions]**&#x200B;或&#x200B;**[!UICONTROL authors]**&#x200B;以拉入串流，或從串流中排除。 使用核取方塊來定義是否也應包含選取作者的&#x200B;**[!UICONTROL Retweets]**&#x200B;或&#x200B;**[!UICONTROL replies]**。

   >[!NOTE]
   >
   >您可以包含或排除作者；您無法將這兩個欄位結合為單一的Twitter規則。

* **[!UICONTROL Minimum number of followers.]** 選取使用者必須從其貼文提取資訊的追隨者人數下限。
* **[!UICONTROL Location]**

   * 輸入位置(城市、zipcode、地址或地理代碼，使用通用的經緯度格式(+/- 90, +/- 180))。 開始輸入位置以顯示含建議的下拉式選單。 從下拉式清單中選取位置。 地圖會顯示該位置的管腳。 調整滑桿，為每個位置選取1英里至25英里半徑。 如果您未選擇半徑，Livefyre會自動選擇預設的8英里。
   >[!NOTE]
   >
   >對於這兩個欄位，將從輸入位置的中心計算距離。

   * 您可以新增多個位置和半徑。 通過按一下框中位置名稱旁的X，可以刪除位置。
   * 結合&#x200B;**[!UICONTROL Is near this location]**&#x200B;和&#x200B;**[!UICONTROL Is not near this location]**&#x200B;欄位，在&#x200B;**[!UICONTROL Is near this location]**&#x200B;欄位中的位置內提取內容，但不在&#x200B;**[!UICONTROL Is not near this location]**&#x200B;欄位中的位置附近。


* **[!UICONTROL Additional Filters]**
   * 使用其他篩選器進一步調整您的Twitter規則。 定義您是否要：
      * 將&#x200B;**[!UICONTROL Replies]**&#x200B;加入目標推文（如果串流變成高速度，此功能會自動停用）。
      * 包含&#x200B;**[!UICONTROL Verified Twitter accounts only.]**&#x200B;的推文
      * 包含&#x200B;**[!UICONTROL All Content]**、**[!UICONTROL Vines Only]**&#x200B;或&#x200B;**[!UICONTROL Images Only.]**
      * 僅包含源自所選&#x200B;**[!UICONTROL Minimum number of followers]**（any、100、500、1000、10,000或100,000）之帳戶的推文。

如需所有串流規則的其他串流規則選項，請參閱[所有串流規則的串流規則選項](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
