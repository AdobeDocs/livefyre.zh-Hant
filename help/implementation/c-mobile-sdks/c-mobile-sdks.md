---
description: 將Livefyre新增至原生行動應用程式。
title: 行動 SDK
exl-id: e05001a4-6199-4d98-a661-123e031b657b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 4%

---

# 行動 SDK{#mobile-sdks}

將Livefyre新增至原生行動應用程式。

行動裝置實作有幾種可用的選項，視您計畫進行的自訂程度而定：

* 行動網路應用程式
* Livefyre Android或iOS SDK
* HTTP API

## 行動網路應用程式{#section_t2k_vpb_11b}

在行動裝置上開啟網頁的客戶會自動取得針對行動裝置最佳化的Livefyre內容串流，包括可符合螢幕大小的樣式，以及可處理觸控事件的修改。

>[!NOTE]
>
>在Android WebView中使用Livefyre應用程式時，Android [WebSettings.setDomStorageEnabled](https://developer.android.com/reference/android/webkit/WebSettings.html)參數必須設為true。 如果未啟用localStorage,Livefyre將無法將使用者登入Livefyre應用程式。

為了針對行動裝置最佳化，Livefyre將「註解」、「即時部落格」和「聊天應用程式」功能集限制為：

* 貼文
* 編輯
* 標幟
* 讚
* 回覆
* 監聽器計數
* 注釋計數
* 內嵌待定協調
* 氣墊船
* 熱門意見
* 熱線程
* 佇列注釋

在「行動網路應用程式」中，按一下作者的名稱會開啟新頁面中的懸浮卡片資訊。

## Livefyre Android SDK或iOS SDK {#section_zdz_spb_11b}

Livefyre也提供兩種行動SDK:iOS SDK和Android SDK。 這些SDK是HTTP端點的包裝函式，旨在提供更輕鬆的資料傳送和接收方法。 這些SDK不提供介面，讓您在行動應用程式中顯示和使用內容時有更大的彈性。

Android和iOS SDK支援下列注釋、即時部落格和聊天功能：

| iOS功能： | Android功能： |
|--- |--- |
| <ul><li> 貼文 </li><li>編輯 </li><li>標幟 </li><li>讚 </li><li>回覆 </li><li>熱線程</li></ul> | <ul><li>貼文 </li><li>編輯 </li><li>讚 </li><li>回覆 </li><li>熱線程</li></ul> |

## HTTP API {#section_yqb_qpb_11b}

HTTP API是端點群組，可讓您在Livefyre平台上建立對話和內容。 此外，它還可讓所有Livefyre立即可用的串流加電。 雖然此解決方案需要工程團隊投入更多的開發時間，但在使用Livefyre產品套件時，卻能提供更大的彈性，並可進行原生行動整合。

>[!IMPORTANT]
>
>**請不** 要在行動用戶端中建立使用者驗證Token，因為這需要您在不安全的應用程式中公開您的Livefyre機密網路金鑰。如需更強穩且安全的解決方案，請參閱「使用者驗證Token」區段。
