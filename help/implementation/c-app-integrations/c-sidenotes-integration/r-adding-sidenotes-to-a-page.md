---
description: null
seo-description: null
seo-title: 將Sitdenes新增至頁面
solution: Experience Manager
title: 將Sitdenes新增至頁面
uuid: 6499c45a-3773-4adb-a6 c7-22a628309 afd
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# 將Sitdenes新增至頁面 {#adding-sidenotes-to-a-page}

Livefyre提供數個設定選項，以便在您的頁面上放置「附屬程式」：

* 選擇器選項定義了SiteNotes應該出現的元素。
* 錨點代表可加以標示的元素。
* 自訂的執行緒容器可讓您定義Sitdandes執行緒與附屬內容相關的位置。
* 「Sitents」計數選項可讓您顯示在指定位置新增的SitedNotes數目。
* 使用多 `ConvConfig` 個物件將SiteNets新增至單一頁面上的數個內文。

## 選擇器 {#section_wyj_4sv_sy}

選擇器選項可讓SiteNotes在頁面上尋找內容。此選項的值可讓您動態決定將使用的元素。它可以是選擇器字串(例如「# content p」、「# content img」)、一個jQuery物件(例如 `$(‘#content’)`)、DOM元素的陣列，或是具有兩個屬性的物件：包含和排除。然後，Sitents應用程式會使用指定的元素或頁面上的相符元素。如果使用了包含和排除屬性，SitedNotes會先剖析頁面以尋找包含屬性上的所有元素，然後移除排除屬性上的任何元素。

## 錨點 {#section_ehq_psv_sy}

錨點代表可呈現內容的元素。錨點元素可以包含文字或影像。在應用程式建構期間傳遞的選擇器選項將決定錨點元素。

## 錨點ID {#section_rsb_rsv_sy}

頁面上的錨點會使用 `data-lf-anchor-id`a.

若要自行設定錨點的ID，請將屬性 `data-lf-custom-anchor-id` 新增至您要對應至錨點的元素。當自動偵測錨點的自動偵測失敗時，這會很有用。

例如，如果您打算針對影像的桌面和行動版本使用不同的URL，可能會將兩個不同的URL對應至不同的錨點。如果您的HTML在行動和 `data-lf-custom-anchor-id` 桌上型電腦上提供相同的內容，則影像元素將會視為單一錨點。

錨點的類型是動態決定的，但也可以使用 `data-lf-custom-anchor-type` 屬性明確設定。

>[!NOTE]
>
>必須使用列舉數字值。

可用類型為：

* **文字：** 1
* **影像：** 2
* **媒體：** 3
* **多樣化：** 4

請參閱 [UpdateCHarchs方法](/help/implementation/c-app-integrations/c-sidenotes-integration/update-anchors-method.md) ，瞭解如何使用 `updateAnchors` 方法來動態新增Sitenote內容至頁面。

## 自訂執行緒容器 {#section_jdh_btv_sy}

使用 `threadContainerEl` 選項來指定Sitdones執行緒的位置，而非預設位置。依預設，當啓動錨點時，SitedNets會出現在相關內容的旁邊或下方。若要變更此預設值，請 `threadContainerEl` 使用要指定執行緒出現的元素。

此選項的值與選擇器選項相同，只有第一個有效元素才會使用。

## Sitents計數 {#section_pld_ntv_sy}

使用 `numSidenotesEl` 選項內嵌選用的Sites，將介面工具集計算在您的頁面上。此選項接受與選擇器選項相同的輸入，但只會使用輸入陣列中的第一個有效元素。

介面工具集會裝飾所提供或相符的元素，並包含Sitdones輸入圖示、在此位置輸入的SitedNotes數目，以及說明圖示。

按一下介面工具集將會顯示一個快顯視窗，其中說明SiteNotes的簡短說明以及如何使用。

說明和範例文字都可使用自訂字串( `questionExplanation` 以及 `questionMockText`分別)設定。計算介面工具集和快顯視窗的外觀也可以使用自訂樣式( `numSidenotes` 以及 `numSidenotesPopover`分別)設定。

## 新增多個Sites將系列設定為單一頁面 {#section_pjl_ptv_sy}

Livefyre可讓您新增多個Sites至單一頁面。例如，如果頁面包含三個新聞故事，您可能希望包含三個不同的Sitents應用程式重復順序。若要這麼做，您必須為想要建立的每個Sitents實例定義個別 `ConvConfig` 物件。例如：

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
