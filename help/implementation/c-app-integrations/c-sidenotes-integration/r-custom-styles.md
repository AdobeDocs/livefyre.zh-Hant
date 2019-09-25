---
description: 自訂樣式會透過插入Sidesors建構函式的物件套用。
seo-description: 自訂樣式會透過插入Sidesors建構函式的物件套用。
seo-title: Sidesirs自訂樣式
title: Sidesirs自訂樣式
uuid: 0f6d7ad6-1f6a-4ed2-b86a-0d03782e591e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Sidesirs自訂樣式{#sidenotes-custom-styles}

自訂樣式會透過插入Sidesors建構函式的物件套用。

"keys"是代表DOM元素的物件索引鍵，而"properties"則是特定索引鍵的支援CSS屬性。 例如，要自定義blockBtn的樣式（即啟動Sidespover的按鈕），可以構建一個對象，例如：

```
var styles = { 
   'blockBtn': { 
      'fontColor': '#555', 
      'fontSize': '18px' 
   } 
}; 
new Livefyre.Sidenotes({ 
   customStyles: styles, 
      ...  
})
```

| **代碼** | **屬性** | 說明 |
|---|---|---|
| `anonymousAvatar` | 「height」、「width」 | 匿名頭像影像，位於文字區域編輯器的左側。 |
| `blockBtn` | 「fontColor」、「fontSize」、「left」、「position」、「right」、「top」 | 「啟動器圖示」會放在指定為可顯示的元素旁。 |
| `blockBtnActive` | 「fontColor」、「fontSize」、「left」、「position」、「right」、「top」 | 啟動程式圖示（在作用中狀態時）。 |
| `commentAvatar` | 「height」、「width」 | 頭等級附註左側的頭像。 |
| `commentBody` | 「fontColor」、「fontFamily」、「fontSize」、「fontWeight」、「lineHeight」 | 串接註解的文本主體。 |
| `commentDisplayName` | 「fontColor」、「fontFamily」、「fontSize」、「fontWeight」、「lineHeight」 | 已留下附註的使用者的顯示名稱。 |
| `commentDownvote` | 「fontColor」、「fontSize」 | 註解上的下投按鈕。 |
| `commentReplyExpand` | 「backgroundColor」、「borderColor」、「borderWidth」、「fontColor」、「fontFamily」、「fontSize」、「fontWeight」、「lineHeight」 | 用於擴展具有大量回覆的線程的按鈕。 |
| `commentTags` | 「fontColor」、「fontFamily」、「fontSize」、「fontWeight」、「lineHeight」 | 註解上的使用者標籤。 |
| `commentUpvote` | 「fontColor」、「fontSize」 | 附註上的上投按鈕。 |
| `editorTextarea` | 「height」、「width」、「fontColor」、「fontFamily」、「fontSize」、「fontWeight」、「lineHeight」 | 用於留言的Textarea輸入框。 |
| `mediaBlockBtn` | 「fontColor」、「fontSize」、「left」、「position」、「right」、「top」 | 媒體啟動程式圖示(在媒體項目（img、視訊）上方時)。 |
| `mediaBlockBtnActive` | 「fontColor」、「fontSize」、「left」、「position」、「right」、「top」 | 處於活動狀態的媒體啟動器表徵圖。 |
| `numSidenotes` | 「fontColor」、「fontFamily」、「fontSize」、「fontWeight」、「lineHeight」、「backgroundColor」、「borderColor」、「borderWidth」、「height」、「width」 | 可點按的按鈕，顯示系列中的字型大小數。 |
| `numSidenotesPopover` | 「fontColor」、「fontFamily」、「fontSize」、「fontWeight」、「lineHeight」、「backgroundColor」、「borderColor」、「borderWidth」、「height」、「width」 | 快顯，並對使用者的「Sides」（表示）作簡要說明。 |
| `popover` | 「backgroundColor」 | 呼叫啟動程式圖示時顯示的快顯視窗。 |
| `popoverArrowLeft` | 「backgroundImage」、「height」、「left」、「right」、「top」、「width」 | 快顯欄位上指向包含啟動器圖示之DOM元素的向左箭頭元素。 |
| `popoverArrorRight` | 「backgroundImage」、「height」、「left」、「right」、「top」、「width」 | 快顯欄位上指向包含啟動器圖示之DOM元素的向右箭頭元素。 |
| `popoverArrowTop` | 「backgroundImage」、「height」、「left」、「right」、「top」、「width」 | 快顯欄位上的頂端箭頭元素，指向包含啟動器圖示的DOM元素。 |
| `replyAvatar` | 「height」、「width」 | 回覆層級附註左側的頭像。 |
| `streamPoweredBy` | 「backgroundColor」、「borderColor」、「lineHeight」 | 快顯視窗上的「Powered by」頁尾。 |
| `streamQueueButton` | 「backgroundColor」、「borderColor」、「borderWidth」、「fontColor」、「fontFamily」、「fontSize」、「fontWeight」、「lineHeight」 | 按鈕，指出新註解何時串流至開啟的快顯視窗。 |
| `userAvatar` | 「height」、「width」 | 已驗證使用者的頭像，位於文字區域編輯器的左側。 |

