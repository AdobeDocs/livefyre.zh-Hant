---
description: 搭配使用Bootstrap和Stream API搭配Livefyre應用程式。
seo-description: 搭配使用Bootstrap和Stream API搭配Livefyre應用程式。
seo-title: 搭配使用Bootstrap和Stream API與Livefyre應用程式
solution: Experience Manager
title: 檢視帳戶詳細資訊
uuid: bace558f-ad8-49d6-abda-9ee754 ce4 ac0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 搭配使用Bootstrap和Stream API與Livefyre應用程式 {#bootstrap-stream-api}

## 啓動載入API {#bootstrap-api}

### 如何擷取超過最新50個片段的內容？ {#howcontentolder}

Bootstrap是Livefyre應用程式中的所有內容。它是快取資料，通常是12-20分鐘。它是以50小塊的區塊傳送，並加以編頁，您可以擷取超過50個片段的內容。

[API參考](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[範例要求](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

上述範例請求載入 `init` 包含「系列設定」的頁面，以及唯一一組~50個最新內容集。若要民調問答舊內容，您必須載入後續的啓動載入頁面作為 `N` 頁碼：

要求： `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

例如，範例應用程式有120個內容片段。內容「1」是最舊的內容片段，「70」是最新的內容片段。

* `Init` 將會以遞減順序載入~120-70個內容片段： [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` 將會以遞增順序載入~1-50個內容片段： [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` 將會以遞增順序載入~51-100個內容片段： [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` 將會以遞增順序載入~101-120個內容片段：[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[按一下此處查看啓動載入民調流程圖。](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## 串流API {#stream-api}

甚麼是Stream API？
串流是一項長民調問答，其設計目的是要保持開啓約30秒。長篇投票技巧說明可在此處找到： [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

這個長輪詢端點串流新內容(例如使用者張貼留言)、內容狀態變更(例如使用者刪除他們的留言、按贊)和協調內容的協調變更(例如協調者核准一個內容)至Livefyre應用程式。

對串流API的要求應為~30秒(長輪詢)，並在沒有新內容串流時30秒後逾時。

API參考： [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

範例要求：

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

請注意： `maxEventId` 串流API回應是此回應中更新的最高事件ID。當您建立下次串流API請求的URL時，請使用此值做為 `lastEventId` 路徑參數，以取得在此回應中所有更新後發生的更新。

下列範例以「注釋應用程式」為基礎：

首先張貼「第一個注釋」備注。「第二個注釋」張貼之後。

第一個注釋串流API回應：

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

回應中的 `maxEventId` 「152028970095369」會用來民調問答 `lastEventId` 端點以取得更新(亦即第二個留言)發生在此回應中的所有更新之後。

第二個意見串流API回應：

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

回應中的 `maxEventID` 「152028970095369」應輪流用來建立 `lastEventID` 下次更新的串流API回應。