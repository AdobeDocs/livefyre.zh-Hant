---
description: 新增即時聊天至您的頁面。
seo-description: 新增即時聊天至您的頁面。
seo-title: 聊天室
solution: Experience Manager
title: 聊天室
uuid: d6761a69-efa5-4ad3-abaf-1ba8e6c17f94
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241
workflow-type: tm+mt
source-wordcount: '1436'
ht-degree: 3%

---


# 聊天室{#chat}

新增即時聊天至您的頁面。

聊天可讓您的觀眾參與即時活動的即時對話。 內容會顯示為連續串流，鼓勵快速參與展開的對話。

目前版本：聊天使用`fyre.conv v3.0.0.`

## 整合 {#concept_0A99792A7E89403F95D082D52D600F17}

內嵌聊天應用程式會遵循內嵌核心應用程式的程式，如「快速入門> [內嵌應用程式」中所述。](../c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md#using-livefyre-js-create-customize-apps)

範例:

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
        new Conv(networkConfig, [convConfig], function(chatWidget) {}); 
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

如[CollectionMeta Token](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent)區段中所述，CollectionMeta是編碼的JSON物件。 在上述範例中，JSON物件在JWT編碼前會採用下列格式：

```
{ 
"url": "https://dev.livefyre.com/articles/test.html",  
"articleId": "1",  
"type": "livechat",  
"title": "Title 1" 
}
```

## NetworkConfig對象{#c-networkconfig-object}

`NetworkConfig`物件是JSON物件，可自訂網路使用者的驗證系統。

`NetworkConfig`物件是包含下列參數的JSON物件：

| 參數 | 類型 | 說明 |
|---|---|---|
| authDelegate | *需求* 物件 | 用於為自定義網路用戶自定義身份驗證系統。 |
| network | *必* 要字串 | Livefyre提供的網路名稱。 例如：*yourname.fyre.co.* |
| attachmentDelegate | 物件 | 用於指定在應用程式串流中可見的媒體附件類型。 如需詳細資訊，請參閱[限制媒體](../c-app-customizations/c-restrict-media.md#c_restrict_media)。 |
| 字串 | *選* 項對象 | 用於自訂任何Livefyre核心應用程式中HTML元素的文字字串。 如需詳細資訊，請參閱[字串自訂](/help/using/c-settings-other/c-translation-sets/c-localize-strings.md)。 |

## ConvConfig對象{#c-convconfig-object}

`convConfig`物件是JSON物件，用於指定Livefyre應用程式在頁面上轉譯的內容。

>[!NOTE]
>
>此處列出的`convConfig`物件參數不適用於「評論」應用程式。 如需使用`convConfig`物件的「檢閱」應用程式的整合資訊，請參閱「檢閱整合」。

`ConvConfig`物件包含下列必要參數：

| 參數 | 類型 | 說明 |
|--- |--- |--- |
| articleId | *必* 要字串 | 唯一識別網站內的系列。 通常，這對應於CMS中的資料庫主鍵或貼文ID。 例如：「42後」。 255 個字元限制.  注意： 如果您使用文章URL做為文章Id，請確定字串是MD5或SHA-1編碼。 |
| collectionMeta | *必* 要字串 | 關於系列的JWT編碼中繼資料。 如需詳細資訊，請參閱[CollectionMeta物件](../c-getting-started/c-implementation-process/c-collectionmeta-tokent.md#collectionmeta-tokent)。 |
| el | *必* 要字串 | 內容串流將呈現至的DOM元素ID。 |
| siteId | *必* 要字串 | Livefyre提供的系列所屬網站或應用程式ID。 例如：「303617」。 |

>[!NOTE]
>
>`app`參數不是「注釋應用程式」實作的必要項。

`ConvConfig`物件也可能包含下列選用參數：

| 參數 | 類型 | 說明 |
|--- |--- |--- |
| actionButtons | *可選* 陣列 | 可新增至「共用」和「標幟」按鈕旁之內容的自訂動作按鈕陣列。 如需詳細資訊，請參閱新增自訂按鈕。 |
| 動畫 | *可選* 布爾值 | 定義動畫是否會在Livefyre應用程式中執行。 設為false可停用動畫。 預設為true。 |
| anonymousPaltingEnabled | *可選* 布爾值 | 定義來賓用戶是否具有標籤內容的選項。 預設為true。 |
| browserType | *選* 項字串 | 定義應為其產生顯示內容的裝置。 這會導致CSS和某些功能依輸入裝置類型而變更。 選項包括桌上型電腦、行動裝置或平板電腦。 （如果保留空白，則會預設為Google Agent對顯示格式的判斷。） |
| 校驗和 | *建* 議字串（建議） | 識別CollectionMeta的目前狀態。 變更此值會導致Livefyre使用CollectionMeta中的新值更新伺服器上的資料。 |
| datetimeFormat | *選* 項字串對象函式 | 指定串流內容的日期時間格式。 如需詳細資訊，請參閱自訂日期和時間戳記。 |
| disableAvatars | *可選* 布爾值 | 避免在應用程式串流中轉譯頭像，進而減少載入至瀏覽器的項目數。 設值為 false。 |
| disableIE8Shim | *可選* 布爾值 | 停用Livefyre用來填入Internet Explorer 8的預設shiv，以支援HTML5元素。 Livefyre使用下列專案： [https://github.com/aFarkas/html5shiv](https://github.com/aFarkas/html5shiv)。 設值為 false。注意： 如果此值為false，則必須先使用某種類型的填色，才能呼叫Livefyre Chat，以取得Internet Explorer 8支援。 |
| disableThirdPartyAnalytics | *選* 項bBoolean | 停用Livefyre可用於內部測量的協力廠商分析系統（Quantserve和Google Analytics）。 設值為 false。 |
| editorCss | *選* 項對象 | 用於自定義注釋編輯器樣式。 您可以對編輯器欄位的背景顏色以及編輯器中顯示的文本的字型顏色、大小和系列進行樣式設定。  例如︰`{background: ‘#ccc’, color: ‘red’, font: ’30px “Helvetica Neue”, Helvetica, Arial, Geneva, sans-serif’}` |
| initialNumVisible | *可選* 整數 | 可讓您設定載入時在應用程式中顯示的預設留言數。 這可以是1到50之間的整數。 |
| initialNumVisibleLegacy | *可選* 整數 | 可讓您設定載入時在應用程式中顯示的舊版內容項目的預設數目。 這可以是1到50之間的整數。 如果未指定此參數，則預設為initialNumVisible。  例如：如果您的系列包含100個作用中和100個舊版註解，請設定initalNumVisible:10和initialNumVisibleLegacy:5，以顯示10個作用中註解（使用「顯示更多」按鈕）+ 5個封存註解（使用「顯示更多」按鈕）。 |
| maxVisible | *可選* 整數 | 設定聊天應用程式中頂層內容的可見片段數目上限。 如果有新的內容串流，則會從頁面移除串流底部的內容。 如果按一下「顯示更多……」按鈕，則會忽略參數，而使用者可自由顯示所需的內容。 （使用此參數可控制高速串流中頁面上出現的項目數。） |
| postToButtons | *可選* 陣列 | 用於設定內嵌即時部落格應用程式時顯示的提供者。 可用選項有兩個(Twitter)、fb(Facebook)和li(LinkedIn)。 預設為[ tw, fb ]。 |
| readOnly | *可選* 布爾值 | 停用系列的所有互動功能。 若為true，使用者將無法登入串流，也無法張貼、編輯、回覆或按贊內容。 若為true，使用者將能夠標幟和共用內容。 設值為 false。 |
| 串流 | *選* 項對象 | 包含設定應用程式串流的選項。 |
| stream.catchup | *可選* 整數 | 指定串流應載入之前的秒數。 依預設，Livefyre會載入50個內容，然後載入這些內容與目前時間之間提交的所有內容。 在非常快速的使用案例中，內容張貼的速度可能太快，使應用程式無法「追趕」目前。 使用此設定可定義內容張貼（在初始內容載入後）之前的秒數。 |
| stream.delay | *可選* 整數 | 指定串流請求之間的秒數。 使用此參數可協助控制內容流程並延遲DOM更新的頻率。  注意： 如果設定得太大，流可能會落後。 |


>[!NOTE]
>
>您可以在應用程式初始化期間傳遞一或多個`convConfig`物件，以在同一頁面上顯示多個應用程式。 請注意，額外的應用程式會使用瀏覽器資源，而效能可能會隨著數目的增加而降低。

## CollectionMeta對象{#c-collectionmeta-object}

`CollectionMeta`物件是JSON物件，可指定要儲存在系列中的中繼資料。

`CollectionMeta` 一律進行編碼，然後再傳送至Livefyre以保障安全性。編碼值會傳入上述的`ConvConfig`物件。

>[!NOTE]
>
>您必須新增伺服器端程式碼，才能編碼`CollectionMeta` JSON物件。 如需詳細資訊，請參閱建立伺服器端Token。

| 參數 | 類型 | 說明 |
|--- |--- |--- |
| articleId | *必* 要字串 | 系列的唯一ID。 |
| title | *必* 要字串 | 您要套用至系列的標題。 這通常與顯示應用程式之頁面的標題相對應。  例如：「整合太有趣了！」  注意： 標題的字元長度上限為255個字元。 標題欄位不支援HTML實體。 請使用UTF-8編碼特殊字元。 |
| url | *必* 要字串 | 您要附加至此系列的標準絕對URL。 此URL將用來從Facebook和Twitter上分享的內容、電子郵件通知和Livefyre Studio產生回應用程式的連結。  注意： Livefyre需要使用完全限定的網域名稱；不需要埠號或回調來解決本地設定。 如果在本機測試，請確定使用有效的基本URL網域。 (例如：`https://customer.com`有效，而`https://localhost:5995`則無效。) 一旦您將本機網站伺服器設定為接受完全限定的網域名稱，就不需要回呼或解析度，而且本機開發可依預期進行。 |
| type | *必* 要字串 | 系列類型。 必須是livechat。 |

`CollectionMeta`物件也可包含下列選用參數：

| 參數 | 類型 | 說明 |
|--- |--- |--- |
| 標籤 | *選* 項字串 | 以逗號分隔的單一關鍵字或片語清單。 在Studio中或使用搜尋API，依標籤搜尋系列。  注意：雖然透過Studio新增的標籤可能包含空格，但透過API輸入的標籤則無法。 使用底線可定義將在UI中顯示空格的標籤。 (例如：使用Monday_Quarterback在Studio中顯示Monday Quarterback。) |

## 添加事件處理程式{#concept_E7C17EFB43F24F1A8572E60C69176C6D}

若要註冊事件處理常式，請在應用程式的回呼函式中使用widget.on呼叫。

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

如需詳細資訊，以及可用事件的清單，請參閱[Javascript Events](../c-app-customizations/c-javascript-events.md#c_javascript_events)。
