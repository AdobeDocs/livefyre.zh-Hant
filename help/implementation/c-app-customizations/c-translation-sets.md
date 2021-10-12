---
description: 翻譯集可讓您指定應用程式的替代語言。
title: 翻譯集
exl-id: 688138bf-f8e9-4fe5-99e2-2451deefd217
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '1302'
ht-degree: 8%

---

# 翻譯集 {#translation-sets}

翻譯集可讓您指定應用程式的替代語言。

使用翻譯設定將各種語言的應用程式本地化，或從Studio中的一個位置為數個應用程式指定替代文字。 例如，您可以確保所有西班牙語網站的所有應用程式欄位都使用西班牙語。 您也可以修改文字，讓所有欄位都符合您網站或網路的聲音和感覺。

您可以為所有應用程式（Storify 2除外）指定翻譯設定。 如需可本地化的欄位的詳細資訊，請參閱[本地化字串](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md)。

評論、即時部落格和聊天在翻譯集內共用相同的字串集。

指定網路、網站、應用程式或使用API的翻譯集。

不同層級的轉換集將按照此模式相互覆蓋：

* API翻譯集會覆寫任何層級（應用程式、網路和網站）的任何翻譯集
* 應用程式翻譯集會覆寫網路層級和網站層級的翻譯集。
* 站點級轉換集覆蓋網路級轉換集。

## 檢閱文字字串 {#c-review-text-strings}

自訂Livefyre評論的文字字串。

此頁面列出並說明可在「檢閱應用程式」中自訂的字串。 此處列出的字串，除了Livefyre核心應用程式的預設字串之外，也是String Customitions中列出的預設字串的替代項目。 其中列出了重複項，這些表格中列出的字串是「查看」應用程式的預設值。

* 實施
* 審核/評等介面
* 資料流資訊
* 作者/內容資訊
* 使用者動作
* 貼文函式
* 錯誤

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
| --------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| 按鈕 |  |  |
|  | editReviewBtn | 編輯審核 |
|  | reviewBtn | 寫評論 |
|  | reviewsClosed | 已結束審核 |
|  | showReviewBtn | 顯示審閱 |
|  | 追隨 | 我感興趣 |
|  | shareText | 我剛寫了個評論。 看看！ |
| 評等工具提示 |  |  |
|  | ratingValues | 陣列. 預設= [&#39;Poor&#39;、&#39;Poor&#39;、&#39;Fair&#39;、&#39;Fair&#39;、&#39;Average&#39;、&#39;Average&#39;、&#39;Good&#39;、&#39;Good&#39;、&#39;Excellent&#39;、&#39;Excellent&#39;]; |
|  |  | 注意：必須複製陣列中的值，才能將每個星號的左半部和右半部指派相同名稱。 |
| 分級子部件 |  |  |
|  | ratingSubpartPlaceholders | 陣列. 預設值 = [] |
|  | ratingSubpartTitles | 陣列. 預設值 = [] |
|  | reviewStreamTitle | 預設為空白。 評論摘要區段的標題。 |
| 雜項 |  |  |
|  | averageRating | 平均使用者評分 |
|  | breakdownHeader | 評等劃分 |
|  | 實用 | 發現%s個 |
|  | lipedPlural | 發現%s個 |
|  | outOf | / |
|  | ratingType | 星星 |

## 資料流資訊 {#section_wmv_yj4_xz}

可用於內容流資訊和顯示的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| *排序* |  |  |
|  | sortBy | *預設為空白。* |
|  | sortHighestActied | 最高評等 |
|  | sortLowestActied | 最低評等 |
|  | sortMostLapid | 最有用 |
| *流雜項* |  |  |
|  | showMore | 顯示更多 |
| *流速* |  |  |
|  | newComment | 新評論 |
|  | newComments | 新評論 |
| *監聽器計數* |  |  |
|  | listenerCount | 人員監聽 |
|  | listenerCountPlural | 聆聽 |
| *註解計數* |  |  |
|  | commentCountLabel | LiveReviews |
|  | commentCountLabelPlural | LiveReviews |
| *注釋通告程式計數* |  |  |
|  | commentNotifier | 新評論 |
|  | commentNotifierPlural | 新評論 |

## 作者/內容資訊 {#section_osx_xj4_xz}

提供作者和個別內容資訊的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| *線程突破* |  |  |
|  | reviewsContentNotFoundMsg | 此審核不再顯示 |
|  | backToComments | 返回評論 |

## 使用者動作 {#section_tlx_wj4_xz}

可用於用戶操作的字串：標幟、共用和標示現有內容是有用的。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| *註解頁尾* |  |  |
|  | wasReviewHalped | 有用嗎？ |
|  | wasReviewHalipedMobile | 有用嗎？ |
|  | ownWasReviewHalped | 發現有用。 |
|  | reviewWasHalip | 是 |
|  | liveDiferer | &amp;vert; |
|  | reviewWasNotLapid | 無 |
| *投票強制回應* |  |  |
|  | voteTitle | 這篇評論有用嗎？ |
|  | voteDownvote | 無 |
|  | voteReplyTitle | 這個回覆有用嗎？ |
|  | voteTitle | 這個評論有用嗎？ |
|  | voteUpvote | 是 |
| *標幟強制回應視窗* |  |  |
|  | flagTitle | 標籤%s的審核 |
|  | flagSuccessMsg | 已標籤審核。 |
| *標幟行動* |  |  |
|  | flagConfirmationMessage | 是否將%s的審核標籤為%s? |
| *提及強制回應* |  |  |
|  | intersDefaultText | 我在Livefyre評論中提到過你！ |
| *共用強制回應* |  |  |
|  | shareTitle | 共用審核 |

## 貼文函式 {#section_yl1_wj4_xz}

可供發佈評論的使用者使用的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| *編輯器* |  |  |
|  | bodyPlaceholder | 寫評論…… |
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
| 錯誤 |  |  |
|  | errorAlreadPosted | 您只能張貼一個審核。 |
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

## 字串表示 {#c_sidenotes_text_strings}

自訂Livefyre Sidenotes的文字字串

<!-- 

c_sidenotes_text_strings.dita

 -->

此頁面列出並說明可在Sidenotes應用程式中自訂的所有字串。 如需核心Livefyre應用程式可用字串的相關資訊，請參閱字串自訂。

* 實施
* 驗證
* 資料流資訊
* 作者/內容資訊
* 使用者動作
* 貼文函式
* 版主介面
* 錯誤

## 實施 {#section_wp2_ql4_xz}

若要實作此功能，請傳入您要覆寫至Javascript設定物件之字串的1-1物件對應。 如果您未提供欄位，則會使用預設文字。

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

## 驗證 {#section_pqf_3l4_xz}

驗證程式和已驗證使用者功能表中可用的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| *驗證功能表字串* |  |  |
|  | menuAuthSignInBtn | 登入 |
|  | menuAuthSignedInMsg | 您必須登錄到{action} |
|  | menuUserEditProfile | 編輯個人資料 |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | 登出 |
|  | menuUserBackBtn | 全部 |

## 資料流資訊 {#section_wpy_gl4_xz}

可用於內容流資訊和顯示的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| *資訊菜單選項* |  |  |
|  | menuInfoCopyright | © Livefyre, Inc. 2014 |
|  | menuInfoHelp | 說明 |
|  | menuInfoLivefyreLink | 請訪問Livefyre.com |

## 作者/內容資訊 {#section_dhb_gl4_xz}

提供作者和個別內容資訊的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
|  | commentDraditorTag | Mod |
|  | commentPendingTag | 待審 |
|  | commentReadMoreLink | 瞭解更多 |
|  | commentReplyLink | 請參閱{number}個回復 |
|  | commentReplyLinkSing | 請參閱回覆 |
|  | commentVoteCount | 投票 |
|  | commentVoteCountSing | 票 |
|  | datetimeMinutePrefix | m |
|  | datetimeMonths | *陣列. 預設= *[ &#39;Janury&#39;、&#39;二月&#39;、&#39;三月&#39;、&#39;四月&#39;、&#39;五月&#39;、&#39;六月&#39;、&#39;七月&#39;、&#39;八月&#39;、&#39;九月&#39;、&#39;十月&#39;、&#39;十一月&#39;、&#39;十二月&#39; ] |
|  | 問題說明 | 您現在可以直接閱讀和撰寫句子、段落、影像和引號的注釋。 <br>反白標示文字，然後按一下圖示或按一下每個段落結尾的圖示。 |
|  | questionMockText | 「熟悉」的原因並不為人所知，只是因為「熟悉」。 |
|  | questionTitle | 什麼是Sidex? |

## 使用者動作 {#section_qxd_fl4_xz}

可用於用戶操作的字串：標幟、共用和按贊現有內容。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| *回覆功能表選項* |  |  |
|  | menuRepliesViewTitle | 詳細資料 |
|  | menuRepliesViewReply | 回復對話 |
| *共用功能表選項* |  |  |
|  | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | 共用 |
| *標幟功能表選項* |  |  |
|  | menuFlagOptionDiscore | 不同意 |
|  | menuFlagOptionOffension | 進攻 |
|  | menuFlagOptionOffTopic | 關閉主題 |
|  | menuFlagOptionSpam | 垃圾訊息 |
|  | menuFlagTitle | 標幟為…… |
|  | facebookShareCaption | 「{title}」上的字元 |
| *行動使用者選項* |  |  |
|  | sliderCommentTally | 的 |
|  | sliderInviteRead | 已讀取 |
|  | sliderInviteWrite | 寫入 |
|  | sliderLoading | 正在載入… |
|  | sliderWriteText | 你覺得呢？ 點擊以寫入。 |

## 貼文函式 {#section_xzf_2l4_xz}

可供發佈內容的使用者使用的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
|  | editorEditBtn | 儲存 |
|  | editorEditPosting | 正在保存…… |
|  | editorEditReplyTitle | 編輯回覆 |
|  | editorEditTitle | 編輯字型 |
|  | editorPlaceholder | 你覺得呢？ |
|  | editorPostBtn | 貼文字型 |
|  | editorPostBtnMobile | 貼文 |
|  | editorPosting | 發佈… |
|  | editorReplyBtn | 公佈回覆 |
|  | editorReplyTitle | 寫回復 |
|  | editorTitle | 寫字表示 |
|  | emptyImageBlockTxt | 你覺得呢？ |
|  | emptyTextBlockTxt | + |
|  | replyBtn | 回覆 |
|  | threadReplyBtn | 回復對話 |
| *刪除菜單選項* |  |  |
|  | menuConfirmAccept | 是，{action} |
|  | menuConfirmCancel | 取消 |
|  | menuConfirmTitle | 是否確定? |
| *等功能表選項* |  |  |
|  | menuEtcOptionApprove | 核准 |
|  | menuEtcOptionDelete | 刪除 |
|  | menuEtcOptionEdit | 編輯 |
|  | menuEtcOptionFlag | 標幟 |
|  | menuEtcOptionShare | 共用 |
|  | menuEtcPostedAt | 發佈於{date} |
|  | menuEtcTitle | 更多 |

## 版主介面 {#section_o5f_dl4_xz}

用戶驗證版主介面的可用字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| *從「更多」功能表顯示確認訊息* |  |  |
|  | notificationApproved | 已核准 |
|  | notificationDeleted | 已刪除 |
|  | notificationLagted | 已標記 |

## 錯誤 {#section_gtk_cl4_xz}

可用於一般錯誤訊息的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
|  | errorConnection | 哦。 你似乎沒有好的聯繫。 |
|  | errorDuplicate | 我們也喜歡你的紙條，但你不能再發一次。 |
|  | errorGeneral | 發生錯誤. 請重試。 |
|  | errorServer | 我們的伺服器出了問題。 再試一次？ |
