---
description: 透過單一智慧型介面協調內容。
seo-description: 透過單一智慧型介面協調內容。
seo-title: 使用ModQ協調內容
title: 使用ModQ協調內容
uuid: c630fb85-7bd0-4da0-ac7 e-080e970 fb4 f9
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 使用ModQ協調內容{#moderate-content-using-modq}

透過單一智慧型介面協調內容。

ModQ會建立網站或網路上所有符合您定義之預先調節規則的內容的即時佇列，讓協調者只關注需要注意的內容。

定義ModQ設定後，進入串流的新內容或使用者標幟的現有內容將會新增至您的佇列。規則變更不會從ModQ移除內容，但會根據新設定新增內容至佇列。

ModQ可讓您：

* 只要按一下滑鼠，就能在內容中協調、檢視整個執行緒，以及核准、垃圾桶或Botzo，或完成個別的內容。
* 提高工作流程的速度和效率。
* 回覆內容，提高您對社群的參與程度。
* 讓多個協調者可透過內容工作，而不會重復彼此的工作。

Livefyre內容在ModQ中列示長達周，且未解決的預先調節串流內容會在ModQ中列示90天。

>[!NOTE]
>
>如果單一內容符合多個規則以納入ModQ，則可多次列出內容。例如，如果某一部分內容觸發了使用者標幟規則，則稍後觸發另一個Propane規則，它會以兩次列出。

未以ModQ顯示的內容包括：

* 已損毀內容。
* 協調者核准的內容。
* 由受禁止使用者張貼的內容，或被禁止使用者所套用的使用者標幟。

## 導覽ModQ {#section_uv4_db2_yy}

ModQ會分割為兩個標籤式面板：

* **[!UICONTROL Items]** 列出所有Livefyre-native和SocialSync內容，以便調節。此標籤包含任何已在協調後標示或編輯的Social Search或stream內容。
* **[!UICONTROL Streams Premoderation]** 列出所有在「串流」啓用「預覽」的內容。(如需詳細資訊，請參閱「建立串流」)。

這兩個標籤提供許多相同的篩選器和協調工具。

* **[!UICONTROL Item Count]** 佇列中剩餘項目的數量會顯示在ModQ的左上角。
* **[!UICONTROL Filter]** 按一下 **[!UICONTROL Filter]** 以定義內容會列在窗格中的參數。
* **[!UICONTROL History]** 按一下畫面右上方的 **[!UICONTROL History]** 按鈕，開啓最近協調的內容清單，讓您檢閱工作，或變更最近的協調動作。再次按一下按鈕，返回您的佇列內容。只會顯示100個最近的動作。**歷史記錄** 不會列出其他協調者採取的動作。

* **[!UICONTROL User Pane]** 按一下頁面右上角的展開或收合按鈕，以開啓或關閉「使用者」窗格。

## 瞭解ModQ內容 {#section_oxm_kgz_y1b}

每個列出的內容片段會顯示預覽資訊，包括張貼的網站及其作者。選取項目會顯示包含任何媒體的整個內容。

>[!NOTE]
>
>Livefyre原生內容會顯示比透過串流或其他社交媒體來源新增至您應用程式的內容更多資訊。

選取項目時，會顯示下列資訊：

* **[!UICONTROL Time in Queue:]** 列出內容新增至ModQ的時間長度。
* **[!UICONTROL App name:]** 內容顯示的應用程式。應用程式的網站連結。
* **[!UICONTROL Content Body:]** 文字和媒體縮圖(如果有的話)。
* **[!UICONTROL Status:]** 內容的目前狀態(擱置中、垃圾訊息等)。
* **[!UICONTROL Author information:]** 作者的名稱和使用者名稱。
* **[!UICONTROL Timestamp:]** 建立內容時的相對時間戳記。永久連結至Studio「應用程式內容」頁面中的內容片段。
* **[!UICONTROL Flag Type:]** 侵犯性、不同意、垃圾郵件等

   * SAFE標幟：垃圾訊息和大量訊息。
   * 您的網路和網站褻瀆度清單所套用的旗標：褻瀆。
   * SAFE套用標幟：仇恨言論、PII(個人身分識別資訊)、侮辱和褻瀆。
   * 使用者標幟：垃圾郵件、非主題、進攻性及不同意。

* **[!UICONTROL Flag origin:]** 列出的標幟來源。可以是SAFE、使用者名稱或Livefyre。
* **[!UICONTROL More info:]** 列出內容的詳細資料，包括按贊次數、使用者標幟、回覆及任何套用至內容的標記。按一下「網站」會開啓內容所在網站的頂層頁面。按一下時間戳記會開啓頁面內容中內容的串連檢視。

## ModQ中的篩選選項 {#section_r2c_qc2_yy}

按一下 **[!UICONTROL Filter]** ModQ視窗左上方的按一下，開啓具備可用篩選選項的面板內容。當您選取選項時，ModQ會自動更新，只列出您的篩選內容。按一下 **[!UICONTROL Clear filters]** 以清除所有選取的選項，然後重新載入完整的項目清單。

不同的篩選選項適用於 **[!UICONTROL Items]** 和 **[!UICONTROL Streams Premoderation]** 標籤。

The following options are available for the ModQ under both **[!UICONTROL Items]** and **[!UICONTROL Streams Premoderation]** :

* **[!UICONTROL App]**. 使用「搜尋應用程式」欄位，依應用程式篩選結果。可能會選取多個應用程式。
* **[!UICONTROL System Flags]**. 依垃圾訊息、褻瀆、SAFE和「預覽」規則等規則來篩選內容。

   * Selecting **[!UICONTROL Spam]** will list all content taged as spam by SAFE.
   * Selecting **[!UICONTROL Profanity]** will list all content taged propane by your Network or Site Profanity List.
   * 選取此 **[!UICONTROL SAFE]** 選項會列出由於您的SAFE規則而輸入ModQ的所有內容。
   * Selecting **[!UICONTROL Premoderation]** will list all content taged for Premiere by your Network，Stream or App Settings.

* **[!UICONTROL User Flags]** 依使用者標幟篩選內容。選項包括冒犯、垃圾訊息、關閉主題及不同意。
* **[!UICONTROL Rights Requests.]** 按一下核取方塊，只顯示具有授予權限的內容。
* **[!UICONTROL Entered the queue.]** 依據內容傳送至ModQ期間的時間範圍篩選內容。傳送內容至ModQ的時間不一定是張貼至應用程式的時間。

以下是ModQ下方 **[!UICONTROL Streams Premoderation]** 的可用選項：

* **[!UICONTROL Social Source]** 依據內容來源的社交來源篩選內容。例如，社交來源的選項包括Twitter、Instagram、Facebook和RSS。

下列選項適用於ModQ下方 **[!UICONTROL Items]** ：

**[!UICONTROL Moderation Recommendations]**. 依據自動化協調建議提供的建議篩選內容。

下列影像顯示Moderation Recommendations在ModQ中的外觀： ![](assets/mod_reco1.png)

在內容設定 **[!UICONTROL Network Settings > Moderation]** 時，會為內容提供協調建議 **[!UICONTROL Network Settings > ModQ]**。

## 您可以在ModQ中使用的動作 {#section_h4g_wrn_z1b}

您可以決定如何使用ModQ中的每一段內容。

選取下列其中一個選項：

* 核准內容 **[!UICONTROL Checkbox]** 的圖示
* 將內容傳送至垃圾筒 **[!UICONTROL Trash can]** 的圖示
* **[!UICONTROL Request Rights]** 向內容擁有者請求內容的權利。

   >[!NOTE]
   >
   >您無法從Instagram取得內容的ModQ權限。您必須使用「資料庫」或「應用程式內容」來傳送Instagram內容的權限要求。

* **[!UICONTROL Feature and Approve]** 來核准內容，而且也包含內容片段。
* **[!UICONTROL Product Tag and Approve]** 將產品從您的產品目錄新增至內容，然後核准它。
* **[!UICONTROL Mark as Pending]** 將內容標示為待定。

>[!NOTE]
>
>當您將內容刪除後，內容部分和所有對內容的回覆都會永久從ModQ中移除。若要將雜湊內容放入應用程式中，請參閱 [「將已損毀項目新增至應用程式](/help/using/c-features-livefyre/c-about-moderation/t-add-trashed-item-back-into-app.md#t_add_trashed_item_back_into_app)」。

如果內容已處於所需狀態，則選擇「垃圾筒」、「波佐」或「核准」，將會確認狀態並移除清單中的項目。協調內容片段會立即將它從佇列中移除，並將它停用於其他協調者的佇列中。

>[!NOTE]
>
>串流內容可能不是Botzo'd。垃圾串流內容會永久將它從串流移除，且無法復原。

協調內容後，將會從協調者的ModQ中移除，其作者無法再從串流中編輯內容。如果協調者關閉項目，或是使用者刪除了他們的注釋，則會即時在其他協調者的佇列中呈現灰色。當內容變灰時 **[!UICONTROL Clear Moderated]**，按鈕會顯示在頁面上，讓協調者從清單中移除它，並維持其位置，不論其他協調者活動為何。

## 在ModQ中使用垃圾筒函數 {#section_tpx_qgz_y1b}

當內容標示為「已銷毀」時，使用設定區段可選取可用選項。

* ****[!UICONTROL Confirm Trash]** ** 啓用此選項，可要求協調者在將內容設定為垃圾筒時確認其動作。啓用後，選取 **[!UICONTROL Trash]** 內容會顯示對話方塊的對話方塊 **[!UICONTROL Reason for Moderation]**，並提供可能輸入的 **[!UICONTROL Note]** 欄位。

   (此設定適用於 **[!UICONTROL only]** 網路層級，並適用於您網路下的所有網站)。

* ****[!UICONTROL Hide Replies]** ** 啓用此選項，可在父項留言被毀壞或Botzo'd時自動垃圾回覆。

## 變更ModQ中的使用者狀態 {#section_tmw_lg1_z1b}

從「User Summary」(使用者摘要)面板中，按一下 **[!UICONTROL User actions]** 「User Summary」(使用者摘要)面板中的按鈕，或「Whitelist」(使用者名單)。

* **[!UICONTROL Mute:]** 可讓您從標幟該內容片段的使用者進行Mute標幟。使用此選項可排除您的預先協調篩選器中的使用者標幟。由於標幟的緣故，他們標幟的內容不會輸入ModQ，標幟將不會包含在旗標規則中。
* **[!UICONTROL Ban:]** 允許您從網站或網路禁止所列使用者。(只有Studio管理員或使用者經理才能禁止使用者使用網路。)
* **[!UICONTROL Whitelist:]** 可讓您為您的網站或網路列入白名單。(只有Studio管理員或使用者經理才能將使用者列入網路名單)。



使用ModQ的應用程式：

* [聊天室](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [注釋](/help/using/c-about-apps/c-comments/c-comments.md)
* [評論](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sitents](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [上傳按鈕](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

