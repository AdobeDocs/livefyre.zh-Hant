---
description: Livefyre垃圾郵件與濫用篩選引擎(Saupar Filter Engine，SAFE)是一種背景程序，可分析所有傳入內容，並為所有Livefyre客戶啓用。
seo-description: Livefyre垃圾郵件與濫用篩選引擎(Saupar Filter Engine，SAFE)是一種背景程序，可分析所有傳入內容，並為所有Livefyre客戶啓用。
seo-title: SAFE規則
title: SAFE規則
uuid: 2f91d0d4-dffe-4651-88af-79bbb96 c1 b5 c
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# SAFE規則{#safe-rules}

Livefyre垃圾郵件與濫用篩選引擎(Saupar Filter Engine，SAFE)是一種背景程序，可分析所有傳入內容，並為所有Livefyre客戶啓用。



SAFE使用模式規則以及統計模型來偵測垃圾郵件、濫用、褻瀆和大量(重復)貼文。您會在其他Livefyre產品中不時看到它，尤其是內容調節工具和ModQ。

>[!NOTE]
>
>SAFE僅提供英文版，但大量郵寄分類除外。如果您需要其他語言的支援，請聯絡您的策略帳戶管理員。

## 使用SAFE的Studio元件 {#section_k34_4tx_vy}

SAFE套用的旗標可與下列Studio元件搭配使用：

* 規則

   您可以定義SAFE規則以自動標幟內容並定義標幟內容應如何處理 **[!UICONTROL Network Settings]**。

   例如，網站可能會對Profanity造成非常低的容限，並定義SAFE規則，將所有標示為Propane的內容設為botzo'd'。其他網站可能會定義規則，在進入串流之前先預先協調Proane內容。

* ModQ

   您可以協調SAFE規則標幟的內容，以及其他預先協調規則(例如SPAM、褻瀆等)，在ModQ中。

* 資料庫中的應用程式內容

   SAFE標幟的內容會列在 **[!UICONTROL Library]** 索引標籤中的應用程式內容中。您可以依標幟篩選內容，以協調內容。

## 安全篩選選項 {#section_pg5_ttx_vy}

SAFE將下列標幟套用至篩選內容，並可用來建立規則並調節Livefyre Studio中的協調內容。

* **[!UICONTROL Profanity List]**：proane內容，由根據一般用途的英文關鍵字所定義。

   「嚴格篩選」會根據測試的字詞清單尋找褻瀆語言。如果偵測到，則會標幟內容。

   >[!NOTE]
   >
   >Livefyre也提供第二個「褻瀆清單」篩選器，您可以在「網站」和「網路」層級進行自訂。使用Profanity List建立的規則優先於來自SAFE Profanity篩選器的自動化規則。如需詳細資訊，請參閱設定文件中的「褻瀆清單」一節。

* **[!UICONTROL Mild Profanity]**：通常無法接受polite對話中的字詞和片語，但通常可用於隨意對話中。通常網路電視允許這些字詞和片語。
* **[!UICONTROL Strong Profanity]**：非常強穩的語言，例如網路電視上不允許的詞彙和片語，並可略過R評等影片和成熟的有線電視節目。一般而言，這些字詞不會用於流行對話或隨意對話中，且會出現在充滿影響力的對話中，意圖傷害聆聽者。
* **[!UICONTROL SPAM]**：未經請求，通常是商業內容。它使用依賴各種功能(包括註解內容和URL)的統計模型，將內容標幟為SPAM。您可以依要求調整垃圾郵件臨界值，自訂網路或網站的SPAM標記比率。
* **[!UICONTROL Mild Insult]**：孤立內容，由關鍵字和片語模式清單所定義。
* **[!UICONTROL Strong Insult]**：孤立內容，由關鍵字和片語模式清單所定義。
* **[!UICONTROL Hate Speech]**：基於性或宗教的侮辱，尤其是當目標群組隸屬於少數族群或受保護時。
* **[!UICONTROL ALL CAPS]**：所有大寫字母中顯示的文字(以yright為單位)。
* **[!UICONTROL Mild Threat]**：一種威脅或侮辱，通常包含某種輕微的粗魯導向。此選項會更常標示可能的威脅，但的誤判率也高於 **[!UICONTROL Strong Threat]**。

* **[!UICONTROL Strong Threat]**：對一位或多人造成嚴重傷害的嚴重威脅或侮辱，通常具有強烈的褻瀆性。此選項會較少提及可能的威脅，但其誤報率也較 **[!UICONTROL Mild Threat]**低。

* **[!UICONTROL Probable Nudity]**：其中可能含有虛名的影像。此選項的匿名度較低，但其誤報率 **[!UICONTROL Possible Nudity]**也較低。

* **[!UICONTROL Possible Nudity]**：其中可能含有虛名的影像。此選項會更常提及虛度，但也會比以前更高的誤報率 **[!UICONTROL Probable Nudity]**。

* **[!UICONTROL PII]** (可識別個人身分資訊)：可識別使用者的資訊。其中包括電子郵件地址、實體地址、社交安全號碼(供美國客戶使用)、信用卡號碼、密碼或任何可用於詐欺或取得某人身分的任何項目。
* **[!UICONTROL Livefyre Recommends Trash]**. 設定當自動協調建議識別拒絕內容時，系統執行的動作。 ![](assets/mod_reco1.png)

   >[!NOTE]
   >
   >若要開啓「協調建議」，請聯絡您的Adobe Livefyre支援專業人員。

## 處理未被SAFE擷取的內容 {#section_pjy_5tx_vy}

有幾種方法可有效處理此篩選器未擷取到的內容。以下選項會列在建議的程序順序中。

1. 做為協調者，移除串流中的內容。
1. 建立「標記規則」，表示如果某個內容被五個使用者標幟為垃圾訊息或冒犯性內容，將其設為Botzo。
1. 禁止張貼不需要內容的使用者，讓他們的所有內容直接進入Botzo狀態。
1. 新增應一律篩選至您的粗俗清單的特定字詞。

>[!NOTE]
>
>如果協調者貼文內容被「垃圾郵件篩選」所捕獲，則仍會標示為垃圾郵件，但會自動「核准」，且不會設為「波佐」。

如果您注意到未被SAFE發現的內容趨勢或模式，請使用注釋ID和文字來電子郵件。



使用此功能的應用程式：

* [轉盤](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [聊天室](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [注釋](/help/using/c-about-apps/c-comments/c-comments.md)
* [功能卡](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [地圖](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaic](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [評論](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sitents](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [上傳按鈕](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

