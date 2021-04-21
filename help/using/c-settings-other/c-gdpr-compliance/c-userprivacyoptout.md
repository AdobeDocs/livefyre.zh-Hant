---
description: 將userPrivacyOptOut旗標新增至頁面，讓網站訪客可選擇退出此追蹤。
title: userPrivacyOptOut
exl-id: 1e935e69-60af-4151-905c-93a1cccbeb49
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# userPrivacyOptOut{#userprivacyoptout}

將`userPrivacyOptOut`標幟新增至頁面，讓網站訪客選擇退出此追蹤。

Livefyre提供JavaScript事件，可追蹤Livefyre應用程式中的使用者活動。

如果您嵌入Livefyre應用程式，而訪客不同意追蹤，您可以動態設定Livefyre以停用功能，以確保訪客的隱私權。

設定後，Livefyre將：

* 停用應用程式中的驗證支援。
* 停用Livecount和事件產生
* 刪除頁面上任何應用程式建立的現有Cookie
* 代理媒體與來自第三方網域的影像，以防止第三方建立Cookie
* 針對需要額外按一下才能檢視的第三方影片啟用視訊遮色片點進功能

## 設定退出頁面

內嵌Livefyre應用程式的整合可在網站訪客未使用單一JavaScript變數授與同意時設定Livefyre。

說明:

1. 將`userPrivacyOptOut`標幟新增至`Livefyre.js` JavaScript之前的頁面：

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. 將`Livefyre.js`新增至`userPrivacyOptOut`後的任何位置。

   Livefyre應用程式會以提升的隱私權設定執行個體化。

   >[!NOTE]
   >
   >載入Livefyre應用程式後，請勿變更`userPrivacyOptOut`的值。

如果網站訪客選擇退出，請確定您的同意工作流程將`userPrivacyOptOut`設為true。
