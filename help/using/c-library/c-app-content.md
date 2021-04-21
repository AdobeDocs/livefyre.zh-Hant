---
description: 管理整個Livefyre網路的內容。
title: 應用程式內容標籤
exl-id: 8b3e5281-59ba-4321-8fee-4160ab7a5d5e
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 0%

---

# 應用程式內容標籤{#app-content-tab}

管理整個Livefyre網路的內容。

您的「資料庫」中的「應用程式內容」索引標籤可讓您搜尋並協調發佈在整個「應用程式」中的內容。 **[!UICONTROL App Content]**&#x200B;標籤可啟用數個使用萬用字元搜尋的搜尋篩選器，讓您更快速輕鬆地定義搜尋參數。

使用「應用程式內容」索引標籤，您可以：

* 搜尋內容
* 檢視內容歷史記錄
* 協調內容
* 新增標籤
* 功能內容
* 將產品目錄中的內容與產品關聯

如需如何使用「應用程式內容」索引標籤協調內容的詳細資訊，請參閱[](../c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content)。

## 通配符搜索{#section_jvr_ntm_zz}

Livefyre搜尋欄位支援萬用字元，可讓您在字詞（或字詞片段）中新增星號(*)，以擷取部分相符項目。

例如：

* 球僅返回球
* ball*返回球和球
* *球返回球和足球
* *ball*返回球和球，並且滾球

## 搜尋內容{#section_fw1_mtm_zz}

「應用程式內容」面板可讓您使用數個不同的內容篩選選項來縮小搜尋範圍。

![](assets/PublishedState-1024x367.png)

使用&#x200B;**[!UICONTROL Quick Filters]**&#x200B;下拉式清單將傳回的內容縮小為&#x200B;**[!UICONTROL All Content]**、**[!UICONTROL All Sidenotes]**、**[!UICONTROL Approved]**、**[!UICONTROL Approved & Flagged]**、**[!UICONTROL Pending]**&#x200B;或&#x200B;**[!UICONTROL Rights Requests]**&#x200B;狀態。 然後選取&#x200B;**[!UICONTROL Filter by]**&#x200B;選項，並使用可用的核取方塊或輸入欄位來縮小搜尋範圍。

使用下拉菜單按&#x200B;**[!UICONTROL Newest]**、**[!UICONTROL Oldest]**、**[!UICONTROL Recently updated]**、**[!UICONTROL Most flags]**&#x200B;或&#x200B;**[!UICONTROL Most liked]**&#x200B;對清單中的內容進行排序。

## 依選項{#section_aqn_xqm_zz}篩選

使用&#x200B;**[!UICONTROL Filter by]**&#x200B;欄可依下列選項篩選：

* **狀** 態可讓您依內容目前的協調狀態進行篩選：** [!UICONTROL All Content]*、 **[!UICONTROL Approved]**、 **[!UICONTROL Pending]**&#x200B;或 **[!UICONTROL Bozo]**。

* **來** 源可讓您依內容來源進行篩選。選擇&#x200B;**[!UICONTROL Livefyre]**&#x200B;以列出使用者產生的直接張貼至串流的內容。 選取&#x200B;**[!UICONTROL Facebook]**、**[!UICONTROL Twitter]**&#x200B;或&#x200B;**[!UICONTROL RSS]**，以包含從這些來源提取至您應用程式的內容。

* **標** 幟選擇標幟可讓您依 **[!UICONTROL User Flags]** （垃圾訊息、非主題、冒犯性或不同意）、 **[!UICONTROL System Flags]** 由SAFE（Profanity、Spam或Magically Comproded）或進行篩選 **[!UICONTROL Moderation Recommendations]**。  ![](assets/appcontentfilter.png)

* **日期/** 時間允許您篩選內容最初（或透過SocialSync或串流提取至應用程式）或最後 **[!UICONTROL Created]**  **[!UICONTROL Modified]** (已編輯、已標幟或狀態變更)的時間。

* **作** 者可讓您依作者的位址、 **[!UICONTROL IP]** ( **[!UICONTROL Display Name]** 在「使用者」面板或作者張貼之內容的上方)或 **[!UICONTROL User ID]**（在「使用者」面板上）進行篩選。

* **包** 含可讓您依或篩選最近90天的 **[!UICONTROL Keyword]** 內容 **[!UICONTROL Content Tag]**。選取&#x200B;**[!UICONTROL Media]**&#x200B;核取方塊，僅傳回包含媒體的內容。 （若要搜尋所有內容，請向下捲動清單中的所有內容，然後按一下&#x200B;**[!UICONTROL Search full data]**。）

   **注意：不** 支援多個關鍵字和內容標籤搜尋。如果輸入了多個關鍵字或標籤，則搜尋會使用最後一個字詞。

   依內容標籤搜尋時，當您在搜尋欄位中輸入時，建議的標籤會自動填入。 搜尋結果會傳回所有指派過標籤的內容。 （使用此欄位來搜尋「精選內容」，或按一下Studio中任何精選內容的&#x200B;**[!UICONTROL Featured]**&#x200B;標籤。）

   **注意：** 在標籤名稱前使用減號(-)符號，以搜尋不包含該標籤的內容。例如：搜尋「-Miley」以搜尋不含「Miley」標籤的所有內容。

* **應** 用程式可讓您依據 **[!UICONTROL Collection ID]**、 **[!UICONTROL App Tag]**&#x200B;或父 **代ID篩選**。依父ID篩選會傳回所有回覆輸入內容ID的內容。 （輸入以逗號分隔的標籤，依多個標籤篩選。）

* **Rights** 允許您依「Rights Requests」狀態進行篩選：**  [!UICONTROL Requested]** **[!UICONTROL Granted]**、 **[!UICONTROL Replied]**&#x200B;或 **[!UICONTROL Expired]**。

## Bozo內容{#section_afl_vqm_zz}

在「應用程式」中，**[!UICONTROL Bozo]**&#x200B;內容只會顯示給內容的作者。 這可讓使用者相信其內容已獲得核准，同時隱藏給其他使用者和協調者。

>[!NOTE]
>
>以SocialSync或Streams **[!UICONTROL cannot]**&#x200B;產生的社交內容設為Bozo。

您可以基於下列原因來使用Bozo內容：

* 由SAFE識別為「垃圾訊息」的內容會自動設為Bozo狀態。
* 來自「禁止使用者」的所有內容都會自動設為Bozo。
* 內容可能會標籤為Studio的Bozo。
* 協調者可直接在串流中Bozo內容。

## 檢視內容歷史記錄{#section_ayz_tqm_zz}

內容面板可讓您檢視所有列出內容的歷史記錄，包括預先協調、垃圾訊息篩選、貼文日期，以及指派給項目的任何使用者標幟或附註。

使用內容面板底部的標籤來檢視其歷史記錄。

* **[!UICONTROL More Info:]** 列出此內容上的所有活動，包括提交、編輯、垃圾郵件檢查、狀態更改和附註。Livefyre內容ID和使用者的IP位址也會顯示在本節中。
* **[!UICONTROL Replies:]** 列出最多6個回覆。按一下&#x200B;**[!UICONTROL Show all replies]**&#x200B;以顯示對貼文的所有回覆。

* **[!UICONTROL Flags & Reports:]** 列出所有使用者標幟，以及標幟內容之使用者的頭像，以及任何報表（使用者在標幟內容時新增的附註）。
* **[!UICONTROL Add a note:]** 可讓您新增註解，供其他管理員或協調者檢視。
* **[!UICONTROL Request Rights:]** 開啟對 **[!UICONTROL New Rights Request]** 話方塊，您可從中發出權利要求。

* **[!UICONTROL Save as Asset:]**開啟&#x200B;**[!UICONTROL Advanced Options]**&#x200B;對話方塊，讓您將選取的項目儲存至資產庫、將它發佈至應用程式，或向其作者要求重複使用權限。

![](assets/PublishedMoreInfo-1024x462.png)

## 新增標籤至內容{#section_xb4_mxr_rdb}

標籤內容可讓您將內容分類並組織，以方便擷取和自訂樣式，或將內容標示為特色內容。

若要新增「標籤」，只需按一下內容下方的加號(**[!UICONTROL +]**)圖示。 輸入新標籤，或從現有標籤清單中選擇。

![](assets/PublishedAddTag-1024x338.png)

## 在所有資產中搜尋影像{#section_zxf_hsf_wcb}

將內容新增至程式庫後，您就可以透過智慧標籤來搜尋內容。

在「資料庫」的「所有資產」下方，按一下&#x200B;**[!UICONTROL Show Filters]**，然後：

* 在搜索欄位中輸入要搜索的文本
* 依相關性排序
* 在&#x200B;**[!UICONTROL Tags]**&#x200B;欄位中輸入文字，以依智慧型標籤搜尋。 智慧型標籤排名演算法會使用智慧型標籤信賴分數來篩選內容、內容的新增功能，以及使用者提供內容的星數。

## 精選內容{#section_emb_kqm_zz}

選取預設的&#x200B;**[!UICONTROL Featured]**&#x200B;標籤，將內容標示為精選內容，並反白標示它對您的使用者而言十分重要。 標籤後，使用自訂樣式選項來自訂應用程式中的「精選內容」。

## 要功能或取消功能內容{#section_ojx_3qm_zz}

* 在Studio中，按一下內容旁的&#x200B;**[!UICONTROL +]**&#x200B;符號，在下拉式清單中選取&#x200B;**[!UICONTROL Featured]**&#x200B;標籤，然後按一下&#x200B;**[!UICONTROL Enter]**&#x200B;以顯示功能內容。 標籤將會儲存並顯示在內容的旁邊。

* 若要取消功能，請按一下內容片段上顯示之&#x200B;**[!UICONTROL Featured]**&#x200B;標籤上的&#x200B;**[!UICONTROL x]**。

* 從「留言」、「即時部落格」或「評論應用程式」中，將滑鼠指標暫留在您要加入的內容上，然後按一下&#x200B;**[!UICONTROL Feature]**。 若要取消功能，只需將滑鼠指標暫留在內容上，然後按一下&#x200B;**[!UICONTROL Unfeature]**。

>[!NOTE]
>
>由於空間限制，聊天內容可能只會使用Studio進行特寫或非特寫，而且可能不會從應用程式本身進行特寫。

## 編輯精選內容{#section_pyw_hqm_zz}

大部分針對內容的常規動作都可針對「特色」內容執行，但下列除外：

* 無法標幟特色內容。
* 使用者在內容經過「精選」後便無法編輯，不過他們仍可視需要加以刪除。 協調者可以編輯精選內容。
