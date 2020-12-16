---
description: 分析您網站的使用者、內容和協調者活動。
seo-description: 分析您網站的使用者、內容和協調者活動。
seo-title: Analytics
solution: Experience Manager
title: Analytics
uuid: b022aa77-59b9-422a-8d9f-fb9d8a1b0478
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 1%

---


# Analytics{#analytics}

分析您網站的使用者、內容和協調者活動。

## Analytics {#topic_22D8FAE581CD440EA02B1595520F60C2}

分析您網站的使用者、內容和協調者活動。

Livefyre Analytics可讓您輕鬆讀取對話、協調和使用者資料的儀表板，以存取您的網路資料。 使用這些控制面板可監控您網站上的活動並執行快速分析。

控制面板可依網站、日期和活動來篩選。 使用視窗左上角的「網路」下拉式清單，選取要顯示的網站。 產生後，按一下要排序的欄標題，或將滑鼠移至圖形上，以取得任何資料點的更多特定資訊。

本頁介紹：

* 為控制面板選擇[日期範圍](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#DateRange)
* [顯示／隱藏可用活動](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ShowHideActivities)
* [匯出控制面板資料](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ExportDashboardData)
* [系列控制面板](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#CollectionsDashboard)
* [協調控制面板](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ModerationDashboard)
* [使用者儀表板](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#UsersDashboard)

>[!NOTE]
>
>Analytics目前支援源自Livefyre核心應用程式與協調的活動。 這些控制面板中包含的大部分活動也可透過[Livefyre JavaScript事件](https://answers.livefyre.com/developers/reference/app-customizations/javascript-events/)取用，此功能可用於您自己的自訂或協力廠商分析工具。

## 日期範圍 {#concept_798C438120E643B6BE262C9997DC87C4}

按一下日期下拉式清單，以選取要顯示的範圍。 使用快速日期，或從提供的日曆中選擇開始和結束日期。

![](assets/analytics-date-range.png)

快速日期：

* **今天：** 顯示從當天午夜至此時刻前最後一個完整小時的資料。
* **昨天：** 顯示前24小時的資料。
* **7天：顯** 示前7天的資料，不包括今天。
* **30天：顯** 示前30天的資料，不包括今天。
* **本週：顯** 示從上週日的午夜至此時刻前最後一個完整小時的資料。
* **本月：顯** 示從當月第一天的午夜到此時刻前最後一個完整小時的資料。
* **上週：顯** 示上週的資料。
* **上個月：** 顯示上個月的資料。

## 顯示／隱藏活動{#concept_022D9851CBCE4A2FB80D0AE52A23744D}

活動是使用者在您的網站上執行的動作，包括加上註解、標幟、共用和協調。 使用&#x200B;**顯示／隱藏活動**&#x200B;下拉式清單，選擇您希望包含在控制面板中的活動。

>[!NOTE]
>
>為篩選選取新事件時，不會變更URL，就會重新呈現頁面。

![](assets/analytics-show-hide-activities.png)

可用活動視控制面板類型和匯出而異，可能包括：

* **貼文：顯** 示從當天午夜到當天上午，直到此時刻前最後一個完整小時的資料。
* **回覆：** 顯示前24小時的資料。
* **按贊次** 數：顯示前7天的資料，不包括今天。
* **收回贊** 次數：顯示前30天的資料，不包括今天。
* **包含媒體：** 顯示從上週日的午夜到此時刻前最後一個完整小時的資料。
* **貼文包含像片上** 傳：顯示當月第一天的午夜至此時刻前最後一個完整小時的資料。
* **貼文具有連結：** 顯示上週的資料。
* **貼文有@mentions:** 顯示上個月的資料。
* **已核准：** 顯示上個月的資料。
* **Bozo&#39;d：顯** 示上個月的資料。
* **Trashed:** 顯示上個月的資料。
* **協調總計：** 顯示上個月的資料。

## 導出控制面板資料{#concept_730DB61A9F894BE6BFB34E0E2A421ED3}

使用&#x200B;**Export**&#x200B;下拉式功能表，將控制面板資料匯出為CSV檔案。

* 每日摘要（僅限系列）:匯出每個「系列」的上一週每日計算。
* 表格資料：匯出所有匯總的「集合」資料（目前報表中的所有欄和所有列）。
* 原始資料：匯出用於建立目前統計報表的所有個別事件。

>[!NOTE]
>
>匯出這些報表可能需要幾分鐘的時間。 所有時間戳記都是Unix時間。

## 集合 {#concept_228D8E5553784DB8BABF3819A5FF0345}

「系列」控制面板會依「系列」列出使用者活動，讓您決定最吸引人的內容。 每個列出的系列都包含可在其中找到其頁面的連結。

![](assets/analytics-collections.png)

## Moderation {#concept_98689B1E804B43CEA21E3F456107CCD9}

「協調」控制面板會依協調者列出事件，讓您評估其活動。 使用此報表可尋找您最活躍的協調者，以及他們最常用的協調動作。

>[!NOTE]
>
>Livefyre協調者名稱Livefyre System的自動協調活動將會列出。

![](assets/analytics-moderation.png)

## 使用者 {#concept_D1A83E31C7B5467F9C844CBF9A740E12}

「使用者」控制面板會依使用者顯示網站活動，讓您分析個別使用者與您網站的互動方式。 使用此控制面板可尋找網站上最活躍的使用者，並評估最熱門的網站活動。

![](assets/analytics-users.png)

