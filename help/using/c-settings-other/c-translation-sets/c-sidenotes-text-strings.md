---
description: 自訂Livefyre Sides的文字字串
title: 字串
exl-id: 132a7c8d-10e1-419c-9d79-a40553e70785
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 13%

---

# 字元號文字字串{#sidenotes-text-strings}

自訂Livefyre Sides的文字字串

本頁列出並說明Sidesars應用程式中可自訂的所有字串。 如需核心Livefyre應用程式可用字串的詳細資訊，請參閱字串自訂。

實作
驗證
串流資訊
作者／內容資訊
使用者動作
貼文功能
協調者介面
錯誤

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
| 驗證菜單字串 | menuAuthSignInBtn | 登入 |
|  | menuAuthSignedInMsg | 您必須登入{action} |
|  | menuUserEditProfile | 編輯個人資料 |
|  | menuUserAdmin | Admin Console |
|  | menuUserLogout | 登出 |
|  | menuUserBackBtn | 全部 |

## 串流資訊{#section_wpy_gl4_xz}

可用於內容串流資訊和顯示的字串。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| 資訊選單選項 | menuInfoCopyright | © Livefyre, Inc. 2014 |
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
|  | datetimeMonths | 陣列. 預設值 =`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | questionExplanation | 您現在可以直接閱讀和寫入句子、段落、影像和引號。<br><br><span class="&rdquo;lf-highlight-text&rdquo;">反白</span> 標示文字， <span class="&rdquo;fycon-write&rdquo;"></span> 然後按一下圖 <span class="&rdquo;fycon-action-view&rdquo;"></span> 示或每個段落結尾的圖示。 |
|  | questionMockText | 「熟悉」的內容並不是眾所周知的，只是因為「熟悉」。 |
|  | questionTitle | 什麼是Sidexer? |

## 用戶操作{#section_qxd_fl4_xz}

用戶操作可用的字串：標幟、分享和按贊現有內容。

| 元素 | 金鑰 | 預設文字 |
|---|---|---|
| 回覆功能表選項 | menuRepliesViewTitle | 詳細資料 |
|  | menuRepliesViewReply | 回覆對話 |
| 共用功能表選項 | menuShareOptionFacebook | Facebook |
|  | menuShareOptionTwitter | Twitter |
|  | menuShareTitle | 共用 |
| 標籤菜單選項 | menuFlagOptionDisproover | 不同意 |
|  | menuFlagOptionOffension | 進攻性 |
|  | menuFlagOptionOffTopic | 關閉主題 |
|  | menuFlagOptionSpam | 垃圾訊息 |
|  | menuFlagTitle | 標幟為…… |
|  | facebookShareCaption | 「{title}」上的字型大小 |
| 行動使用者選項 | sliderCommentTally | 的 |
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
| 刪除菜單選項 | menuConfirmAccept | 是，{action} |
|  | menuConfirmCancel | 取消 |
|  | menuConfirmTitle | 是否確定? |
| Etc功能表選項 | menuEtcOptionApprove | 核准 |
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
| 從「更多」功能表確認訊息 | notificationApproved | 已核准 |
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
