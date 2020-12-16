---
description: 建立拉入端點，以接收並回應存取您使用者識別系統的要求。
seo-description: 建立拉入端點，以接收並回應存取您使用者識別系統的要求。
seo-title: 構建拉式端點
solution: Experience Manager
title: 構建拉式端點
uuid: 1703152f-aaa7-4a88-aa33-d9f8957ad42b
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# 構建拉式端點{#build-the-pull-endpoint}

建立拉入端點，以接收並回應存取您使用者識別系統的要求。

1. 建立HTTPS端點，接收Livefyre請求並以包含最新使用者資料的JSON物件回應。

   >[!NOTE]
   >
   >此端點必須可訪問。 強烈建議透過HTTPS通訊協定傳送請求和回應。

1. 向Studio註冊端點。
