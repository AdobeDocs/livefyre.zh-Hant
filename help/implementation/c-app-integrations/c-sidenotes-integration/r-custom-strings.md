---
title: Siestroms自訂字串
description: Siestroms自訂字串
exl-id: b5e2c18b-5b98-45ff-aa89-dd92a02949a9
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 12%

---

# Siestrops Custom Strings{#sidenotes-custom-strings}

自訂字串會透過插入Sides建構函式的物件套用，並覆寫透過應用程式使用的預設字串。 這些可用來自訂語言的任何部分，以符合您的樣式或語言規格。 字串會自動與預設值合併。

```
var customStrings = { 
   'menuBackBtn': 'return' }; 
new Livefyre.Sidenotes({ 
   strings: customStrings, 
   ...  
});
```

| 金鑰 | 預設值 |
|---|---|
| appName | Siesors |
| commentColdatorTag | 修改 |
| commentPendingTag | 待審 |
| commentReadMoreLink | 瞭解更多 |
| commentReplyLink | 請參閱{number}個回覆 |
| commentReplyLinkSing | 請參閱回覆 |
| commentVoteCount | 投票 |
| commentVoteCountSing | 票 |
| editorPlaceholder | 你覺得呢？ |
| editorPostBtn | 貼文字型大小 |
| editorPostBtnMobile | 貼文 |
| editorPosting | 發佈… |
| editorReplyBtn | 公佈回覆 |
| editorReplyTitle | 寫回覆 |
| editorTitle | 寫注 |
| emptyImageBlockTxt | 你覺得呢？ |
| emptyTextBlockTxt | + |
| errorConnection | 哦。 您似乎沒有良好的關聯。 |
| errorDuplicate | 我們也喜歡您的註解，但您不能再張貼。 |
| errorGeneral | 發生錯誤. 請再試一次。 |
| errorServer | 我們的伺服器出了問題。 再試一次？ |
| facebookShareCaption | 「{title}」上的SideNotes |
| menuAuthSignedInMsg | 您必須登入{action} |
| menuAuthSignInBtn | 登入 |
| menuBackBtn | 上一步 |
| menuConfirmAccept | 是，{action} |
| menuConfirmCancel | 取消 |
| menuConfirmTitle | 是否確定? |
| menuEtcOptionApprove | 核准 |
| menuEtcOptionDelete | 刪除 |
| menuEtcOptionEdit | 編輯 |
| menuEtcOptionFlag | 標幟 |
| menuEtcOptionShare | 共用 |
| menuEtcPostedAt | 張貼於{date} |
| menuEtcTitle | 更多 |
| menuFlagOptionDisproover | 不同意 |
| menuFlagOptionOffension | 進攻性 |
| menuFlagOptionOffTopic | 關閉主題 |
| menuFlagOptionSpam | 垃圾訊息 |
| menuFlagTitle | 標幟為…… |
| menuInfoCopyright | © Livefyre, Inc. 2014 |
| menuInfoHelp | 說明 |
| menuInfoLivefyreLink | 造訪Livefyre.com |
| menuRepliesViewReply | 回覆對話 |
| menuRepliesViewTitle | 詳細資料 |
| menuShareOptionFacebook | Facebook |
| menuShareOptionLink | Copy Permalink |
| menuShareOptionLinkComplete | 已複製 |
| menuShareOptionLinkFailed | 複製失敗 |
| menuShareOptionTwitter | Twitter |
| menuShareTitle | 共用 |
| notificationApproved | 已核准 |
| notificationDeleted | 已刪除 |
| notificationTaged | 已標記 |
| permalinkBackBtn | 全部 |
| permalinkTitle | 佩馬林克 |
| questionExplanation | 您現在可以直接閱讀和寫入句子、段落、影像和引號。<br><br>反白標示文字，然後按一下「fycon-write」圖示，或按一下每個段落結尾的「fycon-action-view」圖示。 |
| questionMockText | 「熟悉」的內容並不是眾所周知的，只是因為「熟悉」。 |
| questionTitle | 什麼是Sidexer? |
| queuedCommentsPlural | {number}新大小表示 |
| queuedCommentsSingular | 1個新字型大小 |
| queuedRepliesPlural | {number}新回覆 |
| queuedRepliesSingular | 1個新回覆 |
| replyBtn | 回覆 |
| signInToPost | 登入以撰寫字型大小 |
| sliderCommentTally | 的 |
| sliderInviteRead | 已讀取 |
| sliderInviteWrite | 寫 |
| sliderWriteText | 你覺得呢？ 點選以寫入 |
| threadCollapseBtn | 收合 |
| threadExpandBtnPlural | 展開{number}個回覆 |
| threadExpandBtnSingular | 展開1個回覆 |
| threadReplyBtn | 回覆對話 |
