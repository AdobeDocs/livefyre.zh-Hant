---
description: null
seo-description: null
seo-title: 使用Livefyre搭配Adobe Analytics和Dynamic Tag Manager(DTM) lk xavvn vefyre with
  Adobe Analytics和Dynamic Tag Manager(DTM)
uuid: 9c25c0-c474-46ff-82ac-e89357007 c7 f
translation-type: tm+mt
source-git-commit: 55bfc0a545bb4a1093c29bd11e764c9799135324

---


# 使用Livefyre搭配Adobe Analytics和Dynamic Tag Manager(DTM){#use-livefyre-with-adobe-analytics-and-dynamic-tag-manager-dtm}

設定Adobe Analytics和Dynamic Tag Manager(DTM)以收集Livefyre應用程式的資料。

## 步驟1：在Adobe Analytics中設定事件 {#section_iks_kgd_4cb}

將Livefyre事件對應至Adobe Analytics報表套裝管理器中的一或多個自訂成功事件。

如需報表套裝管理器的詳細資訊，請參閱 [報表套裝管理器](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)。

1. 以管理員使用者身分登入Adobe Analytics。
1. 開啓Adobe Analytics管理報表套裝管理器。
1. 建立新的報表套裝或選擇現有報表套裝。
1. 按一下報表套裝以修改報表套裝，然後導覽至 **[!UICONTROL Edit Settings > Conversion > Success Events]**報表套裝。
1. 將Livefyre事件映射至一或多個自訂成功事件。

## 步驟2：設定轉換變數

將Livefyre轉換變數(eVar)對應至Adobe Analytics管理報表套裝管理器中的轉換變數。轉換變數會像排序函數一樣運作，以判斷您計劃如何識別從Livefyre事件收集的資料。

1. 在「報表套裝管理器」中按一下 **[!UICONTROL Edit Settings > Conversion > Conversion Variables]**。
1. 選擇自訂轉換變數(eVar)以使用並對應至Livefyre轉換變數。若要將Livefyre轉換變數對應至自訂轉換變數：
* 啓用轉換變數
* 命名轉換變數
* 為轉換變數提供類型
1. 儲存自訂轉換變數。

## 步驟3：使用DTM以Livefyre事件新增您的報表套裝 {#section_t15_2hd_4cb}

將Adobe Analytics新增至DTM以取得Analytics運作。若要這麼做，請建立新的屬性和工具，並將具有Livefyre事件的新報表套裝新增至屬性。如需DTM的詳細資訊，請參閱 [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)。

如果您已為您設定的報表套裝設定Livefyre事件，則不需要執行此步驟。

1. 在DTM中建立或編輯現有屬性。
1. 建立或編輯現有的Adobe Analytics工具。
1. 如果現有Adobe Analytics工具不存在，請按一下 **[!UICONTROL Add a Tool]** 按鈕。
為工具設定下列參數：
* 設 **[!UICONTROL Tool Type]****[!UICONTROL Adobe Analytics]**為。
* 啓用 **[!UICONTROL Automatic Configuration]**。
* 啓用 **[!UICONTROL Authenticate via Marketing Cloud]**。
1. 新增或確認具有Livefyre事件的報表套裝名稱至 **[!UICONTROL Report Suites]** 欄位。

## 步驟4：設定頁面載入規則以設定Analytics處理 {#section_jfj_j3d_4cb}

設定「頁面載入規則」以提取所有資料。「頁面載入規則」可讓您在規則中放置自訂javascript，以便在頁面載入時記錄事件。

>[!NOTE]
>
>請勿使用事件型規則或直接呼叫規則。

1. 在DTM中，選取 **[!UICONTROL Rules]** 標籤。
1. 按一 **[!UICONTROL Page Load Rules]**下。
1. 按一下 **[!UICONTROL Create New Rule]** 按鈕。
1. 按一下按鈕以開啓 **[!UICONTROL Conditions]** 區段 **[!UICONTROL Plus]** 。
1. 觸發規則。如果 **[!UICONTROL DOM Ready]** 您想要延遲或以非同步方式實施規則，請選擇或 **[!UICONTROL Onload]** 觸發類型。
1. (選擇性)新增其他參數以限制顯示Livefyre應用程式的頁面。如需其他設定選項的詳細資訊，請參閱 [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)。
1. 按 **[!UICONTROL Javascript/ Third Party Tags]**一下 **[!UICONTROL Non-sequential]** 標籤，然後按一 **[!UICONTROL Add New Script]**下。
1. 選取 **[!UICONTROL Sequential HTML]** 指令碼類型。
1. 將下列指令碼新增至程式碼編輯器，然後按一下 **[!UICONTROL Save Code]**。
在Livefyre JavaScript載入後，下列指令碼會呼叫 `livefyre_analytics` 直接呼叫規則。下列指令碼範例每400毫秒檢查一次是否 `livefyre.analytics` 位於頁面上。頁面載入後，livefyre. analytics會傳送追蹤資訊。

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

1. 按一 **[!UICONTROL Save Code]**下。
1. 按一 **[!UICONTROL Save Rule]**下。

## 步驟5：建立直接呼叫規則以建立Livefyre的Adobe Analytics對應設定 {#section_gvp_b1g_pdb}

透過使用自訂事件、DTM內的Adobe Analytics UI欄位以及資料元素，有其他方式可透過DTM實作Livefyre。本文件使用自訂Javascript來達成相同的效果。

1. 在DTM中選取「 **規則** 」索引標籤，然後按一下 **「直接呼叫規則**」。
1. 按一下 **「建立新規則** 」按鈕。
1. 命名新規則 **Livefyre Analytics**。
1. 展開 **條件** 設定區域。
1. 在 **字串** 欄位中輸入 `livefyre_analytics`。
1. 展開「Javascript/第三方標籤」區段，然後按一下 **「新增指令碼** 」按鈕。
1. 在「標記名稱」輸入方塊中輸入 **Livefyre** **Analytics** Config。
1. 選取 **「非循序Javascript**」。
1. 在程式碼編輯器中輸入下列Livefyre組態碼，然後按一下 **「儲存代碼** 」按鈕。

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

* 為Livefyre所有分析事件新增分析處理常式。對於每個事件，它會設定全域物件上的資料，然後傳送事件。

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
1. Click on **Save Rule**.

## Step 6: Approve changes for Page Load Rule {#section_pxc_11t_ycb}

1. Go to **[!UICONTROL Approvals]** tab.
1. Click **[!UICONTROL Approve]**.
1. Click **[!UICONTROL Yes, approve]** to confirm your approval.
1. Go to **[!UICONTROL Overview > Publish Queue]**.
1. Select the Rule to publish.
1. Click **[!UICONTROL Publish Selected]**.
1. Click **[!UICONTROL Publish]** to confirm that you want to publish.

## Script {#section_xkb_vft_mcb}

The following sample code maps the specific eVars to available Livefyre eVars. The Livefyre conversion variable ( `eVar`) name (for example, `appId`) maps to the name you set up in the Report Suite Manager (for example, `eVar81`). Change the `eVar` names in this script to the custom conversion variables.
```

var s=_ satellite. getToolsByType`('sc')[0]`. Gets()；
var eVarMap={appID：'eVar81'，AppType：'eVar82'}；

```
The following sample code maps the specific events you set up in the Report Suite Manager with available Livefyre events. In this example, `event82` is set up as any user interaction event without differentiating which kind of user interaction event (for example, liking or sharing content). This is an efficient way to record all user interaction information in a block. You can also map the events in the DTM Analytics UI with Data Element referencing.
```

var eventMap={QuareCancel：'event82'，\
標幟Click：'event82'，\
標幟同意：'event82'，\
旗標攻擊：'event82'，\
標幟主題：'event82'，\
旗標面板：'event82'，\
贊：'event82'，載入：'event81'，\
RequestMore：'event82'，\
ShareBootClick：'event82'，\
ShareFacebook：'event82'，\
ShareOnPostClick：'event82'，\
ShareTwitter：'event82'，\
ShareUrl：'event82'，\
SortStream：'event82'，\
TwitterLikeClick：'event82'，TwitterReplicCyclick：'event82'，\
TwitterRetweetClick：'event82'，\
TwitterUser關注：'event82'}；

```
The following sample states that if there isn't an event in this list, don't do anything. You do not need to modify this section of code.
```

function trackLiveFireEvent(data){\
var event= eventMapData[. type]；
console. log('Track：'，data. type，event)；

if(！event){console.
warning(data. type，'is not appeed to an event in AA')；\
return；}

```
The following code differentiates the event types that `event82` records. The conversion variable, `eVar83` records the type of user interaction, and the script sets up `eVar83` to separate the user interaction data by type. So `eVar83` allows you to break out the recorded data into specific types of user interactions.
```

var vars= ['events']；\
switch(event){case'event82'：s. eVar83= data. type；\
vars. push('eVar83')；\
中斷；
default：}

['Generator'，'evar'].for每個(function(type){\
var obj= datatype[]；
for(var d in obj){if(obj.
hasownProperty(d)& eeMarkAPD[]){\
s[eVarAPD[]]= objd[]；\
vars. push(eVarAPD[])；}}})；

s. linkTrackVars= vars. complement('，')；\
s. linkTrackEvents= event；\
s. events= event；

console. log('linkTrackVars：'，s. linkTrackVars)；\
console. log('linkTrackEvents：'，s. linkTrackEvents)；\
console. log('events：'、s. events)；

s. tl()；}

```
The following code sample adds a handler to listen to all the events that happen. It uses the page load rule on load, waits for events to exist, then sets up handler for all events from the App and tracks them. You do not need to modify this code.
```

/**
* 為Livefyre所有分析事件新增分析處理常式。對於每個事件，它會設定全域物件上的資料，然後傳送事件。

*/function addAnalyticsAndler(){Livefyre.
analytics. addHandler(函數(事件){(events)|| []).for每個(函數(資料){console.
log('Event handled：'，data. type)；
trackLiveFireEvent(data)；})；})；})

```
## More Info

For more information on the topics discussed on this page, see:

* [Report Suite Manager](https://marketing.adobe.com/resources/help/en_US/reference/report_suites_admin.html)
* [DTM](https://marketing.adobe.com/resources/help/en_US/dtm/c_overview.html)
* [Rules](https://marketing.adobe.com/resources/help/en_US/dtm/rules.html)
* [Livefyre.js](/help/implementation/c-livefyre.js.md)

