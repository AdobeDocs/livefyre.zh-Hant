---
description: null
seo-description: null
seo-title: 搭配其他Analytics工具使用Livefyre
solution: Experience Manager
title: 搭配其他Analytics工具使用Livefyre
uuid: 26c835f6-aced-41f7-aobe-418afce8 a829
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 搭配其他Analytics工具使用Livefyre{#use-livefyre-with-other-analytics-tool}

您可以使用分析工具來收集使用者與Livefyre應用程式互動的資料。您可以使用Adobe Analytics或您選擇的工具。

若要搭配您選擇的工具使用Livefyre(而非Adobe Analytics)，請遵循本頁所述的程序。

## 步驟1：設定事件處理常式 {#section_ngm_gzl_pdb}

在您使用Livefyre應用程式的頁面上設定事件處理常式。這可讓您從該頁面上的應用程式收集資料，以便用於分析。

將Livefyre. js新增至頁面以設定事件處理常式。Livefyre. js會非同步載入。為了減少檔案大小並改善載入效能，無法立即使用分析。您必須先輪詢分析物件，直到資料可用為止。將此指令檔置於頁面上的任何位置，或將它整合在您自己編譯的指令碼中。

```
/** 
 * Handler for Livefyre analytics batch events. 
 * @param {Array.<string>} events Array of events that have been fired since 
 * the last batch send. 
 */ 
function analyticsHandler(events) { 
  // Send to analytics 
  console.log(events); 
} 
 
var attempts = 0; 
 
function pollForAnalytics() { 
  if (Livefyre && Livefyre.analytics) { 
    Livefyre.analytics.addHandler(analyticsHandler); 
    return; 
  } 
  if (attempts === 10) { 
    return; 
  } 
  attempts++; 
  setTimeout(pollForAnalytics, 500); 
} 
 
pollForAnalytics(); 
```

## 步驟2：實作處理常式函數

在頁面上提供Livefyre. analytics功能後，請實作AnalyticsAndler函數，將接收的事件傳送給您所選擇的分析提供者。

1. 分析處理常式會接收一系列事件，這些事件必須經過重復並個別傳送，如果您的提供者支援，則加以傳送。
1. 將處理常式收到的事件資料對應至分析提供者所需的格式。
1. 傳送資料給您的分析供應商。

