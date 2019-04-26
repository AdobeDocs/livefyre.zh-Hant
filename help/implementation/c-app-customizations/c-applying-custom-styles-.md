---
description: 若要為使用者群組自訂樣式內容，您必須先新增使用者標記至帳戶，然後使用CSS為內容設定樣式。
seo-description: 若要為使用者群組自訂樣式內容，您必須先新增使用者標記至帳戶，然後使用CSS為內容設定樣式。
seo-title: 套用自訂樣式
solution: Experience Manager
title: 套用自訂樣式
uuid: 0556aa2f-4fcd-4bde-abb5-479ec672 f573
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 套用自訂樣式{#applying-custom-styles}

若要為使用者群組自訂樣式內容，您必須先新增使用者標記至帳戶，然後使用CSS為內容設定樣式。

對於透過Studio或Ping for Draw新增的每個使用者標籤，Livefyre會建立兩個CSS類別，這兩個類別都可用來設定群組內容的樣式。

將使用者標記轉換為CSS類別時：

* Livefyre會建立兩個類別：fyre-author-tag-***< your_ group>*** and fyre-tag-author-***< your_ group>***.兩者皆可用來設定內容的樣式。

* 標籤中包含的任何空格都會轉換為底線。例如：「我的最愛使用者」將成為最愛的_ user。
* 群組名稱中包含的Unicode字元不會轉換，且會顯示為類別名稱中的Unicode。例如：使用者群組'modérateur'將變成fyre-comment-author-tag-modérater。

建立您的使用者群組後，請使用Livefyre的CSS類別，針對內容套用自訂樣式。

## 協調者(和擁有者)的樣式內容 {#section_vjv_2cv_xz}

* 使用CSS class. fyre協調者。

   >[!NOTE]
   >
   >擁有者，因為他們也是協調者，所以也會將此類別套用至串流中的內容。

* 建立CSS規則以顯示或設定群組的徽章：

   ```
   .fyre-moderator { 
       font: 13px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
       text-decoration: none; 
       color: #404040; 
       padding-left: 28px; 
       padding-top: 4px; 
   }
   ```

## 使用者群組的樣式內容 {#section_ghn_s1v_xz}

建立CSS規則以顯示或設定群組的徽章：

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

使用CSS類別fyre-author-tag-***< your_ group>***或fyre-tag-author-***< your_ group>***以針對從與選取標籤關聯的帳戶發佈每個項目的字型和背景。

```
.fyre-comment-author-tag-<your_group> .fyre-comment-author-tag { 
    font: 10px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif; 
    text-decoration: none; 
    color: #404040; 
    padding-left: 28px; 
    padding-top: 4px; 
}
```

