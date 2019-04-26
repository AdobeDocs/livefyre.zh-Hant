---
description: 讓社群內容可供搜尋引擎編目程式使用。
seo-description: 讓社群內容可供搜尋引擎編目程式使用。
seo-title: 啓動載入HTML
solution: Experience Manager
title: 啓動載入HTML
uuid: 137e4382-4e7b-4124-9d35-1d872a497bc7
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 啓動載入HTML

讓社群內容可供搜尋引擎編目程式使用。

有關可用端點的完整清單，請參閱「Livefyre [API參考](https://api.livefyre.com/docs) 」區段。

Livefyre應用程式要求您在頁面上執行JavaScript，以顯示您的系列的內容。由於大部分搜尋引擎編目程式無法執行JavaScript，所以無法查看社群貼文的內容。使用Bootstrap HTML API，將此內容的可搜尋片段新增至頁面的初始HTTP回應，讓您的內容和關鍵字改進搜尋引擎最佳化。

>[!NOTE]
>
>此API僅適用於「留言」和「即時部落格系列」類型。

## 整合

Livefyre的Bootstrap HTML API將傳回使用者內容的HTML片段，該片段可能包含在頁面的HTTP回應中。搜尋引擎編目程式可讀取此回應，而無須執行任何JavaScript。當頁面在使用者瀏覽器中上線時，HTML片段將會更換為完整、互動式Widget，而且使用者將能夠張貼內容。

若要實作Bootstrap HTML API：

1. 將伺服器設為伺服器API要求，以傳送至下方所述的Bootstrap HTML端點。

   >[!NOTE]
   >
   >如果您嘗試擷取尚未存在的對話的Bootstrap HTML(亦即，如果您尚未嵌入App或建立系列)，則會收到200個，但內容看起來像是： `<!- HTTP 404 example.fyre.co/000000/MTEwMTo2NDEyOD1RS/bootstrap.html ->`

1. 如果您的退貨未包含內容的「404」，請將其儲存至字串中。您可能會快取此回應，以避免在每個pageload上請求Bootstrap HTML API。
1. 將Bootstrap HTML字串插入您希望內容出現的網頁中。
1. 將網頁提供給瀏覽器(或搜尋引擎編目程式)。

## 資源

```
GET https://{networkName}.bootstrap.fyre.co/bs3/{networkName}.fyre.co/{siteId}/{base64 encoded article ID}/bootstrap.html 
```

## 參數

* **重新命名** 您的Livefyre提供的網路名稱。例如： *實驗室*`labs.fyre.co`。
* **SiteID** 的「系列的網站ID」。
* **b64ArticleID使用** base64url編碼的文章ID。

## 範例

```
https://labs.bootstrap.fyre.co/bs3/labs.fyre.com/4/NTg0/bootstrap.html 
```

## 回應

```
https://gist.github.com/ec5c2457322faf9cf515 
```
