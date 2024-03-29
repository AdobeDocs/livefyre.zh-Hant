---
description: 擷取特定系列的貼文和留言計數，以便顯示在索引頁面上。
title: 顯示注釋計數
exl-id: 03c911f0-1fdd-4d5c-9262-9ff7485b7b14
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# 顯示注釋計數{#display-comment-count}

擷取特定系列的貼文和留言計數，以便顯示在索引頁面上。

Livefyre的`CommentCount.js`可讓您擷取網站上系列的內容計數。 雖然「應用程式」會顯示目前系列的注釋計數，但讓這些計數在您的網站上匯集是很有用的。 如果您未保存資料庫中的內容（或CMS資料庫未與Livefyre同步），此功能特別有用。

1. 載入JavaScript。

   若要使用`CommentCount.js`，請先將JavaScript檔案內嵌至您要使用之頁面或範本的`<head>`區段。

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. 系結HTML元素。

   載入指令碼後，它會嘗試在頁面上尋找類別名稱為`livefyre-commentcount`的其他元素。 對於這些元素，指令碼會尋找`data-lf-site-id`和`data-lf-article-id` HTML屬性，並使用這些屬性從Livefyre擷取內容，並以最新值更新每個元素。

   例如，下列元素將會更新：

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE]
   >
   >`CommentCount.js`程式碼會檢查數值，以使用實際計數進行更新。 請確定在標籤之間包含數值。

   **範例1** （使用URL做為文章ID）:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **範例2** （使用編號系統做為文章ID）:

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. 設定選項。

   若要進一步控制內容計數的取代方式，請呼叫`LF.CommentCount()`並傳入包含設定選項的物件。 請確定在DOM中所有需要取代的元素之後，呼叫函式。 呼叫此方法的最佳位置在頁尾，因此在載入DOM時，但在檔案和視窗就緒事件之前就會發生。

   我們允許下列配置選項：

* **replacer:** 用於取代每個內容計數的文字的函式或Regex。

* **函式：** 用於對每個元素進行替換。函式的引數為：

   **元素：** 正在更新的HTML元素。
   **count:** 此元素的內容計數。

* **regex:** 用於判斷應由計數取代元素文字的哪個部分。

   **範例**:

   ```
      <script type="text/javascript"> LF.CommentCount({ 
        replacer: function(element, count) { 
            element.innerHTML = count +' Comment'+ (count === 1 ? '' : 's'); 
        } 
    }); 
   </script>
   ```

   >[!NOTE]
   >
   >使用替換器定制或國際化注釋計數消息。
