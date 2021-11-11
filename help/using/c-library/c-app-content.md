---
description: 管理Livefyre網路上的內容。
title: 應用程式內容標籤
exl-id: 8b3e5281-59ba-4321-8fee-4160ab7a5d5e
source-git-commit: 600c9712366f5de303de27cf39045beccd4145eb
workflow-type: tm+mt
source-wordcount: '1115'
ht-degree: 0%

---

# 應用程式內容標籤{#app-content-tab}

管理Livefyre網路上的內容。

資料庫中的「應用程式內容」索引標籤可讓您搜尋及協調在應用程式中發佈的內容。 此 **[!UICONTROL App Content]** 索引標籤可啟用具有萬用字元搜尋的數個搜尋篩選器，讓您更快速輕鬆地定義搜尋參數。

使用「應用程式內容」索引標籤來：

* 搜尋內容
* 檢視內容記錄
* 協調內容
* 新增標籤
* 功能內容
* 將內容與產品目錄中的產品關聯

如需如何使用「應用程式內容」標籤協調內容的詳細資訊，請參閱 [使用「應用程式內容」索引標籤協調內容](../c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).

## 通配符搜索 {#section_jvr_ntm_zz}

Livefyre搜尋欄位支援萬用字元，可讓您在字詞（或字詞片段）中新增星號(*)，以擷取部分相符項目。

例如：

* 球只傳球
* 球*返回球
* *返球球和足球
* *球*返回球和球

## 搜尋內容 {#section_fw1_mtm_zz}

「應用程式內容」面板可讓您使用數個不同的內容篩選選項來縮小搜尋範圍。

![](assets/PublishedState-1024x367.png)

使用 **[!UICONTROL Quick Filters]** 下拉將傳回的內容縮小到 **[!UICONTROL All Content]**, **[!UICONTROL All Sidenotes]**, **[!UICONTROL Approved]**, **[!UICONTROL Approved & Flagged]**, **[!UICONTROL Pending]**，或 **[!UICONTROL Rights Requests]** 狀態。 然後選取 **[!UICONTROL Filter by]** 選項，並使用可用於縮小搜索範圍的複選框或輸入欄位。

使用下拉式功能表，依 **[!UICONTROL Newest]**, **[!UICONTROL Oldest]**, **[!UICONTROL Recently updated]**, **[!UICONTROL Most flags]** 或 **[!UICONTROL Most liked]**.

## 依選項篩選 {#section_aqn_xqm_zz}

使用 **[!UICONTROL Filter by]** 欄來依下列選項篩選：

* **狀態** 可讓您依內容目前的協調狀態進行篩選：** [!UICONTROL All Content]**, **[!UICONTROL Approved]**, **[!UICONTROL Pending]**，或 **[!UICONTROL Bozo]**.

* **來源** 可讓您依內容的來源篩選。 選擇 **[!UICONTROL Livefyre]** 列出使用者產生的內容，並直接張貼至資料流中。 選擇 **[!UICONTROL Facebook]**, **[!UICONTROL Twitter]**，或 **[!UICONTROL RSS]** 納入從這些來源提取至您應用程式的內容。

* **標幟** 選取旗標可讓您依 **[!UICONTROL User Flags]** （垃圾郵件、非主題、攻擊或不同意）, **[!UICONTROL System Flags]** 由SAFE套用（設定檔、垃圾訊息或神奇地協調），或 **[!UICONTROL Moderation Recommendations]**. ![](assets/appcontentfilter.png)

* **日期/時間** 可讓您依內容最初的時間篩選 **[!UICONTROL Created]** （或透過SocialSync或資料流提取至應用程式），或最後 **[!UICONTROL Modified]** （已編輯、已標籤或狀態已變更）。

* **作者** 可讓您依作者的 **[!UICONTROL IP]** 地址， **[!UICONTROL Display Name]** （可在「使用者」面板上或作者張貼之內容上方找到），或 **[!UICONTROL User ID]**（可在「使用者」面板上找到）。

* **包含** 可讓您依 **[!UICONTROL Keyword]** 或 **[!UICONTROL Content Tag]**. 選取 **[!UICONTROL Media]** 核取方塊，僅傳回包含媒體的內容。 (若要搜尋所有內容，請向下捲動清單中的所有內容，然後按一下 **[!UICONTROL Search full data]**.)

   **注意：** 不支援多個關鍵字和內容標籤搜尋。 如果輸入了多個關鍵字或標籤，則搜索將使用最後一個字。

   依「內容標籤」搜尋時，當您在搜尋欄位中輸入內容時，會自動填入建議的標籤。 搜尋結果會傳回所有已指派標籤的內容。 (使用此欄位來搜尋精選內容，或按一下 **[!UICONTROL Featured]** 標籤。)

   **注意：** 在標籤名稱前使用減號(-)來搜尋不包含該標籤的內容。 例如：搜尋「 — Miley」，以搜尋不包含「Miley」標籤的所有內容。

* **應用程式** 可讓您依 **[!UICONTROL Collection ID]**, **[!UICONTROL App Tag]**，或 **父ID**. 依上層ID篩選會傳回所有回覆輸入內容ID的內容。 （輸入以逗號分隔的標籤，依多個標籤篩選。）

* **權限** 可讓您依權限請求狀態進行篩選：** [!UICONTROL Requested]**, **[!UICONTROL Granted]**, **[!UICONTROL Replied]**，或 **[!UICONTROL Expired]**.

## 博佐內容 {#section_afl_vqm_zz}

在應用程式中， **[!UICONTROL Bozo]** 內容只會對內容的作者顯示。 這可讓使用者相信其內容已通過核准，同時將其隱藏給其他所有使用者和協調者。

>[!NOTE]
>
>源自SocialSync或資料流的社交內容 **[!UICONTROL cannot]** 被設定為博佐。

Bozo內容的原因如下：

* 由SAFE標識為垃圾郵件的內容會自動設定為Bozo狀態。
* 來自「禁止用戶」的所有內容都自動設定為Bozo。
* 內容可以在Studio中標籤為Bozo。
* 協調者可以直接在資料流中播放Bozo內容。

## 檢視內容記錄 {#section_ayz_tqm_zz}

「內容」面板可讓您檢閱所有列出內容的歷史記錄，包括預先協調、垃圾訊息篩選、貼文日期，以及指派給項目的任何使用者標幟或附註。

使用內容面板底部的標籤來檢視其歷史記錄。

* **[!UICONTROL More Info:]** 列出此內容上的所有活動，包括提交、編輯、垃圾郵件檢查、狀態更改和附註。 Livefyre內容ID和使用者的IP位址也會顯示在本節中。
* **[!UICONTROL Replies:]** 最多列出6個回覆。 按一下 **[!UICONTROL Show all replies]** 來顯示對貼文的所有回覆。

* **[!UICONTROL Flags & Reports:]** 列出所有使用者標幟，以及標幟內容之使用者的頭像和任何報表（在標幟內容時由使用者新增的附註）。
* **[!UICONTROL Add a note:]** 可讓您新增附註，供其他管理員或協調者看見。
* **[!UICONTROL Request Rights:]** 開啟 **[!UICONTROL New Rights Request]** 對話，可從中發出權利要求。

* **[!UICONTROL Save as Asset:]**開啟 **[!UICONTROL Advanced Options]** 對話方塊，可讓您將選取的項目儲存至資產資料庫、發佈至應用程式，或向其作者要求重複使用權限。

![](assets/PublishedMoreInfo-1024x462.png)

## 新增標籤至內容 {#section_xb4_mxr_rdb}

將內容標籤可讓您對內容進行分類和組織，以方便擷取和自訂樣式，或將內容標示為特色內容。

若要新增標籤，只需按一下加號( **[!UICONTROL +]**)圖示。 輸入新標籤，或從現有標籤清單中選取。

![](assets/PublishedAddTag-1024x338.png)

## 在所有資產中搜尋影像 {#section_zxf_hsf_wcb}

將內容新增至程式庫後，您就可以使用智慧標籤來搜尋內容。

在「資料庫」的「所有資產」下，按一下 **[!UICONTROL Show Filters]** 然後：

* 在搜索欄位中輸入要搜索的文本
* 依關聯性排序
* 在 **[!UICONTROL Tags]** 欄位以依智慧標籤搜尋。 智慧標籤排名演算法會使用智慧標籤可信度分數來篩選內容、內容的新增程度，以及使用者為內容提供的星數。

## 精選內容 {#section_emb_kqm_zz}

選取預設值 **[!UICONTROL Featured]** 標籤，將內容標示為精選內容，並強調對使用者而言非常重要。 標籤後，使用自訂樣式選項來自訂應用程式中的精選內容。

## 功能或取消功能內容 {#section_ojx_3qm_zz}

* 在Studio中，按一下 **[!UICONTROL +]** 在內容旁簽名，選擇 **[!UICONTROL Featured]** 標籤，然後按一下 **[!UICONTROL Enter]** 功能內容。 標籤會儲存並顯示在內容旁。

* 若要取消功能，請按一下 **[!UICONTROL x]** 在 **[!UICONTROL Featured]** 標籤。

* 在「留言」、「即時部落格」或「審閱應用程式」中，將游標暫留在您要加以處理的內容上，然後按一下 **[!UICONTROL Feature]**. 若要取消功能，只需將滑鼠指標暫留在內容上，然後按一下 **[!UICONTROL Unfeature]**.

>[!NOTE]
>
>由於空間限制，聊天內容可能只能使用Studio進行特色介紹或取消特色介紹，也可能不能在應用程式本身進行特色介紹。

## 編輯精選內容 {#section_pyw_hqm_zz}

大部分針對內容的一般動作都可對精選內容採取，但下列除外：

* 無法標籤精選內容。
* 使用者在內容完成功能後，即無法編輯其內容，但仍可視需要刪除。 協調者可以編輯精選內容。
