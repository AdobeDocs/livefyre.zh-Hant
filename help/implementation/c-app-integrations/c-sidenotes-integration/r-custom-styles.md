---
description: 自訂樣式會透過插入到Sitdenes建構函式中的物件套用。
seo-description: 自訂樣式會透過插入到Sitdenes建構函式中的物件套用。
seo-title: Sitdenes自訂樣式
title: Sitdenes自訂樣式
uuid: 0f6d7ad6-1f6a-4ed2-b86 a-0d03782 e591 e
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Sitdenes自訂樣式{#sidenotes-custom-styles}

自訂樣式會透過插入到Sitdenes建構函式中的物件套用。

「keys」是代表DOM元素的物件索引鍵，而「屬性」則是特定索引鍵的支援CSS屬性。例如，若要自訂BlockTn的樣式(即啓動Sidents popup的按鈕)，則會建構物件，例如：

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

| **索引鍵** | **屬性** | 說明 |
|---|---|---|
| `anonymousAvatar` | 'height'，'width' | 匿名頭像，在文字區域編輯器左側。 |
| `blockBtn` | 'fontColor'，'fontSize'，'left'，'position'，'right'，'top' | 放置於指定為sidenoTe元素之元素旁的「啓動程式圖示」。 |
| `blockBtnActive` | 'fontColor'，'fontSize'，'left'，'position'，'right'，'top' | 啓動圖示時啓動圖示。 |
| `commentAvatar` | 'height'，'width' | 最上層注意事項左側的「頭像」影像。 |
| `commentBody` | 'fontColor'，'fontFamily'，'fontSize'，'fontWave'，'LinHeight' | 執行緒附註的文字內文。 |
| `commentDisplayName` | 'fontColor'，'fontFamily'，'fontSize'，'fontWave'，'LinHeight' | 顯示留下附註之使用者的名稱。 |
| `commentDownvote` | 'fontColor'，'fontSize' | 註解上的「投票」按鈕。 |
| `commentReplyExpand` | 'backgroundColor'，'borderColor'，'BorderWidth'，'fontColor'，'fontFamily'，'fontSize'，'fontWth'，'LinHeight' | 包含大量回覆之執行緒展開的按鈕。 |
| `commentTags` | 'fontColor'，'fontFamily'，'fontSize'，'fontWave'，'LinHeight' | 附註上有關使用者的標記。 |
| `commentUpvote` | 'fontColor'，'fontSize' | 註解上的「投票」按鈕。 |
| `editorTextarea` | 'height'，'width'，'FontColor'，'fontFamily'，'fontSize'，'fontWth'，'LinHeight' | Textarea輸入方塊，以保留附註。 |
| `mediaBlockBtn` | 'fontColor'，'fontSize'，'left'，'position'，'right'，'top' | 媒體啓動器圖示，位於媒體項目(img、視訊)之上。 |
| `mediaBlockBtnActive` | 'fontColor'，'fontSize'，'left'，'position'，'right'，'top' | 媒體啓動器圖示處於作用中狀態。 |
| `numSidenotes` | 'fontColor'、'fontFamily'、「FontSize」、「FontWave」、「Linhight」、「backgroundColor」、「BorderColor」、「borderWidth」、「height」、「width」 | 可點按按鈕，顯示系列中的SitedNotes數目。 |
| `numSidenotesPopover` | 'fontColor'、'fontFamily'、「FontSize」、「FontWave」、「Linhight」、「backgroundColor」、「BorderColor」、「borderWidth」、「height」、「width」 | Popover，並概述使用者的Sitents說明。 |
| `popover` | 'backgroundColor' | 啓動啓動程式圖示時所顯示的POOver。 |
| `popoverArrowLeft` | 'backgroundImage'、'height'、'right'、'right'、'top'、'width' | 快顯視窗上的向左箭頭元素，指向包含啓動器圖示的DOM元素。 |
| `popoverArrorRight` | 'backgroundImage'、'height'、'right'、'right'、'top'、'width' | 快顯視窗上的向右箭頭元素，指向包含啓動器圖示的DOM元素。 |
| `popoverArrowTop` | 'backgroundImage'、'height'、'right'、'right'、'top'、'width' | 快顯視窗上的頂端箭頭元素，指向包含啓動器圖示的DOM元素。 |
| `replyAvatar` | 'height'，'width' | 回覆層級附註左側的頭像影像。 |
| `streamPoweredBy` | 'backgroundColor'，'borderColor'，'Linheight' | 快顯視窗上的「Powered by」頁尾。 |
| `streamQueueButton` | 'backgroundColor'，'borderColor'，'BorderWidth'，'fontColor'，'fontFamily'，'fontSize'，'fontWth'，'LinHeight' | 按鈕以指出新的附註串流何時會變成開啓的快顯視窗。 |
| `userAvatar` | 'height'，'width' | 已驗證使用者的頭像，位於文字區域編輯器左側。 |

