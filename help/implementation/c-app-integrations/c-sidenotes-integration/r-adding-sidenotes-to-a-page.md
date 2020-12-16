---
description: 'null'
seo-description: 'null'
seo-title: 將字元號新增至頁面
solution: Experience Manager
title: 將字元號新增至頁面
uuid: 6499c45a-3773-4adb-a6c7-22a628309afd
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---


# 向頁面{#adding-sidenotes-to-a-page}添加字元號

Livefyre提供數個設定選項，可讓您將Siestrom定位在您的頁面上：

* 選擇器選項定義了Siresform應顯示的元素。
* 錨點表示可表示的元素。
* 自定義線程容器允許您定義表示線程相對於所表示內容的位置。
* 「表示計數」選項允許您顯示在給定位置添加的表示數。
* 使用多個`ConvConfig`物件，將Siestrom新增至單一頁面上的數個內文。

## 選擇器{#section_wyj_4sv_sy}

選擇器選項可讓Sidesors在頁面上尋找內容。 此選項的值可讓您動態決定要使用的元素。 它可以是選擇器字串（例如「#content p, #content img」）、jQuery物件（例如`$(‘#content’)`）、DOM元素的陣列，或具有兩個屬性的物件：包含和排除。 然後，「Sides App」（表示應用程式）會使用頁面上的指定元素或相符元素。 如果使用包含和排除屬性，Sidestrops會先剖析頁面以尋找包含屬性上的所有元素，然後移除排除屬性上找到的所有元素。

## 錨點{#section_ehq_psv_sy}

錨點代表其內容可表示的元素。 錨點元素可以包含文字或影像。 應用程式建構期間傳遞的選擇器選項將決定錨點元素。

## 錨點ID {#section_rsb_rsv_sy}

頁面上的錨點是使用`data-lf-anchor-id`來識別。

若要自行設定錨點的ID，請將屬性`data-lf-custom-anchor-id`新增至要對應至錨點的元素。 在自動偵測錨點失敗的情況下，這很有幫助。

例如，如果您打算針對影像的桌上型電腦和行動版本使用不同的URL，兩個不同的URL可能會對應至不同的定位點。 如果您的HTML在行動裝置和桌上型電腦上都提供相同的`data-lf-custom-anchor-id`，則影像元素會被視為單一錨點。

錨點具有動態確定的類型，但也可使用`data-lf-custom-anchor-type`屬性顯式設定。

>[!NOTE]
>
>必須使用枚舉編號值。

可用類型包括：

* **文字：** 1
* **影像：** 2
* **媒體：** 3
* **豐富：** 4

如需如何使用`updateAnchors`方法將Sidexhere內容動態新增至頁面的詳細資訊，請參閱[updateAnchors方法](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md)。

## 自訂執行緒容器{#section_jdh_btv_sy}

使用`threadContainerEl`選項指定Sidestraws線程的位置（預設位置除外）。 依預設，當錨點啟動時，Sidesars會出現在相關內容旁或下方。 要更改此預設值，請使用`threadContainerEl`指定線程應出現的元素。

此選項的此值與選擇器選項的作用相同，只會使用第一個有效元素。

## Siestroms Count {#section_pld_ntv_sy}

使用`numSidenotesEl`選項，在您的頁面上內嵌選用的Sidestroms計數介面工具集。 此選項接受與選擇器選項相同的輸入，但僅使用輸入陣列中的第一個有效元素。

介面工具集將裝飾提供或符合的元素，並包含「字型大小」輸入圖示、在此位置輸入的字型大小數，以及說明圖示。

按一下介面工具集會顯示快顯視窗，其中簡短說明為「Sides」，以及如何使用它們。

說明和範例文字都可使用自訂字串（分別為`questionExplanation`和`questionMockText`）來設定。 計數介面工具集和快顯視窗的外觀也可使用自訂樣式（分別為`numSidenotes`和`numSidenotesPopover`）來設定。

## 新增多個網站表示系列至單頁{#section_pjl_ptv_sy}

Livefyre可讓您將多個Sidestrops系列新增至單一頁面。 例如，如果頁面包含三則新聞報導，您可能希望包含三個不同的Sidesars應用程式小版本。 要執行此操作，您必須為每個Sidesform實例定義一個單獨的`ConvConfig`對象，以表示您希望構建。 例如：

```
<html> 
   <head> 
      <script src="//cdn.livefyre.com/Livefyre.js"></script> 
   </head> 
<body> 
   <h2>Story #1</h2> 
   <div id="story1"> 
      <p class="sidenotes">stuff #1</p> 
      <p class="sidenotes">more stuff #1</p> 
   </div> 
   <hr /> 
   <h2>Story #2</h2> 
   <div id="story2"> 
      <p class="sidenotes">stuff #2</p> 
      <p class="sidenotes">more stuff #2</p> 
      <p class="sidenotes">more and more stuff</p> 
   </div> 
   <hr /> 
   <script type="text/javascript"> 
      var convConfig_story1 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Article ID>', 
         selectors: '#story1 > p.sidenotes', 
         collectionMeta: '<First collectionMeta>' 
      }; 
  
      var convConfig_story2 = { 
         network: '<Your Network>', 
         siteId: '<Site ID>', 
         articleId: '<Your Second Article ID>', 
         selectors: '#story2 > p.sidenotes', 
         collectionMeta: '<Second collectionMeta>' 
      }; 
  
      Livefyre.require(['sidenotes#1', 'auth'], function(Sidenotes, auth) { 
         new Sidenotes(convConfig_story1); 
         new Sidenotes(convConfig_story2); 
         auth.delegate({ 
            login: function (callback) { 
               callback(null,{livefyre: '<Login Token>'}); 
            } 
         }); 
      }); 
   </script> 
</body> 
</html>
```
