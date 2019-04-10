---
description: 翻譯集可讓您指定應用程式的替代語言。
seo-description: 翻譯集可讓您指定應用程式的替代語言。
seo-title: 翻譯集
solution: Experience Manager
title: 翻譯集
uuid: 8ba66a61-5520-482a-bc0 b-e4 f6 b57 f1744
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 翻譯集 {#translation-sets}

翻譯集可讓您指定應用程式的替代語言。

<!-- 
c_translation_sets.dita
-->

使用翻譯設定，將各種語言的應用程式當地語系化，或從Studio的一個位置指定多個應用程式的替代文字。例如，您可以確保所有西班牙文語言網站都使用西班牙文語言，適用於所有應用程式欄位。您也可以修改文字，讓所有欄位都符合您網站或網路的語音和感覺。

您可以為所有應用程式指定轉譯設定，但Storify除外。如需您可本地化之欄位的詳細資訊，請參閱 [本地化字串](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md)。

「留言」、「即時部落格」和「聊天」會在翻譯集中共用同一組字串。

指定網路、網站、應用程式或使用API的翻譯集。

不同層級的翻譯集會依照下列模式覆蓋彼此：

* API轉譯集會覆寫任何層級的翻譯集(應用程式、網路和網站)
* 應用程式翻譯集會覆寫網路層級和網站層級轉譯集。
* 網站層級轉譯集會覆寫網路層級轉譯集。

## 檢閱文字字串 {#c-review-text-strings}

自訂Livefyre評論的文字字串。

此頁面列出並說明可供「檢閱」應用程式自訂的字串。此處列出的字串除了適用於Livefyre核心應用程式的預設字串外，也包含在字串自訂中。若列出重復項目，這些表格中列出的字串就是「檢閱」應用程式的預設值。

* 實施
* 審查/評分介面
* 串流資訊
* 作者/內容資訊
* 使用者動作
* 貼文函數
* 錯誤

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
| --------------- | ------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| 按鈕 |  |  |
|  | editReviewBTn | 編輯評論 |
|  | ReviewBTn | 寫作評論 |
|  | 重新檢視關閉 | 評論已關閉 |
|  | ShowreviewBtn | 顯示評論 |
|  | following | 我很感興趣 |
|  | ShareText | 我剛撰寫了評論。立即查看！ |
| 評分工具提示 |  |  |
|  | ratingValues | 陣列。預設=['Poor'、「Poor」、「Fair」、「Fair」、「平均」、「Good」、「Good」、「Good」、「Excine」、「Excine」]； |
|  |  | 注意：陣列中的值必須重復，以指派每個星號的左側和右側名稱。 |
| 分級子集 |  |  |
|  | ratingSubpartpleets | 陣列。預設=[] |
|  | ratingSubpartitals | 陣列。預設=[] |
|  | reviewStreamTitle | 預設為空白。評論摘要區段的標題。 |
| Misc |  |  |
|  | averagering | 使用者平均評分 |
|  | 劃分標題 | 排名劃分 |
|  | 有用 | %s的%s發現實用 |
|  | HelpFultimultiple | %s的%s發現實用 |
|  | Out Over | / |
|  | ratingType | 星形 |

## 串流資訊 {#section_wmv_yj4_xz}

用於內容串流資訊和顯示的字串。

| 元素 | 索引鍵 | 預設文字 |
|---|---|---|
| *排序順序* |  |  |
|  | SortBy | *預設為空白。* |
|  | SorthigheSoft | [最高評分](https://d.pr/i/huTd) |
|  | sortloweSoft | [最低評分](https://d.pr/i/huTd) |
|  | sortmosthelpful | [最實用](https://d.pr/i/huTd) |
| *串流錯誤。* |  |  |
|  | 展示更多資訊 | 顯示更多資訊 |
| *串流高速* |  |  |
|  | NewComment | 新評論 |
|  | NewComments | 新評論 |
| *偵聽程式計數* |  |  |
|  | ListenerCount | 個人監聽 |
|  | listenercountmtium | 受眾監聽 |
| *注釋計數* |  |  |
|  | 注釋標籤 | LivereViews |
|  | 注釋縮寫 | LivereViews |
| *注釋通知計數* |  |  |
|  | CommentNotifier | 新評論 |
|  | comnotifiertimtional | 新評論 |

## 作者/內容資訊 {#section_osx_xj4_xz}

可供作者和個別內容資訊使用。

| 元素 | 索引鍵 | 預設文字 |
|---|---|---|
| *執行緒劃分* |  |  |
|  | reviewsContentNotectNotsg | [此評論不再顯示](https://d.pr/i/svXs) |
|  | 回覆注釋 | 返回評論 |

## 使用者動作 {#section_tlx_wj4_xz}

適用於使用者動作的字串：標記、共用和標示現有內容有幫助。

| 元素 | 索引鍵 | 預設文字 |
|---|---|---|
| *注釋頁尾* |  |  |
|  | WasreviewWhilful | [有用嗎？](https://d.pr/i/Q0mA) |
|  | WasreviewHelpFulmobile | 有用嗎？ |
|  | ownwasreviewWhelpful | [發現實用。](https://d.pr/i/Q0mA) |
|  | 評論實用 | [是](https://d.pr/i/Q0mA) |
|  | HelpFuldi除der | [& amp；vert；](https://d.pr/i/Q0mA) |
|  | ReviewWarnotElpful | [否](https://d.pr/i/Q0mA) |
| *投票模式* |  |  |
|  | VoteTitle | 這項審閱是否有用？ |
|  | VotteDown投票 | 否 |
|  | VoterePlyTitle | 這個回覆是否有用？ |
|  | VoteTitle | 這個注釋是否有用？ |
|  | VodeUps投票 | 是 |
| *標幟模型* |  |  |
|  | 標幟標題 | 標記%s的檢閱 |
|  | 標幟成功 | 已標示評論。 |
| *標幟Mobile* |  |  |
|  | 標幟確認訊息 | 將%s的審核視為%s嗎？ |
| *提及模式* |  |  |
|  | mentionDefaultText | 我在Livefyre評論中提到了您！ |
| *共用模型* |  |  |
|  | ShareTitle | 分享評論 |

## 貼文函數 {#section_yl1_wj4_xz}

供使用者張貼評論的字串。

| 元素 | 索引鍵 | 預設文字 |
|---|---|---|
| *編輯者* |  |  |
|  | bodyplaceHolder | 撰寫評論… |
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
| 錯誤 |  |  |
|  | errorAlreadReaded | 您只能張貼一個評論。 |
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

## Sites設定文字字串 {#c_sidenotes_text_strings}

自訂Livefyre SitenDocs的文字字串

<!-- 

c_sidenotes_text_strings.dita

 -->

此頁面列出並說明所有可在Sitents應用程式中自訂的字串。如需核心Livefyre應用程式可用字串的詳細資訊，請參閱字串自訂。

* 實施
* Auth
* 串流資訊
* 作者/內容資訊
* 使用者動作
* 貼文函數
* 協調者介面
* 錯誤

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
| *Auth功能表字串* |  |  |
|  | menuAuthSignInBtn | 登入 |
|  | MenuauthedNedInMsg | 您必須登入{action} |
|  | menuuseredProfile | 編輯描述檔 |
|  | Menuusermin | Admin Console |
|  | 功能表登出 | 登出 |
|  | MenuuserBackBtn | all |

## 串流資訊 {#section_wpy_gl4_xz}

用於內容串流資訊和顯示的字串。

| 元素 | 索引鍵 | 預設文字 |
|---|---|---|
| *資訊功能表選項* |  |  |
|  | menuInfocoright | © Livefyre，Inc2014 |
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
|  | dateTimeMonthes | *陣列。預設=*[ '月'、'月'、'月'、'月'、'月'、'月'、'月'、'月'、'月'、'11月'、'11月'、'12月'、'12月'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、'12'、''7d'、'12'、''7d'、'12'、'''、''' ] |
|  | 問題說明 | 您現在可以直接在句子、段落、影像和報價上閱讀及撰寫注釋。<br>反白標示文字並按一下圖示，或按一下每個段落結尾處的圖示。 |
|  | QuestionModkText | 「熟悉的」是不正確的，只是因為它是「熟悉」的原因。 |
|  | QuestionTitle | 甚麼是Sitenote？ |

## 使用者動作 {#section_qxd_fl4_xz}

適用於使用者動作的字串：標幟、分享和美化現有內容。

| 元素 | 索引鍵 | 預設文字 |
|---|---|---|
| *回覆功能表選項* |  |  |
|  | 功能表檢視標題 | 詳細資料 |
|  | 功能表檢視回覆 | 回覆對話 |
| *共用選單選項* |  |  |
|  | MenuShareoptionFacebook | Facebook |
|  | menuShareoptionTwitter | Twitter |
|  | MenuShareTitle | Share |
| *旗標功能表選項* |  |  |
|  | 功能表選擇不同意 | 不同意 |
|  | MenustlaoptionAttensive | 侵犯性 |
|  | MenuFLAoptionOff主題 | 關閉主題 |
|  | MenuFLAoptionSpam | 垃圾訊息發送者 |
|  | 功能表標題 | 標幟為… |
|  | FacebookShaRerection | Sitdents on「{title}」 |
| *行動使用者選項* |  |  |
|  | 投影片注釋 | of |
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
| *刪除功能表選項* |  |  |
|  | menuConfirmAccept | 是的，{action} |
|  | MenuConfirmCancel | 取消 |
|  | menuConfirmTitle | 您確定嗎？ |
| *功能表選項* |  |  |
|  | 功能表內容核准 | 批准 |
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
| *來自「更多」功能表的確認訊息* |  |  |
|  | notificationApproved | 已核准 |
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
