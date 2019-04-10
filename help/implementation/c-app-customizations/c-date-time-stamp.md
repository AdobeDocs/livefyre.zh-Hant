---
description: 使用Livefyre. js自訂日期和時間戳記。
seo-description: 使用Livefyre. js自訂日期和時間戳記。
seo-title: 自訂日期和時間戳記
solution: Experience Manager
title: 自訂日期和時間戳記
uuid: 632ea405-56b7-4664-8d2b-0dd0a7611bd8
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 自訂日期和時間戳記{#customize-the-date-and-time-stamp}

使用Livefyre. js自訂日期和時間戳記。

Livefyre應用程式提供選項參數dateTimeFormat，以指定日期格式，如下所述。

* [術語](#c_date_time_stamp/section_xsk_jn4_xz)
* [格式設定](#c_date_time_stamp/section_ynx_gn4_xz)
* [符號指定](#c_date_time_stamp/section_inq_2n4_xz)

## 術語 {#section_xsk_jn4_xz}

* **絕對時間戳記** 定義為精確和特定時間(例如2012年月日12：00pm)
* **相對時間戳記** 定義為一般和較不精確的時間(例如25秒前、14分鐘前、天前、年前等)。

## 格式設定 {#section_ynx_gn4_xz}

dateTimeFormat參數在沒有引數時具有下列預設行為：

* 資料時間格式：MMMM d yyyy(2012年月日)
* 20160分鐘(14天)直到絕對時間(14天)直到相對時間戳記變成絕對時間戳記)

dateTimeFormat參數接受三種可能的引數類型：日期時間、格式和字串。

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

指定SocialFormat及/或targetSuntiableSolution的物件。使用值-1的SundetSuntilabsolution時間可縮短時間絕對時間。

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

將「日期」物件視為引數的函數，並傳回要顯示的日期時間字串

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

## 符號指定 {#section_inq_2n4_xz}

資料時間格式函數依JDK、ICU和CLDR中定義的模式規格而定，並對JS中的一般用法進行小幅修改。如需詳細資訊，請參閱 [Google關閉資料庫文件](https://developers.google.com/closure/library/docs/overview)。

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

目前尚未支援標示為'*'的項目。

標示為「#」的項目與Java不同。

圖樣字母的計數會決定格式。

* **文字：** 或以上，使用完整表格。少於4，使用簡短或縮寫表格存在。(例如：「EEE」製作「星期一」，「EEE」製作「Mon」)。
* **數字：** 最小值。較短的數字會以零填補至此金額(例如：如果「m」產生「6」，「mm」會產生「06」。年度處理；也就是說，如果「y」的計數為2，則「年」將被截斷為位數。(例如：如果「yyyy」產生「1997」，「yy」會產生「97」。)不同於其他欄位，分數秒會以零填補在右側。
* **文字與數字：** 或以上，使用文字。少於3，使用數字。(例如：「M」製作「1」、「MM」製作「01」、「MMM」產生「Jan」，而「MMMM」製作「一月」。)

未在 [「a」範圍內的任何字元。''」z'] 和 ['A'.''」Z將] 視為引用文字。例如，例如'：'，'.'、'、'#'和'@'會出現在產生的時間文字中，即使不是以單引號也不是。
