---
description: 分析您網站的使用者、內容和協調者活動。
seo-description: 分析您網站的使用者、內容和協調者活動。
seo-title: Analytics
solution: Experience Manager
title: Analytics
uuid: b022aa77-59b9-422a-8d9f-fb9 d8 a1 b0478
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Analytics{#analytics}

分析您網站的使用者、內容和協調者活動。

## Analytics {#topic_22D8FAE581CD440EA02B1595520F60C2}

分析您網站的使用者、內容和協調者活動。

Livefyre Analytics可讓您輕鬆存取您的網路資料，輕鬆閱讀「交談」、「協調」和「使用者」資料的控制面板。使用這些控制面板監視活動並在網站上執行快速分析。

控制面板可依網站、日期和活動進行篩選。使用視窗左上方的「網路」下拉式清單，選取要顯示的網站。產生後，按一下欄標題以排序，或將滑鼠移到圖形上方，以取得任何資料點的詳細資訊。

此頁面說明：

* Selecting a [Date Range](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#DateRange) for your dashboard
* [顯示/隱藏可用活動](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ShowHideActivities)
* [匯出控制面板資料](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ExportDashboardData)
* [系列控制面板](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#CollectionsDashboard)
* [協調控制面板](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ModerationDashboard)
* [使用者控制面板](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#UsersDashboard)

>[!NOTE]
>
>Analytics目前支援源自Livefyre核心應用程式和協調的活動。這些控制面板中包含的大部分活動也可透過 [Livefyre JavaScript事件取得，這些事件](https://answers.livefyre.com/developers/reference/app-customizations/javascript-events/)可能用來強化您自己的自訂或第三方分析工具。

## 日期範圍 {#concept_798C438120E643B6BE262C9997DC87C4}

按一下日期下拉式清單以選取要顯示的範圍。使用快速日期，或從提供的日曆選取開始和結束日期。

![](assets/analytics-date-range.png)

快速日期：

* **今天：** 顯示當天凌晨的資料，直到目前的最後一個完整小時。
* **昨天：** 顯示前24小時的資料。
* **天：** 顯示前天的資料，不包括今天。
* **30天：** 顯示前30天的資料，而非今天。
* **本週：** 顯示從上個周日凌晨到最後一個完成時間的資料。
* **本月：** 顯示目前每月的第一天早上的資料，直到目前的最後一個完整小時。
* **上周：** 顯示上周的資料。
* **上個月：** 顯示上個月的資料。

## 顯示/隱藏活動 {#concept_022D9851CBCE4A2FB80D0AE52A23744D}

活動是使用者在您的網站上執行的動作，包括註解、標記、共用和協調。使用 **「顯示/隱藏活動** 」下拉式清單選擇要納入控制面板中的活動。

>[!NOTE]
>
>選取篩選器的新事件會重新轉換頁面，而不會變更URL。

![](assets/analytics-show-hide-activities.png)

可用活動視控制面板類型和匯出而異，可能包括：

* **貼文：** 顯示當天凌晨的資料，直到目前的最後一個完整小時。
* **回覆：** 顯示前24小時的資料。
* **按贊：** 顯示前天的資料，不包括今天。
* **收回贊：** 顯示前30天的資料，而非今天。
* **包含媒體：** 顯示從上個周日凌晨到最後一個完成時間的資料。
* **貼文具有像片上傳：** 顯示目前每月的第一天早上的資料，直到目前的最後一個完整小時。
* **貼文具有連結：** 顯示上周的資料。
* **貼文有@提及次數：** 顯示上個月的資料。
* **核准：** 顯示上個月的資料。
* **Bodo'd：** 顯示上個月的資料。
* **已損毀：** 顯示上個月的資料。
* **協調總計：** 顯示上個月的資料。

## 匯出控制面板資料 {#concept_730DB61A9F894BE6BFB34E0E2A421ED3}

使用 **「匯出** 」下拉式選單，將控制面板資料匯出為CSV檔案。

* 每日摘要(僅限系列)：匯出每個系列的最後一個完整星期記錄。
* 表格資料：匯出所有已捲動的系列資料(所有欄和目前報表中的所有列)。
* 原始資料：匯出用於建立目前統計報表的所有個別事件。

>[!NOTE]
>
>這些報告可能需要幾分鐘的時間才能匯出。所有時間戳記都是Unix時間。

## 系列 {#concept_228D8E5553784DB8BABF3819A5FF0345}

「系列」控制面板會列出「Collection」(系列)的使用者活動，讓您判斷最(和最低)吸引人的內容。每個列出的系列都包含可找到其頁面的連結。

![](assets/analytics-collections.png)

## 協調 {#concept_98689B1E804B43CEA21E3F456107CCD9}

「協調」控制面板會依協調者列出事件，讓您評估其活動。使用此報表可尋找最活躍的協調者及其最常用的協調動作。

>[!NOTE]
>
>「自動化Livefyre」協調活動將列在協調者名稱Livefyre System中。

![](assets/analytics-moderation.png)

## 使用者 {#concept_D1A83E31C7B5467F9C844CBF9A740E12}

「使用者」控制面板會依使用者顯示網站活動，讓您分析個別使用者如何與您的網站互動。使用此控制面板可尋找您網站上最活躍的使用者，並評估最受歡迎的網站活動。

![](assets/analytics-users.png)

