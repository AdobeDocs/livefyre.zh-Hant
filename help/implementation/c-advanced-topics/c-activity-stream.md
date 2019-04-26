---
description: 瞭解如何監視和儲存流經Livefyre系統的使用者產生的內容。
seo-description: 瞭解如何監視和儲存流經Livefyre系統的使用者產生的內容。
seo-title: 活動資料流
solution: Experience Manager
title: 活動資料流
uuid: f40dec1-58ab-41c9-aac4-d2 d8 d8 c9192 bb9
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 活動資料流 {#activity-stream}

瞭解如何監視和儲存流經Livefyre系統的使用者產生的內容。

使用Activity Stream API，使用使用者產生的資料來瀏覽您網路或網站上的Livefyre系統。例如：使用此API的資料來根據評分更新您的搜尋索引，或根據第三方系統來管理使用者的標章。

Activity Stream API：

有關可用端點的完整清單，請參閱「Livefyre API參考」區段。

## 資源 {#section_aql_n4l_b1b}

有兩個端點，一個用於測試環境，另一個用於生產環境。

### 測試階段

```
GET https://bootstrap.t402.livefyre.com/api/v3.1/activity/ 
```

### Production

```
GET https://bootstrap.livefyre.com/api/v3.1/activity/ 
```

### 參數

* **資源：***字串* 的字串A URN，用於請求活動資料。

* **因為：***整數* A64位元整數，代表您最後收到之事件的ID。如果您沒有舊資料，請指定「0」。

## URN字串 {#section_skl_q4l_b1b}

範例:

* **urn：livefyre：**`example.fyre.co` 活動的活動串流 `example.fyre.co`。
* **urn：livefyre：**`example.fyre.co:site=54321``example.fyre.co` 網路下網站54321的活動串流。

## Token政策 {#section_nwh_c5j_11b}

Activity Stream API使用OAuth Beader Token進行驗證。Bearer Token是OAuth2.0規格的一部分，並正式說明 [](https://tools.ietf.org/html/rfc6750#section-1.2)。

Token包含幾個項目：

* 建立代號的對象。
* 有人收到代號。
* 不再有效的時間。
* 我們正在進行的工作。
* 已授予的權限清單。

### 步驟

建立OAuth Beader Token的步驟包括：

* 建立包含發行商、對象、主旨、有效期和範圍的地圖/字典。
* 使用JWT程式庫(含您的機密)來編碼JWT Token。
* 新增「驗證：您的HTTP要求。

下面的程式碼範例顯示Python中的上述步驟：

```
import time 
import jwt 
  
# network data goes here: 
network = "timeout-0.fyre.co" 
network_secret = "...replaceme..." 
  
# api URN 
api_urn = "urn:livefyre:api:core=GetActivityStream" 
  
# expires in 10 seconds 
expiration = int(time.time() + 10) 
  
network_urn = "urn:livefyre:" + network 
  
data = dict(iss=network_urn, aud=network_urn, sub=network_urn, scope=api_urn, exp=expiration) 
  
token = jwt.encode(data, key=network_secret)
```

定位代碼金鑰的定義如下：

* **iss***(發行商)* 具有產生Token權限的實體。這可能是Livefyre、網站或網路。(如果是遲到的注意事項，則是您的家長。)
* **ad***(對象)* 產生此代號的人員。如果您要自行建立代號，則是網站或網路。
* **子***(主旨)* 要授予權限的主旨。例如，如果您要在系列上作業，主旨必須是系列的識別碼。(在學校的範例中，就是您。)
* **exp***(過期)* 的時間點，該點不會再有效。
* **範圍***(範圍)* 這是主旨授予的權限清單。範例為「遲到」。API的名稱就是另一個範例。

## 範例 {#section_dhl_ytj_11b}

```
curl -H "Authorization: Bearer <BEARER TOKEN>" https://bootstrap.livefyre.com/api/v3.1/activity/?resource=&since=
```

## 回應 {#section_gs2_stj_11b}

```
{ 
"code": 200,  
"data": { 
  "annotations": {},  
  "authors": {  
      /** "a set of every author who generated activity within this window" */ 
      "_up1770425@livefyre.com": { 
        "avatar": "https://gravatar.com/avatar/68c789597150d3e941769a5c0a0c4249/?s=50&d=https://avatars-qa.fyre.co/a/anon/50.jpg",  
        "displayName": "ross_pfahler",   
        "id": "_up1770425@livefyre.com",  
        "profileUrl": "https://www.qa-ext.livefyre.com/profile/1770425/",  
        "tags": [],  
        "type": 1 
      },  
  ... 
  },  
  "collections": {  
      /** "a set of every collection for which an activity was generated" */ 
      "2486601": { 
        "articleIdentifier": "75",  
        "id": "2486601",  
        "site": "290596",  
        "title": "Live Blog",  
        "url": "https://orangesaregreat.com/..." 
      }, 
  ... 
  },  
  /** "the maximum event ID for this window" */ 
  "maxEventId": 1383508243715211, 
  "states": {  
      /** "a set of messages (comments, reviews, etc) for which activity  
           was generated in this window, represents the compiled 
           'state' of the object including visible actions on that object 
           (up-votes, likes, and etc.)" */ 
      "3ad6480eb00c4895b29b7a972380f489@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "annotations": { 
                "rating": [ 90 ], /** "this object is a Rating (4.5)" */ 
                "vote": [ 
                    { 
                      "author": "_up1792695@livefyre.com",  
                      "collectionId": "2486685",  
                      "value": 1 
                    } 
                ] 
              },  
              "attachments": [  
              /** "a list of oembeds; the body of this Rating included  
                  this Youtube video" */ 
                { 
                  "author_name": "mauricio890",  
                  "author_url": "https://www.youtube.com/user/mauricio890",  
                  "height": 480,  
                  "html": "<iframe width=\"854\" height=\"480\" src=\"https://www.youtube.com/embed/pmMAw5a7POU?autoplay=1&feature=oembed\" frameborder=\"0\" allowfullscreen></iframe>",  
                  "link": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "provider_name": "YouTube",  
                  "provider_url": "https://www.youtube.com/",  
                  "thumbnail_height": 360,  
                  "thumbnail_url": "https://i1.ytimg.com/vi/pmMAw5a7POU/hqdefault.jpg",  
                  "thumbnail_width": 480,  
                  "title": "Napoleon Dynamite dance scene",  
                  "type": "video",  
                  "url": "https://www.youtube.com/watch?v=pmMAw5a7POU",  
                  "version": "1.0",  
                  "width": 854 
                } 
              ],  
              // "who authored the content" 
              "authorId": "_up1793160@livefyre.com",  
              "bodyHtml": "<p><strong>Pros:</strong>Boom</p><p><strong>Cons:</strong>Goes</p><p><strong>Description:</strong>The dynamite:</p><p><a href=\"https://www.youtube.com/watch?v=pmMAw5a7POU\" target=\"_blank\" rel=\"nofollow\">https://www.youtube.com/watch?v=pmMAw5a7POU</a><br/></p>",  
              // "UNIX timestamp" 
              "createdAt": 1383257354,  
              "id": "3ad6480eb00c4895b29b7a972380f489@livefyre.com",  
              // "non-empty only if this were a reply" 
              "parentId": "", 
              // "UNIX timestamp"  
              "updatedAt": 1383257356  
          },  
          // "the event ID of this state." 
          "event": 1383369320554187,  
          "lastVis": 3,  
          "source": 0,  
          "type": 0,  
          // "Object visibility: 0 = deleted, 1 = everyone, 2 = bozo,  
          // 3 = owner + admins (e.g. premod)" 
          "vis": 1  
      },  
      "5943789": { 
          "collectionId": "2486688",  
          "content": { 
            "annotations": { 
                // "posted by a moderator" 
                "moderator": true  
            },  
            "authorId": "_up1792872@livefyre.com",  
            "bodyHtml": "<p>This is a regular comment from a moderator</p>",  
            "createdAt": 1383372338,  
            "id": "5943789",  
            "parentId": "",  
            "updatedAt": 1383372338 
          },  
          "event": 1383372338732492,  
          "lastVis": 0,  
          "source": 5,  
          "type": 0,  
          "vis": 1 
      },  
      "863c616a2c0c44239feed0914c282d7c@livefyre.com": { 
          "collectionId": "2486685",  
          "content": { 
              "id": "863c616a2c0c44239feed0914c282d7c@livefyre.com" 
          },  
          "event": 1383371303805767,  
          "lastVis": 1,  
          "source": 0,  
          "type": 0,  
          "vis": 0 // "0 = deleted; this object was removed" 
      },  
  ... 
},  
"meta": { 
  // "this describes position in the stream" 
  "cursor": {  
    // "maximum number of objects returned in a single call through this API" 
    "limit": 50,  
    // "the final position in the stream, and from where data should be requested" 
    "next": 1383508243715211, 
    // "the initial position (the 'since' parameter value in this request)" 
    "self": 0  
  } 
},  
"status": "ok" 
} 
```

自上次請求以來的新資料回應：

```
{ 
    "code": 200,  
    "data": { 
        "annotations": {},  
        "authors": {},  
        "collections": {},  
        "maxEventId": -1,  
        "states": {} 
    },  
    "meta": { 
        "cursor": { 
            "limit": 50, 
            /** "indicates there is no data beyond 1383508243715211" */  
            "next": null, 
            "self": 1383508243715211 
        } 
    },  
    "status": "ok" 
}
```

## 附註 {#section_hj3_crj_11b}

* 成功呼叫API將會產生HTTP200狀態代碼。所有其他狀態代碼都應視為錯誤。
* 如果非null，請將值當做 `data.meta.cursor.next` 下一個請求 `since` 的參數使用。
* 如果值是 `data.meta.cursor.next` 空值，表示沒有要使用的新資料。您應稍後再重新要求 `since` ，以查看新資料是否已送達。
* 實際上，如果 `data.meta.cursor.next` 值為非null，您應立即請求更多資料。
* 在生產中，最新的資料大約需要小時。
* 您應設定程序，經常在cron工作上輪詢此端點，以避免遺失資料。在大多數實施中，分鐘間隔應非常適當。
