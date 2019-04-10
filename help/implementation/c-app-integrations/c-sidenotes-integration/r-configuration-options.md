---
description: Sitents config物件是JSON物件，用來指定Livefyre App在頁面上呈現的內容。
seo-description: Sitents config物件是JSON物件，用來指定Livefyre App在頁面上呈現的內容。
seo-title: Sites設定設定選項
solution: Experience Manager
title: Sites設定設定選項
uuid: 067e51e6-9720-4226-a805-c7 a07 c8 cda0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Sites設定設定選項{#sidenotes-configuration-options}

Sitents config物件是JSON物件，用來指定Livefyre App在頁面上呈現的內容。

物件包含下列參數：

| 參數 | Type | 說明 |
|--- |--- |--- |
| AuthDelegate | *必要* 物件 | 新樣式或舊樣式初始化驗證委派。 |
| CollectionMeta | *必要* 物件 | 如需詳細資訊，請參閱CollectionMeta Token。 |
| Customicon | *選用* 字串 | 設定自訂啓動程式圖示的URL。預設為Livefyre泡泡。 |
| customStyles | *選擇性* 物件 | 新增自訂樣式以變更SiteNotes的外觀和感覺。如需詳細資訊，請參閱自訂樣式。 |
| SocialStream | *Optional* Boolean | 若為true，請停用此Sitents例項中的即時串流(非其他備注串流)。預設為false。 |
| environment | *選用* 字串 | 指定Livefyre UAT環境。唯一可能的值 `t402.livefyre.com`是。對於生產，必須移除此參數。 |
| IconVisibility | *選擇性* 物件或字串 | 定義當滑鼠停留或靜態時，Sitenets圖示是否會顯示。如果這是字串，則此字串將用於區塊圖示的兩個版本(空白且有SitenNuts)。如果物件是物件，您必須指定每個類型：{empty：'hover'，num：'static'}。預設為靜態。 |
| inlineThreads | *選擇性* 布林值 | 如果是true，則Sitenote螺紋會在關聯的區塊後面直接插入。預設為false。 |
| numsideNoteSale | *選擇性* 物件、字串或陣列 | 指定Sitents計數Widget將會裝飾的元素。(此介面工具集顯示頁面上的sidents數和關於SitedNotes的資訊。)如果字串選擇器符合多個元素，則會選擇第一個元素。(使用CSS DOM選擇器規格)。 |
| position | *選用* 字串 | 在已啓用「已啓用Sitents」的元素時，決定彈出式視窗的位置。可能的值為「smart」、「left」、「right」、「bottom」。預設值為'Smart'，會將彈出式視窗對齊頁面右側，除非空間不足(在這種情況下，它會移到內容下方)。 |
| 選擇器 | *必要* 物件、字串或陣列 | 指定啓動程式圖示應該出現的元素。(使用CSS DOM選擇器規格)。如果物件包含「includes」區段和「excludes」區段，則會將CSS選取器套用至任何相符項目，並移除符合排除的任何元素。若字串為字串，則會在頁面上包含任何相符元素。若為陣列，請列出要包含的元素。 |
| 字串 | *選擇性* 物件 | 新增自訂文字字串，變更應用程式中的任何語言或文字。如需詳細資訊，請參閱自訂字串。 |
| EnterpriseContail | *選擇性* 物件、字串或陣列 | 指定將出現的元素執行緒的元素。此參數可讓您重新定位執行緒。如果字串選擇器符合多個元素，則會選擇第一個元素。(使用CSS DOM選擇器規格)。 |

