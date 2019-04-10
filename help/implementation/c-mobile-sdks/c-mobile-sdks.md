---
description: 將Livefyre新增至您的原生行動應用程式。
seo-description: 將Livefyre新增至您的原生行動應用程式。
seo-title: 行動SDK
solution: Experience Manager
title: 行動SDK
uuid: 84c7ca1c-3401-492a-bfa5-62b996947 a44
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 行動SDK{#mobile-sdks}

將Livefyre新增至您的原生行動應用程式。

行動實作有幾個可用選項，視您打算進行的自訂程度而定：

* 行動網頁應用程式
* Livefyre Android或iOS SDK
* HTTP API

## 行動網頁應用程式 {#section_t2k_vpb_11b}

在行動裝置上開啓網頁的客戶會自動取得已針對行動裝置最佳化的Livefyre內容串流，包括樣式，以符合螢幕大小和修改來處理觸控事件。

>[!NOTE]
>
>在Android WebView中使用Livefyre應用程式時，Android [WebSettings. setDomStoreEnabled](https://developer.android.com/reference/android/webkit/WebSettings.html) 參數必須設為true。如果localStorage未啓用，Livefyre將無法將使用者記錄至Livefyre應用程式。

若要針對行動裝置最佳化，Livefyre會限制「注釋」、「即時部落格」和「聊天應用程式」功能集，以包括：

* 貼文
* 編輯
* 旗標
* 贊
* 回覆
* 偵聽程式計數
* 注釋計數
* 內嵌協調
* 暫存卡片
* 熱門意見
* 熱門話題
* 佇列註解

在「行動Web應用程式」中，按一下作者的名稱會開啓新頁面中的暫存卡片資訊。

## Livefyre Android SDK或iOS SDK {#section_zdz_spb_11b}

Livefyre也提供兩種行動SDK：iOS SDK和Android SDK。這些SDK會包住我們的HTTP端點，以提供更輕鬆的方式來傳送和接收資料。這些SDK不提供介面，因此可提供更大的彈性，讓您運用內容在行動應用程式中顯示和使用的方式。

Android和iOS SDK支援「注釋」、「即時部落格」和「聊天」的下列功能：

| iOS功能： | Android功能： |
|--- |--- |
| <ul><li> 貼文 </li><li>編輯 </li><li>旗標 </li><li>贊 </li><li>回覆 </li><li>熱門話題</li></ul> | <ul><li>貼文 </li><li>編輯 </li><li>贊 </li><li>回覆 </li><li>熱門話題</li></ul> |

## HTTP API {#section_yqb_qpb_11b}

HTTP API是可讓您在Livefyre平台上建立對話和內容的端點群組。它還能讓所有Livefyre擺脫包裝串流的束縛。雖然此解決方案需要從您的工程團隊獲得更多的開發時間，但在使用Livefyre產品套件時提供更大的彈性，並允許原生行動整合。

>[!IMPORTANT]
>
>**請勿** 在行動用戶端建立使用者驗證Token，因為這會要求您在不安全的應用程式中公開Livefyre機密網路金鑰。如需更強穩且安全的解決方案，請參閱「使用者驗證預付碼」區段。

