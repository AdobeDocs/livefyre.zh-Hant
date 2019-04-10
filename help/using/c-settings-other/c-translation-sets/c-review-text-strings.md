---
description: 自訂Livefyre評論的文字字串。
seo-description: 自訂Livefyre評論的文字字串。
seo-title: 檢閱文字字串
solution: Experience Manager
title: 檢閱文字字串
uuid: 86251e49-bc73-4eec-9f9 b-b4 b0 b0 b42099
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 檢閱文字字串{#review-text-strings}

自訂Livefyre評論的文字字串。

此頁面列出並說明可供「檢閱」應用程式自訂的字串。此處列出的字串除了適用於Livefyre核心應用程式的預設字串外，也包含在字串自訂中。若列出重復項目，這些表格中列出的字串就是「檢閱」應用程式的預設值。

實施審查/分級介面資料作者/內容資訊使用者動作貼文函數錯誤

## 實施 {#section-vsy-1k4-xz}

若要實施此功能，請傳遞您要覆寫至Javascript組態物件之字串的1-1物件對應。如果您未提供欄位，則會使用預設文字。

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

## 審查/評分介面 {#section_iyv_zj4_xz}

用於審查和分級使用者介面的字串。

| 元素 | 索引鍵 | 預設文字 |
|--- |--- |--- |
| 按鈕 | editReviewBTn | 編輯評論 |
|  | ReviewBTn | [寫作評論](https://d.pr/i/QscA) |
|  | 重新檢視關閉 | [評論已關閉](https://d.pr/i/zr7M) |
|  | ShowreviewBtn | [顯示評論](https://d.pr/i/onxU) |
|  | following | 我很感興趣 |
|  | ShareText | 我剛撰寫了評論。立即查看！ |
| 評分工具提示 | ratingValues | 陣列。預設= `[‘Poor’, ‘Poor’, ‘Fair’, ‘Fair’, ‘Average’, ‘Average’, ‘Good’, ‘Good’, ‘Excellent’, ‘Excellent’]`； <br>注意：陣列中的值必須重復，以指派每個星號的左側和右側名稱。 |
| 分級子集 | ratingSubpartpleets | 陣列。預設= `[]` |
|  | ratingSubpartitals | 陣列。預設= `[]` |
|  | reviewStreamTitle | 預設為空白。評論摘要區段的標題。 |
| Misc | averagering | [使用者平均評分](https://d.pr/i/QscA) |
|  | 劃分標題 | [排名劃分](https://d.pr/i/QscA) |
|  | 有用 | %s的%s發現實用 |
|  | HelpFultimultiple | %s的%s發現實用 |
|  | Out Over | / |
|  | ratingType | 星形 |

## 串流資訊 {#section_wmv_yj4_xz}

用於內容串流資訊和顯示的字串。

| 元素 | 索引鍵 | 預設文字 |
|---|---|---|
| 排序順序 | SortBy | 預設為空白。 |
|  | SorthigheSoft | [最高評分](https://d.pr/i/huTd) |
|  | sortloweSoft | [最低評分](https://d.pr/i/huTd) |
|  | sortmosthelpful | [最實用](https://d.pr/i/huTd) |
| 串流錯誤。 | 展示更多資訊 | 顯示更多資訊 |
| 串流高速 | NewComment | 新評論 |
|  | NewComments | 新評論 |
| 偵聽程式計數 | ListenerCount | 個人監聽 |
|  | listenercountmtium | 受眾監聽 |
| 注釋計數 | 注釋標籤 | LivereViews<strong> | </strong>%s |
|  | 注釋縮寫 | LivereViews<strong> | </strong>%s |
| 注釋通知計數 | CommentNotifier | 新評論 |
|  | comnotifiertimtional | 新評論 |

## 作者/內容資訊 {#section_osx_xj4_xz}

可供作者和個別內容資訊使用。

| 元素 | 索引鍵 | 預設文字 |
|---|---|---|
| 執行緒劃分 | reviewsContentNotectNotsg | [此評論不再顯示](https://d.pr/i/svXs) |
|  | 回覆注釋 | 返回評論 |

## 使用者動作 {#section_tlx_wj4_xz}

適用於使用者動作的字串：標記、共用和標示現有內容有幫助。

| 元素 | 索引鍵 | 預設文字 |
|---|---|---|
| 注釋頁尾 | WasreviewWhilful | [有用嗎？](https://d.pr/i/Q0mA) |
|  | WasreviewHelpFulmobile | 有用嗎？ |
|  | ownwasreviewWhelpful | [發現實用。](https://d.pr/i/Q0mA) |
|  | 評論實用 | [是](https://d.pr/i/Q0mA) |
|  | HelpFuldi除der | [& amp；vert；](https://d.pr/i/Q0mA) |
|  | ReviewWarnotElpful | [否](https://d.pr/i/Q0mA) |
| 投票模式 | VoteTitle | 這項審閱是否有用？ |
|  | VotteDown投票 | 否 |
|  | VoterePlyTitle | 這個回覆是否有用？ |
|  | VoteTitle | 這個注釋是否有用？ |
|  | VodeUps投票 | 是 |
| 標幟模型 | 標幟標題 | 標記%s的檢閱 |
|  | 標幟成功 | 已標示評論。 |
| 標幟Mobile | 標幟確認訊息 | 將%s的審核視為%s嗎？ |
| 提及模式 | mentionDefaultText | 我在Livefyre評論中提到了您！ |
| 共用模型 | ShareTitle | 分享評論 |

## 貼文函數 {#section_yl1_wj4_xz}

供使用者張貼評論的字串。

| 元素 | 索引鍵 | 預設文字 |
|---|---|---|
| 編輯者 | bodyplaceHolder | 撰寫評論… |
|  | PostedButton | 編輯 |
|  | PostedVisitButton | 取消 |
|  | PostSutton | 貼文審核… |
|  | PostButton | 貼文審核 |
|  | PostReplicasButton | 貼文… |
|  | potreplyButton | 貼文 |
|  | ShareButton | Share |
|  | titleplaceHolder | 標題… |

## 錯誤 {#section_jbc_vj4_xz}

一般錯誤訊息的可用字串。

| 元素 | 索引鍵 | 預設文字 |
|---|---|---|
| 錯誤 | errorAlreadReaded | 您只能張貼一個評論。 |
|  | errorAutherError | 您無權在此對話中張貼評論 |
|  | errorcomments Notowed | 目前無法張貼評論 |
|  | 錯誤收回意見 | 您不喜歡自己的評論 |
|  | errorDuplicate | 雖然您很喜歡您的評論，但不允許張貼兩次。 |
|  | erroredDuplicate | 當您編輯時，必須變更評論的內文。 |
|  | erroredNotAllowed | 您不得編輯此對話的評論。 |
|  | erroredTimeTimeed | 抱歉，您的評論編輯期間已過期。 |
|  | errorEmpty | 您似乎嘗試張貼空白審核。 |
|  | errorEmptyTitle | 您似乎嘗試張貼空白標題 |
|  | errorfieldering | 星形分級 |
|  | errorfieldReview | review |
|  | errorfieldTitle | title |
|  | errormaxChars | 抱歉，您的評論太長了。請編輯並再試一次。 |
|  | errorMissingFields | 請輸入 |
|  | erroratingEmpty | 您無法提交空白評等 |
|  | erroratingNotSet | 所有評分必須設定 |
|  | erroratingNotValid | 評分必須是物件 |
|  | errorShowmore | 載入更多評論時發生錯誤。 |
|  | errortitlemaChars | 抱歉，您的標題太長。請編輯並再試一次。 |
|  | errorVOTownment | 您無法自行投票 |

