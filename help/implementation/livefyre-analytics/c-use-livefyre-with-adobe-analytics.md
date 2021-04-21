---
description: 'null'
exl-id: a866782d-fca6-48bf-9fb8-5080e396919b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 1%

---

# 搭配使用Livefyre和Adobe Analytics和動態標籤管理器(DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

設定Adobe Analytics和動態標籤管理器(DTM)以收集Livefyre應用程式的資料。

## 步驟1:在Adobe Analytics設定事件{#section_iks_kgd_4cb}

將Livefyre事件對應至「Adobe Analytics報表套裝管理員」中的一或多個自訂成功事件。

如需「報表套裝管理員」的詳細資訊，請參閱[報表套裝管理員](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)。

1. 以管理員用戶身份登錄Adobe Analytics。
1. 開啟Adobe Analytics管理報表套裝管理員。
1. 建立新的報表套裝或選擇現有的報表套裝。
1. 按一下要修改的報表套裝，然後導覽至&#x200B;**[!UICONTROL Edit Settings > Conversion > Success Events]**，以編輯報表套裝。
1. 將Livefyre事件對應至一或多個自訂成功事件。

## 步驟2:設定轉換變數

將Livefyre轉換變數(eVar)對應至「Adobe Analytics管理報表套裝管理員」中的轉換變數。 轉換變數的作用類似排序函式，可決定您打算如何識別從Livefyre事件收集的資料。

1. 在「報表套裝管理員」中按一下&#x200B;**[!UICONTROL Edit Settings > Conversion > Conversion Variables]**。
1. 選擇要使用的自訂轉換變數(eVar)，並將它們對應至Livefyre轉換變數。 若要將Livefyre轉換變數對應至自訂轉換變數：
* 啟用轉換變數
* 命名轉換變數
* 為轉換變數指定類型
1. 儲存自訂轉換變數。

## 步驟3:使用DTM將報表套裝與Livefyre事件一起新增{#section_t15_2hd_4cb}

將Adobe Analytics加入DTM，讓Analytics運作。 若要這麼做，請建立新屬性和工具，並新增包含Livefyre事件的報表套裝至屬性。 如需DTM的詳細資訊，請參閱[DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html)。

如果您已針對使用Livefyre事件設定的報表套裝設定屬性或工具，則不需要執行此步驟。

1. 在DTM中，建立或編輯現有屬性。
1. 建立或編輯現有的Adobe Analytics工具。
1. 如果現有的Adobe Analytics工具不存在，請按一下&#x200B;**[!UICONTROL Add a Tool]**按鈕。
為工具設定以下參數：

   * 將&#x200B;**[!UICONTROL Tool Type]**&#x200B;設為&#x200B;**[!UICONTROL Adobe Analytics]**。
   * 啟用 **[!UICONTROL Automatic Configuration]**.
   * 啟用 **[!UICONTROL Authenticate via Marketing Cloud]**.
1. 將含有Livefyre事件的報表套裝名稱新增或確認至&#x200B;**[!UICONTROL Report Suites]**&#x200B;欄位。

## 步驟4:設定頁面載入規則以設定Analytics處理{#section_jfj_j3d_4cb}

設定頁面載入規則以提取所有資料。 「頁面載入規則」可讓您將自訂javascript放入規則中，以記錄頁面載入時的事件。

>[!NOTE]
>
>請勿使用事件型規則或直接呼叫規則。

1. 在DTM中，選擇&#x200B;**[!UICONTROL Rules]**&#x200B;頁籤。
1. 按一下 **[!UICONTROL Page Load Rules]**.
1. 按一下&#x200B;**[!UICONTROL Create New Rule]**&#x200B;按鈕。
1. 按一下&#x200B;**[!UICONTROL Plus]**&#x200B;按鈕以開啟&#x200B;**[!UICONTROL Conditions]**&#x200B;部分。
1. 觸發規則。 如果要延遲或非同步實施規則，請選擇&#x200B;**[!UICONTROL DOM Ready]**&#x200B;或&#x200B;**[!UICONTROL Onload]**&#x200B;觸發器類型。
1. （可選）新增其他參數以限制顯示Livefyre應用程式的頁面。 如需其他設定選項的詳細資訊，請參閱[DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html)。
1. 在&#x200B;**[!UICONTROL Javascript/ Third Party Tags]**&#x200B;下方，按一下&#x200B;**[!UICONTROL Non-sequential]**&#x200B;標籤，然後按一下&#x200B;**[!UICONTROL Add New Script]**。
1. 選擇&#x200B;**[!UICONTROL Sequential HTML]**&#x200B;作為指令碼類型。
1. 將下列指令碼新增至程式碼編輯器，然後按一下&#x200B;**[!UICONTROL Save Code]**。

   下列指令碼在Livefyre JavaScript載入後呼叫`livefyre_analytics`直接呼叫規則。 以下指令碼示例每400毫秒檢查一次，以查看頁面上是否有`livefyre.analytics`。 頁面載入後，livefyre.analytics會傳送追蹤資訊。

   ```
   /** 
   * Poll for Livefyre.analytics object to exist since it gets loaded via the 
   * Livefyre.js JavaScript file. Depending on the timing, this could already 
   * exist or need a little time. 
   */ 
   function pollForAnalytics() {  
   if (Livefyre.analytics) { 
     _satellite.track('livefyre_analytics'); 
       return true; 
     } 
     setTimeout(pollForAnalytics, 400); 
   } 
   setTimeout(pollForAnalytics, 400);
   ```

1. 按一下 **[!UICONTROL Save Code]**.
1. 按一下 **[!UICONTROL Save Rule]**.

## 步驟5:建立直接呼叫規則以建立Livefyre {#section_gvp_b1g_pdb}的Adobe Analytics對應設定

有其他方式可透過使用自訂事件、DTM中的Adobe AnalyticsUI欄位和資料元素，將Livefyre與DTM一起實作。 本檔案使用自訂Javascript來達成相同的效果。

1. 在DTM中，選擇&#x200B;**Rules**&#x200B;標籤，然後按一下&#x200B;**Direct Call Rules**。
1. 按一下&#x200B;**建立新規則**&#x200B;按鈕。
1. 為新規則命名&#x200B;**Livefyre Analytics**。
1. 展開&#x200B;**conditions**&#x200B;配置區域。
1. 在&#x200B;**字串**&#x200B;欄位中，輸入`livefyre_analytics`。
1. 展開「Javascript /第三方標籤」區段，然後按一下「新增指令碼&#x200B;**」按鈕。**
1. 在&#x200B;**標籤名稱**&#x200B;輸入方塊中輸入&#x200B;**Livefyre Analytics Config**。
1. 選擇「**非循序Javascript**」。
1. 在程式碼編輯器中輸入下列Livefyre組態程式碼，然後按一下「儲存程式碼」按鈕。****

   ```
   var s = _satellite.getToolsByType('sc')[0].getS(); 
   
   var evarMap = {  
     appId: 'eVar81',  
     appType: 'eVar82' 
   }; 
   
   var eventMap = { 
     FlagCancel: 'event82',  
     FlagClick: 'event82',  
     FlagDisagree: 'event82',  
     FlagOffensive: 'event82',  
     FlagOffTopic: 'event82',  
     FlagSpam: 'event82',  
     Like: 'event82', 
     Load: 'event81',  
     RequestMore: 'event82',  
     ShareButtonClick: 'event82',  
     ShareFacebook: 'event82',  
     ShareOnPostClick: 'event82',  
     ShareTwitter: 'event82',  
     ShareURL: 'event82',  
     SortStream: 'event82',  
     TwitterLikeClick: 'event82', 
     TwitterReplyClick: 'event82',  
     TwitterRetweetClick: 'event82',  
     TwitterUserFollow: 'event82' 
   }; 
   
    function trackLivefyreEvent(data) {  
     var event = eventMap[data.type]; 
     console.log('Track:', data.type, event); 
   
     if (!event) { 
       console.warn(data.type, 'is not mapped   to an event in AA');  
       return; 
     } 
     var vars = ['events'];  
     switch (event) { 
       case 'event82': s.eVar83 = data.type;  
         vars.push('eVar83');  
         break; 
       default: 
     } 
       ['generator', 'evars'].forEach(function (type) {  
       var obj = data[type]; 
       for (var d in obj) { 
         if (obj.hasOwnProperty(d) && evarMap[d]) {  
           s[evarMap[d]] = obj[d];  
           vars.push(evarMap[d]); 
         } 
       } 
     }); 
     s.linkTrackVars = vars.join(',');  
     s.linkTrackEvents = event;  
     s.events = event; 
   
     console.log('linkTrackVars:',  s.linkTrackVars);  
     console.log('linkTrackEvents:',  s.linkTrackEvents);  
     console.log('events:', s.events); 
     s.tl(); 
     } 
     ]
   
     /** 
   ```

   * 新增Livefyre所有分析事件的分析處理常式。 對於每個事件，它都會在全域物件上設定資料，然後調度事件。

   ```
   */ 
   function addAnalyticsHandler() {  
     Livefyre.analytics.addHandler(function (events) { 
       (events || []).forEach(function (data) {  
         console.log('Event handled:', data.type);  
         trackLivefyreEvent(data); 
       }); 
     }); 
   } 
   addAnalyticsHandler();  
   ```

1. 按一下&#x200B;**保存規則**。

## 步驟6:批准頁面載入規則{#section_pxc_11t_ycb}的變更

1. 前往&#x200B;**[!UICONTROL Approvals]**&#x200B;標籤。
1. 按一下 **[!UICONTROL Approve]**.
1. 按一下&#x200B;**[!UICONTROL Yes, approve]**&#x200B;以確認您的批准。
1. 前往 **[!UICONTROL Overview > Publish Queue]**.
1. 選取要發佈的規則。
1. 按一下 **[!UICONTROL Publish Selected]**.
1. 按一下&#x200B;**[!UICONTROL Publish]**&#x200B;以確認您要發佈。

## 指令碼 {#section_xkb_vft_mcb}

下列范常式式碼會將特定eVar對應至可用的Livefyre eVar。 Livefyre轉換變數(`eVar`)名稱（例如`appId`）會對應至您在「報表套裝管理員」中設定的名稱（例如`eVar81`）。 將此指令碼中的`eVar`名稱更改為自定義轉換變數。


```
var s = _satellite.getToolsByType`('sc')[0]`.getS(); 
var evarMap = { 
  appId: 'eVar81', 
  appType: 'eVar82' 
};
```

下列范常式式碼會將您在「報表套裝管理員」中設定的特定事件與可用的Livefyre事件對應。 在此範例中，`event82`會設為任何使用者互動事件，而不會區分哪些類型的使用者互動事件（例如，按贊或分享內容）。 這是記錄區塊中所有使用者互動資訊的有效方式。 您也可以使用資料元素參考來對應DTM Analytics UI中的事件。

```
var eventMap = { 
  FlagCancel: 'event82',  
  FlagClick: 'event82',  
  FlagDisagree: 'event82',  
  FlagOffensive: 'event82',  
  FlagOffTopic: 'event82',  
  FlagSpam: 'event82',  
  Like: 'event82', 
  Load: 'event81',  
  RequestMore: 'event82',  
  ShareButtonClick: 'event82',  
  ShareFacebook: 'event82',  
  ShareOnPostClick: 'event82',  
  ShareTwitter: 'event82',  
  ShareURL: 'event82',  
  SortStream: 'event82',  
  TwitterLikeClick: 'event82', 
  TwitterReplyClick: 'event82',  
  TwitterRetweetClick: 'event82',  
  TwitterUserFollow: 'event82' 
};
```

下列範例指出，如果此清單中沒有事件，則不要執行任何動作。 您不需要修改此程式碼區段。

```
function trackLivefyreEvent(data) {  
  var event = eventMap[data.type]; 
  console.log('Track:', data.type, event); 
   
  if (!event) { 
    console.warn(data.type, 'is not mapped to an event in AA');  
    return; 
  }
```

下列程式碼會區分`event82`記錄的事件類型。 轉換變數`eVar83`會記錄使用者互動的類型，指令碼會設定`eVar83`，依類型來分隔使用者互動資料。 因此，`eVar83`可讓您將記錄的資料劃分為特定類型的使用者互動。

```
  var vars = ['events'];  
  switch (event) { 
    case 'event82': s.eVar83 = data.type;  
      vars.push('eVar83');  
      break; 
    default: 
  } 
   
  ['generator', 'evars'].forEach(function (type) {  
    var obj = data[type]; 
    for (var d in obj) { 
      if (obj.hasOwnProperty(d) && evarMap[d]) {  
        s[evarMap[d]] = obj[d];  
        vars.push(evarMap[d]); 
      } 
    } 
  }); 
   
  s.linkTrackVars = vars.join(',');  
  s.linkTrackEvents = event;  
  s.events = event; 
   
  console.log('linkTrackVars:', s.linkTrackVars);  
  console.log('linkTrackEvents:', s.linkTrackEvents);  
  console.log('events:', s.events); 
   
  s.tl(); 
}
```

下列程式碼範例會新增一個處理常式，以監聽所有發生的事件。 它會在載入時使用頁面載入規則，等待事件存在，然後為應用程式中的所有事件設定處理常式並追蹤它們。 您不需要修改此程式碼。

```
/** 
* Adds an analytics handler for all analytics events from Livefyre. For each event, it sets the data on a global object and then dispatches the event. 
*/ 
function addAnalyticsHandler() { 
  Livefyre.analytics.addHandler(function (events) { 
    (events || []).forEach(function (data) { 
      console.log('Event handled:', data.type); 
      trackLivefyreEvent(data); 
    }); 
  }); 
}
```

## 更多資訊

如需本頁所討論主題的詳細資訊，請參閱：

* [報告套裝管理員](https://docs.adobe.com/content/help/en/analytics/admin/manage-report-suites/report-suites-admin.html)
* [DTM](https://docs.adobe.com/content/help/en/dtm/using/c-overview.html)
* [規則](https://docs.adobe.com/content/help/en/dtm/using/resources/rules/create-rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)
