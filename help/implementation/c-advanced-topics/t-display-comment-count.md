---
description: 擷取特定系列的貼文和留言計數，以便顯示在索引頁面上。
seo-description: 擷取特定系列的貼文和留言計數，以便顯示在索引頁面上。
seo-title: 顯示注釋計數
solution: Experience Manager
title: 顯示注釋計數
uuid: 0f39b25e-11e0-4945-be71-55fb4798b6c7
translation-type: tm+mt
source-git-commit: c2594f919f153d1230b3dc0370f31d64cb698146
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# 顯示注釋計數{#display-comment-count}

擷取特定系列的貼文和留言計數，以便顯示在索引頁面上。

Livefyre可讓 `CommentCount.js` 您擷取網站上系列的內容計數。 雖然「應用程式」會顯示目前系列的注釋計數，但讓這些計數在您的網站上匯集是很有用的。 如果您未保存資料庫中的內容（或CMS資料庫未與Livefyre同步），此功能特別有用。

1. 載入JavaScript。

   若要使 `CommentCount.js`用，請先將JavaScript檔案內嵌 `<head>` 至您要使用的頁面或範本區段。

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. 系結HTML元素。

   載入指令碼後，它會嘗試在頁面上尋找其他類別名稱為的元素 `livefyre-commentcount`。 針對這些元素，指令碼會尋找 `data-lf-site-id` 和 `data-lf-article-id` HTML屬性，並使用這些屬性從Livefyre擷取內容，並以最新值更新每個元素。

   例如，下列元素將會更新：

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE]
   >
   >程式 `CommentCount.js` 碼會檢查數值，以便與實際計數一起更新。 請確定在標籤之間包含數值。

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

   若要進一步控制內容計數的取代方式，請呼 `LF.CommentCount()` 叫並傳入包含設定選項的物件。 請確定在DOM中所有需要取代的元素之後，呼叫函式。 呼叫此方法的最佳位置在頁尾，因此在載入DOM時，但在檔案和視窗就緒事件之前就會發生。

   我們允許下列配置選項：

* **替換器：** 用來取代每個內容計數的文字的函式或Regex。

* **函式：** 用於替換每個元素。 函式的引數為：

   **元素：** 正在更新的HTML元素。
   **計數：** 此元素的內容計數。

* **regex:** 用來判斷應由計數取代元素文字的哪一部分。

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
