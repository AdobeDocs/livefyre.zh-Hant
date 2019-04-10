---
description: 建立要傳遞至Livefyre的CollectionMeta Token，建立新的系列。
seo-description: 建立要傳遞至Livefyre的CollectionMeta Token，建立新的系列。
seo-title: 使用CollectionMeta Token建立系列
solution: Experience Manager
title: 使用CollectionMeta Token建立系列
uuid: 5e18e8-8568-45bb-9070-d0 fa43 dd819 b
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 使用CollectionMeta Token建立系列{#create-a-collection-using-the-collectionmeta-token}

建立要傳遞至Livefyre的CollectionMeta Token，建立新的系列。

1. 建立CollectionMeta Token。
1. 建立檢查加總。

   如果您想通知Livefyre您已對您的系列進行任何變更，則需要使用此核取加總。只有在提供的查核加總不同於先前傳送的查核加總時，Livefyre才會更新您的Collection。Creating a checksum is just like creating a `collectionMeta` token but instead of calling `buildCollectionMetaToken` you call `buildChecksum`.

建立使用者Token以驗證至Livefyre。