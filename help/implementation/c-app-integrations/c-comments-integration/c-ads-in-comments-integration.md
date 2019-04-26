---
description: 在「注釋」串流中插入廣告。
seo-description: 在「注釋」串流中插入廣告。
seo-title: 注釋中的廣告
solution: Experience Manager
title: 注釋中的廣告
uuid: f8d6372f-4468-4884-a384-116180b4 c748
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 注釋中的廣告{#ads-in-comments}

在「注釋」串流中插入廣告。

## 注釋中的廣告 {#topic_CDD2ACF16AED4DE782725EE90089C04E}

在「注釋」串流中插入廣告。

「留言(Comments)」功能中的「Livefyre Ads」(Livefyre廣告)功能可讓您將廣告插入您的註解串流、定義廣告在串流中的播放頻率，以及建立同步和非同步廣告植入委派。

Livefyre提供您使用廣告管理解決方案供應商來插入廣告的容器。

若要插入廣告，請傳遞Livefyre兩個值：

* 廣告應插入注釋串流的頻率
* 提供適當廣告的函數。

>[!NOTE]
>
>只有當廣告位置位於檢視區時，才會顯示廣告。廣告只會在父留言後顯示(而非在螺紋中)，使用者將無法對這些廣告加上註解。此API不允許您指定廣告將放入的元素大小。

## 整合 {#concept_C99029E618EC49779E3117D2C303E4F1}

若要使用此功能，請在要放置廣告的頁面上建立div元素，然後從廣告提供者傳入HTML。

Livefyre提供兩種廣告位置類型：同步和非同步。這兩種類型的廣告僅會在使用者捲動頁面時載入，使廣告的位置在檢視中。同時也要求您傳回DOM元素(iFrame或div)。

若要取得廣告，則同步方法呼叫到本機存放庫，而非同步呼叫外部服務。

### 同步

若要建立同步位置，請在委派中包含廣告，然後傳回廣告元素本身。同步方法呼叫至本機存放庫，可讓您處理自己的廣告產生。

### 非同步

非同步方法需要在您呼叫廣告供應商之前，將元素插入DOM中。然後，您的提供者決定要傳送的廣告，然後傳回它。

若要實施非同步廣告，請建立會傳回廣告的委派，以及將執行廣告位置的回呼。委派中傳回的元素必須具有要定位的唯一ID。回呼會將廣告插入到唯一ID所提供的元素中。

>[!NOTE]
>
>根據您的廣告提供者，回呼的行為會有所不同。

載入頁面時，「留言中的廣告」會點擊委派、插入元素，然後呼叫回呼，以更新(先前定義)與廣告的元素。

## 參數 {#concept_D7E27B0C21EF405C8EB826083DBB53EC}

下列參數可用於此呼叫。

針對廣告物件：

* **延遲：****(選擇性)整數** -設定第一個廣告將顯示後的留言數。預設為10。
* **頻率：(選擇性)整數** -設定每個後續廣告在其後顯示的留言數。例如：輸入2，將廣告顯示為每個評注。預設為10。
* **委派：*****必要* 函數** -呼叫將廣告插入留言串流的函數。

委派物件支援同步和非同步廣告觸發。指定給委派函數的參數將包含：

* **標題：****字串** -系列的標題。
* **標記：****array** -與系列相關聯的標籤清單。
* **id：****字串** -系列的文章識別碼。
* **url：****字串** -系列的URL。
* **Target：****字串** -系列的網路ID。
* **SiteID：****int** -系列的網站ID。

這些項目透過我們範例中的Conconfig物件傳遞，並在 [「快速入門」](/help/implementation/c-app-integrations/c-comments-integration/c-comments-integration.md#section_656AAC97903F485084650269A6C7EBCE) 區段中詳細說明。

### 同步

委派會傳回包含下列項目的物件：

* **元素：*****必要* DOM元素** -包含要插入應用程式之廣告的元素。

**非同步**：委派會傳回包含下列項目的物件：委派會傳回包含兩個屬性的物件：元素和回呼：

* **元素：*****必要* DOM元素** -包含要插入應用程式之廣告的元素。
* **回呼：*****必要* 函數** -將處理廣告插入DOM元素的回呼。

對於該物件 `Conv` ，您可以傳入字串來標示廣告區段的標題：

* **字串：****(選用)** -用來自訂廣告的標題文字。預設為「贊助」。

## 同步範例 {#concept_E733E4431D9948638B8102ADE398735F}

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
<div id="livefyre-app-17"></div> 
<script> 
  
(function() { 
  var nextSlotId = 1; 
  function generateNextSlotName() { 
    var id = nextSlotId++; 
    return 'adslot' + id; 
  } 
  Livefyre.require(['fyre.conv#qa'], function(Conv) { 
    new Conv({ 
      network: 'qa-0.fyre.co', 
        env: 'qa', 
        strings: { 
          'sponsored': 'Sponsored by: Livefyre' 
        } 
      }, [{ 
        app: 'main', 
        siteId: '291206', 
        articleId: '17', 
        el: 'livefyre-app-17', 
        ad: { 
          delay: 5, 
          frequency: 10, 
          delegate: function(data) { 
            var elem = document.createElement('div'); 
            elem.id = generateNextSlotName(); 
            return { 
              element: elem 
            }; 
          } 
        } 
      }], function (widget) { 
        // Initialize or Auth 
      }); 
    }); 
}()); 
</script>
```

## 非同步範例 {#concept_16B798C7EB20423DAA53ACCC71540051}

```
<script src="//cdn.livefyre.com/Livefyre.js"></script> 
<div id="livefyre-app-17"></div> 
<script> 
  
(function() { 
  var nextSlotId = 1; 
  function generateNextSlotName() { 
    var id = nextSlotId++; 
    return 'adslot' + id; 
  } 
  function insertSlot(slotName) { 
    var adElem = document.createElement("img"); 
    var ad = "https://your-ad-here.com/great-ad-image.image"; 
    adElem.setAttribute("src", ad); 
    document.getElementById(slotName).appendChild(adElem); 
  } 
  Livefyre.require(['fyre.conv#qa'], function(Conv) { 
    new Conv({ 
      network: 'qa-0.fyre.co', 
        env: 'qa', 
        strings: { 
          'sponsored': 'Sponsored by: Livefyre' 
        } 
      }, [{ 
        app: 'main', 
        siteId: '291206', 
        articleId: '17', 
        el: 'livefyre-app-17', 
        ad: { 
          delay: 5, 
          frequency: 10, 
          delegate: function(data) { 
            var elem = document.createElement('div'); 
            elem.id = generateNextSlotName(); 
            return { 
              element: elem, 
              callback: function() { 
                insertSlot(elem.id); 
              } 
            }; 
          } 
        } 
      }], function (widget) { 
        // Initialize or Auth 
      }); 
    }); 
}()); 
</script>
```
