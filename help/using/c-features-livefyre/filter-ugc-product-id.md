---
description: 依產品ID篩選UGC可讓您在多個頁面上內嵌完全相同的應用程式，同時針對每個頁面顯示不同的產品特定UGC。
seo-description: 依產品ID篩選UGC可讓您在多個頁面上內嵌完全相同的應用程式，同時針對每個頁面顯示不同的產品特定UGC。
seo-title: 依產品ID篩選UGC
title: 依產品ID篩選UGC
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 76efa427b59a709009a3c2d3744ea65e0c959816
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---


# 依產品ID {#filter-ugc-product-id}篩選UGC

依產品ID篩選UGC可讓您在多個頁面上內嵌完全相同的應用程式，同時針對每個頁面顯示不同的產品特定UGC。

若要依產品ID篩選UGC，請遵循下列步驟：

1. 在Livefyre Studio中，導覽至&#x200B;**[!UICONTROL Apps]**&#x200B;標籤。

1. 選取您要修改的應用程式。

1. 在左側導軌中選取「設計器」標籤。

1. 啟用 **[!UICONTROL Filter UGC by Product ID]**.

![](assets/filter-ugc-product-id.png)

1. 選擇頂層產品資料夾，其中包含您要依據篩選UGC的產品或產品。
使用CTRL/Command +按一下可選擇多個資料夾。

1. 禁用&#x200B;**[!UICONTROL Show related content]**。
啟用後，使用`data-lf-attr-product`屬性篩選的內容會先顯示，接著是應用程式中的所有其他內容。

1. 按一下 **[!UICONTROL Publish]**.

1. 將您要篩選依據的產品ID插入結果代碼中。

>[!NOTE]
>
>若要找到產品ID，請導覽至&#x200B;**[!UICONTROL Settings > Products]**。 找出所要的產品並選取它，然後會顯示ID。

例如，會為媒體塗鴉牆應用程式產生下列程式碼：

```
<script type="text/javascript" src="https://cdn.livefyre.com/
Livefyre.js"></script><div class="lf-app-embed" data-lfapp="
59dc41fa-85a5-49ed-8d60-d74616b3ccd1/tagged/published" datalf-
env="prod" data-lf-read-only="" data-lf-attr-product="<product
 1>,<product 2>"></div><script>Livefyre.require(["app-embed#1.0.11"],
 function (appEmbed) {appEmbed.loadAll().done(function(embed)
 {embed = embed[0];if (embed.el.onload && embed.getConfig)
 {embed.el.onload(embed.getConfig());}});});</script>
```

若要標籤產品，請將`data-lf-attr-product`屬性中的`<product 1>`取代為所需的產品ID。 您可以新增其他以逗號分隔的產品ID，以標籤一或多個產品。 產品必須包含在步驟5中選取的頂層產品資料夾或資料夾中。

修改後的程式碼區段會顯示為：

```
<script type="text/javascript" src="https://cdn.livefyre.com/
Livefyre.js"></script><div class="lf-app-embed" data-lfapp="
59dc41fa-85a5-49ed-8d60-d74616b3ccd1/tagged/published"
 data-lf-env="prod" data-lf-read-only="" data-lf-attrproduct="
109,47"></div><script>Livefyre.require(["app-embed#1.0.11"],
 function (appEmbed) {appEmbed.loadAll().done(function(embed)
 {embed = embed[0];if (embed.el.onload && embed.getConfig)
 {embed.el.onload(embed.getConfig());}});});</script>
```

應用程式現在只會顯示標籤的產品ID。