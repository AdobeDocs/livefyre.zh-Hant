---
description: 使用可用的CSS類別自訂您的應用程式顯示。
seo-description: 使用可用的CSS類別自訂您的應用程式顯示。
seo-title: CSS類別
solution: Experience Manager
title: CSS類別
uuid: 8714e7e5-3858-458f-a464-de87fd2f0ff0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 1%

---


# CSS類{#css-classes}

使用可用的CSS類別自訂您的應用程式顯示。

適用於聊天、留言、即時部落格、評論和Sidestrom。

使用CSS自訂Livefyre應用程式，只要使用您自己的樣式表覆寫預設的App CSS，即可與您的頁面進行更完整的整合。 本節說明可用的CSS自訂。

* [編輯器CSS](#c_css_classes/section_edx_prh_xz)
* [排序選項CSS](#c_css_classes/section_btq_4rh_xz)
* [注釋CSS](#c_css_classes/section_mlv_nrh_xz)
* [精選注釋CSS](#c_css_classes/section_m2v_mrh_xz)
* [封存的注釋CSS](#c_css_classes/section_bs5_lrh_xz)
* [注釋通告程式CSS](#c_css_classes/section_dy4_krh_xz)
* [Storify CSS類別](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## 編輯器CSS {#section_edx_prh_xz}

使用這些類來更改後置編輯器介面。

| 類別 | 說明 |
|---|---|
| .fyre-comment-count | 顯示注釋數的文字。 |
| .fyre-login-bar | 包含登入列和選項的邊界方框。 |
| .fyre-live-container | 圍繞接聽人數和頭像的邊界方框。 |
| .fyre編輯器 | .fyre-login-bar、.fyre-live-container和使用者在文字區域中撰寫註解的邊界方塊。 |
| .fyre-stream-sort | 排序選項周圍的邊界框。 |

您也可以在應用程式設定中編輯樣式，包括編輯器欄位背景顏色，以及編輯器中顯示的文字字型顏色、大小和系列。

若要自訂註解編輯器，請將editorCss:{}物件新增至fyre.conv.load()，並包含您想要的樣式。 例如，若要使用您的自訂CSS更新編輯器：

```
fyre.conv.load(networkConfig, [{ 
   siteId: LF_siteId, 
   el: 'livefyre', 
   articleId: LF_articleId, 
   collectionMeta: #CollectionMeta 
   editorCss: { 
      background: '#ccc', 
      color: 'red', 
      font: '30px "Helvetica Neue", Helvetica, Arial, Geneva, sans-serif' 
   } 
}]);
```

## 排序選項CSS {#section_btq_4rh_xz}

| 類別 | 說明 |
|---|---|
| .fyre-stream-sort | 整個排序選項div。 |
| .fyre-stream-sort-newst | 「最新」選項。 |
| .fyre-stream-sort-mollest | 「最舊」選項。 |
| .fyre-stream-sort-bar | 選項之間的分隔欄。 |
| .fyre-stream-sort-selected | 當前選擇的排序選項。 |

HTML結構：

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

隱藏分隔排序選項的「|」。

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## 注釋CSS {#section_mlv_nrh_xz}

| 類別 | 說明 |
|---|---|
| .fyre-comment-author-tag- *`custom tag name`* | Livefyre會針對透過Livefyre的Studio [描述檔同步](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md)新增的每個使用者標籤，以此格式建立CSS類別。 此類別可用來為使用者帳戶張貼的任何內容（包括該標籤）設定背景樣式。 |
| .fyre-tag-content-icon- *`tag name`* | Livefyre會針對透過Livefyre [Studio](/help/implementation/c-app-customizations/c-adding-users-to-groups.md)新增的每個內容標籤，以此格式建立CSS類別。 此類別可用於設定您新增標籤之任何內容的樣式。 |
| .fyre-comment-user | 包含使用者描述檔圖片的邊界方框。 |
| .fyre-comment-username | 使用者名稱。 |
| .fyre協調者 | 協調者邊界方框。 |
| .fyre注釋 | 注釋文字／連結周圍的邊界方框。 |
| .fyre-comment-article | 整個注釋內容的邊界方框。 |
| .fyre-comment-date | 附加至「自發佈以來的時間」元素的標籤。 |
| .fyre-comment-media | 媒體內容周圍的邊界方框。 |
| .fyre-comment-actions | 可用動作周圍的邊界方框，可對注釋執行。 |
| .fyre-comment-like | 「贊」連結周圍的邊界方框。 |
| .fyre-comment-reply | 「回覆」連結周圍的邊界方框。 |

## 精選注釋CSS {#section_m2v_mrh_xz}

>[!NOTE]
>
>所有注釋CSS類別也可套用至「精選內容」。

| 類別 | 說明 |
|---|---|
| .fyre-featured-content-wrapper | 讀者的容器div。 |
| .fyre-featured-header | 前導標題列。 |
| .fyre-featured-header-icon | 標題的箭頭圖示。 |
| .fyre-featured-title | 標題文字。 |
| .fyre-featureed-body | 讀者中精選內容的容器div。 |
| .fyre-feature-quote | 開始每個內容項目的引號圖示。 |

## 封存的註解CSS {#section_bs5_lrh_xz}

>[!NOTE]
>
>所有內容CSS類別也可套用至封存的內容。

| 類別 | 說明 |
|---|---|
| .fyre-archive-stream-title | 「來自封存」文字。 |
| .fyre-archive-stream-title-icon | 「從封存」頁首的標誌。 |

## 注釋通告程式CSS {#section_dy4_krh_xz}

這些類允許您自定義Livefyre注釋通告程式。

| 類別 | 說明 |
|---|---|
| .fyre通知 | 清單項目的div（新內容和封存內容）。 |
| .fyre通告程式 | 通告程式內容的包裝函式。 |
| .fyre通告程式歸檔檔案 | 除了最近貼文以外，所有新內容的包裝函式。 |
| .fyre通告程式頭像 | 頭像的影像。 |
| .fyre-notifier-avatar-container | 使用者頭像的容器div。 允許您定義定位。 |
| .fyre-notifier-avatar-shading | 頭像div的陰影。 |
| .fyre通告程式橫幅 | 通告程式預覽內容的容器，顯示用戶頭像和最近發佈項目的內容片段。 |
| .fyre通告程式庫 | 通告程式資訊部分的容器，其中列出了新注釋的數量、通告程式標題和關閉按鈕。 |
| .fyre通告程式-base-close | 通告程式關閉按鈕(x)的容器div。 |
| .fyre通告程式-base-shadow | 通告程式基底的陰影。 |
| .fyre-notifier-caption | 為通告程式顯示的文本。 預設為「新留言」。 |
| .fyre通告程式-close | 關閉通告程式的按鈕。 |
| .fyre通告程式容器 | 通告程式的容器包括橫幅和基底。 |
| .fyre通告程式計數器 | 通告程式中列出的編號的容器。 |
| .fyre通告程式清單 | 最新內容的容器。 |
| .fyre通告程式消息 | 顯示內容的前~30個字元。 |
| .fyre通告程式——消息容器 | 標題訊息的容器div。 |
