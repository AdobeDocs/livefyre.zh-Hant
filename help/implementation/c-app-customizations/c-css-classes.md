---
description: 使用可用的CSS類別來自訂您的應用程式。
seo-description: 使用可用的CSS類別來自訂您的應用程式。
seo-title: CSS類別
solution: Experience Manager
title: CSS類別
uuid: 8714e7e5-3858-458f-a464-de87 fd2 f0 ff0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# CSS類別{#css-classes}

使用可用的CSS類別來自訂您的應用程式。

適用於聊天、留言、即時部落格、評論和SiteNotes。

使用CSS自訂您的Livefyre應用程式，以便更完整地與您的頁面整合，只要使用您自己的樣式表覆寫預設的應用程式CSS即可。本節說明可用的CSS自訂。

* [編輯器CSS](#c_css_classes/section_edx_prh_xz)
* [排序選項CSS](#c_css_classes/section_btq_4rh_xz)
* [注釋CSS](#c_css_classes/section_mlv_nrh_xz)
* [精選評論CSS](#c_css_classes/section_m2v_mrh_xz)
* [封存注釋CSS](#c_css_classes/section_bs5_lrh_xz)
* [注釋通知CSS](#c_css_classes/section_dy4_krh_xz)
* [Storify CSS類別](../c-app-customizations/c-storify-css-classes.md#c_storify_css_classes)

## 編輯器CSS {#section_edx_prh_xz}

使用這些類別可變更貼文編輯器介面。

| 類別 | 說明 |
|---|---|
| . fyre-comment-count | 顯示留言數的文字。 |
| . fyre-login-bar | 包含登入列和選項的邊界方框。 |
| . fyre-live-container | 邊界方框周圍的接聽人數及其avatar。 |
| . fyre-editor | 圍繞. fyre-login-bar、. fyre-live-container和使用者編寫注釋的文字區域四周的邊界方塊。 |
| . fyre-stream-sort | 排序選項四周的邊界方塊。 |

您也可以編輯應用程式設定本身的樣式，包括編輯器欄位背景顏色，以及編輯器中出現的字型顏色、大小和系列文字。

若要自訂註解編輯器，請新增EditorCSS：{}物件to fyre. config. load()並包含您所要的樣式。例如，若要使用自訂CSS更新編輯器：

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
| . fyre-stream-sort | 整個排序選項div。 |
| . fyre-stream-sort-newest | 「Newest」選項。 |
| . fyre-stream-sortly-latest | 「最舊」選項。 |
| . fyre-stream-sorting-bar | 選項之間的分隔符號列。 |
| . fyre-stream-sort-selected | 目前選取的排序選項。 |

HTML結構：

```
<div class="fyre-stream-sort"> 
   <a href="#" class="fyre-stream-sort-newest fyre-stream-sort-selected">Newest</a>  
   <span class="fyre-stream-sort-bar"> | </span> 
   <a href="#" class="fyre-stream-sort-oldest">Oldest</a> 
</div>
```

隱藏「|'分隔排序選項'。

```
.fyre-stream-sort .fyre-stream-sort-bar { 
    display: none !important; 
}
```

## 注釋CSS {#section_mlv_nrh_xz}

| 類別 | 說明 |
|---|---|
| . fyre-comment-author-tag- *`custom tag name`* | Livefyre將針對透過Livefyre Studio、 [Profile Sync新增的每個使用者標籤，以此格式建立CSS類別](/help/implementation/t-about-identity-integration/t-sync-with-livefyre-using-ping-for-pull/t-sync-with-livefyre-using-ping-for-pull.md)。此類別可用來針對使用者帳戶所張貼的任何內容設定背景，包括該標記。 |
| . fyre-tag-content-icon- *`tag name`* | Livefyre將針對透過Livefyre [Studio新增的每個內容標籤，以此格式建立CSS類別](/help/implementation/c-app-customizations/c-adding-users-to-groups.md)。此類別可用來設定您已新增標記的任何內容。 |
| . fyre-comment-user | 包含使用者個人資料的邊界方框。 |
| . fyre-comment-username | 使用者名稱。 |
| . fyre協調者 | 協調者邊界方框。 |
| . fyre-comment | 環繞文字/連結周圍的邊界方塊。 |
| . fyre-comment-article | 整個注釋內容的邊界方框。 |
| . fyre-comment-date | 附加至「之後時間」元素的標籤。 |
| . fyre-comment-media | 媒體內容周圍的邊界方框。 |
| . fyre-comment-actions | 圍繞可用動作的邊界方塊進行註解。 |
| . fyre-comment-like | 圍繞「贊」連結的邊界方框。 |
| . fyre-comment-reprection | 圍繞「回覆」連結的邊界方框。 |

## 精選評論CSS {#section_m2v_mrh_xz}

>[!NOTE]
>
>所有評論CSS類別也可能套用至「精選內容」。

| 類別 | 說明 |
|---|---|
| . fyre-professional-content-blogper | 讀者的容器div。 |
| . fyre-profeatures-header | 領先標題列。 |
| . fyre-profeatures-header-icon | 標題的問題圖示。 |
| . fyre-profetional-title | 標題文字。 |
| . fyre-professional-body | 讀者中精選內容的容器div。 |
| . fyre-profeatures-quote | 開始每個內容項目的引號圖示。 |

## 封存注釋CSS {#section_bs5_lrh_xz}

>[!NOTE]
>
>所有內容CSS類別也可以套用至已封存的內容。

| 類別 | 說明 |
|---|---|
| . fyre-archive-stream-title | 「From the Archive」文字。 |
| . fyre-archive-stream-title-icon | 「From the Archive」標題的標誌。 |

## 注釋通知CSS {#section_dy4_krh_xz}

這些類別可讓您自訂Livefyre注釋通知。

| 類別 | 說明 |
|---|---|
| . fyre-notification | 清單項目的div(新增和封存內容)。 |
| . fyre-notter | 「通知」內容的包裝函式。 |
| . fyre-nottifier-archive | 所有新內容以外的所有新內容的發行者。 |
| . fyre-natifier-avatar | 頭像的影像。 |
| . fyre-natifier-avatar-container | 使用者頭像的容器div。可讓您定義定位。 |
| . fyre-natifier-avatar-shading | 頭像div div的陰影。 |
| . fyre-natifier-anner | 通知內容的容器，它會顯示使用者頭像，並顯示最近張貼之項目的內容片段。 |
| . fyre-nottifier-base | 「通知」的資訊容器容器，其中列出新留言數、「通知」標題和關閉按鈕。 |
| . fyre-notifier-base-close | 「通知」的關閉按鈕(x)的容器div。 |
| . fyre-natifier-base-shadow | 「通知」基底的陰影。 |
| . fyre-nottifier-caption | 通知的文字。預設為「新留言」。 |
| . fyre-natifier-close | 關閉通知的按鈕。 |
| . fyre-nottifier-container | 「通知」的容器，包含橫幅和基底。 |
| . fyre-nottifier-cf | 「通知」中所列數字的容器。 |
| . fyre-nottifier-list | 最新內容片段的容器。 |
| . fyre-natifier-message | 顯示內容的前~30個字元。 |
| . fyre-natifier-message-container | 標題訊息的容器div。 |
