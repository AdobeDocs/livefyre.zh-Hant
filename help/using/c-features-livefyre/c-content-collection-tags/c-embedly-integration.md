---
description: 直接在應用程式中使用 embed.ly 顯示多種媒體格式。
seo-description: 直接在應用程式中使用 embed.ly 顯示多種媒體格式。
seo-title: Embedly 整合
solution: Experience Manager
title: Embedly 整合
uuid: 1f27e32c-c2c3-4f7c-93de-c9c7bf783d6a
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# Embedly 整合{#embedly-integration}

Use `embed.ly` to display multiple media formats, directly in the App.

為了更好地啟用來自多種來源的內嵌媒體內容，包括Google地圖、YouTube、Flickr、Facebook、Instagram、Spotify和Tumblr,Livefyre Apps使用Embedly做為URL擴充的協力廠商提供者。 如果使用者或協調者在貼文中包含支援的連結，則連結中包含的媒體會在張貼至系列時展開。

這可讓Livefyre應用程式存取Embedly支援的250多種不同內嵌媒體選項。

>[!NOTE]
>
>Livefyre只會擴充Embedly完整提供者清單的子集。 只有提供者是Twitter、YouTube、Imgur、Vine、Wikipedia或SoundCloud時，內嵌影像才會在HTTPS頁面上展開。 如需連結擴充或來源的進一步問題，請連絡您的技術客戶經理。

本頁列出一些常用內嵌媒體類型的範例，以及它們可接受的URL模式。 `Embed.ly` 不斷新增來源。 如需提供者的完整清單，請前往 `https://embed.ly/embed/features/providers`。

>[!NOTE]
>
>內嵌格式需要完整的權限。 縮短的連結將無法運作。

只有可公開檢視的內容可內嵌。 如果您嘗試內嵌非公開的內容，內容的連結會出現在部落格文章中，並隨附一個預留位置圖示。 按一下連結後，該連結會將讀者帶至代管內容之服務的錯誤訊息，例如僅限朋友的像片的Facebook訊息。 如果您發現媒體未如預期般擴充，請連絡您的客戶經理。

## 內嵌URL範例

| 類型 | 提供者 | URL |
|--- |--- |--- |
| 地圖 | Google地圖 | <ul><li>`https://maps.google.com/maps?*`</li><li>`https://maps.google.com/?*`</li><li>`https://maps.google.com/maps/ms?*`</li></ul><br>**注意**:URL必須以 `http` 開頭，而非 `https.` |
| 社交網路 | Google+ | <ul><li>`https://plus.google.com/*`</li><li>`https://www.google.com/profiles/*`</li><li> `https://plus.google.com/*`</li><li>`https://google.com/profiles/*`</li></ul> |
| 影片 | YouTube | <ul><li>`https://*youtube.com/watch*`</li><li> `https://*.youtube.com/v/*`</li><li>`https://*youtube.com/watch*` </li><li>`https://*.youtube.com/v/*`</li><li>`https://youtu.be/*`</li><li>`https://*.youtube.com/user/*` </li><li>`https://*.youtube.com/*#*/*`</li><li>`https://m.youtube.com/watch*`</li><li>`https://m.youtube.com/index*`</li><li>`https://*.youtube.com/profile*`</li><li>`https://*.youtube.com/view_play_list*`</li><li>`https://*.youtube.com/playlist*`</li></ul> |
| 相片 | Flickr | `https://www.flickr.com/photos/*`<br>`https://flic.kr/*` |
|  | Instagram | `https://instagr.am/p/*`<br>`https://instagram.com/p/*` |
|  | TwitPic | <ul><li>`https://twitpic.com/*`</li><li>`https://www.twitpic.com/*`</li><li>`https://twitpic.com/photos/*`</li><li>`https://www.twitpic.com/photos/*`</li></ul> |
|  | Facebook | `https://www.facebook.com/photo.php*` |
|  | `Ow.ly` （Hootsuite的內容上傳服務） | `https://ow.ly/i/*` |
| 民調 | GoPollGo | `https://gopollgo.com/*`<br>`https://www.gopollgo.com/*` |
|  | Droplr | `https://d.pr/i/*` |
| 音訊 | SoundCloud | <ul><li>`https://soundcloud.com/*`</li><li>`https://soundcloud.com/*/*` </li><li>`https://soundcloud.com/*/sets/*` </li><li>`https://soundcloud.com/groups/*` </li><li>`https://snd.sc/*`</li></ul> |
|  | Spotify | `https://open.spotify.com/*` |
| 部落格 | Tumblr | `https://tumblr.com/*`<br>`https://*.tumblr.com/post/*` |

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
* [上傳按鈕](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

