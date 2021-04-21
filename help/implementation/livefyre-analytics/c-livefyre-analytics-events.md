---
title: Livefyre Analytics事件
description: Livefyre Analytics事件
exl-id: ec32414c-0580-44dc-ae5b-6df0b42c0ec3
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 4%

---

# Livefyre Analytics事件

## 事件對象定義{#section_dh1_yhn_pdb}

下列程式碼定義事件物件中，頁面上的分析處理常式所接收的欄位。

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

## Livefyre Analytics事件和eVar {#section_u3k_tft_mcb}

下列Livefyre事件可對應至使用「報表套裝管理員」的自訂事件，以用於報表。 如需Adobe Analytics地區報表套裝的詳細資訊，請參閱[報表套裝管理員](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)。 如需如何搭配報表套裝管理員使用Livefyre事件的詳細資訊，請參閱[](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb)。

## Livefyre Analytics事件

| 事件 | 說明 |
|---|---|
| 初始化 | 載入至少包含一個Livefyre應用程式的頁面時 |
| 載入 | 任何時候，無論使用者檢視為何，應用程式都會載入頁面 |
| 檢視 | 當應用程式第一次進入檢視區時。 |
| 貼文 | 每當使用者張貼評論或內容時，包括：頂層貼文、回覆、評論、媒體塗鴉牆上傳 |
| 已張貼 | 當貼文成功時。 |
| Twitter_回覆 | 只要使用者在Twitter回覆 |
| Twitter | 將內容共用給的位置：回推 |
| Livefyre_Like | 只要Livefyre贊功能在應用程式中使用， |
| Livefyre_Niliked | 只要使用者不喜歡Livefyre, |
| ShareOnPost | 每當使用者張貼內容並使用分享貼文功能時 |
| ShareButtonClick | 只要使用者按一下留言上的分享按鈕 |
| ShareTwitter | 按一下「分享給Twitter」 |
| ShareFacebook | 按一下「分享給Facebook」 |
| ShareURL | 選取／複製「共用至URL」文字區域時。 |
| 展開回覆 | 當使用者按一下+或展開連結，以檢視頂層貼文上的所有回覆時 |
| 收合回覆 | 當使用者按一下——或收合連結以檢視頂層貼文上的所有回覆時 |
| FlagClick | 只要使用者開啟「標幟模式」 |
| FlagSpam | 當使用者將內容標示為垃圾訊息 |
| FlagSaverious | 當使用者將內容標示為不同意 |
| FlagOffension | 當使用者將內容標示為冒犯性 |
| FlagOffTopic | 當使用者將內容標示為關於主題時 |
| 標幟取消 | 只要使用者在提交標幟時按X或「取消」, |
| FollowCollection | 只要在對話之後（「我對評論感興趣」） |
| UnfollowCollection | 取消對話時 |
| 請求更多 | 每當使用者在應用程式中載入更多內容時（也需要高速度） |
| ModalView | 只要使用者按一下以檢視模式中的內容， |
| TwitterRetweetClick | 將內容共用給的位置：回推 |
| PostButtonClick | 當使用者按一下貼文時（「您在想什麼？」） 按鈕 |
| 登入 | 任何使用者登入 |
| 登出 | 任何使用者登出時 |

以下是Livefyre提供的轉換變數(eVar)清單。

## 轉換變數- eVar

| 事件 | 說明 |
|--- |--- |
| 網路ID | Livefyre中的網路ID/名稱 |
| 應用程式 ID | 應用程式的URN |
| 內容ID | Livefyre中的內容ID |
| 應用程式類型 | Livefyre應用程式類型。 選項: <br><ul><li>即時部落格  </li><li> 功能卡</li><li>轉盤</li><li>聊天室 </li><li>意見</li><li>幻燈片</li><li>地圖</li><li>馬賽克</li><li>媒體牆</li><li>趨勢分析</li><li>上傳按鈕</li></ul> |
| 內容類型 | Instagram、Twitter、Facebook、LiveFyre、YouTube等 |

## 更多資訊 {#section_b3d_4yl_pdb}

如需本頁所討論主題的詳細資訊，請參閱：

* [報表套裝管](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)[理器DTM](https://docs.adobe.com/content/help/en/livefyre/using/apps/filmstrip/c-filmstrip-app.html)

* [規則](https://docs.adobe.com/content/help/en/dtm/using/resources/rules/create-rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
