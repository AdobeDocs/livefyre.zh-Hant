---
description: Livefyre垃圾訊息和濫用篩選引擎(SAFE)是分析所有傳入內容的背景程式，已針對所有Livefyre客戶啟用。
seo-description: Livefyre垃圾訊息和濫用篩選引擎(SAFE)是分析所有傳入內容的背景程式，已針對所有Livefyre客戶啟用。
seo-title: 安全規則
title: 安全規則
uuid: 2f91d0d4-dffe-4651-88af-79bbb96c1b5c
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '885'
ht-degree: 0%

---


# SAFE規則{#safe-rules}

Livefyre垃圾訊息和濫用篩選引擎(SAFE)是分析所有傳入內容的背景程式，已針對所有Livefyre客戶啟用。



SAFE使用模式規則和統計模型來偵測垃圾訊息、濫用、褻瀆和大量（重複）貼文。 您會在其他Livefyre產品中不時看到它，尤其是內容協調工具和ModQ。

>[!NOTE]
>
>SAFE僅提供英文版，但大量郵寄分類除外。 如果您需要其他語言的支援，請連絡您的策略客戶經理。

## 使用SAFE {#section_k34_4tx_vy}的Studio元件

SAFE所套用的標幟可與下列Studio元件搭配使用：

* 規則

   您可以定義SAFE規則，以自動標幟內容，並定義在&#x200B;**[!UICONTROL Network Settings]**&#x200B;中如何處理標幟內容。

   例如，網站可能會設定Profanity的低容忍度，並定義SAFE規則，將所有標幟為Profane的內容設定為Bozo』d。其他網站可定義規則，規則會在輸入串流前，先將Profane內容設定為預先協調。

* ModQ

   您可以在ModQ中協調由SAFE規則和其他預先協調規則（例如，SPAM、profity等）標幟的內容。

* 資料庫中的應用程式內容

   由SAFE標幟的內容會列在&#x200B;**[!UICONTROL Library]**&#x200B;標籤的「應用程式內容」中。 您可以依標幟篩選內容，以協調內容。

## SAFE過濾器選項{#section_pg5_ttx_vy}

SAFE會將下列標幟套用至篩選的內容，並可用於從Livefyre Studio中建立規則和協調內容。

* **[!UICONTROL Profanity List]**:Profane內容，如英文關鍵字清單所定義，以常用為基礎。

   「粗體篩選」會根據經測試的字詞清單來尋找粗體語言。 如果偵測到，內容會標幟為Profane。

   >[!NOTE]
   >
   >Livefyre也提供第二個「Profity List」篩選器，您可在「網站」和「網路」層級自訂。 使用「檔案清單」建立的規則優先於「SAFE檔案清單」篩選器所產生的自動化規則。 如需詳細資訊，請參閱「設定」檔案中的「Profity List」一節。

* **[!UICONTROL Mild Profanity]**:在禮貌的交談中，通常不能接受詞語和短語，但在閒聊中，通常可以接受。一般來說，這些字詞和片語是允許在網路電視上播放的。
* **[!UICONTROL Strong Profanity]**:非常強的語言，例如網路電視上不允許的俗語和片語，在R級電影和成熟的有線電視節目中也很少使用。通常，這些詞不會用在禮貌或隨意的交談中，而是在不禮貌的交談中說，目的是傷害聽眾。
* **[!UICONTROL SPAM]**:未經請求，通常是商業內容。它使用依賴多種功能（包括註解內容和URL）的統計模型，將內容標幟為SPAM。 您可以根據請求調整垃圾郵件閾值以自定義網路或站點的垃圾郵件標籤率。
* **[!UICONTROL Mild Insult]**:侮辱性內容，由關鍵字和片語模式清單定義。
* **[!UICONTROL Strong Insult]**:侮辱性內容，由關鍵字和片語模式清單定義。
* **[!UICONTROL Hate Speech]**:基於種族或宗教的侮辱，特別是當目標群體屬於少數或受保護時。
* **[!UICONTROL ALL CAPS]**:以所有大寫字母（讀作吼叫）呈現的案文。
* **[!UICONTROL Mild Threat]**:這種威脅或侮辱通常包括對他人的輕度褻瀆。此選項會更常標籤可能的威脅，但假陽性率也高於&#x200B;**[!UICONTROL Strong Threat]**。

* **[!UICONTROL Strong Threat]**:一種嚴重威脅或侮辱，提到對一個或多個人可採取行動的人身傷害，這種傷害往往帶有強烈的褻瀆。此選項標籤可能威脅的頻率較低，但誤報率也低於&#x200B;**[!UICONTROL Mild Threat]**。

* **[!UICONTROL Probable Nudity]**:可能有裸體的影像。此選項會較少標示裸度，但假陽性率也比&#x200B;**[!UICONTROL Possible Nudity]**&#x200B;低。

* **[!UICONTROL Possible Nudity]**:可能有裸體的影像。此選項會更常標示裸度，但假陽性率也高於&#x200B;**[!UICONTROL Probable Nudity]**。

* **[!UICONTROL PII]** （個人識別資訊）:可識別使用者的資訊。這可能包括電子郵件地址、實體地址、社交安全號碼（針對美國客戶）、信用卡號碼、密碼，或可用於詐騙或取得某人身分的任何資訊。
* **[!UICONTROL Livefyre Recommends Trash]**。設定當自動協調建議識別要拒絕的內容時系統所執行的動作。 ![](assets/mod_reco1.png)

   >[!NOTE]
   >
   >若要開啟「協調建議」，請連絡您的Adobe Livefyre支援專業人員。

## 處理SAFE {#section_pjy_5tx_vy}未捕獲的內容

有數種方法可有效處理未被此篩選器擷取的內容。 以下選項依建議的程式順序列出。

1. 身為協調者，從串流移除內容。
1. 建立標幟規則，指出如果有五個使用者將某個內容標幟為「垃圾訊息」或「冒犯性」，請將其設為Bozo。
1. 禁止張貼不想要內容的使用者，因此其所有內容都會直接進入Bozo狀態。
1. 將應一律篩選的特定字詞新增至您的粗細清單。

>[!NOTE]
>
>如果協調者張貼被我們的垃圾訊息篩選器擷取的內容，該內容仍會標幟為垃圾訊息，但會自動「核准」，且不會設為Bozo。

如果您注意到SAFE未捕捉到的內容趨勢或模式，請以注釋ID和文字寄送電子郵件給您的CSM。



使用此功能的應用程式：

* [轉盤](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [聊天室](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [意見](/help/using/c-about-apps/c-comments/c-comments.md)
* [功能卡](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [地圖](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [媒體牆](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [馬賽克](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [評論](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Siesors](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [上傳按鈕](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

