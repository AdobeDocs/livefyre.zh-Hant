---
description: 在客戶歷程的特定點提供特定產品的UGC，以利用UGC商務功能提高購買意願和轉化率。
seo-description: 在客戶歷程的特定點提供特定產品的UGC，以利用UGC商務功能提高購買意願和轉化率。
seo-title: UGC商務
solution: Experience Manager
title: UGC商務
uuid: 71e64901-a2b6-4957-ba88-058e4eaca537
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# UGC商務{#ugc-commerce}

在客戶歷程的特定點提供特定產品的UGC，以利用UGC商務功能提高購買意願和轉化率。

使用「UGC商務」功能可影響UGC和產品詳細資訊頁面上的購買意圖和轉換。 將UGC與產品庫存緊密關聯，以縮短上市時間。 使用UGC建立社群，強調真實的客戶故事，以建立品牌忠誠度。

AEM Livefyre提供數種匯入產品目錄資訊的方式，包括SKU、縮圖影像、價格和產品名稱。 使用AEM Livefyre的權限要求、自動串流規則標籤及協調工作流程，輕鬆管理產品與UGC的關聯。

除了影響購買，AEM Livefyre的UGC商務產品功能還可運用在其他方式推動轉換，包括：

* B2B潛在客戶開發：在UGC下放置行動要求按鈕以擷取銷售機會
* B2C應用程式下載：提示使用者下載應用程式
* 文章引薦：將使用者連結至與UGC相關的文章

將產品呼叫動作與UGC一起放置，以推動轉換。 您可以:

* 將產品專用的UGC大規模新增至數千個產品詳細資訊頁面。
* 將AEM Livefyre的視覺化應用程式內嵌在產品詳細資料頁面上，以支援UGC商務功能，例如Media Wall和Mosaic。
* 將可設定的反向連結追蹤代碼與分析解決方案搭配使用，以測量來自置於UGC和UGC之產品CTA（置於產品詳細資料頁面）的轉換。

AEM Commerce使用者可將現有的產品目錄完美整合至Livefyre，以推動使用者參與Livefyre的視覺化應用程式。 不使用AEM Commerce的Livefyre使用者可以手動將其產品目錄匯入Livefyre。 如需詳 [細資訊，請參閱「使用檔案上傳將產品上傳至Livefyre](/help/using/c-features-livefyre/c-ugc-commerce.md)」。

使用此功能的應用程式：

* [功能卡](../c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)。 如需如何在功能卡中使用UGC商務的詳細資訊，請參閱功能 [卡自訂](../c-about-apps/c-feature-card-app/c-feature-card-app.md#section_uds_gzm_5y)。

* [](../c-about-apps/c-filmstrip-app/c-filmstrip-app.md#concept_jpc_n2j_jbb). 如需如何在Filmstrip中使用UGC商務的詳細資訊，請參閱 [Filmstrip自訂](../c-about-apps/c-filmstrip-app/c-filmstrip-customizations.md#c_filmstrip_customizations)。

* [媒體牆](../c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)。 如需如何在媒體塗鴉牆中使用UGC商務的詳細資訊，請參閱媒體塗鴉牆 [自訂項目](../c-about-apps/c-media-wall-app/r-media-wall-customizations.md#r_media_wall_customizations)。

* [馬賽克](../c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)。 如需如何在Mosaic中使用UGC商務的詳細資訊，請參閱 [Mosaic自訂](../c-about-apps/c-mosaic-app/c-mosaic-customizations.md#c_mosaic_customizations)。

## 概觀：如何使用「UGC商務行動要求」按鈕 {#section_s2d_tln_n1b}

1. 使用「動作要求」按鈕建立應用程式。 請 [參閱新增動作要求按鈕至應用程式](/help/using/c-features-livefyre/c-call-to-action-button.md#task_36190DD1C8204C7793CB7EEA379C2155)。
1. 將您的產品目錄新增至Livefyre。 您可以透過下列兩種方式之一匯入內容：

   * [如果您使用AEM Commerce](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/livefyre.html) ，請將產品匯入Livefyre。
   * [如果您不使用AEM Commerce](/help/using/c-features-livefyre/c-ugc-commerce.md) ，請將產品上傳至Livefyre。

1. 將產品與內容建立關聯。 您可以透過下列四種方式之一：

   * 從資料庫。 請參 [閱使用程式庫將產品與內容建立關聯](../c-library/t-associate-products-with-content-using-the-library.md#t_associate_products_with_content_using_the_library)
   * 來自ModQ。 請參 [閱使用ModQ協調內容](/help/using/c-features-livefyre/c-about-moderation/c-modq.md)
   * 來自應用程式內容。 請 [參閱新增動作要求按鈕至應用程式](/help/using/c-features-livefyre/c-call-to-action-button.md)
   * 來自串流。 請參 [閱所有串流規則的串流規則選項](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。

## 使用檔案上傳將產品上傳至Livefyre {#section_n1s_4hz_m1b}

上傳產品以搭配您的「動作要求按鈕」使用，以新增產品以與內容建立關聯，或編輯和刪除現有檔案。

>[!NOTE]
>
>將包含現有檔案的檔案上傳至檔案夾將會刪除該檔案夾中的所有檔案，並以新檔案覆寫檔案。

1. 導覽至 **[!UICONTROL Network Settings > Products.]**
1. 建立 **[!UICONTROL Product Folder]** 或使用現有 **[!UICONTROL Product Folder]**。

1. 按一下以 **[!UICONTROL Product Folder]** 選擇它。
1. Click the **[!UICONTROL Upload Products]** button.
1. 以下列其中一種格式上傳產品檔案：

   * Google產品檔案格式
   * Livefyre格式（請參閱下方）
   以標準格式上傳JSON檔案。 您可以下載範本，以檢視標準格式的範例。 以下是範本中一個產品系列的範例。 它遵循順序 `{"key": "value", "key": "value"}, {"key": "value", "key": "value"}`:

   ```
   {"id": "1", "title": "Flex RN 2017", "isFolder": false, "description": "Flex RN 2017", "price": "$85", "sku": "sku11111", "summary": "This brand is a member of the Sustainable Apparel Coalition", "features": "Cushioning: Lightweight, flexible response", "url": "www.shopping.com/shoes-flex-rn-2017/product/9", "attributes": [{"type": "color", "value": "blue"}
   ```

   下表說明您上傳產品所需的金鑰和值配對：

## 產品目錄上傳標準格式的鍵／值對

| 機碼 | 類型 | 說明 |
|--- |--- |--- |
| id | 字串 | 產品的唯一ID。 |
| oembed | 物件 | Image attachment `0embed $ref: '../partials/schemas.yaml#/oEmbed'` |
| title | 字串 | 產品標題。 |
| isFolder | 布林值 | 如果為true，則產品會被視為資料夾（例如mens、womens等）。 |
| parentId | 字串 | 定義產品所在的資料夾。 |
| 描述 | 字串 | 產品說明。 |
| 價格 | 字串 | 產品價值（美元）。 例如，'23.36'。 |
| sku | 字串 | 產品的庫存單位(SKU)。 |
| url | 字串 | 連結至產品頁面。 |
| 已啟用 | 布林值 | 值為True表示產品處於活動狀態。 |
| 屬性 | 陣列 | 定義產品的類型和值（例如顏色、大小等）。 這是一組對象。</br>**** 屬性：類 </br>型 </br>類型：字</br>串說明：顏色，大小 </br>值 </br>類型：字串 </br>說明：綠色、XS |
| 標籤 | 陣列 | 定義內容類別（例如汽車、鞋等）的標籤。 這是一組字串。 |

## ModQ {#section_os1_v4t_n1b}

您可以在ModQ中將產品目錄中的內容與產品建立關聯，以符合您現有的協調工作流程。 如需如何搭配ModQ使用UGC商務的詳細資訊，請參 [閱使用ModQ協調內容](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md)。

## 串流 {#section_qtj_v4t_n1b}

您可以使用串流規則自動將產品與內容建立關聯，然後自動將內容發佈至應用程式、將內容儲存在「資料庫」中，或使用ModQ進行協調。 如需如何搭配串流規則使用UGC商務的詳細資訊，請參 [閱所有串流規則的串流規則選項](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
