---
description: 依產品ID篩選UGC可讓您在多個頁面上內嵌完全相同的應用程式，同時顯示每個頁面的不同產品特定UGC。
seo-description: 依產品ID篩選UGC可讓您在多個頁面上內嵌完全相同的應用程式，同時顯示每個頁面的不同產品特定UGC。
seo-title: 依產品ID篩選UGC
title: 依產品ID篩選UGC
uuid: 98108ddb-5710-4331-891b-7e1bbb106059
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 依產品ID篩選UGC {#filter-ugc-product-id}

依產品ID篩選UGC可讓您在多個頁面上內嵌完全相同的應用程式，同時顯示每個頁面的不同產品特定UGC。

若要依產品ID篩選UGC，請遵循下列步驟：

1. 在Livefyre Studio中，導覽至 **[!UICONTROL Apps]** 標籤。

1. 選取您要修改的應用程式。

1. 選取左側邊欄中的「設計人員」標籤。

1. 啓用 **[!UICONTROL Filter UGC by Product ID]**。

![](assets/filter-ugc-product-id.png)

1. 選取包含您要依「UGC」篩選的產品或產品的頂層產品資料夾。
使用CTRL/Command+按一下以選取多個檔案夾。

1. 停用 **[!UICONTROL Show related content]**。
啓用後，會先顯示使用 `data-lf-attr-product` 屬性篩選的內容，然後再顯示應用程式中的所有其他內容。

1. 按一 **[!UICONTROL Publish]**下。

1. 將您要篩選的產品ID插入到結果代碼中。

>[!NOTE]
>
>若要尋找產品ID，請導覽至 **[!UICONTROL Settings > Products]**。找出所需的產品，然後選取ID並顯示ID。

例如，針對媒體塗鴉牆應用程式產生下列程式碼：

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

若要標記產品，請在 `<product 1>``data-lf-attr-product` 屬性中取代所需的產品ID。您可以新增其他逗號分隔的產品ID，以標記一個或多個產品。產品必須包含在步驟中所選的頂層產品資料夾或資料夾中。

修改後的代碼區段會顯示為：

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

應用程式現在只會顯示標記的產品ID。