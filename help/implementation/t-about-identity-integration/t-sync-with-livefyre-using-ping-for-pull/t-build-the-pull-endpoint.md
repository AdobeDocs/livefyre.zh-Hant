---
description: 建立拉入端點，以接收並回應存取您使用者識別系統的要求。
title: 構建拉式端點
exl-id: cc66365b-0d5f-4a0b-954f-ee014e75d4a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---

# 構建拉式端點{#build-the-pull-endpoint}

建立拉入端點，以接收並回應存取您使用者識別系統的要求。

1. 建立HTTPS端點，接收Livefyre請求並以包含最新使用者資料的JSON物件回應。

   >[!NOTE]
   >
   >此端點必須可訪問。 強烈建議透過HTTPS通訊協定傳送請求和回應。

1. 向Studio註冊端點。
