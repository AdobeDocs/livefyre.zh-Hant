---
description: 從單一智慧型介面協調內容。
seo-description: 從單一智慧型介面協調內容。
seo-title: 使用ModQ協調內容
title: 使用ModQ協調內容
uuid: c630fb85-7bd0-4da0-ac7e-080e970fb4f9
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '1465'
ht-degree: 0%

---


# 使用ModQ{#moderate-content-using-modq}協調內容

從單一智慧型介面協調內容。

ModQ會建立網站或網路上所有符合您所定義之預先協調規則之內容的即時佇列，讓協調者只能專注在需要他們注意的內容上。

定義ModQ設定後，進入串流的新內容或您的使用者標幟的現有內容，就會新增至您的佇列。 變更規則不會從ModQ移除內容，但會根據您的新設定，將新內容新增至佇列。

ModQ允許您：

* 在內容中協調、檢視整個執行緒，並按一下「核准」、「垃圾桶」或「Bozo」，即可檢視個別內容片段或完成執行緒。
* 提高工作流程的速度和效率。
* 回覆內容，以增加您對社群的參與。
* 讓多位協調者可以處理內容，毋需重複彼此的工作。

Livefyre內容會列在ModQ中長達6週，而未處理的預先協調串流內容則會列在ModQ中90天。

>[!NOTE]
>
>如果單一內容符合ModQ中要包含的多個規則，則可多次列出該內容。 例如，如果某個內容觸發Offension的使用者標幟規則，接著又觸發Profane的其他規則，則會在ModQ中列出兩次。

ModQ中未顯示的內容包括：

* 垃圾內容。
* 協調者核准的內容。
* 禁止使用者張貼的內容，或禁止使用者套用的使用者標幟。

## 導航ModQ {#section_uv4_db2_yy}

ModQ分為兩個標籤式面板：

* **[!UICONTROL Items]** 列出所有預定要進行協調的Livefyre原生和SocialSync內容。此標籤包含任何在協調後已標幟或編輯過的社交搜尋或串流內容。
* **[!UICONTROL Streams Premoderation]** 列出從串流進入您應用程式且啟用「預先協調」的所有內容。（如需詳細資訊，請參閱建立串流。）

這兩個標籤都提供許多相同的篩選器和協調工具。

* **[!UICONTROL Item Count]** 隊列中剩餘的項目數顯示在ModQ的左上角。
* **[!UICONTROL Filter]** 按一 **[!UICONTROL Filter]** 下可定義參數，讓內容列在窗格中。
* **[!UICONTROL History]** 按一下 **[!UICONTROL History]** 畫面右上方的按鈕，以開啟最近協調的內容清單，讓您檢閱作品，或變更最近協調動作。再按一下按鈕，返回佇列的內容。 只會顯示您最近的100個動作。 **歷史** 記錄不會列出其他協調者採取的動作。

* **[!UICONTROL User Pane]** 按一下頁面右上方的展開或收合按鈕，以開啟或關閉「使用者」窗格。

## 瞭解ModQ內容{#section_oxm_kgz_y1b}

每個列出的內容會顯示預覽資訊，包括張貼內容的網站及其作者。 選取項目會顯示整段內容，包括任何媒體。

>[!NOTE]
>
>Livefyre原生內容會顯示比透過串流或其他社交媒體來源新增至應用程式的內容更多資訊。

當您選取項目時，會顯示下列資訊：

* **[!UICONTROL Time in Queue:]** 列出內容被添加到ModQ的時間長度。
* **[!UICONTROL App name:]** 顯示內容的應用程式。連結至含有應用程式的網站。
* **[!UICONTROL Content Body:]** 文字和媒體縮圖（如果有的話）。
* **[!UICONTROL Status:]** 內容的目前狀態（擱置中、已刪除等）。
* **[!UICONTROL Author information:]** 作者的名稱和使用者名稱。
* **[!UICONTROL Timestamp:]** 內容建立時的相對時間戳記。預覽Studio的「應用程式內容」頁面中的內容片段。
* **[!UICONTROL Flag Type:]** 冒犯性、不同意、垃圾郵件等

   * 安全標幟：垃圾訊息和大量散發。
   * 您的網路和網站屬性清單所套用的旗標：粗俗。
   * SAFE所套用的標幟：仇恨言論、個人識別資訊(PII)、侮辱和褻瀆。
   * 使用者標幟：垃圾訊息、非主題、冒犯性和不同意見。

* **[!UICONTROL Flag origin:]** 列出旗標的來源。可能是SAFE、使用者名稱或Livefyre。
* **[!UICONTROL More info:]** 列出內容的詳細資訊，包括按贊次數、使用者標幟、回覆和套用至內容的任何標籤。按一下「網站」會開啟內容所在網站的頂層頁面。 按一下時間戳記會開啟頁面上內容的串接檢視。

## ModQ {#section_r2c_qc2_yy}中的篩選選項

按一下「ModQ」視窗左上角的&#x200B;**[!UICONTROL Filter]**，以開啟具有列出內容可用篩選選項的面板。 當您選取選項時，ModQ會自動更新，只列出您篩選的內容。 按一下&#x200B;**[!UICONTROL Clear filters]**&#x200B;以清除所有選取的選項，然後重新載入完整的項目清單。

**[!UICONTROL Items]**&#x200B;和&#x200B;**[!UICONTROL Streams Premoderation]**&#x200B;標籤有不同的篩選選項。

**[!UICONTROL Items]**&#x200B;和&#x200B;**[!UICONTROL Streams Premoderation]**&#x200B;下的ModQ提供以下選項：

* **[!UICONTROL App]**。使用「搜尋應用程式」欄位，依應用程式篩選結果。 可以選取多個應用程式。
* **[!UICONTROL System Flags]**。依「垃圾訊息」、「褻瀆」、「安全」和「預先協調」規則等規則篩選內容。

   * 選擇&#x200B;**[!UICONTROL Spam]**&#x200B;將列出SAFE標籤為垃圾郵件的所有內容。
   * 選擇&#x200B;**[!UICONTROL Profanity]**&#x200B;將列出您的「網路」或「網站粗細清單」標籤的所有內容。
   * 選擇&#x200B;**[!UICONTROL SAFE]**&#x200B;將列出因您的SAFE規則而進入ModQ的所有內容。
   * 選取&#x200B;**[!UICONTROL Premoderation]**&#x200B;會列出您的「網路」、「串流」或「應用程式設定」標籤為「預先協調」的所有內容。

* **[!UICONTROL User Flags]** 依使用者標幟篩選內容。選項包括「冒犯」、「垃圾訊息」、「非主題」和「不同意見」。
* **[!UICONTROL Rights Requests.]** 按一下核取方塊，僅顯示已授予權限的內容。
* **[!UICONTROL Entered the queue.]** 依傳送內容至ModQ的時段篩選內容。內容傳送至ModQ的時間不一定是內容張貼至其應用程式的時間。

在&#x200B;**[!UICONTROL Streams Premoderation]**&#x200B;下，ModQ的選項如下：

* **[!UICONTROL Social Source]** 依據產生內容的社交來源篩選內容。例如，社交來源的選項包括Twitter、Instagram、Facebook和RSS。

**[!UICONTROL Items]**&#x200B;下的ModQ可使用以下選項：

**[!UICONTROL Moderation Recommendations]**。依自動協調建議所提供的建議篩選內容。

下列影像顯示ModQ中的「協調建議」外觀： ![](assets/mod_reco1.png)

在&#x200B;**[!UICONTROL Network Settings > Moderation]**&#x200B;和&#x200B;**[!UICONTROL Network Settings > ModQ]**&#x200B;中設定內容時，會針對內容提供協調建議。

## 可在ModQ {#section_h4g_wrn_z1b}中使用的操作

您可以決定如何處理ModQ中的每段內容。

選擇下列選項之一：

* 要批准內容的&#x200B;**[!UICONTROL Checkbox]**&#x200B;圖示
* 傳送內容至垃圾桶的&#x200B;**[!UICONTROL Trash can]**&#x200B;圖示
* **[!UICONTROL Request Rights]** 向內容擁有者要求內容的權限。

   >[!NOTE]
   >
   >您無法在ModQ中要求Instagram內容的權限。 您必須使用「資料庫」或「應用程式內容」，才能從Instagram傳送內容的權限要求。

* **[!UICONTROL Feature and Approve]** 核准內容，並加入內容。
* **[!UICONTROL Product Tag and Approve]** 將產品從產品目錄新增至內容，然後加以核准。
* **[!UICONTROL Mark as Pending]** 來標籤內容為待審。

>[!NOTE]
>
>一旦您將內容廢棄後，內容片段及對內容的所有回覆都會從ModQ中永久移除。 若要將已銷毀的內容放入應用程式，請參閱「將已銷毀的項目新增至應用程式」[。](/help/using/c-features-livefyre/c-about-moderation/t-add-trashed-item-back-into-app.md#t_add_trashed_item_back_into_app)

如果內容已處於所需狀態，選擇「垃圾筒」、「Bozo」或「核准」將確認狀態並從清單中移除項目。 協調一段內容會立即從您的佇列中移除，並將其停用在其他協調者的佇列中。

>[!NOTE]
>
>串流內容可能不是Bozo的。刪除串流內容會永久從串流中移除，且無法復原。

內容協調後，就會從協調者的ModQ中移除，其作者也無法再從串流中編輯內容。 如果協調者關閉項目，或使用者刪除其注釋，則其他協調者佇列中會即時顯示為灰色。 當內容呈灰色顯示時，頁面上會顯示&#x200B;**[!UICONTROL Clear Moderated]**&#x200B;按鈕，讓協調者將其從清單中移除，而且不論其他協調者活動為何，都能維持其在頁面上的位置。

## 在ModQ {#section_tpx_qgz_y1b}中使用垃圾桶函式

使用「設定」區段，選取當內容標示為「轉換」時可用的選項。

* ****[!UICONTROL Confirm Trash]**** 啟用此選項，要求協調者在將內容設定為垃圾筒時確認其動作。啟用後，選擇內容的&#x200B;**[!UICONTROL Trash]**&#x200B;將顯示要求&#x200B;**[!UICONTROL Reason for Moderation]**&#x200B;的對話框，並提供可輸入&#x200B;**[!UICONTROL Note]**&#x200B;的欄位。

   （此設定在網路級別&#x200B;**[!UICONTROL only]**&#x200B;可用，並適用於您網路下的所有站點。）

* ****[!UICONTROL Hide Replies]**** 啟用此選項，可在父留言被刪除或Bozo被刪除時，自動將回覆刪除。

## 在ModQ {#section_tmw_lg1_z1b}中更改用戶狀態

按一下「用戶摘要」面板中的&#x200B;**[!UICONTROL User actions]**&#x200B;按鈕，將用戶靜音、禁止或允許列出。

* **[!UICONTROL Mute:]** 可讓您將標籤所列內容之使用者的「靜音旗標」。使用這個選項，可將使用者的旗標從您的預先協調篩選中排除。 他們標幟的內容不會因為標幟而進入ModQ，其標幟也不會包含在標幟規則中。
* **[!UICONTROL Ban:]** 允許您禁止列出的用戶訪問您的站點或網路。（只有Studio管理員或使用者管理員才能透過網路禁止使用者。）
* **[!UICONTROL Whitelist:]** 允許您列出您的站點或網路的列出用戶。（只有Studio管理員或使用者管理員才能透過網路允許列出使用者。）



使用ModQ的應用程式：

* [聊天室](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [意見](/help/using/c-about-apps/c-comments/c-comments.md)
* [評論](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Siesors](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [上傳按鈕](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

