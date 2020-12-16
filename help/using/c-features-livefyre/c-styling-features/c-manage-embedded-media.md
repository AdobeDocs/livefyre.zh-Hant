---
description: 定義使用者可張貼媒體的來源，以及禁止發佈媒體的來源。
seo-description: 定義使用者可張貼媒體的來源，以及禁止發佈媒體的來源。
seo-title: 管理嵌入式媒體
title: 管理嵌入式媒體
uuid: d8621be1-dcfb-429f-954e-b21fdcf02715
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---


# 管理嵌入式介質{#manage-embedded-media}

定義使用者可張貼媒體的來源，以及禁止發佈媒體的來源。

預設情況下，所有介質附件都可嵌入到注釋中。 如需完整的支援供應商清單，請參閱embed.ly/providers。

Livefyre使用Embed.ly和標準的oEmbed通訊協定，將媒體內嵌在應用程式串流中，並將透過其來源提供的所有媒體資料。

Embed.ly會傳遞所有可用資訊，包括任何提供URL的媒體標題、說明、縮圖和內嵌程式碼。 這些項目的可用性因供應商而異。 例如：Facebook不會傳回其視訊的縮圖，而且只會傳送可內嵌的視訊。 按一下「播放」會啟動影片（類似YouTube的顯示格式）。 Twitter僅傳送靜態影像，不會傳送影片。 因此，Twitter原生影片不得從Livefyre串流中播放。

嵌入注釋流時，您可能會阻止某些附件嵌入到注釋中。 您也可以選擇使用Studio隱藏網路、網站和對話層級的所有Embed.ly擴充功能，只顯示媒體的連結，而非完全內嵌的媒體。

使用此功能的應用程式：

* [功能卡](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [地圖](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [媒體牆](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)

