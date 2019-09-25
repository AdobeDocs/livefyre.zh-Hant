---
description: 建立傳遞至Livefyre的collectionMeta Token，以建立新的系列。
seo-description: 建立傳遞至Livefyre的collectionMeta Token，以建立新的系列。
seo-title: 使用CollectionMeta Token建立系列
solution: Experience Manager
title: 使用CollectionMeta Token建立系列
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e

---


# 使用CollectionMeta Token建立系列{#create-a-collection-using-the-collectionmeta-token}

建立傳遞至Livefyre的collectionMeta Token，以建立新的系列。

1. 建立collectionMetaToken。
1. 建立校驗和。

   如果您想要通知Livefyre您對系列所做的任何變更，則需要進行校驗和。 Livefyre只會在提供的校驗和與先前傳送的校驗和不同時，才會更新您的Collection。 建立校驗和就像建立令牌， `collectionMeta` 而不是呼叫您 `buildCollectionMetaToken` 調用 `buildChecksum`。

建立使用者Token以驗證至Livefyre。