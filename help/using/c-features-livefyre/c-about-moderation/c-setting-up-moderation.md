---
description: 使用「協調」標籤來設定傳入內容的預先協調規則，包括褻瀆清單、標幟規則和禁止的IP位址。
seo-description: 使用「協調」標籤來設定傳入內容的預先協調規則，包括褻瀆清單、標幟規則和禁止的IP位址。
seo-title: 設定協調
solution: Experience Manager
title: 設定協調
uuid: 0ec53fdb-08c2-4058-88cb-2f6f4b56a95b
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 設定協調{#setting-up-moderation}

使用「協調」標籤來設定傳入內容的預先協調規則，包括褻瀆清單、標幟規則和禁止的IP位址。

## 協調如何運作 {#section_kyf_gvc_t1b}

您可以透過下列方式協調內容：

* 根據您在發佈內容之前設定的規則，自動調節內容，以篩選不想要的內容。
* 使用程式庫中的ModQ或應用程式內容，手動刪除或核准已標記為標記的內容。
* 識別會重復張貼有攻擊性內容的網站訪客，讓他們避開特定Livefyre使用者、社交使用者或IP位址，以免張貼。
* 識別可透過白名單使用者或關閉特定串流、網站或網路篩選的人員和內容。

您可以透過下列方式自動調節內容：

* 設定規則以自動標幟特定類型的內容：

   * 設定網站訪客標幟標幟的內容標幟規則 **[!UICONTROL Settings > Moderation > Rules]**
   * 使用 **[!UICONTROL Settings > Moderation > Rules]**
   * 禁止使用特定Twitter使用者 **[!UICONTROL Settings > Streams]**
   * 禁止使用IP位址 **[!UICONTROL Settings > Bans]**
   * 依要求依國家/地區代碼禁止IP地區。禁止的內容將標示為SPAM。

* 在您的網路或網站下 **[!UICONTROL Settings > Moderation > Rules]** ，建立您認為褻瀆性清單中褻瀆之字詞清單。
* 白名單使用者(一律允許來自這些使用者的內容)使用或關閉特定串流、網站或網路的篩選。

在您設定好粗俗清單、SAFE篩選器和規則之後，您可以選擇是否要預先調節內容，並將SAFE篩選器套用在串流中。如需詳細資訊，請參閱 [所有串流規則的串流規則選項](/help/using/c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。

Livefyre標記內容， **[!UICONTROL Approved]****[!UICONTROL Pending]**等 **[!UICONTROL Junk]**。取決於內容所在位置、內容的發佈位置，以及您在系統中設定的規則。下表說明Livefyre採取的動作，具體取決於這些因素。

## 協調如何運作

| 內容來自： | 傳送內容至： | 核准狀態 |
|--- |--- |--- |
| Library | 應用程式 | 核准內容 |
| 社交搜尋 | 應用程式 | 核准內容 |
| 串流規則 | 應用程式 | 內容標示為「Junk by SAFE篩選」嗎？ <br><ul><li>否-串流至應用程式協調工作流程</li><li>是-內容已損毀</li></ul> |
| Library | 資料夾 | 無狀態(資料夾中未發佈，未發佈) |
| 社交搜尋 | 資料夾 | 無狀態(資料夾中未發佈，未發佈) |
| 串流規則 | 資料夾 | 內容標示為「Junk by SAFE篩選」嗎？ <br><ul><li>否-無狀態(位於資料夾中，未發佈，未被破壞)</li><li>是-內容已損毀</li></ul> |
| 應用程式貼文 | 應用程式 | 內容標示為「Junk by SAFE篩選」嗎？ <br><ul><li>否-應用程式後協調工作流程</li><li>是-內容已損毀</li></ul> |

## 串流至應用程式協調工作流程 {#section_z5z_w4d_t1b}

![](assets/stream_to_app_workflow.png)

「串流」的內容發佈至應用程式之前，Livefyre會執行下列檢查以判斷內容的用途：

1. 如果SAFE將內容標示為垃圾郵件或下落，Livefyre會捨棄內容。
1. 如果SAFE並未將內容標示為垃圾訊息，Livefyre會檢查是否有預備。
1. 如果預備開啓，Livefyre將會標記內容為擱置中。
1. 如果您設定ModQ規則，Livefyre會將內容傳送至ModQ。
1. 如果未開啓預備，Livefyre會檢查SAFE是否標幟內容。
1. 如果SAFE標幟內容，Livefyre會核准內容並將內容重新整理至應用程式。
1. 如果SAFE標幟內容，但您未設定SAFE規則，則Livefyre會核准內容並將內容重新整理至應用程式。
1. 如果SAFE標幟內容並設定SAFE規則，Livefyre會檢查您是否為串流設定了SAFE規則。
1. 如果您為串流設定SAFE規則，Livefyre會核准內容並將內容重新整理至應用程式。如果您未設定串流的SAFE規則，Livefyre會使用協調SAFE規則判斷如何處理內容(傳送至ModQ、垃圾筒等)。

## 應用程式後協調工作流程 {#section_fwn_w4d_t1b}

![](assets/post_to_app_workflow.png)

在應用程式貼文的內容發佈至應用程式之前，Livefyre會執行下列檢查以判斷內容的用途：

1. 如果SAFE篩選器將內容標示為下落，Livefyre會捨棄內容。
1. 如果SAFE不會將內容標示為下降，Livefyre會檢查是否有預備。如果預備開啓，Livefyre將會標記內容為擱置中。如果您設定ModQ規則，Livefyre將會將內容傳送至ModQ擱置中。如果沒有，內容會保留在程式庫中應用程式內容中的擱置狀態中。
1. 如果未開啓預備，Livefyre會檢查SAFE是否標幟內容。如果沒有，Livefyre會核准內容並將內容重新整理至應用程式。
1. 如果SAFE標幟內容，並設定SAFE規則，Livefyre會使用SAFE規則判斷如何處理內容(傳送至ModQ、垃圾筒等)。如果SAFE標幟內容，但您未設定SAFE規則，則Livefyre會核准內容並將內容重新整理至應用程式。

## 大量篩選 {#section_lyk_ktx_vy}

「大量篩選」會在短時間範圍內尋找張貼在所有Livefyre網路上的重復內容。如果偵測到此內容，則會將此內容標示為「大量」，然後依預設進行損毀。雖然批量內容可能是使用者產生的(例如「TouchDown！」在熱門足球遊戲中重復張貼，大部分是使用垃圾郵件宣傳。此篩選器不受語言影響，而且適用於任何語言。若要自訂批量篩選，您必須聯絡Livefyre支援。

## 規則 {#section_gqz_ksk_f1b}

使用「規則」區段，根據SAFE和使用者套用的旗標建立預先協調規則。此面板提供兩種規則：

* **[!UICONTROL Flag Rules:]** 指定應在使用者標幟的注釋上執行的動作。
* ****[!UICONTROL SAFE Rules:]結合SAFE標幟與採取標幟內容的動作。

若要建立「標幟規則」，請選取標幟(冒犯性、關閉主題、不同意或垃圾訊息)，輸入必須套用至內容片段的次數，並選取要採取的動作。您可以為每個旗標選項(「進攻」、「關閉主題」、「不同意」或「垃圾郵件」)設定一個「旗標規則」。

您可以在「網路」、「網站」和「串流」層級建立規則。除非您設定網站規則，否則網站層級規則繼承網路規則。串流規則繼承網站規則，除非您設定不同。

可用動作：

* ****[!UICONTROL Trash it:]將標幟的註解傳送至垃圾筒。
* **[!UICONTROL Bozo it:]** 隱藏所有使用者的標幟留言，但其作者除外，但其作者除外。
* **[!UICONTROL Pending:]** 將內容設為擱置中。如果您將「預覽」設定為「開啓」， **[!UICONTROL Settings > ModQ]**則它會位於ModQ中。否則，它只會位於「應用程式內容」中。

>[!NOTE]
>
>Livefyre建議您建立規則至由五名使用者標幟為垃圾郵件或冒犯性的Bozo注釋。

## 協調建議 {#section_ec3_vr3_2cb}

您可以使用協調建議來幫助您決定如何協調Livefyre應用程式中網站訪客張貼的內容。「協調建議指示符」會根據您先前在類似內容上採取的動作，建議您將內容毀損。若要使用協調建議：

1. 聯絡您的Adobe Livefyre支援專業人員，開啓「協調建議」功能。
1. 在「網路設定」中設定協調建議。

   使用下一個 **[!UICONTROL Livefyre Recommends Trash]** 設定設定協調建議 **[!UICONTROL Network Settings]**。

   ![](assets/image_mod_reco_trash.png)

1. 設定SAFE規則，告知Livefyre如何處理協調建議識別為可能被毀壞內容的內容。如需如何設定 **[!UICONTROL Livefyre Recommends Trash]** 選項的SAFE規則的詳細資訊，請參閱 [「協調](/help/using/c-features-livefyre/c-about-moderation/c-moderation.md#c_moderation)」。

   ![](assets/modreco4.png)

1. 使用ModQ或應用程式內容 **[!UICONTROL Moderation Recommendation Indicator]** 中的篩選內容來篩選協調建議識別可能被毀壞的內容。

   在ModQ中，指標看起來就像這樣： ![](assets/mod_reco1.png)

   如需如何使用Moderation Recommendations協調ModQ內容的詳細資訊，請參閱 [ModQ](/help/using/c-features-livefyre/c-about-moderation/c-modq.md#c_modq)。

   在應用程式內容中，協調建議類似於： ![](assets/modreco3.png)

   如需如何在應用程式內容中使用協調建議的詳細資訊，請參閱 [「使用應用程式內容協調內容](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content)」。
