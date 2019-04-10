---
description: 直接在應用程式中使用 embed.ly 顯示多種媒體格式。
seo-description: 直接在應用程式中使用 embed.ly 顯示多種媒體格式。
seo-title: Embedly 整合
solution: Experience Manager
title: Embedly 整合
uuid: 1f27e32c-c2 c3-4f7 c-93de-c9 c7 f783 d6 a
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Embedly 整合{#embedly-integration}

可用來 `embed.ly` 直接在應用程式中顯示多種媒體格式。

為了更好地從各種來源(包括Google地圖、YouTube、Flickr、Facebook、Instagram、Spotify和Tumblr)啓用內嵌媒體內容，Livefyre應用程式將Embey作為協力廠商提供商用於URL擴增。如果使用者或協調者在貼文中包含支援的連結，連結中包含的媒體將會在張貼至系列時展開。

這提供Livefyre應用程式存取超過250種不同支援的內嵌媒體選項的存取權。

>[!NOTE]
>
>Livefyre僅擴充Embey完整提供者清單的子集。只有當提供者是Twitter、YouTube、Imgur、Vine、維基百科或SoundCloud時，內嵌影像才會放大至HTTPS頁面。有關連結擴充或來源的任何進一步問題，請聯絡您的Technical帳戶管理員。

本頁列出一些常用內嵌媒體類型的範例，以及可接受的URL模式。`Embed.ly` 持續增加新來源。若需完整的供應商清單 `https://embed.ly/embed/features/providers`，請前往。

>[!NOTE]
>
>「電子郵件」格式需要完整的權限。縮短的連結將無法運作。

只有公開可檢視的內容才能內嵌。如果您嘗試內嵌不公開的內容，內容的連結將會出現在部落格文章中，而預留位置圖示則會隨附。在按下時，連結會將讀者帶往代管內容的服務中的錯誤訊息，例如僅適用於朋友像片的Facebook訊息。如果您發現媒體未如預期般擴展，請連絡您的帳戶管理員。

## 範例內嵌URL

| Type | 供應商 | URL |
|--- |--- |--- |
| 地圖 | Google地圖 | <ul><li>`https://maps.google.com/maps?*`</li><li>`https://maps.google.com/?*`</li><li>`https://maps.google.com/maps/ms?*`</li></ul><br>**Note**: URL must begin with `http` and not `https.` |
| Social Networking | Google Plus | <ul><li>`https://plus.google.com/*`</li><li>`https://www.google.com/profiles/*`</li><li> `https://plus.google.com/*`</li><li>`https://google.com/profiles/*`</li></ul> |
| Video | YouTube | <ul><li>`https://*youtube.com/watch*`</li><li> `https://*.youtube.com/v/*`</li><li>`https://*youtube.com/watch*` </li><li>`https://*.youtube.com/v/*`</li><li>`https://youtu.be/*`</li><li>`https://*.youtube.com/user/*` </li><li>`https://*.youtube.com/*#*/*`</li><li>`https://m.youtube.com/watch*`</li><li>`https://m.youtube.com/index*`</li><li>`https://*.youtube.com/profile*`</li><li>`https://*.youtube.com/view_play_list*`</li><li>`https://*.youtube.com/playlist*`</li></ul> |
| Photos | Flickr | `https://www.flickr.com/photos/*`<br>`https://flic.kr/*` |
|  | Instagram | `https://instagr.am/p/*`<br>`https://instagram.com/p/*` |
|  | TwitPic | <ul><li>`https://twitpic.com/*`</li><li>`https://www.twitpic.com/*`</li><li>`https://twitpic.com/photos/*`</li><li>`https://www.twitpic.com/photos/*`</li></ul> |
|  | Facebook | `https://www.facebook.com/photo.php*` |
|  | `Ow.ly` (Hootsuite’s Content Uploading Service) | `https://ow.ly/i/*` |
| Polls | GoPollGo | `https://gopollgo.com/*`<br>`https://www.gopollgo.com/*` |
|  | Droplr | `https://d.pr/i/*` |
| Audio | SoundCloud | <ul><li>`https://soundcloud.com/*`</li><li>`https://soundcloud.com/*/*` </li><li>`https://soundcloud.com/*/sets/*` </li><li>`https://soundcloud.com/groups/*` </li><li>`https://snd.sc/*`</li></ul> |
|  | Spotify | `https://open.spotify.com/*` |
| Blogs | Tumblr | `https://tumblr.com/*`<br>`https://*.tumblr.com/post/*` |

Apps that use this feature:

* [Carousel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [Chat](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [Comments](/help/using/c-about-apps/c-comments/c-comments.md)
* [Feature Card](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [Map](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [Media Wall](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaic](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [Polls](/help/using/c-about-apps/c-polls-app/c-polls-app.md#c_polls_app)
* [Reviews](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidenotes](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [Trending](/help/using/c-about-apps/c-trending-app/c-trending-app.md#c_trending_app)
* [上傳按鈕](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

