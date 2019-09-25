---
description: 並非所有符合規則的推文都會出現在串流中。
seo-description: 並非所有符合規則的推文都會出現在串流中。
seo-title: 推文的調節與頻率
solution: Experience Manager
title: 推文的調節與頻率
uuid: b9edfb1e-e6cf-4a48-8756-05f5f18d8799
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 推文的調節與頻率{#throttling-and-frequency-of-tweets}

並非所有符合規則的推文都會出現在串流中。

Twitter規則限制和Twitter動態消息中斷可限制串流中可見的推文數。

>[!NOTE]
>
>若要保證特定推文會包含在您的串流中，請使用「所有資產」頁面中的「上傳資產」選項。

* Twitter規則會限制內容，每5秒提取1個推文。 這可讓Livefyre應用程式中顯示的內容更加平衡，而且不會因推文而不知所措。 以此方式限制傳入的推文也有助於防止串流在高流量期間被淹沒或無法讀取。

   >[!NOTE]
   >
   >為了確保高價值作者的內容出現在您的「應用程式」中，即使是在高速串流中，特定作者的「規則」也不會被調節。

* Twitter動態消息中斷可能會發生，原因有多種。 在某些情況下，Twitter不會推出推文，因此Livefyre不會收到新內容的通知，而且無法顯示。 Twitter API的服務中斷或大量主題標籤／關鍵字的流量，也可能導致推文遺失。

