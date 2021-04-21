---
description: 讓客戶對您的產品方案進行評分和審核。
title: 評論
exl-id: 2f10646e-59c4-459c-ae1b-749f951a06d2
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# 評論{#reviews}

讓客戶對您的產品方案進行評分和審核。

評論可讓社群成員針對任何產品或服務提供星級評價和定性評論。

## 整合 {#section_kk5_15b_c1b}

若要整合「評論應用程式」，請依照「整合對話應用程式」的程式進行。 請參閱[內嵌應用程式](/help/implementation/c-livefyre-identity-comp/t-using-studio-to-connect-your-social-apps-to-your-livefyre-implementation.md)。 以下是內嵌的「評論應用程式」的範例。

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

如「建立`CollectionMeta`」區段中所述，`CollectionMeta`是編碼的JSON物件。 在上述範例中，JSON物件在進行JWT編碼前會採用下列格式：

```
{ 
"url": "https://www.directv.com/person/Anna-Paquin-b2FSL0drK3NubWc9-reviews",  
"siteId": "304059",  
"articleId": "sh_col_22_1373478370_reviews",  
"type": "reviews",  
"title": "TB_Paquin_ratings_reviews" 
}
```

## convConfig對象{#section_pzv_ytb_c1b}

如果您已完成「快速入門」區段，您應該熟悉convConfig物件。 若要啟用「檢閱」，請使用下列欄位更新convConfig:

* **** ** alwaysShowEditoroptionalboolean:依預設，只有在使用者按下「寫入審核」按鈕後，才會顯示審核編輯器。將此參數設為true，以一律顯示編輯器。

* **** ** apprequiredstring:用於審核的應用程式名稱。必須是「評論」。

* **** ** defaultSortoptionalstring:允許您為「審閱」(Reviews)選擇預設排序選項。可能的值包括：最有用、最高評級、最低評級、最新和最舊。

* **disableTitleoptionalboolean** ** :停用並隱藏審核編輯器中的標題欄位，此為必要欄位，預設為可見欄位。預設為true。

* **enableHalfRatingoptional** ** 布林值：用於在預設星號選擇模組上啟用半評分。預設為true。

* **hideShowReviewButtonoptional** ** 布林值：控制是否 [!UICONTROL Show My Review] 顯示按鈕。設為true可讓您的使用者選擇是否顯示或顯示自己的審核。

* **** ** maxRatingoptionalinteger用於設定預設星號選擇模組上顯示的星號數。預設為 5。最多可以配置100個。

* **ratingSummaryEnabledoptionalboolean** ** :用於在「評論應用程式」上方顯示評分摘要檢視。必須啟用此選項，才能使用ratingSummaryDelegate。 預設為true。

## 檢閱系列中繼資料{#section_k1s_sqb_c1b}

* **type:** ** requiredstring:定義系列類型。必須是`reviews`。

* **ratingDimensionsoptionalarray:** ** 此系列將使用之每種維度類型的字串陣列。如果未指定，則僅允許1個維。

   例如，若要讓使用者對您的產品進行「設計」、「功能」和「效能」評分，請將陣列設定為：`ratingDimensions: [‘design’, ‘features’, ‘performance’]`

* **評** ** 分子部分索引整數：要在審閱文字方塊中顯示的分區數。子部件標籤會與參數一起傳遞，如下所示。

   >[!NOTE]
   >必須為每個子部件定義標籤。

* **ratingSubparts** ** Idsoptionalarray:可讓您為「分級收集」中的每個子部件定義ID，此ID可用於定位CSS和JavaScript中的這些子部件元素。當使用者張貼審核時，每個`ratingSubpart`都會有「`data-lf-subpart-id`」屬性，並填入此ID。

>[!NOTE]
>
>要使用`ratingSubpartsIds`，還必須定義`ratingSubparts`參數，並且兩個陣列的長度必須匹配。

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
>如果您使用`ratingDimensions`，則必須使用`ratingSelectionDelegate`、`ratingDisplayDelegate`和`ratingSummaryDelegate`（如果您要顯示評分摘要）。

## 查看自定義{#section_khz_xmb_c1b}

### 配置星形映像

若要變更完整星形的影像，類別為`goog-ratings-star`。 將背景影像變更為您想要的任何影像。 依預設，星形為28 x 28像素。

### 使用半星形設定星形影像

有半星，有兩門課，一門課 半星的左側為`fyre-rating-half-odd`，右側為`fyre-rating-half-even`。 依預設，半星數為28 x 14像素。

### 設定星形工具提示值

若要設定星形的工具提示值，請遵循「字串自訂」中所述的自訂文字。 設定好後，請使用鍵`ratingValues`和包含工具提示字串的陣列值。 如果停用半星形，則陣列中的元素數應與`maxRating`（上）相同。 如果您已啟用半星形，則元素數應為2x `maxRating`。 陣列中的第一個元素對應至最左星形（或半星形）元素，並依左至右繼續。

### 切換「顯示我的評論」選項

若要開啟或關閉[!UICONTROL Show My Review]選項，請在應用程式設定中定位`hideShowReviewButton`參數。

### 依預設顯示文字編輯器

只有在用戶按下[!UICONTROL write review]按鈕後，才會顯示審閱編輯器。 若要依預設顯示此表單，請定位應用程式設定中的`alwaysShowEditor`參數。
