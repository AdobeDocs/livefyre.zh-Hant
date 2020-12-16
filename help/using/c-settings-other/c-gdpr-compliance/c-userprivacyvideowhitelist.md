---
description: 您可以允許列出您的視訊網域。
seo-description: 您可以允許列出您的視訊網域。
seo-title: userPrivacyVideoWhitelist
solution: Experience Manager
title: userPrivacyVideoWhitelist
uuid: adfead18-b73b-4ac4-97a0-d39f528b7606
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# userPrivacyVideoWhitelist{#userprivacyvideowhitelist}

如果您使用自己的自訂視訊和播放器，作為Livefyre視覺化應用程式中顯示視訊的一部分，您就可以允許列出視訊網域。 允許列出您的視訊網域會移除自訂視訊和播放器的視訊遮色片。

>[!NOTE]
>
>使用特定路徑，確保僅允許列出安全的視訊。 如果您放入廣泛的路徑（例如sampledomain.com），則可能允許列出不安全的視訊。

* 在`userPrivacyOptOut`後面添加`userPrivacyVideoWhitelist`。 您可以一次新增所有Livefyre隱私權標幟，作為Livefyre物件的一部分。
* `userPrivacyVideoWhitelist` 僅適用於未內嵌於社交媒體的內容。

在下列範例中，「應用程式」中顯示具有`sampledomain.com/cdn/videos`路徑的視訊會允許列出：

```
userPrivacyVideoWhitelist: ["sampledomain.com/cdn/videos"]
```
