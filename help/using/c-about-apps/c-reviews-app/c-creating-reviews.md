---
description: 評論提供廣泛的自訂功能，讓您建立符合需求和品牌的審核應用程式。
seo-description: 評論提供廣泛的自訂功能，讓您建立符合需求和品牌的審核應用程式。
seo-title: 建立評論應用程式
solution: Experience Manager
title: 建立評論應用程式
uuid: 6caeafe7-c04 e-484e-b02 f-98dc6 d9 b3184
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 建立評論應用程式{#creating-a-reviews-app}

評論提供廣泛的自訂功能，讓您建立符合需求和品牌的審核應用程式。

使用Reviews應用程式將Reviews應用程式自訂為JS應用程式。您無法在Livefyre Studio中建立評論應用程式。若要在您的網站上建立評論應用程式，請參閱 [評論整合](/help/implementation/c-app-integrations/c-reviews-integration.md)。


## 評分 {#section_hs5_c4h_21b}

評分是使用者指派給評論的數值。每項審核都必須包含評等，依預設會顯示為個星形系統。(雖然應用程式中的評分會顯示為0.5-5，Livefyre會儲存在後端的X/100比例，如此，個星號是20/100，而星形是40/100。在Studio中檢視評論時，會顯示此比例。)

分級等級為0.5到5，最高可設定為100，而且還有一半的評分。

如需詳細資訊，請參閱評論Config物件的maxPremium欄位。

## 分級圖示樣式 {#section_cqn_c4h_21b}

您可以自訂圖示圖示，以符合品牌和風格。

如需詳細資訊，請參閱 **[!UICONTROL Configure Star Ratings]** 「檢閱自訂」。

## 排名維度 {#section_cnx_snh_21b}

排名維度是評量者對產品或服務評分的類別。排名維度的範例為「效能」、「設計」、「成本」、「整體」或任何您選擇的其他類別。

預設是顯示一個「整體」分級維度，但您可以定義並實作多個分級維度，如下列範例所示。

如需詳細資訊，請參閱「檢閱系列中繼資料」下方的「RatingDimensions」欄位。

## 檢閱文字欄位 {#section_xcm_4nh_21b}

您也可以在所檢視的產品或體驗中加入其他文字欄位。(例如，文字欄位可能包括Profs和Cons，或不要錯過。)欄位的數字、標題和預設文字是可自訂的。使用者必須填寫所有文字欄位，以及檢閱標題、內文和評分，才能發佈評論。無法包含選擇性文字欄位。

如需詳細資訊，請參閱「檢閱系列中繼資料的RatingDimensions」欄位。

## 檢閱摘要 {#section_ysz_lnh_21b}

根據預設，摘要區段會顯示在評論應用程式的頂端。本節包含「平均使用者評分」和「評論系列評分劃分」的視覺化，僅顯示整數。此區域為唯讀，可視需要隱藏。

如需詳細資訊，請參閱「檢閱conconConfig」物件的「RatingSummityEnabled」欄位。

## 垃圾訊息和嚴格篩選 {#section_hcm_jnh_21b}

評論張貼後，「檢閱」標題和「內文」的文字就會通過我們的垃圾訊息篩選和「嚴格篩選」。

## 文字自訂 {#section_tjf_hnh_21b}

文字字串，包括工具提示和標籤，可以針對語言自訂或符合您的品牌。

## 回覆評論 {#section_yng_fnh_21b}

使用者可在每個評論系列中回覆自己或其他的評論。只有登入的使用者可以張貼回覆給審核。

在Studio中啓用使用者回覆評論的選項。擁有者可切換此設定為「網路」、「網站」或「系列」層級。協調者只能針對其系列啓用此設定。

## SocialSync與Curgate {#section_llh_2nh_21b}

由於「評論」是為了新增每個提交內容的數值而設計，因此「評論」並不支援「同步」和「組織」。

## 評論API {#section_xrh_wmh_21b}

評論API可讓您顯示平均使用者評分和分級劃分資訊，以及使用者檢閱網站上其他區段的活動。

[評分與評鑒](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** Bootstrap API端點可讓搜尋引擎(例如Google)讀取您的檢閱，讓內容和關鍵字改善搜尋引擎最佳化。

* **[!UICONTROL Average User Ratings]** 「平均使用者評分API」會擷取一或多個「檢閱系列」的平均使用者評分，讓您在索引頁面上建立此資訊的視覺化，或新增至搜尋索引頁面。

* **[!UICONTROL Ratings Breakdown]** 「分級劃分API」會擷取特定評論集合的所有評分劃分，並讓您建立視覺化，以顯示與每個星級評分關聯的評論數目。

* **[!UICONTROL User Reviews]** 使用者評論API會擷取特定使用者的最近評論。此活動可用來在其公開描述檔頁面上顯示使用者的評論。
