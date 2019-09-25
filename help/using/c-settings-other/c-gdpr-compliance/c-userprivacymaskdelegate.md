---
description: 您可以使用。
seo-description: 您可以使用。
seo-title: userPrivacyMaskDelegate
solution: Experience Manager
title: userPrivacyMaskDelegate
uuid: 8e5a2750-bf45-4e70-a5f9-37f5e7c61f8e
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

您可以使用。

本文旨在符合GDPR規則。 如果來源不支援Proxy，則Livefyre會在內容上顯示此文字和遮色片，除非使用者點按視訊並核准來自該來源的潛在追蹤。

如果您不使用， `userPrivacyMaskDelegate`會顯示下列預設文字：

在之 `userPrivacyMaskDelegate` 後加 `userPrivacyOptOut`入。 您可以一次新增所有Livefyre隱私權標幟，作為Livefyre物件的一部分。

以下是如何使用的範例 `userPrivacyMaskDelegate`:

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
