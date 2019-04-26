---
description: 不是每個符合規則的推文都會出現在串流中。
seo-description: 不是每個符合規則的推文都會出現在串流中。
seo-title: 推文的縮動與頻率
solution: Experience Manager
title: 推文的縮動與頻率
uuid: b9edfb1e-e6 cf-4a48-8756-05f5 f18 d8799
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 推文的縮動與頻率{#throttling-and-frequency-of-tweets}

不是每個符合規則的推文都會出現在串流中。

Twitter規則調節和Twitter動態消息中斷可限制串流中可見的推文數目。

>[!NOTE]
>
>為確保您的串流包含特定推文，請從「所有資產」頁面使用「上傳資產」選項。

* Twitter規則節流內容，每個規則每個規則提取一個推文。這可讓Livefyre應用程式中出現的內容更平衡，而不會被推文淹沒。以此方式限制傳入推文也有助於防止串流在高流量期間變成洪水或無法讀取。

   >[!NOTE]
   >
   >為確保高價值作者的內容出現在您的應用程式中，即使在高速串流中，特定作者的規則永遠不會被調節。

* 可能會發生Twitter摘要中斷，原因有數個。在某些情況下，Twitter不會推送推文，因此Livefyre不會收到新內容的通知，也無法顯示。對Twitter API的服務中斷或大量雜湊標籤/關鍵字上的流量，也可能導致推文遺失。

