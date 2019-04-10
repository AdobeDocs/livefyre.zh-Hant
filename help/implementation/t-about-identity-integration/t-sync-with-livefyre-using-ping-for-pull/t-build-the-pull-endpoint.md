---
description: 建立提取端點以接收並回應存取使用者身分系統的要求。
seo-description: 建立提取端點以接收並回應存取使用者身分系統的要求。
seo-title: 建立提取端點
solution: Experience Manager
title: 建立提取端點
uuid: 1703152f-alta7-4a88-aa33-d9 f8957 ad42 b
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 建立提取端點{#build-the-pull-endpoint}

建立提取端點以接收並回應存取使用者身分系統的要求。

1. 建立接收Livefyre請求的HTTPS端點，並使用包含最新使用者資料的JSON物件回應。

   >[!NOTE]
   >
   >此端點必須可存取。建議您同時透過HTTPS通訊協定傳送要求和回應。

1. 使用Studio註冊端點。
