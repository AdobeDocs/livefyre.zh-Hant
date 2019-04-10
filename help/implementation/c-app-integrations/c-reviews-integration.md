---
description: 允許客戶評量並檢閱您的產品方案。
seo-description: 允許客戶評量並檢閱您的產品方案。
seo-title: 評論
solution: Experience Manager
title: 評論
uuid: b740ee28-f6 f9-4ae7-9a7-1a5 cde97 bbb
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 評論 {#reviews}

允許客戶評量並檢閱您的產品方案。

評論可讓社群成員為任何產品或服務貢獻星級評分和定性審核。

## 整合 {#section_kk5_15b_c1b}

若要整合評論應用程式，請遵循整合對話應用程式的程序。請參閱 [內嵌應用程式](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md)。以下是內嵌評論應用程式的範例。

### 範例

```
var networkConfig = { 
   network: "client-solutions-uat.fyre.co" 
}; 
  
var convConfig = { 
   siteId: '304059', 
   articleId: 'sh_col_22_1373478370_reviews', 
   el: 'livefyre-comments', 
   app: 'reviews', 
   ratingSummaryEnabled: true, 
   maxRating: 5, 
   collectionMeta: 'eyJhbGciOiAiSFMyNTYiLCAidHlwIjogIkpXVCJ9.eyJ1cmwiOiAiaHR0cDovL3d3dy5kaXJlY3R2LmNvbS9wZXJzb24vQW5uYS1QYXF1aW4tYjJGU0wwZHJLM051YldjOS1yZXZpZXdzIiwgInNpdGVJZCI6ICIzMDQwNTkiLCAiYXJ0aWNsZUlkIjogInNoX2NvbF8yMl8xMzczNDc4MzcwX3Jldmlld3MiLCAidHlwZSI6ICJyZXZpZXdzIiwgInRpdGxlIjogIlRCX1BhcXVpbl9yYXRpbmdzX3Jldmlld3MifQ.hes3KMwygCG-fFDQlkaB-XlxGjW6-iZ68xA4RRGqUl0' 
}; 
  
Livefyre.require(['fyre.conv#3'], function (Review) { 
   new Review(networkConfig, [convConfig], function (reviewWidget) {}); 
   auth.delegate({ 
      login: function (callback) { 
         callback(null,{livefyre:'<userauthtoken>'}); 
      }, 
   }); 
});
```

如「建立 `CollectionMeta` 」區段中所示， `CollectionMeta` 為編碼JSON物件。在上述範例中，JSON物件採用下列格式，JWT編碼之前：

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## conconfig物件 {#section_pzv_ytb_c1b}

如果您已完成「快速入門」區段，您應該熟悉Conconfig物件。若要啓用「評論」，請使用下列欄位更新Conconfig：

* **AlwaysShowEditor***選用* 布林值：根據預設，只有在使用者按下「寫入審核」按鈕後，才會顯示評論編輯器。將此參數設為true，一律顯示編輯器。

* **應用程式***所需* 字串：用於審查的應用程式名稱。必須「檢閱」。

* **DefaultSortable**** 字串：可讓您選擇「評論」的預設排序選項。可能的值為：Mosthelpful、Highearch、LoweSoft、最新和最舊。

* **SocialTitle***選用* 布林值：停用並隱藏評論編輯器中的標題欄位，此欄位為必填且預設顯示。預設為true。

* **更新***可選* 布林值：用於在預設的星形選取模組上啓用半分級。預設為true。

* **HideShowReviewButton***選用* 布林值：控制 [!UICONTROL Show My Review] 按鈕是否顯示。設為true可讓使用者選擇是否顯示或顯示自己的評論。

* **maxPremium***可選* 整數用來設定預設星形選擇模組上顯示的星號數目。預設值為5。最多可設定100個。

* **ratingSummitEnabled***選擇性* 布林值：用來顯示評論應用程式上方的排名摘要檢視。這必須啓用，才能使用RatingSummitDelegate。預設為true。

## 檢閱系列中繼資料 {#section_k1s_sqb_c1b}

* **type：***必要* 字串：定義系列類型。`reviews`必須。

* **RatingDimensions***選用* 陣列：此Collection將使用之每類型維度的字串陣列。如果未指定此項目，則只允許使用個維度。

   例如，若要讓使用者對「設計」、「功能」和「效能」評分，請將陣列設定為： `ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **RatingSubparts***可選* 整數：要顯示在評論文字方塊中的分割數。子部分標籤會以參數傳入，如下所示。

   >[!NOTE]
   >您必須為每個子部分定義標籤。

* **ratingSubpartSID***選用* 陣列：可讓您為「排名收集」中的每個子部分定義ID，此ID可用來定位CSS和JavaScript中的這些子部分元素。當使用者張貼審核時，每個 `ratingSubpart` 人都有「 `data-lf-subpart-id`」屬性，填入此ID。

>[!NOTE]
>
>若要使用 `ratingSubpartsIds`， `ratingSubparts` 也必須定義參數，而且兩個陣列的長度必須相符。

```
networkConfig["strings"] = { 
   ratingSubpartPlaceholders: ['Pros...', 'Cons...'], 
   ratingSubpartTitles: ['Pros:', 'Cons:'], 
   ratingSubpartIds: ['pros', 'cons'], 
   reviewStreamTitle: 'Description:' 
} 
fyre.conv.load(networkConfig, [{ 
   app: 'reviews', 
   ratingSubparts: 2, 
    ... // More conv config settings 
}]);
```

>[!NOTE]
>
>如果您正在使用 `ratingDimensions`，則必須使用 `ratingSelectionDelegate`、 `ratingDisplayDelegate`和 `ratingSummaryDelegate` (如果您想要顯示排名摘要)。

## 評論自訂 {#section_khz_xmb_c1b}

### 設定星形影像

若要變更完整星形的影像，類別是 `goog-ratings-star`。將背景影象變更為您想要的影像。依預設，星形是28x28像素。

### 設定包含半顆星的星形影像

有了半顆星，就有兩個類別，分別為星形的每一側。上半部是星形 `fyre-rating-half-odd``fyre-rating-half-even`，右邊是。依預設，半顆星形是28像素。

### 設定星形的工具提示值

若要設定星形的工具提示值，請遵循字串自訂中所述的自訂文字。設定好之後，請使用索引鍵 `ratingValues` 和值，其中包含工具提示字串的陣列。如果您已停用一半的星形，陣列中的元素數目應與(以上) `maxRating` 相同。如果您啓用了一半的星形，元素的數目應為倍 `maxRating`。陣列中的第一個元素對應至最左方(或半顆星形)元素，並繼續由左至右。

### 切換「顯示我的評論」選項

若要開啓或關閉 [!UICONTROL Show My Review] 選項，請定位應用程式設定中的 `hideShowReviewButton` 參數。

### 依預設顯示文字編輯器

只有在使用者按下 [!UICONTROL write review] 按鈕後，才會顯示評論編輯器。若要依預設顯示此表單，請定位應用程式設定中的 `alwaysShowEditor` 參數。
