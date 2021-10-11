---
description: 自訂Livefyre評論的文字字串。
title: 檢閱文字字串
exl-id: 82ced091-d573-4514-9b91-3451a94ed5d3
source-git-commit: 1d9088eecf797e1af881cb6be55b3c96284f75e5
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 5%

---

# 檢閱文字字串{#review-text-strings}

自訂Livefyre評論的文字字串。

此頁面列出並說明可在「檢閱應用程式」中自訂的字串。 此處列出的字串，除了Livefyre核心應用程式的預設字串之外，也是String Customitions中列出的預設字串的替代項目。 其中列出了重複項，這些表格中列出的字串是「查看」應用程式的預設值。

實作
審核/評等介面
資料流資訊
作者/內容資訊
使用者動作
貼文函式
錯誤

## 實施 {#section-vsy-1k4-xz}

若要實作此功能，請傳入您要覆寫至Javascript設定物件之字串的1-1物件對應。 如果您未提供欄位，則會使用預設文字。

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

## 審核/評等介面 {#section_iyv_zj4_xz}

「檢閱與評等」使用者介面可用的字串。

| 元素 | 金鑰 | 預設文字 |
|--- |--- |--- |
| 按鈕 | editReviewBtn | 編輯審核 |
|  | reviewBtn | 寫評論 |
|  | reviewsClosed | 已結束審核 |
|  | showReviewBtn | 顯示審閱 |
|  | 追隨 | 我感興趣 |
|  | shareText | 我剛寫了個評論。 看看！ |
| 評等工具提示 | ratingValues | 陣列. 預設= `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`;<br>注意：必須複製陣列中的值，才能將每個星號的左半部和右半部指派相同名稱。 |
| 分級子部件 | ratingSubpartPlaceholders | 陣列. 預設值 = `[]` |
|  | ratingSubpartTitles | 陣列. 預設值 = `[]` |
|  | reviewStreamTitle | 預設為空白。 評論摘要區段的標題。 |
| 雜項 | averageRating | 平均使用者評分 |
|  | breakdownHeader | 評等劃分 |
|  | 實用 | 發現%s個 |
|  | lipedPlural | 發現%s個 |
|  | outOf | / |
|  | ratingType | 星星 |

## 資料流資訊 {#section_wmv_yj4_xz}

可用於內容流資訊和顯示的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| 排序 | sortBy | 預設為空白。 |
|  | sortHighestActied | 最高評等 |
|  | sortLowestActied | 最低評等 |
|  | sortMostLapid | 最有用 |
| 流雜項 | showMore | 顯示更多 |
| 流速 | newComment | 新評論 |
|  | newComments | 新評論 |
| 監聽器計數 | listenerCount | 人員監聽 |
|  | listenerCountPlural | 聆聽 |
| 註解計數 | commentCountLabel | LiveReviews<strong> | </strong>%s |
|  | commentCountLabelPlural | LiveReviews<strong> | </strong>%s |
| 注釋通告程式計數 | commentNotifier | 新評論 |
|  | commentNotifierPlural | 新評論 |

## 作者/內容資訊 {#section_osx_xj4_xz}

提供作者和個別內容資訊的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| 線程突破 | reviewsContentNotFoundMsg | 此審核不再顯示 |
|  | backToComments | 返回評論 |

## 使用者動作 {#section_tlx_wj4_xz}

可用於用戶操作的字串：標幟、共用和標示現有內容是有用的。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| 註解頁尾 | wasReviewHalped | 有用嗎？ |
|  | wasReviewHalipedMobile | 有用嗎？ |
|  | ownWasReviewHalped | 發現有用。 |
|  | reviewWasHalip | 是 |
|  | liveDiferer | &amp;vert; |
|  | reviewWasNotLapid | 無 |
| 投票強制回應 | voteTitle | 這篇評論有用嗎？ |
|  | voteDownvote | 無 |
|  | voteReplyTitle | 這個回覆有用嗎？ |
|  | voteTitle | 這個評論有用嗎？ |
|  | voteUpvote | 是 |
| 標幟強制回應視窗 | flagTitle | 標籤%s的審核 |
|  | flagSuccessMsg | 已標籤審核。 |
| 標幟行動 | flagConfirmationMessage | 是否將%s的審核標籤為%s? |
| 提及強制回應 | intersDefaultText | 我在Livefyre評論中提到過你！ |
| 共用強制回應 | shareTitle | 共用審核 |

## 貼文函式 {#section_yl1_wj4_xz}

可供發佈評論的使用者使用的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| 編輯器 | bodyPlaceholder | 寫評論…… |
|  | postEditButton | 編輯 |
|  | postEditCancelButton | 取消 |
|  | postAsButton | 貼文審核為…… |
|  | postButton | 貼文審核 |
|  | postReplyAsButton | 貼文為…… |
|  | postReplyButton | 貼文 |
|  | shareButton | 共用 |
|  | titlePlaceholder | 標題… |

## 錯誤 {#section_jbc_vj4_xz}

可用於一般錯誤訊息的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| 錯誤 | errorAlreadPosted | 您只能張貼一個審核。 |
|  | errorAuthError | 您無權對此對話發佈評論 |
|  | errorCommentsNotAllowed | 此時無法發佈評論 |
|  | errorDislikeOwnComment | 你不能不喜歡自己的評論 |
|  | errorDuplicate | 雖然你喜歡評論，但你不得發佈兩次。 |
|  | errorEditDuplicate | 編輯審閱時，必須更改其正文。 |
|  | errorEditNotAllowed | 您不能編輯此對話的評論。 |
|  | errorEditTimeExceeded | 很抱歉，您的審核編輯期已過。 |
|  | errorEmpty | 你似乎想張空白的評論。 |
|  | errorEmptyTitle | 看來你想張空標題 |
|  | errorFieldRating | 星級 |
|  | errorFieldReview | 審查 |
|  | errorFieldTitle | title |
|  | errorMaxChars | 抱歉，你的評論太長了。 請編輯並重試。 |
|  | errorMissingFields | 請輸入 |
|  | errorRatingEmpty | 您無法提交空評級 |
|  | errorRatingNotSet | 必須設定所有評級 |
|  | errorRatingNotValid | 評等必須是物件 |
|  | errorShowMore | 載入更多評論時出錯。 |
|  | errorTitleMaxChars | 抱歉，你的標題太長了。 請編輯並重試。 |
|  | errorVoteOwnComment | 你不能自行投票 |
