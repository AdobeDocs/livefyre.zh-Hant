---
description: Sidesorp設定物件是JSON物件，用於指定Livefyre應用程式在頁面上轉譯的內容。
seo-description: Sidesorp設定物件是JSON物件，用於指定Livefyre應用程式在頁面上轉譯的內容。
seo-title: Sidesform配置選項
solution: Experience Manager
title: Sidesform配置選項
uuid: 067e51e6-9720-4226-a805-c7a07c8cdaa0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 2%

---


# Sidesk配置選項{#sidenotes-configuration-options}

Sidesorp設定物件是JSON物件，用於指定Livefyre應用程式在頁面上轉譯的內容。

對象包含以下參數：

| 參數 | 類型 | 說明 |
|--- |--- |--- |
| authDelegate | *需求* 物件 | 新樣式或舊樣式已初始化驗證委派。 |
| collectionMeta | *需求* 物件 | 如需詳細資訊，請參閱collectionMeta Token。 |
| customIcon | *選* 項字串 | 設定自訂啟動程式圖示的URL。 預設為Livefyre泡泡。 |
| customStyles | *選* 項對象 | 新增自訂樣式以變更Siestror的外觀和感覺。 如需詳細資訊，請參閱自訂樣式。 |
| disableStream | *可選布* 林值 | 如果為true，則停用此Sidesirvs例項（不在其他注釋串流中）中的即時串流。 設值為 false。 |
| 環境 | *選* 項字串 | 指定Livefyre UAT環境。 唯一可能的值是`t402.livefyre.com`。 對於生產，必須移除此參數。 |
| iconVisibility | *選* 項對象或字串 | 定義暫留或靜態時是否顯示Sides圖示。 如果這是字串，則會用於區塊圖示的兩個版本（空白且含有Sides）。 如果對象，則必須指定每種類型：{empty:「hover」，數字：「static」}。 預設為靜態。 |
| inlineThreads | *可選* 布爾值 | 如果為true，則Sirexheare線程將直接插入與其關聯的塊之後。 設值為 false。 |
| numSiresEl | *選* 項對象、字串或陣列 | 指定Sidesars計數構件將裝飾的元素。 （此介面工具集顯示頁面上的表示號碼，以及有關表示號的資訊。） 如果字串選取器符合多個元素，則會選擇第一個元素。 （使用CSS3 DOM選擇器規格。） |
| position | *選* 項字串 | 當點按已啟用「表示」的元素時，會決定彈出畫面的位置。 可能的值為「smart」、「left」、「right」、「bottom」。 預設值為「智慧型」，會將快顯視窗對齊頁面右側，除非空間不足（在此情況下，會移至內容下方）。 |
| 選擇器 | *需* 求物件、字串或陣列 | 指定啟動器表徵圖應顯示的元素。 （使用CSS3 DOM選擇器規格。） 如果物件包含「包含」區段和「排除」區段，這些區段將針對任何符合的包含套用CSS選擇器，並移除符合排除的任何元素。 若為字串，則會在頁面上包含任何相符的元素。 如果是陣列，則列出要包含的元素。 |
| 字串 | *選* 項對象 | 新增自訂文字字串，以變更應用程式中的任何語言或文字。 如需詳細資訊，請參閱自訂字串。 |
| threadContainerEl | *選* 項對象、字串或陣列 | 指定將顯示sidesirf線程的元素。 此參數允許您重新定位線程。 如果字串選取器符合多個元素，則會選擇第一個元素。 （使用CSS3 DOM選擇器規格。） |

