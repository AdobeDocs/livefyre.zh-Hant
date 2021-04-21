---
description: 您可以使用。
title: userPrivacyMaskDelegate
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# userPrivacyMaskDelegate{#userprivacymaskdelegate}

您可以使用。

本文旨在符合GDPR規則。 如果來源不支援Proxy，則Livefyre會在內容上顯示此文字和遮色片，除非使用者點按視訊並核准來自該來源的潛在追蹤。

如果您不使用`userPrivacyMaskDelegate`，則會顯示下列預設文字：

在`userPrivacyOptOut`後面添加`userPrivacyMaskDelegate`。 您可以一次新增所有Livefyre隱私權標幟，作為Livefyre物件的一部分。

以下是如何使用`userPrivacyMaskDelegate`的範例：

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
