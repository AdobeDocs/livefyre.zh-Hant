---
description: 監聽器計數是追蹤頁面上應用程式的網站訪客數並顯示此數目的計數器。
title: 監聽器計數
exl-id: a07e83c2-7465-42ec-9d24-821aac5ab74b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---

# 監聽器計數{#listener-count}

監聽器計數是追蹤頁面上應用程式的網站訪客數並顯示此數目的計數器。

「監聽器計數」是指瀏覽器開啟至應用程式執行個體化之頁面的網站訪客數。 這可讓您隨時得知頁面上有多少網站訪客，以便在他們即時檢視串流或即時內容時追蹤他們。

Livefyre的監聽器計數的運作方式如下：

1. 包含您應用程式的網站每60秒ping一次Livefyre伺服器。
1. Livefyre伺服器會回應顯示應用程式之頁面上的網站訪客數量（定義為該頁面有瀏覽器開啟的網站訪客數量）。
1. 頁面上含有應用程式的網站訪客數，會顯示在應用程式上。

使用此功能的應用程式：

* [聊天室](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [意見](/help/using/c-about-apps/c-comments/c-comments.md)
* [評論](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

## 監聽器Avatars {#section_wcn_kxp_vz}

監聽器計數最多顯示10個頭像，並且僅顯示對話的&#x200B;**[!UICONTROL Follow]**&#x200B;點擊者的頭像。

>[!NOTE]
>
>由於空間限制，行動介面只會顯示聆聽器數目，並顯示一個小「人員」圖示。

「Livefyre監聽器計數」會顯示頁面上任何指定時間的活躍訪客人數，以及對話後的訪客人數。 如果有人在頁面上並關注對話，則不會重複計算該使用者。 例如，如果使用者在頁面上按一下&#x200B;**[!UICONTROL Follow]**，監聽器計數不會增加；如果該使用者接著按一下&#x200B;**[!UICONTROL Unfollow]**，計數不會減少。

使用此功能的應用程式：

* [聊天室](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [意見](/help/using/c-about-apps/c-comments/c-comments.md)
* [評論](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](../c-about-apps/c-storify2/c-storify2.md#c_storify2)
