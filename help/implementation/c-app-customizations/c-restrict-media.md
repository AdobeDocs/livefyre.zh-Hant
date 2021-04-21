---
description: 限制進入應用程式串流的媒體類型。
title: 限制媒體
exl-id: ae09a058-41de-4b63-8654-cc82f5abad14
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '97'
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
