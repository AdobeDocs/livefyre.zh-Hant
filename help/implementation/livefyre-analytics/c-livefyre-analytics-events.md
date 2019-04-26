---
description: null
seo-description: null
seo-title: Livefyre Analytics Events
solution: Experience Manager
title: Livefyre Analytics Events
uuid: 4eb5a196-ca33-40f8-a96 d-ed46469223 de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre Analytics Events {#livefyre-analytics-events}

## 事件物件定義 {#section_dh1_yhn_pdb}

下列程式碼定義了頁面上分析處理常式收到之事件物件中的欄位。

```
{
  evars: {
    appId : string : URN ID of the app
    appType : string : Type of the app
    contentType : string : Type of the content that this event pertains to
    contextId : string : URN ID of the contextual item that this event pertains to
    environment : string : Environment that this app is using
    networkId : string : Network that this app is using
    publishedDate : number : Epoch time when the app was published
    userLoggedIn : boolean : If a user is logged in
  },
  generator: {
    env : string: Environment that this app is using
    id : string: URN ID of the app
    name : string: Name of the app
    networkId : string: Network that this app is using
    source : string: URN of the collection
    version : string: Semver version of the app
  },
  startTime : number: Epoch time when event was created
  type : string: Event type (Table 1)
}
```

## Livefyre Analytics Events和eVar {#section_u3k_tft_mcb}

下列Livefyre事件，可映射至使用報表套裝管理器在報表中使用的自訂事件。如需Adobe Analytics中報表套裝的詳細資訊，請參閱 [報表套裝管理器](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)。如需如何搭配「報表套裝管理器」使用Livefyre事件的詳細 [](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb)資訊，請參閱。

## Livefyre Analytics Events

| Event | 說明 |
|---|---|
| Init | 當包含至少一個Livefyre應用程式的頁面載入時 |
| 載入 | 無論使用者檢視，任何時候都載入應用程式至頁面 |
| 檢視 | 應用程式第一次進入檢視區時。 |
| 貼文 | 每當使用者張貼留言或內容包含前：頂層貼文、回覆、評論、媒體塗鴉牆上傳 |
| 已張貼 | 當貼文成功時。 |
| Twitter_回覆 | 任何時候使用者在Twitter上回覆 |
| Twitter_贊 | 內容分享至：回推 |
| Livefyre_贊 | 任何時候livefyre like功能都會用於應用程式 |
| Livefyre_收回贊 | 任何時候使用者收回livefyre livefyre |
| ShareOnPost | 隨時張貼使用者貼文內容並使用貼文功能上的分享 |
| ShareBootClick | 每當使用者按一下注釋上的分享按鈕時 |
| ShareTwitter | 按一下「分享至Twitter」 |
| ShareFacebook | Clare to Facebook is clicked |
| ShareUrl | 「共用至URL」文字區域已選取/複製。 |
| ExpandReprections | 使用者按一下+或展開連結，以檢視頂層貼文上的所有回覆 |
| 折疊功能 | 使用者按一下或折疊連結時，檢視頂層貼文上的所有回覆 |
| 旗標 | 使用者隨時開啓標幟模型 |
| 旗標 | 當使用者將內容標幟為垃圾訊息時 |
| 標幟同意 | 當使用者標幟內容時， |
| 旗標侵犯性 | 當使用者將內容標示為冒犯性 |
| 標幟主題 | 使用者將內容標示為off主題 |
| 旗標取消 | 當使用者提交標幟時，只要按一下X或「取消」 |
| FourboCollection | 隨時關注對話(「我有興趣」在評論中) |
| UnForboCollection | 未關注對話 |
| 詳細資訊 | 每當使用者在應用程式中載入更多內容(需要高速執行時) |
| ModalView | 使用者每次點按以檢視模式中的內容 |
| TwitterRetweetClick | 內容分享至：回推 |
| PostbuttonClick | 當使用者點按貼文時(「您的心思是甚麼？「))button |
| 登入 | 任何使用者登入 |
| 登出 | 使用者登出時 |

以下是Livefyre提供的轉換變數(eVar)清單。

## 轉換變數- eVar

| Event | 說明 |
|--- |--- |
| 網路ID | Livefyre中的網路ID/名稱 |
| 應用程式ID | 應用程式的URN |
| 上下文ID | Livefyre中的內容ID |
| 應用程式類型 | Livefyre App Type.選項： <br><ul><li>即時部落格  </li><li> 功能卡</li><li>轉盤</li><li>聊天室 </li><li>注釋</li><li>幻燈片幻燈片</li><li>地圖</li><li>Mosaic</li><li>Media Wall</li><li>趨勢分析</li><li>上傳按鈕</li></ul> |
| 內容類型 | Instagram、Twitter、Facebook、Livefyre、YouTube等等 |

## 更多資訊 {#section_b3d_4yl_pdb}

如需本頁討論主題的詳細資訊，請參閱：

* [Report Suite ManagerDTM](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)[](https://marketing.adobe.com/resources/help/en_US/livefyre/c_filmstrip_app.html)

* [規則](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre. js](/help/implementation/c-livefyre.js.md)