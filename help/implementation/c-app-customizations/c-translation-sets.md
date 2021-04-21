---
description: 翻譯集可讓您指定應用程式的替代語言。
title: 翻譯集
exl-id: 688138bf-f8e9-4fe5-99e2-2451deefd217
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1343'
ht-degree: 7%

---

# 翻譯集{#translation-sets}

翻譯集可讓您指定應用程式的替代語言。

<!-- 
c_translation_sets.dita
-->

使用翻譯設定，將應用程式當地語系化為多種語言，或從Studio中的一個位置為數個應用程式指定替代文字。 例如，您可以確保所有西班牙文網站在所有應用程式欄位都使用西班牙文。 您也可以修改文字，讓所有欄位都符合您網站或網路的語音和感覺。

您可以為所有應用程式（Storify 2除外）指定翻譯設定。 有關可本地化的欄位的詳細資訊，請參閱[本地化字串](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md)。

「注釋」、「即時部落格」和「聊天」在翻譯集內共用相同的字串集。

指定網路、網站、應用程式或使用API的轉譯集。

不同級別的翻譯集會按照此模式相互覆蓋：

* API轉換集會覆寫任何層級（應用程式、網路和網站）的轉換集
* 應用程式轉譯集會覆寫網路層級和網站層級的轉譯集。
* 站點級翻譯集覆蓋網路級翻譯集。

## 查看文本字串{#c-review-text-strings}

自訂Livefyre評論的文字字串。

此頁面列出並說明可在「檢閱」應用程式中自訂的字串。 此處列出的字串除了Livefyre核心應用程式的預設字串外，也會覆寫，列在「字串自訂」中。 其中列出重複項目時，這些表格中列出的字串是「檢閱」應用程式的預設值。

* 實施
* 審查／評分介面
* 串流資訊
* 作者／內容資訊
* 使用者動作
* 貼文功能
* 錯誤

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
| --------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| 按鈕 |  |  |
|  | editReviewBtn | 編輯審核 |
|  | reviewBtn | 撰寫審核 |
|  | reviewsClosed | 已結束審核 |
|  | showReviewBtn | 顯示審核 |
|  | follow | 我感興趣 |
|  | shareText | 我剛寫了個評論。 看看！ |
| 評分工具提示 |  |  |
|  | ratingValues | 陣列. 預設值= [「貧窮」、「貧窮」、「公平」、「公平」、「平均」、「平均」、「良好」、「良好」、「優秀」、「優秀」]; |
|  |  | 注意：必須複製陣列中的值，才能將每個星形的左半部和右半部都指定為相同名稱。 |
| 分級子部件 |  |  |
|  | ratingSubpartPlaceholders | 陣列. 預設值 = [] |
|  | ratingSubpartTitles | 陣列. 預設值 = [] |
|  | reviewStreamTitle | 預設為空白。 評論摘要部分的標題。 |
| 其他 |  |  |
|  | averageRating | 平均使用者評分 |
|  | breakdownHeader | 分級劃分 |
|  | 幫助 | 發現%s有幫助 |
|  | helpedPlural | 發現%s有幫助 |
|  | outOf | / |
|  | ratingType | 星星 |

## 串流資訊{#section_wmv_yj4_xz}

可用於內容串流資訊和顯示的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| *排序* |  |  |
|  | sortBy | *預設為空白。* |
|  | sortHighestAdied | [最高評分](https://d.pr/i/huTd) |
|  | sortLeomthAding | [最低評分](https://d.pr/i/huTd) |
|  | sortMostHappiled | [最有用](https://d.pr/i/huTd) |
| *串流雜項。* |  |  |
|  | showMore | 顯示更多 |
| *流高速* |  |  |
|  | newComment | 新評論 |
|  | newComments | 新評論 |
| *監聽器計數* |  |  |
|  | listenerCount | 監聽 |
|  | listenerCountPlural | 傾聽 |
| *注釋計數* |  |  |
|  | commentCountLabel | LiveReviews |
|  | commentCountLabelPlural | LiveReviews |
| *注釋通告程式計數* |  |  |
|  | 注釋通告程式 | 新評論 |
|  | commentNotifierPlural | 新評論 |

## 作者／內容資訊{#section_osx_xj4_xz}

可供作者和個別內容資訊參考。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| *線程插頭* |  |  |
|  | reviewsContentNotFoundMsg | [此審閱不再顯示](https://d.pr/i/svXs) |
|  | backToComments | 返回評論 |

## 用戶操作{#section_tlx_wj4_xz}

用戶操作可用的字串：標幟、共用和標示現有內容有用。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| *注釋頁尾* |  |  |
|  | wasReviewHappiled | [有用嗎？](https://d.pr/i/Q0mA) |
|  | wasReviewHampileMobile | 有用嗎？ |
|  | ownWasReviewHappiled | [發現有幫助。](https://d.pr/i/Q0mA) |
|  | reviewWasHappiled | [是](https://d.pr/i/Q0mA) |
|  | libledDiferar | [&amp;vert;](https://d.pr/i/Q0mA) |
|  | reviewWasNotHappiled | [否](https://d.pr/i/Q0mA) |
| *投票模式* |  |  |
|  | voteTitle | 此評論有用嗎？ |
|  | voteDownvote | 無 |
|  | voteReplyTitle | 這個回覆有用嗎？ |
|  | voteTitle | 這句評論有用嗎？ |
|  | voteUpvote | 是 |
| *標幟模式* |  |  |
|  | flagTitle | 標籤%s的審核 |
|  | flagSuccessMsg | 已標籤審核。 |
| *標幟行動* |  |  |
|  | flagConfirmationMessage | 是否將%s的審核標幟為%s? |
| *提及模式* |  |  |
|  | 提及次數DefaultText | 我在Livefyre評論中提到過你！ |
| *共用模式* |  |  |
|  | shareTitle | 分享評論 |

## 貼文函式{#section_yl1_wj4_xz}

發佈審核的使用者可使用的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| *編輯器* |  |  |
|  | bodyPlaceholder | 撰寫評論…… |
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
| 錯誤 |  |  |
|  | errorAlreadyPosted | 您只能張貼一份審核。 |
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

## 字元號文字字串{#c_sidenotes_text_strings}

自訂Livefyre Sides的文字字串

<!-- 

c_sidenotes_text_strings.dita

 -->

本頁列出並說明Sidesars應用程式中可自訂的所有字串。 如需核心Livefyre應用程式可用字串的詳細資訊，請參閱字串自訂。

* 實施
* 驗證
* 串流資訊
* 作者／內容資訊
* 使用者動作
* 貼文功能
* 協調者介面
* 錯誤

## 實施 {#section_wp2_ql4_xz}

若要實作此功能，請傳入您要覆寫之字串的1-1物件對應至Javascript設定物件。 如果您未提供欄位，則會使用預設文字。

範例:

```
var customStrings = { 
   postAsButton: "New Post As Text", 
   postEditButton: "New Post Edit Text" 
}; 
networkConfig["strings"] = customStrings; fyre.conv.load( 
   networkConfig, 
   [convConfig], 
   function(){} 
);
```

## 驗證{#section_pqf_3l4_xz}

驗證程式和已驗證用戶菜單中可用的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| *驗證菜單字串* |  |  |
|  | menuAuthSignInBtn | 登入 |
|  | menuAuthSignedInMsg | 您必須登入{action} |
|  | menuUserEditProfile | 編輯個人資料 |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | 登出 |
|  | menuUserBackBtn | 全部 |

## 串流資訊{#section_wpy_gl4_xz}

可用於內容串流資訊和顯示的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| *資訊選單選項* |  |  |
|  | menuInfoCopyright | © Livefyre, Inc. 2014 |
|  | menuInfoHelp | 說明 |
|  | menuInfoLivefyreLink | 造訪Livefyre.com |

## 作者／內容資訊{#section_dhb_gl4_xz}

可供作者和個別內容資訊參考。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
|  | commentColdatorTag | 修改 |
|  | commentPendingTag | 待審 |
|  | commentReadMoreLink | 瞭解更多 |
|  | commentReplyLink | 請參閱{number}個回覆 |
|  | commentReplyLinkSing | 請參閱回覆 |
|  | commentVoteCount | 投票 |
|  | commentVoteCountSing | 票 |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | *陣列. 預設值= *[ 「1月」、「2月」、「3月」、「4月」、「5月」、「6月」、「7月」、「8月」、「9月」、「10月」、「11月」、「12月」] |
|  | questionExplanation | 您現在可以直接閱讀和寫入句子、段落、影像和引號。 <br>反白標示文字，然後按一下圖示，或按一下每個段落結尾的圖示。 |
|  | questionMockText | 「熟悉」的內容並不是眾所周知的，只是因為「熟悉」。 |
|  | questionTitle | 什麼是Sidexer? |

## 用戶操作{#section_qxd_fl4_xz}

用戶操作可用的字串：標幟、分享和按贊現有內容。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| *回覆功能表選項* |  |  |
|  | menuRepliesViewTitle | 詳細資料 |
|  | menuRepliesViewReply | 回覆對話 |
| *共用功能表選項* |  |  |
|  | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | 共用 |
| *標籤菜單選項* |  |  |
|  | menuFlagOptionDisproover | 不同意 |
|  | menuFlagOptionOffension | 進攻性 |
|  | menuFlagOptionOffTopic | 關閉主題 |
|  | menuFlagOptionSpam | 垃圾訊息 |
|  | menuFlagTitle | 標幟為…… |
|  | facebookShareCaption | 「{title}」上的字型大小 |
| *行動使用者選項* |  |  |
|  | sliderCommentTally | 的 |
|  | sliderInviteRead | 已讀取 |
|  | sliderInviteWrite | 寫 |
|  | sliderLoading | 正在載入… |
|  | sliderWriteText | 你覺得呢？ 點選以寫入。 |

## 貼文函式{#section_xzf_2l4_xz}

可供發佈內容之使用者使用的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
|  | editorEditBtn | 儲存 |
|  | editorEditPosting | 正在保存…… |
|  | editorEditReplyTitle | 編輯回覆 |
|  | editorEditTitle | 編輯字型大小 |
|  | editorPlaceholder | 你覺得呢？ |
|  | editorPostBtn | 貼文字型大小 |
|  | editorPostBtnMobile | 貼文 |
|  | editorPosting | 發佈… |
|  | editorReplyBtn | 公佈回覆 |
|  | editorReplyTitle | 寫回覆 |
|  | editorTitle | 寫字型大小 |
|  | emptyImageBlockTxt | 你覺得呢？ |
|  | emptyTextBlockTxt | + |
|  | replyBtn | 回覆 |
|  | threadReplyBtn | 回覆對話 |
| *刪除菜單選項* |  |  |
|  | menuConfirmAccept | 是，{action} |
|  | menuConfirmCancel | 取消 |
|  | menuConfirmTitle | 是否確定? |
| *Etc功能表選項* |  |  |
|  | menuEtcOptionApprove | 核准 |
|  | menuEtcOptionDelete | 刪除 |
|  | menuEtcOptionEdit | 編輯 |
|  | menuEtcOptionFlag | 標幟 |
|  | menuEtcOptionShare | 共用 |
|  | menuEtcPostedAt | 張貼於{date} |
|  | menuEtcTitle | 更多 |

## 協調者介面{#section_o5f_dl4_xz}

用戶驗證的協調器介面可用的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| *從「更多」功能表確認訊息* |  |  |
|  | notificationApproved | 已核准 |
|  | notificationDeleted | 已刪除 |
|  | notificationTaged | 已標記 |

## 錯誤 {#section_gtk_cl4_xz}

一般錯誤訊息的字串可用。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
|  | errorConnection | 哦。 您似乎沒有良好的關聯。 |
|  | errorDuplicate | 我們也喜歡您的註解，但您不能再張貼。 |
|  | errorGeneral | 發生錯誤. 請再試一次。 |
|  | errorServer | 我們的伺服器出了問題。 再試一次？ |
