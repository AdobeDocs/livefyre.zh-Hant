---
description: 將userPrivacyOptOut標幟新增至頁面，允許網站訪客退出此追蹤。
seo-description: 將userPrivacyOptOut標幟新增至頁面，允許網站訪客退出此追蹤。
seo-title: userPrivacyOptOut
title: userPrivacyOptOut
uuid: a043c50e -a02-4c83-bbce-54b9 b51316 a5
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# userPrivacyOptOut{#userprivacyoptout}

將 `userPrivacyOptOut` 標幟新增至頁面，允許網站訪客退出此追蹤。

Livefyre提供JavaScript事件來追蹤Livefyre應用程式中的使用者活動。

如果您嵌入Livefyre應用程式，而訪客不同意追蹤，則可以動態設定Livefyre以停用功能以確保訪客的隱私權。

設定後，Livefyre將會：

* 停用應用程式中的驗證支援。
* 停用Livecount和事件產生
* 刪除頁面上任何應用程式建立的現有Cookie
* 含有第三方網域影像的Proxy媒體，以防止第三方建立Cookie
* 針對需要額外按一下以檢視的第三方影片，啓用視訊遮色片點進

## 設定退出頁面

內嵌Livefyre應用程式的整合可在網站訪客未使用單一JavaScript變數授予同意時設定Livefyre。

說明：

1. 將 `userPrivacyOptOut` 標幟新增至 `Livefyre.js` JavaScript之前的頁面：

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. 隨處皆可新增 `Livefyre.js` 至頁面 `userPrivacyOptOut`。

   Livefyre應用程式利用提升的隱私權設定進行個體化。

   >[!NOTE]
   >
   >請勿變更Livefyre應用程式載入 `userPrivacyOptOut` 後的值。

如果網站訪客選擇退出，請確定您的同意工作流程將設 `userPrivacyOptOut` 為true。
