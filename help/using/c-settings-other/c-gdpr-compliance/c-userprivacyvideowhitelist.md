---
description: 您可以使用將視訊網域加入白名單。
seo-description: 您可以使用將視訊網域加入白名單。
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

如果您使用自己的自訂視訊和播放器，作為Livefyre視覺化應用程式中顯示視訊的一部分，您可以將視訊網域加入白名單。 將視訊網域加入白名單會移除自訂視訊和播放器的視訊遮色片。

>[!NOTE]
>
>使用特定路徑，確保僅將安全的視訊列入白名單。 如果您放入廣泛的路徑（例如sampledomain.com），您可能會將不安全的視訊列入白名單。

* 在之 `userPrivacyVideoWhitelist` 後加 `userPrivacyOptOut`入。 您可以一次新增所有Livefyre隱私權標幟，作為Livefyre物件的一部分。
* `userPrivacyVideoWhitelist` 僅適用於未內嵌於社交媒體的內容。

在下列範例中，包含路徑的「應用程式」中顯示的視訊 `sampledomain.com/cdn/videos` 會列入白名單：

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
