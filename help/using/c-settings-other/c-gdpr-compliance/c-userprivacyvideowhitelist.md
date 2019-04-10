---
description: 您可以將您的視訊網域列入白名單。
seo-description: 您可以將您的視訊網域列入白名單。
seo-title: userPrivacyVideoHiteList
solution: Experience Manager
title: userPrivacyVideoHiteList
uuid: adfead18-b73 b-4ac4-97a0-d39 f528 b7606
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# userPrivacyVideoHiteList{#userprivacyvideowhitelist}

如果您使用自己的自訂視訊和播放器做為Livefyre視覺化應用程式中顯示的視訊的一部分，則可將您的視訊網域列入白名單。為您的自訂影片和播放器刪除視訊網域會移除視訊遮色片。

>[!NOTE]
>
>使用特定路徑以確保只有安全的視訊已列入白名單。如果您放置廣泛路徑(例如sampledomain.com)，您可以將不安全的影片列入白名單。

* 新增 `userPrivacyVideoWhitelist``userPrivacyOptOut`後，您可以一次將所有Livefyre隱私標幟加入一個Livefyre物件中。
* `userPrivacyVideoWhitelist` 僅適用於未從社交媒體內嵌的內容。

在下列範例中，在具有 `sampledomain.com/cdn/videos` 路徑的應用程式中顯示的影片會列入白名單：

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
