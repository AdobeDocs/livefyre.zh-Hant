---
description: 讓搜尋引擎爬蟲程式可使用社群內容。
title: BootstrapHTML
exl-id: 22ab4f2d-f433-4805-b0dd-16d4531e425d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---

# BootstrapHTML

讓搜尋引擎爬蟲程式可使用社群內容。

如需可用端點的完整清單，請參閱「Livefyre [API參考](https://api.livefyre.com/docs)」一節。

Livefyre應用程式要求您在頁面上執行JavaScript，以顯示系列的內容。 由於大部分搜尋引擎爬蟲程式無法執行JavaScript，因此無法看到您社群所張貼的內容。 使用BootstrapHTML API，將此內容的可搜尋片段新增至頁面的初始HTTP回應，讓您的內容和關鍵字可改善搜尋引擎最佳化。

>[!NOTE]
>
>此API僅適用於「注釋」和「即時部落格集合」類型。

## 整合

Livefyre的BootstrapHTML API會傳回您的使用者內容的HTML片段，該片段可能會包含在頁面的HTTP回應中。 搜尋引擎爬蟲程式可讀取此回應，而不執行任何JavaScript。 當頁面在使用者的瀏覽器上線後，HTML片段將會以完整的互動式介面工具集取代，而且使用者將能夠張貼內容。

要實施BootstrapHTML API:

1. 向下述BootstrapHTML端點提出伺服器對伺服器API的要求。

   >[!NOTE]
   >
   >如果您嘗試擷取BootstrapHTML以進行尚未存在的對話（亦即，如果您尚未內嵌應用程式或建立系列），您將會收到200份，但內容看起來類似：`<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. 如果您的傳回不包含內容中包含&quot;404&quot;，請將其儲存為字串。 您可快取此回應以供日後使用，以避免在每個頁面載入時要求BootstrapHTML API。
1. 將BootstrapHTML字串插入您希望內容出現的網頁。
1. 將您的網頁提供給瀏覽器（或搜尋引擎爬蟲）。

## 資源

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## 參數

* **networkName** 您的Livefyre提供的網路名稱。例如：*labs*&#x200B;在`labs.fyre.co`中。
* **網** 站ID系列的網站ID。
* **b64articleId** 使用base64url編碼的系列文章ID。

## 範例

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## 回應

```
https://gist.github.com/ec5c2457322faf9cf515 
```
