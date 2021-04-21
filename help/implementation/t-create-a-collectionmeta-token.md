---
description: 建立傳遞至Livefyre的collectionMeta Token，以建立新的系列。
title: 使用CollectionMeta Token建立系列
exl-id: d2dafc90-de21-4998-8e85-83f970524329
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# 使用CollectionMeta Token建立系列{#create-a-collection-using-the-collectionmeta-token}

建立傳遞至Livefyre的collectionMeta Token，以建立新的系列。

1. 建立collectionMetaToken。
1. 建立校驗和。

   如果您想要通知Livefyre您對系列所做的任何變更，則需要進行校驗和。 Livefyre只會在提供的校驗和與先前傳送的校驗和不同時，才會更新您的Collection。 建立校驗和就像建立`collectionMeta`標籤，而不是調用`buildCollectionMetaToken`調用`buildChecksum`。

建立使用者Token以驗證至Livefyre。
