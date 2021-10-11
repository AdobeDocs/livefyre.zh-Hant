---
title: Livefyre Analytics事件
description: Livefyre Analytics事件
exl-id: ec32414c-0580-44dc-ae5b-6df0b42c0ec3
source-git-commit: 53aead87db517e6f68266a66115889509287a287
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 4%

---

# Livefyre Analytics事件

## 事件對象定義 {#section_dh1_yhn_pdb}

下列程式碼會定義事件物件中的欄位，頁面上的分析處理常式會收到這些欄位。

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

下列Livefyre事件可對應至自訂事件，以便使用「報表套裝管理器」用於報表。 如需Adobe Analytics中報表套裝的詳細資訊，請參閱[報表套裝管理器](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en)。 如需如何搭配「報表套裝管理器」使用Livefyre事件的詳細資訊，請參閱[](../livefyre-analytics/c-use-livefyre-with-adobe-analytics.md#section_iks_kgd_4cb)。

## Livefyre Analytics事件

| 事件 | 說明 |
|---|---|
| 初始化 | 載入至少包含一個Livefyre應用程式的頁面時 |
| 載入 | 無論使用者檢視為何，應用程式只要載入頁面上 |
| 檢視 | 當應用程式首次進入檢視區時。 |
| 貼文 | 每當使用者張貼留言或內容時，包括：頂層貼文、回覆、評論、媒體塗鴉牆上傳 |
| 已張貼 | 貼文成功時。 |
| Twitter_Reply | 使用者每次在Twitter上回覆 |
| Twitter_Like | 內容共用給的位置：回推 |
| Livefyre_Like | 任何時候app中都會使用livefyre贊功能 |
| Livefyre_Noliked | 每當使用者不喜歡Livefyre時， |
| ShareOnPost | 使用者隨時張貼內容並使用分享貼文功能 |
| ShareButtonClick | 每當使用者按一下留言的分享按鈕時 |
| ShareTwitter | 按一下共用至Twitter時 |
| ShareFacebook | 按一下共用至Facebook時 |
| ShareURL | 選取/複製「共用至URL」文字區域時。 |
| 展開回覆 | 當使用者按一下+或展開連結，檢視頂層貼文上的所有回覆時 |
| 折疊回覆 | 使用者按一下 — 或折疊連結時，檢視頂層貼文上的所有回覆 |
| FlagClick | 每次使用者開啟標幟強制回應視窗時 |
| FlagSpam | 當使用者將內容標示為垃圾訊息時 |
| FlagAssore | 當使用者將內容標示為不同意 |
| FlagOffensive | 當使用者將內容標示為冒犯 |
| FlagOffTopic | 使用者將內容標示為關閉主題時 |
| 標籤取消 | 每次使用者提交標幟時按X或「取消」 |
| FollowCollection | 每次有對話（「我對評論感興趣」） |
| UnfollowCollection | 取消對話時 |
| RequestMore | 每當使用者在應用程式中載入更多內容時（也需要有高速度） |
| ModalView | 每當使用者按一下以在強制回應視窗中檢視內容時 |
| TwitterRetweetClick | 內容共用給的位置：回推 |
| PostButtonClick | 當使用者點按貼文時（「您在想什麼？」） 按鈕 |
| 登入 | 每次使用者登入時 |
| 登出 | 每次使用者登出時 |

以下為Livefyre提供的轉換變數(eVar)清單。

## 轉換變數 — eVar

| 事件 | 說明 |
|--- |--- |
| 網路ID | Livefyre中的網路ID/名稱 |
| 應用程式 ID | 應用程式的URN |
| 內容ID | Livefyre中的內容ID |
| 應用程式類型 | Livefyre應用程式類型。 選項: <br><ul><li>即時部落格  </li><li> 功能卡</li><li>轉盤</li><li>聊天室 </li><li>意見</li><li>膠片</li><li>地圖</li><li>馬賽克</li><li>媒體牆</li><li>趨勢分析</li><li>上傳按鈕</li></ul> |
| 內容類型 | Instagram、Twitter、Facebook、LiveFyre、YouTube等 |

## 更多資訊 {#section_b3d_4yl_pdb}

如需本頁討論主題的詳細資訊，請參閱：

* [報表套裝管](https://experienceleague.adobe.com/docs/analytics/admin/manage-report-suites/report-suites-admin.html?lang=en)[理器DTM](https://experienceleague.adobe.com/docs/livefyre/using/apps/filmstrip/c-filmstrip-app.html?lang=en)

* [規則](https://experienceleague.adobe.com/docs/dtm/using/resources/rules/create-rules.html?lang=en)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
