---
description: 並非所有符合規則的推文都會出現在串流中。
title: 調節推文與頻率
exl-id: 6b963f8a-1b61-4252-866b-567d7f556aca
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# 推文的調節和頻率{#throttling-and-frequency-of-tweets}

並非所有符合規則的推文都會出現在串流中。

Twitter規則限制和Twitter動態消息中斷可限制流中可見的推文數。

>[!NOTE]
>
>若要保證特定推文會包含在您的串流中，請使用「所有資產」頁面中的「上傳資產」選項。

* Twitter規則會限制內容，每5秒提取1個推文。 這可讓Livefyre應用程式中顯示的內容更加平衡，而且不會因推文而不知所措。 以此方式限制傳入的推文也有助於防止串流在高流量期間被淹沒或無法讀取。

   >[!NOTE]
   >
   >為了確保高價值作者的內容出現在您的「應用程式」中，即使是在高速串流中，特定作者的「規則」也不會被調節。

* Twitter的餵食中斷可能出於幾個原因。 在某些情況下，Twitter不會推出推文，因此Livefyre不會收到新內容的通知，而且無法顯示。 twitterAPI的服務中斷或大量主題標籤／關鍵字的流量，也可能導致推文遺失。
