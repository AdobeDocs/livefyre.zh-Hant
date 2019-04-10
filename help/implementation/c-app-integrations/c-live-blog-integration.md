---
description: 即時部落格可讓您在涵蓋即時活動時，從網站本身的編輯器提供即時更新和影像。
seo-description: 即時部落格可讓您在涵蓋即時活動時，從網站本身的編輯器提供即時更新和影像。
seo-title: 即時部落格
solution: Experience Manager
title: 即時部落格
uuid: ca373f1-2008-45ab-9ec295af4e368
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 即時部落格{#live-blog}

即時部落格可讓您在涵蓋即時活動時，從網站本身的編輯器提供即時更新和影像。

## 即時部落格 {#topic_574DEE2125A94B85BFB5C3D2C57C337E}

即時部落格可讓您在涵蓋即時活動時，從網站本身的編輯器提供即時更新和影像。

## 整合 {#c_live_blog_integration}

即時部落格可讓您在涵蓋即時活動時，從網站本身的編輯器提供即時更新和影像。

若要內嵌即時部落格應用程式，請遵循內嵌應用程式的程序。請參閱 [內嵌應用程式](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md)。以下是內嵌Blog應用程式外觀的範例。

### 範例

```
<html> 
  <head> 
    <script src="//cdn.livefyre.com/Livefyre.js"> 
    </script> 
  </head> 
<body> 
    <script type="text/javascript"> 
    var networkConfig = { 
      network: "client-solutions.fyre.co" 
    }; 
    var convConfig = { 
      siteId: '347674', 
      articleId: '1', 
      el: 'livefyre', 
      collectionMeta: 'eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6IlRpdGxlIDEiLCJ1cmwiOiJodHRwOlwvXC9kZXYubGl2ZWZ5cmUuY29tIiwidGFncyI6InRhZzEsdGFnMiIsImNoZWNrc3VtIjoiY2Q0YTJjYWJkMTIxOTkyM2FjZGJhMjExOWY2NmYwNTUiLCJhcnRpY2xlSWQiOiIxIn0.Dq-ghi9KYmEPmagvCS1NPyYDRMGBujm735QaTRb7E7k', 
      checksum: '6e2e4faf7b95f896260fe695eafb34ba' 
    }; 
    
    Livefyre.require(['fyre.conv#3'], function(Conv) { 
        new Conv(networkConfig, [convConfig], function(blogWidget) {}); 
        auth.delegate({ 
          login: function (callback) { 
            callback(null,{livefyre:'<userauthtoken>'}); 
          }, 
        }); 
    }); 
  
    </script> 
    <div id="livefyre"> 
    </div> 
   </body> 
</html>
```

CollectionMeta是編碼的JSON物件。在上述範例中，JSON物件採用下列格式，JWT編碼之前：

```
{ 
"url": "https://dev.livefyre.com/articles/test.html",  
"articleId": "1",  
"type": "liveblog",  
"title": "Title 1" 
}
```

## SocialConfig物件 {#c-networkconfig-object}

`NetworkConfig` 物件是JSON物件，可自訂網路使用者的驗證系統。

`NetworkConfig` 物件是一個JSON物件，包含下列參數：

| 參數 | Type | 說明 |
|---|---|---|
| **AuthDelegate** | *必要* 物件 | 用來自訂自訂網路使用者的驗證系統。 |
| **網路** | *必要* 字串A Livefyre提供的網路名稱。例如： *yourname. fyre. co.* |
| **AttachmentDelegate** | *選擇性* 物件 | 用來指定應用程式串流中可見的媒體附件類型。如需詳細資訊，請參閱 [限制媒體](../c-app-customizations/c-restrict-media.md#c_restrict_media)。 |
| **字串** | *選擇性* 物件 | 用來自訂任何Livefyre核心應用程式中HTML元素的文字字串。如需詳細資訊，請參閱 [字串自訂](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md)。 |

## conconfig物件 {#c-convconfig-object}

`convConfig` 物件是JSON物件，用來指定Livefyre App在頁面上呈現的內容。

>[!NOTE]
>
>此處列出的 `convConfig` 物件參數不適用於Reviews應用程式。如需使用 `convConfig` 物件的「評論」應用程式的整合資訊，請參閱「檢閱整合」。

`ConvConfig` 物件包含下列必要參數：

| 參數 | Type | 說明 |
|--- |--- |--- |
| **articleID** | *必要* 字串 | 唯一識別您的網站內的系列。這通常會對應至資料庫中的資料庫主要金鑰或貼文ID。例如：「post-42」。255字元限制。注意：如果您使用文章URL做為ArticleID，請確定字串是MD或SHA-1編碼。 |
| **CollectionMeta** | *必要* 字串 | 關於系列的JWT編碼中繼資料。如需詳細資訊，請參閱CollectionMeta物件。 |
| **el** | *必要* 字串 | 內容串流將呈現的DOM元素ID。 |
| **SiteID** | *必要* 字串 | Collection所屬之網站或應用程式的Livefyre提供ID。例如：「303617」。 |

>[!NOTE]
>
>「注釋應用程式」實施不需要 `app` 參數。

`ConvConfig` 物件也可能包含下列選擇性參數：

| 參數 | Type | 說明 |
|--- |--- |--- |
| **ActionButton** | *選擇性* 陣列 | 自訂動作按鈕陣列，可新增至「共用」和「標幟」按鈕旁邊的內容片段。如需詳細資訊，請參閱「新增自訂按鈕」。 |
| **動畫** | *選擇性* 布林值 | 定義動畫是否會在Livefyre應用程式中執行。設為false以停用動畫。預設為true。 |
| **OpenMousingEnabled** | 布林值 | 定義來賓使用者是否有權標記內容。預設為true。 |
| browserType | *可選* 字串 | 定義應產生內容的裝置。這會使CSS和部分功能變更為符合輸入裝置類型。選項包括桌上型電腦、行動裝置或平板電腦。(如果保留空白，則會預設為顯示格式的Google代理判斷。) |
| **checksum** | *選用* 字串(建議) | 識別CollectionMeta的目前狀態。變更此值會使Livefyre在伺服器上更新資料與CollectionMeta中的新值。 |
| **dateTimeFormat** | *選擇性* 字串物件函數 | 指定串流內容的日期格式。如需詳細資訊，請參閱自訂日期和時間戳記。 |
| disableAVatars | *選擇性* 布林值 | 防止App串流中顯示avatar，因此減少載入瀏覽器的項目數。預設為false。 |
| disableIE8Shim | *選擇性* 布林值 | 停用Livefyre使用的預設shav，使其能夠填入Internet Explorer8，以便支援HTML元素。Livefyre使用下列專案： [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv) 。預設為false。注意：如果此值為false，則必須在Livefyre聊天呼叫Internet Explorer支援之前使用某些類型的多邊形。 |
| **disableThirdPartyAnalytics** | *選擇性* 布林值 | 停用Livefyre可用於內部測量的第三方分析系統(隨堂服務和Google Analytics)。預設為false。 |
| **editorCSS** | *選擇性* 物件 | 用來自訂註解編輯器樣式。您可以設定編輯器欄位的背景顏色，以及編輯器中出現的字型顏色、大小和系列文字。例如：{背景：'# cc'，color：'red'，字型：'30px「Helvetica Neue」，Helvetica，Arial，日內瓦，sans-serif'} |
| **initialNumible** | *可選* 整數 | 可讓您在載入時，將預設的注釋設定在應用程式中。這可以是到50的整數。 |
| **initialNumpublisher** | *可選* 整數 | 可讓您在載入時設定應用程式中可見的舊版內容項目。這可以是到50的整數。如果未指定此參數，預設為initialNum可見。例如：如果您的Collection包含100個活動中和100個舊留言，請設定InitalnumVisible：和initialNumpublish Clogs：5，顯示10個作用中註解(使用「顯示更多」按鈕)+封存檔注釋(使用「顯示更多」按鈕)。 |
| **maxVisible** | *可選* 整數 | 設定聊天應用程式中頂層內容可見部分的最大數量。如果新的內容串流出現，則串流底部的內容將從頁面移除。如果按一下「顯示更多…」按鈕，則會忽略參數，而且使用者可以自由顯示所需的內容。(使用此參數來控制高速串流中頁面上出現的項目數。) |
| **PostTo按鈕** | *選擇性* 陣列 | 用於設定內嵌即時部落格應用程式時所顯示的提供者。可用選項為tw(Twitter)、fb(Facebook)和li(LinkedIn)。預設為 [ tw，fb ]. |
| **ReadOnly** | *選擇性* 布林值 | 停用系列的所有互動功能。在true時，使用者將無法登入串流，且無法張貼、編輯、回覆或按贊內容。在true時，使用者將能夠標記和共用內容。預設為false。 |
| **串流** | *選擇性* 物件 | 包含設定應用程式串流的選項。 |
| stream. catchup | *可選* 整數 | 指定串流應載入的目前秒數。Livefyre預設會載入50個內容片段，然後載入所有提交到目前時間之間的內容。在非常快速的使用案例中，內容可能會過快張貼，讓應用程式「往上追趕」。使用此設定可定義內容張貼後(初始內容載入後)的秒數。 |
| **stream. delay** | *可選* 整數 | 指定串流請求之間的秒數。使用此參數可協助控制內容流程，並延遲DOM的更新頻率。注意：如果設定過大，串流可能會落後。 |


>[!NOTE]
>
>您可以在應用程式初始化期間傳遞一或多 `convConfig` 個物件，以在同一頁上顯示多個應用程式。請注意，當數量增加時，額外應用程式會使用瀏覽器資源和效能。

## CollectionMeta物件 {#c-collectionmeta-object}

`CollectionMeta` 物件是JSON物件，用來指定要在系列內儲存的中繼資料。

`CollectionMeta` 在傳遞至Livefyre以確保安全性之前，一律加以編碼。編碼的值會傳遞至上方顯示的 `ConvConfig` 物件。

>[!NOTE]
>
>您必須新增伺服器端程式碼來編碼 `CollectionMeta` JSON物件。如需詳細資訊，請參閱建立伺服器端Token。

| 參數 | Type | 說明 |
|--- |--- |--- |
| **articleID** | *必要* 字串 | 系列的唯一ID。 |
| **title** | *必要* 字串 | 您要套用至系列的標題。這通常會對應顯示應用程式之頁面的標題。例如：「整合真是太有趣了！」注意：標題的字元長度上限為255個字元。標題欄位不支援HTML實體。請使用UTF-8編碼特殊字元。 |
| **url** | *必要* 字串 | 您要附加至此系列的標準絕對URL。此URL將用來從Facebook和Twitter上共用的內容、電子郵件通知和Livefyre Studio產生連結回應用程式。注意：Livefyre需要使用完全合格的網域名稱；不需要連接埠號碼或回呼來解決本機設定。如果在本機測試，請確定使用有效的基本URL網域。(例如： `https://customer.com` 有效，但並非如此。 `https://localhost:5995` )當您設定本機伺服器以接受完全合格的網域名稱後，就不需要回呼或解析度，而本機開發也可以如預期進行。 |
| **type** | *必要* 字串 | 系列類型。必須是livechat。 |

`CollectionMeta` 物件也可以包含下列選擇性參數：

| 參數 | Type | 說明 |
|---|---|---|
| **標記** | *選用* 字串 | 以逗號分隔的單一關鍵字或片語清單。依Studio內的標記或搜尋API搜尋系列。**注意：** 雖然透過Studio新增的標籤可能含有空格，但透過API輸入的標記無法使用。使用底線來定義將在UI中顯示空格的標籤。(例如：使用星期一_ Quarterback在Studio中顯示星期一四分衛。) |

## 新增事件處理常式 {#concept_D835C710A7214F6D921571E0770B6BC5}

若要註冊事件處理常式，請在應用程式的回呼函數中使用widget. on呼叫。

例如：

```
Livefyre.require(['fyre.conv#3'], function(Conv) { 
   new Conv(networkConfig, [convConfig], function(widget) { 
      widget.on('<strong><eventName></strong>', function (data) { 
         // Do something, perhaps using data 
      }); 
   }); 
});
```

