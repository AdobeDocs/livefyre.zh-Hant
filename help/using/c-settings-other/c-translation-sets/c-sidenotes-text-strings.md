---
description: 自訂Livefyre SitenDocs的文字字串
seo-description: 自訂Livefyre SitenDocs的文字字串
seo-title: Sites設定文字字串
solution: Experience Manager
title: Sites設定文字字串
uuid: a3735237-e55 d-4bc0-b88 d-8a323980 ee09
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Sites設定文字字串{#sidenotes-text-strings}

自訂Livefyre SitenDocs的文字字串

此頁面列出並說明所有可在Sitents應用程式中自訂的字串。如需核心Livefyre應用程式可用字串的詳細資訊，請參閱字串自訂。

實作驗證串流資訊作者/內容資訊使用者動作貼文函數協調者介面錯誤

## 實施 {#section_wp2_ql4_xz}

若要實施此功能，請傳遞您要覆寫至Javascript組態物件之字串的1-1物件對應。如果您未提供欄位，則會使用預設文字。

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

## 驗證身份 {#section_pqf_3l4_xz}

用於驗證程序的字串，以及來自已驗證的使用者功能表的字串。

| 元素 | 索引鍵 | 預設文字 |
|---|---|---|
| Auth功能表字串 | menuAuthSignInBtn | 登入 |
|  | MenuauthedNedInMsg | 您必須登入{action} |
|  | menuuseredProfile | 編輯描述檔 |
|  | Menuusermin | Admin Console |
|  | 功能表登出 | 登出 |
|  | MenuuserBackBtn | all |

## 串流資訊 {#section_wpy_gl4_xz}

用於內容串流資訊和顯示的字串。

| 元素 | 索引鍵 | 預設文字 |
|---|---|---|
| 資訊功能表選項 | menuInfocoright | © Livefyre，Inc2014 |
|  | 功能表說明 | 說明 |
|  | menuInfoLivefyRelink | 瀏覽Livefyre.com |

## 作者/內容資訊 {#section_dhb_gl4_xz}

可供作者和個別內容資訊使用。

| 元素 | 索引鍵 | 預設文字 |
|---|---|---|
|  | commentModerOrtag | Mod |
|  | 註解標記 | 擱置中 |
|  | commentReadMoreLink | 閱讀更多資訊 |
|  | commentReplicLink | 請參閱{number}回覆 |
|  | CommentReplicyLinkScript | 請參閱回覆 |
|  | CommentVodeCount | 投票數 |
|  | commentVoeCountSING | 投票 |
|  | dateTimeminutePrefix | m |
|  | dateTimeMonthes | 陣列。預設=`[‘January’, ‘February’, ‘March’, ‘April’, ‘May’, ‘June’, ‘July’, ‘August’, ‘September’, ‘October’, ‘November’, ‘December’]` |
|  | 問題說明 | 您現在可以直接在句子、段落、影像和報價上閱讀及撰寫注釋。<br><br><span class="&rdquo;lf-highlight-text&rdquo;">反白標示文字</span> 並按一下 <span class="&rdquo;fycon-write&rdquo;"></span> 圖示，或按一下每個段落結尾處的 <span class="&rdquo;fycon-action-view&rdquo;"></span> 圖示。 |
|  | QuestionModkText | 「熟悉的」是不正確的，只是因為它是「熟悉」的原因。 |
|  | QuestionTitle | 甚麼是Sitenote？ |

## 使用者動作 {#section_qxd_fl4_xz}

適用於使用者動作的字串：標幟、分享和美化現有內容。

| 元素 | 索引鍵 | 預設文字 |
|---|---|---|
| 回覆功能表選項 | 功能表檢視標題 | 詳細資料 |
|  | 功能表檢視回覆 | 回覆對話 |
| 共用選單選項 | MenuShareoptionFacebook | Facebook |
|  | menuShareoptionTwitter | Twitter |
|  | MenuShareTitle | Share |
| 旗標功能表選項 | 功能表選擇不同意 | 不同意 |
|  | MenustlaoptionAttensive | 侵犯性 |
|  | MenuFLAoptionOff主題 | 關閉主題 |
|  | MenuFLAoptionSpam | 垃圾訊息發送者 |
|  | 功能表標題 | 標幟為… |
|  | FacebookShaRerection | Sitdents on「{title}」 |
| 行動使用者選項 | 投影片注釋 | of |
|  | SliderInviteRead | Read |
|  | 投影片編寫 | 寫入 |
|  | 投影片載入 | 正在載入… |
|  | SliderWriteExt | 您想甚麼？點選以寫入。 |

## 貼文函數 {#section_xzf_2l4_xz}

適用於張貼內容的使用者可用字串。

| 元素 | 索引鍵 | 預設文字 |
|---|---|---|
|  | editoredBtn | 儲存 |
|  | editoredPoking | 儲存… |
|  | editoredReplicyTitle | 編輯回覆 |
|  | editoredTitle | 編輯Sitenote |
|  | editorPlaceHolder | 您想甚麼？ |
|  | editorPostBtn | Post Sidenote |
|  | editorPostBnobile | 貼文 |
|  | editorPosting | 張貼… |
|  | editorRebytn | 貼文回覆 |
|  | editorReplicyTitle | 寫入回覆 |
|  | editorTitle | Write Sitenote |
|  | EmptyImageBocktXT | 您想甚麼？ |
|  | EmptyTextBlockXT | + |
|  | ReplicTBN | 回覆 |
|  | PublishRebtn | 回覆對話 |
| 刪除功能表選項 | menuConfirmAccept | 是的，{action} |
|  | MenuConfirmCancel | 取消 |
|  | menuConfirmTitle | 您確定嗎？ |
| 功能表選項 | 功能表內容核准 | 批准 |
|  | menueToptionDelete | 刪除 |
|  | menueToptionEdit | 編輯 |
|  | menueToptionFlag | 旗標 |
|  | menueToptionShare | Share |
|  | MenuetcPostStedat | 張貼於{date} |
|  | menuetCit標題 | 更多 |

## 協調者介面 {#section_o5f_dl4_xz}

用戶驗證的協調者介面可用字串。

| 元素 | 索引鍵 | 預設文字 |
|---|---|---|
| 來自「更多」功能表的確認訊息 | notificationApproved | 已核准 |
|  | notifications已刪除 | 已刪除 |
|  | 通知標幟 | 已標記 |

## 錯誤 {#section_gtk_cl4_xz}

一般錯誤訊息的可用字串。

| 元素 | 索引鍵 | 預設文字 |
|---|---|---|
|  | errorConnection | 嗯h-h.您似乎沒有良好的聯繫。 |
|  | errorDuplicate | 我們也喜歡您的注意事項，但無法張貼兩次。 |
|  | errorGeneral | 發生錯誤。請再試一次。 |
|  | errorServer | 我們的伺服器發生錯誤。再試一次嗎？ |

