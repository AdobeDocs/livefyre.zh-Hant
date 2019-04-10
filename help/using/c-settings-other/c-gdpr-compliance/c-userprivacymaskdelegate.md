---
description: 您可以變更使用視訊遮色片上顯示的警告文字。
seo-description: 您可以變更使用視訊遮色片上顯示的警告文字。
seo-title: userPrivacyMaskDelegate
solution: Experience Manager
title: userPrivacyMaskDelegate
uuid: 8e5a2750-bb45-4e70-a5 f9-37f5 e7 c61 f8 e
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

您可以變更使用視訊遮色片上顯示的警告文字。

此文字適用於遵循GDPR法規。如果來源不支援Proxy，則Livefyre會在內容上顯示此文字和遮罩，除非使用者按一下視訊並核准來源的潛在追蹤。

如果您未使用 `userPrivacyMaskDelegate`，則會顯示下列預設文字：

新增 `userPrivacyMaskDelegate``userPrivacyOptOut`後，您可以一次將所有Livefyre隱私標幟加入一個Livefyre物件中。

以下是如何使用 `userPrivacyMaskDelegate`的範例：

```
userPrivacyMaskDelegate: function () { 
    var container = document.createElement('div'); 
    var firstParagraph = document.createElement('p'); 
    firstParagraph.innerHTML = 'Text of first paragraph'; 
    var secondParagraph = document.createElement('p'); 
    secondParagraph.innerHTML = 'Text of second paragraph'; 
    container.appendChild(firstParagraph); 
    container.appendChild(secondParagraph); 
    return container; 
}
```
