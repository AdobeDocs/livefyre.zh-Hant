---
description: 將userPrivacyOptOut旗標新增至頁面，讓網站訪客可選擇退出此追蹤。
seo-description: 將userPrivacyOptOut旗標新增至頁面，讓網站訪客可選擇退出此追蹤。
seo-title: userPrivacyOptOut
title: userPrivacyOptOut
uuid: a043c50e-0a02-4c83-bbce-54b9b51316a5
translation-type: tm+mt
source-git-commit: 9e01dd4515c01154e3566a39b367b8efa4ec082a

---


# userPrivacyOptOut{#userprivacyoptout}

將旗標 `userPrivacyOptOut` 新增至頁面，讓網站訪客可選擇退出此追蹤。

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

1. 將標幟 `userPrivacyOptOut` 新增至JavaScript之前的 `Livefyre.js` 頁面：

   ```
   window.Livefyre = {userPrivacyOptOut: true};
   ```

1. 隨 `Livefyre.js` 處新增至頁面 `userPrivacyOptOut`。

   Livefyre應用程式會以提升的隱私權設定執行個體化。

   >[!NOTE]
   >
   >Livefyre應用程式載入後， `userPrivacyOptOut` 請勿變更其值。

如果網站訪客選擇退出，請確 `userPrivacyOptOut` 定您的同意工作流程將設為true。
