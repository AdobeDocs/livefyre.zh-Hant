---
description: 將您的內容或內容從其他使用者分享到Facebook、Twitter或LinkedIn。
seo-description: 將您的內容或內容從其他使用者分享到Facebook、Twitter或LinkedIn。
seo-title: 社交分享
solution: Experience Manager
title: 社交分享
uuid: 3fd8a628-2414-45b5-b91c-2ad33aad2634
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 1%

---


# 社交分享{#social-sharing}

將您的內容或內容從其他使用者分享到Facebook、Twitter或LinkedIn。

社交分享可讓您的社群在社交網路（包括Facebook、Twitter和LinkedIn）上，將他們從您的應用程式分享想法給朋友，並將其他使用者的內容分享到Facebook和Twitter。 啟用社交共用功能可讓您的社群將最佳回應散布至您的內容，並為您的網站帶來更多流量。

## 將內容分享至社交網路{#section_t1q_mz2_wy}

您可以設定您的網路，讓使用者在將內容張貼到您的Livefyre應用程式時，能夠分享到Twitter、Facebook或LinkedIn。 預設的Livefyre **[!UICONTROL Share Modal]**&#x200B;包含所有三個網站的連結。 您可以使用「貼文至API」自訂此模式，以覆寫Livefyre預設值，並實作您自己的模式。 如需詳細資訊，請參閱進階主題>啟用社交共用。

當使用者按一下&#x200B;**[!UICONTROL Share]**&#x200B;將其留言張貼至社交網路（Facebook、Twitter或LinkedIn）時，會提示他們透過社交應用程式登入。 購股權清單可予自訂。 依預設，Facebook和Twitter共用核取方塊會顯示在所有應用程式上。) 對於自訂網路，社交應用程式應設定為您的社交應用程式。 在整合程式中，透過Studio的「整合設定」頁面新增您的應用程式認證。

>[!NOTE]
>
>Livefyre社群注釋預設會包含LinkedIn。 自訂網路在內嵌應用程式時，必須傳入「li」值，才能在注釋工具列上啟用LinkedIn按鈕。 （如需詳細資訊，請參閱開發人員檔案中的啟用社交共用功能。）

## 將其他使用者的內容分享至社交網路{#section_blw_vy2_wy}

按一下其他使用者貼文上的&#x200B;**[!UICONTROL Share]**&#x200B;會開啟「分享留言」窗格，其中包含可編輯的文字欄位、您已啟用的分享選項，以及貼文的永久連結。

按一下&#x200B;**[!UICONTROL Share]**&#x200B;貼文：

* 使用者可以按一下Twitter或Facebook圖示，連線至其社交網路。
* 授權頁面張貼至使用者的社交網路後，Twitter或Facebook按鈕會亮起，讓使用者知道這些按鈕處於作用中。
* 使用者可以個人化分享貼文方塊中的內容。
* 按一下&#x200B;**[!UICONTROL Share]**&#x200B;會傳送內容至使用者的作用中社交網路，並附上連結，讓其他人前往使用者想要分享的確切貼文。
* 使用者也可以選擇將Permalink貼在電子郵件、部落格貼文或社交網路中，以分享特定留言的連結。

>[!NOTE]
>
>在整合期間，您可以決定哪些社交網路可供您的使用者共用。 您也可以整合自訂的Permalink，以便與目前的媒體連結保持一致。

按一下其他使用者貼文上的&#x200B;**[!UICONTROL Share]**&#x200B;會開啟&#x200B;**[!UICONTROL Share Comment]**&#x200B;窗格，其中包含可編輯的文字欄位、您已啟用的共用選項，以及貼文的永久連結。

按一下&#x200B;**[!UICONTROL Share]**&#x200B;貼文：

* 使用者可以按一下Twitter或Facebook圖示，連線至其社交網路。
* 授權頁面張貼至使用者的社交網路後，Twitter或Facebook按鈕會亮起，讓使用者知道這些按鈕處於作用中。
* 使用者可以個人化分享貼文方塊中的內容。
* 按一下&#x200B;**[!UICONTROL Share]**&#x200B;會傳送內容至使用者的作用中社交網路，並附上連結，讓其他人前往使用者想要分享的確切貼文。
* 使用者也可以選擇將Permalink貼在電子郵件、部落格貼文或社交網路中，以分享特定留言的連結。

>[!NOTE]
>
>在整合期間，您可以決定哪些社交網路可供您的使用者共用。 您也可以整合自訂的Permalink，以便與目前的媒體連結保持一致。



使用此功能的應用程式：

* [轉盤](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [聊天室](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [意見](/help/using/c-about-apps/c-comments/c-comments.md)
* [功能卡](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [地圖](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [媒體牆](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [馬賽克](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [民調](/help/using/c-about-apps/c-polls-app/c-polls-app.md#c_polls_app)
* [評論](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Siesors](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [趨勢分析](/help/using/c-about-apps/c-trending-app/c-trending-app.md#c_trending_app)

