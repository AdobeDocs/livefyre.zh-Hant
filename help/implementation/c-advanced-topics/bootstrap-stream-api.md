---
description: 搭配Livefyre應用程式使用Bootstrap和串流API。
title: 查看帳戶詳細資訊
exl-id: b8458954-3727-4c4d-93dd-d21a4328e069
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# 搭配Livefyre應用程式使用Bootstrap和串流API {#bootstrap-stream-api}

## BootstrapAPI {#bootstrap-api}

### 如何擷取早於最新50個片段的內容？ {#howcontentolder}

Bootstrap是Livefyre應用程式中的所有內容。 這是快取的資料，通常為12到20分鐘。 它會以50個片段的大塊傳送，並經過編頁處理，讓您可以擷取50個以上片段的內容。

[API 參考](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[範例要求](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

上述範例要求會載入`init`頁面，其中包含「集合設定」，以及約50個最新內容的唯一初始集合。 若要輪詢舊內容，必須載入後續引導頁面，其中`N`為頁碼：

請求: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

例如，範例應用程式有120個內容片段。 內容「1」是最舊的內容，內容「70」是最新的內容。

* `Init` 會以遞減順序載入~120-70個內容： [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` 會以升序載入~ 1-50個內容：  `https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json`
* `1.json` 會以升序載入~ 51-100個內容：  `https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json`
* `2.json` 會以升序載入~101-120個內容：`https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json`

[按一下這裡查看Bootstrap民調問答流程圖。](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## 串流API {#stream-api}

什麼是Stream API?
資料流是長輪詢，根據設計，此輪詢大約會保持開啟30秒。 如需長輪詢技術的說明，請前往：[https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

此長輪詢端點會將新內容（例如，使用者張貼留言）、內容狀態變更（例如，使用者刪除其留言、按贊）及內容的協調變更（例如，版主核准內容片段）串流至Livefyre應用程式。

當中沒有新內容資料流時，對串流API的要求應約為30秒（長輪詢），且會在30秒後逾時。

API參考：[https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:api:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

範例要求：

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

請注意：串流API回應中的`maxEventId`是此回應中更新的最高事件ID。 建置下一個串流API請求的URL時，請將此值設為`lastEventId`路徑參數，以取得此回應中所有更新之後發生的更新。

以下範例是以「注釋應用程式」為基礎：

首先發佈了「第一條評論」。 「第二條評論」在之後發佈。

第一個注釋流API響應：

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

回應中的`maxEventId`為「1520289700953369」，將作為`lastEventId`輪詢端點，以取得此回應中所有更新之後發生的更新（即第二個註解）。

第二個注釋流API響應：

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

回應中的`maxEventID` &quot;1520289700953369&quot;應循序用作`lastEventID`以建立下次更新的串流API回應。
