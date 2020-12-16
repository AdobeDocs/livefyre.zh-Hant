---
description: 自訂Livefyre評論的文字字串。
seo-description: 自訂Livefyre評論的文字字串。
seo-title: 檢閱文字字串
solution: Experience Manager
title: 檢閱文字字串
uuid: 86251e49-bc73-4eec-9f9b-b4b0a5b42099
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 5%

---


# 查看文本字串{#review-text-strings}

自訂Livefyre評論的文字字串。

此頁面列出並說明可在「檢閱」應用程式中自訂的字串。 此處列出的字串除了Livefyre核心應用程式的預設字串外，也會覆寫，列在「字串自訂」中。 其中列出重複項目時，這些表格中列出的字串是「檢閱」應用程式的預設值。

實作
審查／評分介面
串流資訊
作者／內容資訊
使用者動作
貼文功能
錯誤

## 實施 {#section-vsy-1k4-xz}

若要實作此功能，請傳入您要覆寫之字串的1-1物件對應至Javascript設定物件。 如果您未提供欄位，則會使用預設文字。

範例:

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" }; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## 審查／評分介面{#section_iyv_zj4_xz}

「檢閱」和「評分」使用者介面的可用字串。

| 元素 | 金鑰 | 預設文字 |
|--- |--- |--- |
| 按鈕 | editReviewBtn | 編輯審核 |
|  | reviewBtn | [撰寫審核](https://d.pr/i/QscA) |
|  | reviewsClosed | [已結束審核](https://d.pr/i/zr7M) |
|  | showReviewBtn | [顯示審核](https://d.pr/i/onxU) |
|  | follow | 我感興趣 |
|  | shareText | 我剛寫了個評論。 看看！ |
| 評分工具提示 | ratingValues | 陣列. 預設值= `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`;<br>注意：必須複製陣列中的值，才能將每顆星的左半部和右半部都指定相同的名稱。 |
| 分級子部件 | ratingSubpartPlaceholders | 陣列. 預設值 = `[]` |
|  | ratingSubpartTitles | 陣列. 預設值 = `[]` |
|  | reviewStreamTitle | 預設為空白。 評論摘要部分的標題。 |
| 其他 | averageRating | [平均使用者評分](https://d.pr/i/QscA) |
|  | breakdownHeader | [分級劃分](https://d.pr/i/QscA) |
|  | 幫助 | 發現%s有幫助 |
|  | helpedPlural | 發現%s有幫助 |
|  | outOf | / |
|  | ratingType | 星星 |

## 串流資訊{#section_wmv_yj4_xz}

可用於內容串流資訊和顯示的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| 排序 | sortBy | 預設為空白。 |
|  | sortHighestAdied | [最高評分](https://d.pr/i/huTd) |
|  | sortLeomthAding | [最低評分](https://d.pr/i/huTd) |
|  | sortMostHappiled | [最有用](https://d.pr/i/huTd) |
| 串流雜項。 | showMore | 顯示更多 |
| 流高速 | newComment | 新評論 |
|  | newComments | 新評論 |
| 監聽器計數 | listenerCount | 監聽 |
|  | listenerCountPlural | 傾聽 |
| 注釋計數 | commentCountLabel | LiveReviews<strong> | </strong>%s |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| 注釋通告程式計數 | 注釋通告程式 | 新評論 |
|  | commentNotifierPlural | 新評論 |

## 作者／內容資訊{#section_osx_xj4_xz}

可供作者和個別內容資訊參考。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| 線程插頭 | reviewsContentNotFoundMsg | [此審閱不再顯示](https://d.pr/i/svXs) |
|  | backToComments | 返回評論 |

## 用戶操作{#section_tlx_wj4_xz}

用戶操作可用的字串：標幟、共用和標示現有內容有用。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| 注釋頁尾 | wasReviewHappiled | [有用嗎？](https://d.pr/i/Q0mA) |
|  | wasReviewHampileMobile | 有用嗎？ |
|  | ownWasReviewHappiled | [發現有幫助。](https://d.pr/i/Q0mA) |
|  | reviewWasHappiled | [是](https://d.pr/i/Q0mA) |
|  | libledDiferar | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewWasNotHappiled | [否](https://d.pr/i/Q0mA) |
| 投票模式 | voteTitle | 此評論有用嗎？ |
|  | voteDownvote | 無 |
|  | voteReplyTitle | 這個回覆有用嗎？ |
|  | voteTitle | 這句評論有用嗎？ |
|  | voteUpvote | 是 |
| 標幟模式 | flagTitle | 標籤%s的審核 |
|  | flagSuccessMsg | 已標籤審核。 |
| 標幟行動 | flagConfirmationMessage | 是否將%s的審核標幟為%s? |
| 提及模式 | 提及次數DefaultText | 我在Livefyre評論中提到過你！ |
| 共用模式 | shareTitle | 分享評論 |

## 貼文函式{#section_yl1_wj4_xz}

發佈審核的使用者可使用的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| 編輯器 | bodyPlaceholder | 撰寫評論…… |
|  | postEditButton | 編輯 |
|  | postEditCancelButton | 取消 |
|  | postAsButton | 將審核貼文為…… |
|  | postButton | 貼文審核 |
|  | postReplyAsButton | 張貼為…… |
|  | postReplyButton | 貼文 |
|  | shareButton | 共用 |
|  | titlePlaceholder | 標題… |

## 錯誤 {#section_jbc_vj4_xz}

一般錯誤訊息的字串可用。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| 錯誤 | errorAlreadyPosted | 您只能張貼一份審核。 |
|  | errorAuthError | 您無權對此對話發表評論 |
|  | errorCommentsNotAllowed | 目前無法張貼評論 |
|  | errorDislikeOwnComment | 您不能不喜歡自己的評論 |
|  | errorDuplicate | 雖然您很喜歡您的評論，但是您不得張貼兩次。 |
|  | errorEditDuplicate | 編輯審閱時，必須更改其正文。 |
|  | errorEditNotAllowed | 您無法編輯此對話的評論。 |
|  | errorEditTimeExceeded | 抱歉，您的審核編輯期間已過期。 |
|  | errorEmpty | 您似乎在嘗試張貼空白的評論。 |
|  | errorEmptyTitle | 您似乎在嘗試張貼空白標題 |
|  | errorFieldRating | 星級 |
|  | errorFieldReview | 審查 |
|  | errorFieldTitle | title |
|  | errorMaxChars | 抱歉，您的評論太長了。 請編輯並再試一次。 |
|  | errorMissingFields | 請輸入 |
|  | errorRatingEmpty | 您無法提交空白評分 |
|  | errorRatingNotSet | 必須設定所有評分 |
|  | errorRatingNotValid | 分級必須是物件 |
|  | errorShowMore | 載入更多評論時發生錯誤。 |
|  | errorTitleMaxChars | 抱歉，您的標題太長。 請編輯並再試一次。 |
|  | errorVoteOwnComment | 您無法依自己的意見投票 |

