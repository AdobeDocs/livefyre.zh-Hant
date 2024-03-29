---
title: 搭配使用Livefyre和其他Analytics工具
description: 搭配使用Livefyre和其他Analytics工具
exl-id: da29e281-5095-4e99-a248-19390f2059a2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# 搭配使用Livefyre和其他Analytics工具{#use-livefyre-with-other-analytics-tool}

您可以使用分析工具收集使用者與Livefyre應用程式互動的資料。 您可以使用Adobe Analytics或您選擇的工具。

若要搭配您選擇的工具(而非Adobe Analytics)使用Livefyre，請依照本頁所述的程式。

## 步驟1:設定事件處理常式{#section_ngm_gzl_pdb}

在您使用Livefyre應用程式的頁面上設定事件處理常式。 這可讓您從該頁面上的「應用程式」收集資料，以便用於分析。

將Livefyre.js新增至頁面以設定事件處理常式。 Livefyre.js以非同步方式載入。 為了減少檔案大小並改善載入效能，無法立即使用分析。 您必須輪詢分析物件，直到資料可供使用為止。 將此指令碼放在頁面上的任意位置，或將它整合在您自己編譯的指令碼中。

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

## 步驟2:實作處理常式函式

在頁面上提供Livefyre.analytics功能後，請實作analyticsHandler函式，將收到的事件傳送給您選擇的分析提供者。

1. 分析處理常式會接收必須經過迭代並個別傳送的事件陣列，或是以批次形式傳送（如果您的提供者支援）。
1. 將處理常式接收的事件資料對應至您的分析提供者所要求的格式。
1. 傳送資料給您的分析提供者。
