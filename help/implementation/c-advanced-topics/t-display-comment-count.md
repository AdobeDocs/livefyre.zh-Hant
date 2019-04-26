---
description: 擷取在索引頁面上顯示特定系列的貼文和留言計數。
seo-description: 擷取在索引頁面上顯示特定系列的貼文和留言計數。
seo-title: 顯示註解計數
solution: Experience Manager
title: 顯示註解計數
uuid: 0f39b25e-11e0-4945-be71-55fb4798 b6 c7
translation-type: tm+mt
source-git-commit: c287e7a880f956f0444af746adee682571fe5a72

---


# 顯示註解計數{#display-comment-count}

擷取在索引頁面上顯示特定系列的貼文和留言計數。

Livefyre可 `CommentCount.js` 讓您擷取網站上系列的內容計數。雖然應用程式會顯示目前系列的註解計數，但在您的網站上進行這些計算可能會很有用。如果您不保存資料庫中的內容(或您的CMS資料庫與Livefyre同步)，此功能特別有用。

1. 載入JavaScript。

   若要使用 `CommentCount.js`，請先將JavaScript檔案內嵌在您想要使用之頁面或範本 `<head>` 區段中。

   ```
   <script 
      type="text/javascript" 
      data-lf-domain="{network name (domain.fyre.co)}" 
      src="//cdn.livefyre.com/libs/commentcount/v1.0/commentcount.js"> 
   </script>
   ```

1. 系結HTML元素。

   載入指令碼後，會嘗試在具有類別名稱的頁面上尋找其他元素 `livefyre-commentcount`。對於這些元素，指令碼會尋找 `data-lf-site-id``data-lf-article-id` 和HTML屬性，並使用這些屬性從Livefyre擷取內容，並使用最新值更新每個元素。

   例如，下列元素將會更新：

   ```
   <span class="livefyre-commentcount" data-lf-site-id="{site_id}" data-lf-article-id="{article_id}"> 
   0 Comments  
   </span>
   ```

   >[!NOTE] {importance=「high」}
   >
   >`CommentCount.js` 程式碼會檢查數值是否以實際計數更新。請確定標籤之間包含數值。

   **範例(** 使用URL做為文章ID)：

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="https://mikesoldner.com/blog.php">  
   0 Comments  
   </span>
   ```

   **範例(** 使用編號系統做為文章ID)：

   ```
   <span class="livefyre-commentcount" data-lf-site-id="311458" data-lf-article-id="25"> 0 Comments </span>
   ```

1. 設定選項。

   為進一步控制如何取代內容計數，請呼叫並 `LF.CommentCount()` 傳入包含設定選項的物件。請務必呼叫函數之後，所有需要取代的元素都位於DOM中。呼叫此方法最好的地方就在頁尾，如此當DOM載入時，就會發生在文件和視窗就緒事件之前。

   我們允許下列組態選項：

* **取代程式：** 函數或Regex用來取代每個內容計數的文字。

* **函數：** 用於取代每個元素。函數的引數為：

   **元素：** 正在更新的HTML元素。
   **計數：** 此元素的內容計數。

* **regex：** 用於判斷元素文字的哪一部分應由計數取代。

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
   >使用取代程式來自訂或國際化注釋計數訊息。
