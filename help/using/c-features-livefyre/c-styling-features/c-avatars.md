---
description: 允許使用者自訂與其內容一起顯示的影像。
title: Avatars
exl-id: cff7f6be-3660-4d71-949b-6ac04379d68d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---

# Avatars{#avatars}

允許使用者自訂與其內容一起顯示的影像。

使用者變數會（依預設）顯示在所有應用程式中的內容旁，並從您實作中使用的識別描述檔系統提取。 這些變數會根據顯示在其中的應用程式而有所不同。

（如果您不想在應用程式中顯示Avatar,Livefyre可讓您停用Avatar。）

>[!NOTE]
>
>「聊天」的Avatar顯示為25p x 25p，而其他大部分的「應用程式」則顯示為50p x 50p。

## 頭像儲存{#section_zbh_x1f_wy}

Livefyre會以非同步方式載入Avatar。 當使用者第一次登入應用程式或變更其相關的頭像影像檔案時，他們的設定檔影像會新增至工作佇列。 （當使用者上傳至Livefyre頭像儲存位置時，會暫時顯示預設頭像。）

## 凹版{#section_mqh_p1f_wy}

Livefyre支援Gravatars的使用。 如果使用者的使用者設定檔中沒有自訂頭像，Livefyre會檢查該使用者的Gravatar。 如果沒有Gravatar，則會使用預設頭像。


使用此功能的應用程式：

* [轉盤](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [聊天室](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [意見](/help/using/c-about-apps/c-comments/c-comments.md)
* [功能卡](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [地圖](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [媒體牆](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [馬賽克](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [評論](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
