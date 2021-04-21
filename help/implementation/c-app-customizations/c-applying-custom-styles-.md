---
description: 若要自訂使用者群組的樣式內容，您必須先將使用者標籤新增至帳戶，然後使用CSS來設定內容的樣式。
title: 套用自訂樣式
exl-id: 54692525-32ce-487a-b3c3-da1261b58da1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# 套用自訂樣式{#applying-custom-styles}

若要自訂使用者群組的樣式內容，您必須先將使用者標籤新增至帳戶，然後使用CSS來設定內容的樣式。

對於透過Studio或Ping for Pull新增的每個使用者標籤，Livefyre將建立兩個CSS類別，這兩個類別都可用於設定群組內容的樣式。

將使用者標籤轉換為CSS類別時：

* Livefyre會建立兩個類別：fyre-author-tag-***&lt;your_group>***和fyre-tag-author-***&lt;your_group>****。 兩者皆可用於設定內容的樣式。

* 標籤中包含的任何空格都將轉換為下划線。 例如：「我的最愛使用者」將變成favorite_user。
* 群組名稱中包含的Unicode字元將不會轉換，並會在類別名稱中顯示為Unicode。 例如：使用者群組「modérateur」將成為fyre-comment-author-tag-modérateur。

在您的使用者群組建立後，請使用Livefyre的CSS類別，為內容套用自訂樣式。

## 協調者（和擁有者）的樣式內容{#section_vjv_2cv_xz}

* 使用CSS類別。fyre-codriator。

   >[!NOTE]
   >
   >擁有者（因為他們也是協調者）也會將此類別套用至其串流中的內容。

* 建立CSS規則以顯示或設定群組徽章的樣式：

   ```
   .fyre-moderator { 
       font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
       text-decoration: none; 
       color: #404040; 
       padding-left: 28px; 
       padding-top: 4px; 
   }
   ```

## 使用者群組的樣式內容{#section_ghn_s1v_xz}

建立CSS規則以顯示或設定群組徽章的樣式：

```
<span class="fyre-comment-author-tag fyre-comment-author-tag-writer fyre-comment-plus" data-fyre-author-tag="staff">Staff Writer</span>
```

```
.livechat-comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag, .comments-container .fyre .fyre-comment-wrapper .fyre-comment-author-tag { 
    display: inline-block !important; 
    background: #603url('/etc/designs/site/images/comments-icon-staff.8db5be91.png?1438807177') no-repeat left center !important; 
    padding-right: 3px !important; 
    padding-left: 20px !important; 
    text-transform: uppercase !important; 
    font-weight: bold !important; 
    font-size: 11px !important; 
    border-radius: 0 !important; 
    color: #ffffff !important; 
}
```

使用CSS類別fyre-author-tag-****&lt;your_group>**或fyre-tag-author-***&lt;your_group>****來設定從與所選標籤相關聯的帳戶張貼的每個項目的字型和背景樣式。

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```
