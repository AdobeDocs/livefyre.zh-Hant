---
description: 搭配Livefyre應用程式使用引導和串流API。
seo-description: 搭配Livefyre應用程式使用引導和串流API。
seo-title: 搭配Livefyre應用程式使用引導和串流API
solution: Experience Manager
title: 檢視帳戶詳細資訊
uuid: bace558f-ade8-49d6-abda-9ee754ce4ac0
translation-type: tm+mt
source-git-commit: d615705ccf5e4511cc735ce91d95c3e15d0c0160

---


# 搭配Livefyre應用程式使用引導和串流API {#bootstrap-stream-api}

## 引導API {#bootstrap-api}

### 我要如何擷取最新50個以前的內容？ {#howcontentolder}

引導是Livefyre應用程式中的所有內容。 這是快取的資料，通常是12-20分鐘。 它會以50個片段的區塊傳送，並經過編頁，因此您可以擷取50個以上片段的內容。

[API 參考](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:bootstrap:operations:bs3:v3.1:network:site:article:init:method=get)

[範例要求](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

上述範例請求會載入 `init` 包含「系列設定」和約50個最新內容的唯一初始集合的頁面。 若要輪詢舊內容，您必須載入後續的引導頁面， `N` 其頁碼為：

請求: `https://{networkName}.bootstrap.fyre.co/bs3/v3.1/{network}/{siteId}/{b64articleId}/N.json`

例如，範例應用程式有120個內容。 內容"1"是最舊的內容片段，內容"70"是最新的內容片段。

* `Init` 將以遞減順序載入~120-70個內容： [https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init](https://data.livefyre.com/bs3/v3.1/dharam.fyre.co/384931/NTU1NQ==/init)

* `O.json` 將以遞增順序載入~ 1-50個內容： [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/0.json)

* `1.json` 將以遞增順序載入~ 51-100個內容： [https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/1.json)

* `2.json` 將以遞增順序載入~101-120個內容：[https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json](https://data.livefyre.com/bs3/v3.1//dharam.fyre.co/384931/NTU1NQ==/2.json)

[按一下這裡查看引導輪詢流程圖。](https://marketing-resource-help.s3.amazonaws.com/resources/help/en_US/livefyre/bootstrap-poll-flowchart.pdf)

## 串流API {#stream-api}

什麼是串流API?
串流是一項長時間的民調問答，根據設計，可維持約30秒的開啟時間。 有關長輪詢技術的說明，請參閱： [https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet](https://stackoverflow.com/questions/11077857/what-are-long-polling-websockets-server-sent-events-sse-and-comet)

此長輪詢端點會將新內容（例如，使用者張貼留言）、內容狀態變更（例如使用者刪除其留言、按贊）以及協調內容變更（例如協調者核准某段內容）串流至Livefyre應用程式。

對串流API的請求應為約30秒（長輪詢），在30秒後（當未傳入任何新內容串流時）預期逾時。

API參考： [https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get](https://api.livefyre.com/docs/apis/by-category/collections#operation=urn:livefyre:apis:stream1:operations:v3.1:collection:updates:method=get)

請求範例：

`{"timeout":true,"parked":true,"h":"ct245.dsr.livefyre.com"}`

請注意：串流 `maxEventId` API回應中的事件ID是此回應中最高的事件ID。 當建立下一個 `lastEventId` 串流API請求的URL時，請將此值當做路徑參數，以取得在此回應中所有更新之後發生的更新。

以下範例是以注釋應用程式為基礎：

先張貼「第一條留言」。 「第二條評論」是在之後發佈的。

第一個注釋串流API回應：

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

回 `maxEventId``lastEventId` 覆中的是「1520289700953369」，將用來輪詢端點，以取得在回應中所有更新之後發生的更新（即「第二條評論」）。

第二個注釋流API回應：

`{"timeout":true,"parked":true,"h":"ct239.dsr.livefyre.com"}`

回 `maxEventID` 應中的"1520289700953369"反過來應用於建立串流API回應，以用於下 `lastEventID` 次更新。