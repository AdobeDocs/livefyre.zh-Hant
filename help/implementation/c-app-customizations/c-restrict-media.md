---
description: 限制進入應用程式串流的媒體類型。
seo-description: 限制進入應用程式串流的媒體類型。
seo-title: 限制媒體
solution: Experience Manager
title: 限制媒體
uuid: c470c985-d221-4f39-8bd4-4e44ec14db95
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# 限制介質{#restrict-media}

限制進入應用程式串流的媒體類型。

依預設，所有媒體附件都可內嵌至「應用程式」中。 Livefyre可讓您變更此選項，以防止使用者將選取的附件類型張貼至您的應用程式。

>[!NOTE]
>
>Livefyre與Embedly合作，以整合媒體。 如需詳細資訊，請參閱「內容整合>內嵌整合」。 如需連結擴充或來源的相關問題，請連絡您的技術客戶經理。

此範例會封鎖YouTube和Vimeo內嵌於您的留言串流：

```
var attachmentDelegate = function(embedObj) { 
   var providersToBlock = ['youtube', 'vimeo']; 
   for (var i=0, len=providersToBlock.length; i<len; i++) { 
      if (embedObj.provider_url.indexOf(providersToBlock[i]) > -1) { 
         return false; 
      } 
   } 
   return true; 
};
```

載入對話時：

```
networkConfig["attachmentDelegate"] = attachmentDelegate; 
fyre.conv.load(networkConfig, [convConfig]);
```

