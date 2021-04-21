---
description: 使用Livefyre.js自訂日期和時間戳記。
title: 自訂日期和時間戳記
exl-id: 77130793-00ba-4a5c-8318-4221d971da6c
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 0%

---

# 自訂日期和時間戳記{#customize-the-date-and-time-stamp}

使用Livefyre.js自訂日期和時間戳記。

Livefyre應用程式提供選項參數datetimeFormat，以指定日期格式，如下所述。

* [術語](#c_date_time_stamp/section_xsk_jn4_xz)
* [格式](#c_date_time_stamp/section_ynx_gn4_xz)
* [符號指定](#c_date_time_stamp/section_inq_2n4_xz)

## 術語 {#section_xsk_jn4_xz}

* **絕對** 時間戳記定義為精確和特定時間（例如2012年1月1日12:00pm）
* **相對** 時間戳記定義為一般且不精確的時間（例如25秒前、14分鐘前、1天前、1年前等）

## 格式{#section_ynx_gn4_xz}

當未提供引數時，datetimeFormat參數具有以下預設行為：

* 日期時間格式：MMMM d yyyy（2012年1月8日）
* 20160分鐘（14天），直到絕對時間（14天，直到相對時間戳記變成絕對時間戳記）

datetimeFormat參數接受三種可能的參數類型：日期時間、格式和字串。

```
// Example 1 (Datetime format string)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": 'MMM d y Ka' 
}; 
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

指定absoluteFormat和／或minutesUntilAbsoluteTime的對象。 值為-1的minutesUntilAbsoluteTime會使時間絕對時間立即生效。

```
// Example 2 (Object)  
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": { 
      minutesUntilAbsoluteTime: 10, 
      absoluteFormat: 'MMM d y Ka' 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

作為Date對象的參數並返回要顯示的日期時間字串的函式

```
// Example 3 (Function accepting a Date object, returning a datetime string to display) 
var convConfig = { 
   "collectionMeta":"eyJ0eXAiOiJqd3QiLCJhbGciOiJIUzI1NiJ9.eyJ0aXRsZSI6InBvc3QgMiIsInVybCI6Imh0dHA6XC9cL29yYW5nZXNhcmVncmVhdC5jb21cL3VzZWExcDcwXzEyXC8_cD01IiwidGFncyI6IiIsImNoZWNrc3VtIjoiYjBiYzRkMmVmY2UyZWZkYzZkYTE4NmQ2ZGZhNmVkYzAiLCJhcnRpY2xlSWQiOjV9.XZJTJgwpiFZCQ6dv8vvl91sMbFSJndzZPTHhmtOaImo", 
   "checksum":"b0bc4d2efce2efdc6da186d6dfa6edc", 
   "siteId":"12345", 
   "articleId":5, 
   "el":"comments1", 
   "datetimeFormat": function(theDateInput) { 
      return +theDateInput; 
   } 
};  
var conv = fyre.conv.load(networkConfig, [convConfig]);
```

## 符號標識{#section_inq_2n4_xz}

按照JDK、ICU和CLDR中定義的模式規範進行日期時間格式設定函式，對JS中的典型用法進行小幅修改。 如需詳細資訊，請參閱[Google Closure Library Documentation](https://developers.google.com/closure/library/docs/overview)。

```
  Symbol Meaning Presentation        Example 
  ------   -------                 ------------        ------- 
  G        era designator          (Text)              AD 
  y#       year                    (Number)            1996 
  Y* year (week of year)     (Number)            1997 
  u* extended year           (Number)            4601 
  M        month in year           (Text & Number)     July & 07 
  d        day in month            (Number)            10 
  h        hour in am/pm (1~12)    (Number)            12 
  H        hour in day (0~23)      (Number)            0 
  m        minute in hour          (Number)            30 
  s        second in minute        (Number)            55 
  S        fractional second       (Number)            978 
  E        day of week             (Text)              Tuesday 
  e* day of week (local 1~7) (Number)            2 
  D* day in year             (Number)            189 
  F* day of week in month    (Number)            2 (2nd Wed in July) 
  w* week in year            (Number)            27 
  W* week in month           (Number)            2 
  a        am/pm marker            (Text)              PM 
  k        hour in day (1~24)      (Number)            24 
  K        hour in am/pm (0~11)    (Number)            0 
  z        time zone               (Text)              Pacific Standard Time 
  Z        time zone (RFC 822)     (Number)            -0800 
  v        time zone (generic)     (Text)              Pacific Time 
  g* Julian day              (Number)            2451334 
  A* milliseconds in day     (Number)            69540000 
  '        escape for text         (Delimiter)         'Date=' 
  ''       single quote            (Literal)           'o''clock'
```

尚未支援標有「*」的項目。

標有「#」的項目的運作方式與Java不同。

模式字母的計數決定格式。

* **文字：** 4或更多，請使用完整表格。少於4，請使用短格式或縮寫形式（如果存在）。 (例如：&quot;EEE&quot;產生&quot;Monady&quot;,&quot;EEE&quot;產生&quot;Mon&quot;)。
* **數字：** 最小位數。較短的數字會以零填充為此數量(例如：如果&quot;m&quot;產生&quot;6&quot;,&quot;mm&quot;產生&quot;06&quot;。) 年是專門處理的；亦即，如果「y」的計數為2，則「年」將截斷為2位數。 (例如：如果&quot;yyyy&quot;產生&quot;1997&quot;,&quot;yy&quot;會產生&quot;97&quot;)。 與其他欄位不同，小數秒在右邊填充為零。
* **文字與數字：** 3或以上，使用文字。少於3，請使用數字。 (例如：&quot;M&quot;產生&quot;1&quot;, &quot;MM&quot;產生&quot;01&quot;, &quot;MMM&quot;產生&quot;Jan&quot;, &quot;MMM&quot;產生&quot;Jan&quot;。)

模式中不在[『a』...」範圍內的任何字元z』]和[『A』..」Z』]將被視為引號文字。 例如，字元如「:」、「.」、「『#』和『@」，即使未以單引號括住，也會出現在產生的時間文字中。
