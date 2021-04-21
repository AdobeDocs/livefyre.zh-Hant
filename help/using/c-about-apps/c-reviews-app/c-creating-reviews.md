---
description: 審核提供廣泛的自訂設定，讓您建立符合您需求和品牌的審核應用程式。
title: 建立審核應用程式
exl-id: 14f074d2-922c-4997-8d7d-f2c92f069e07
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---

# 建立審核應用程式{#creating-a-reviews-app}

審核提供廣泛的自訂設定，讓您建立符合您需求和品牌的審核應用程式。

將「審核應用程式」自訂內嵌在您的網站上，做為JS應用程式使用。 您無法在Livefyre Studio中建立評論應用程式。 若要在您的網站上建立評論應用程式，請參閱[評論整合](/help/implementation/c-app-integrations/c-reviews-integration.md)。


## 評分{#section_hs5_c4h_21b}

評分是您的使用者指派給「評論」的數值。 每個評論都必須包含評分，預設會顯示為5星型系統。 (雖然「應用程式」中的分級顯示為0.5 - 5，但Livefyre在後端儲存的X/100比例是1星為20/100,2星為40/100。 在Studio中檢視審核時，會顯示此比例。)

0.5到5的評分等級可設定為最高100的評分，也提供一半的評分。

如需詳細資訊，請參閱「檢閱convConfig」物件的maxRating欄位。

## 分級圖示樣式{#section_cqn_c4h_21b}

您可自訂評分圖示，以符合您的品牌和風格。

如需詳細資訊，請參閱「檢閱自訂」下方的&#x200B;**[!UICONTROL Configure Star Ratings]**。

## 評分Dimension{#section_cnx_snh_21b}

評分維度是您的審核者對產品或服務評分的類別。 評等維度的範例包括「效能」、「設計」、「成本」、「整體」或您選擇的任何其他類別。

預設值是顯示一個「整體」評分維度，但您可以定義並實作多個評分維度，如下例所示。

如需詳細資訊，請參閱「檢閱系列中繼資料」下方的ratingDimensions欄位。

## 查看文本欄位{#section_xcm_4nh_21b}

您也可以在正在審閱的產品或體驗中加入其他文字欄位。 （例如，文字欄位可能包含「利弊」或「不要錯過」。） 可自訂欄位的編號、標題和預設文字。 使用者必須填寫所有文字欄位，以及審閱標題、內文和評分，才能發佈其審閱。 無法包含可選文字欄位。

如需詳細資訊，請參閱「檢閱系列中繼資料」的ratingDimensions欄位。

## 查看摘要{#section_ysz_lnh_21b}

依預設，摘要區段會顯示在「審核應用程式」的頂端。 此區段包含「評論系列」的「平均使用者評分」和「評分劃分」的視覺化，僅顯示整數。 此區段為唯讀，視需要可隱藏。

如需詳細資訊，請參閱「檢閱convConfig」物件的ratingSummaryEnabled欄位。

## 垃圾訊息和褻瀆篩選{#section_hcm_jnh_21b}

一旦張貼「審閱」,「檢閱的標題和內文」就會透過我們的「垃圾訊息篩選」和「粗細篩選」傳遞。

## 文字自訂{#section_tjf_hnh_21b}

文字字串（包括工具提示和標籤）可能會針對語言自訂，或符合您的品牌。

## 回覆評論{#section_yng_fnh_21b}

使用者可以回覆每個「評論系列」中自己或其他人的「評論」。 只有登入的使用者可以張貼回覆至審核。

Studio中啟用了使用者回覆審核的選項。 擁有者可以針對網路、網站或系列層級切換此設定。 協調者只能為其系列啟用此設定。

## SocialSync和組織{#section_llh_2nh_21b}

由於「審核」的設計是為每個已提交的內容新增數值，因此「審核」不支援SocialSync和「組織」。

## 審核API {#section_xrh_wmh_21b}

審核API可讓您顯示平均使用者評分和評分劃分資訊，以及使用者審核網站其他區域的活動。

[評分與評論](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** 「BootstrapAPI端點」可讓Google等搜尋引擎讀取您的審核，讓內容和關鍵字可改善您的搜尋引擎最佳化。

* **[!UICONTROL Average User Ratings]** 「平均使用者評分API」會擷取一或多個「評論系列」的平均使用者評分，讓您在索引頁面上建立此項資訊的視覺化效果，或新增至搜尋索引頁面。

* **[!UICONTROL Ratings Breakdown]** 「分級劃分API」會擷取特定「評論系列」的所有分級劃分，並可讓您建立視覺化，顯示與每個星號評分相關聯的評論數。

* **[!UICONTROL User Reviews]** 「使用者檢閱API」會擷取特定使用者的最新檢閱。此活動可用於在使用者的公開設定檔頁面上顯示使用者的審核。
