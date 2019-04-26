---
description: 變更地圖應用程式的大小、寬度和互動選項。
seo-description: 變更地圖應用程式的大小、寬度和互動選項。
seo-title: 功能卡片自訂
solution: Experience Manager
title: 功能卡片自訂
uuid: dd43c076-027f-42c8-be2 e-7d863 d4 e3976
translation-type: tm+mt
source-git-commit: a014b5cd618672934843f1adf20d6b2cc504e2d8

---


# 功能卡片自訂{#feature-card-customizations}

變更地圖應用程式的大小、寬度和互動選項。

<!-- 
r_feature_card_customization.dita
 -->

「功能卡片應用程式」僅包含標準自訂：** [!UICONTROL Theme]**、品牌色彩、字體系列和字體大小。

您可以使用下列項目來自訂功能卡：

* **[!UICONTROL Style]** 以及所有應用程式中的 **[!UICONTROL Config]** 選項 **[!UICONTROL App Designer]**。如需所有應用程式中所有應用程式之標準 **[!UICONTROL Style]** 和 **[!UICONTROL Config]** 選項的詳細資訊，請參閱自訂應用程式 **[!UICONTROL App Designer]**。

* 整合工具。如需如何使用整合工具自訂應用程式的詳細資訊，請參閱應用程式整合。
* **[!UICONTROL Call-to-action button]** 您可以使用產品目錄的「呼叫動作」按鈕，將使用者導向產品或網站，以進行進一步的動作。

   * **[!UICONTROL Call-to-action button]** 切換切換至開啓以顯示「呼叫動作」按鈕。
   * **[!UICONTROL Require rights to display products]** 將切換切換為要求內容擁有者已授與內容權限，然後內容的「呼叫動作」按鈕會顯示內容。

      >[!NOTE]
      >
      >即使內容未授與權限，內容仍會顯示，但除非授予內容的權限，否則「呼叫動作」按鈕不會與內容一起顯示。

   * **[!UICONTROL Call-to-action header text]** 要顯示在內容模型中「呼叫收貨人」按鈕上方標題上方的字詞。預設字詞為「Shop these products：「.
   * **[!UICONTROL Call-to-action button text]** 自訂「呼叫動作」按鈕上的文字。預設文字為「立即購買」。
   * **[!UICONTROL Product display options]** 選擇是否要顯示和 **[!UICONTROL Photo]****[!UICONTROL Product name]** 使用「呼叫動作」按鈕。
   * **[!UICONTROL Product URL referral tracking]** 切換切換至開啓，以追蹤從此應用程式到相關聯產品頁面的反向連結。
   * **[!UICONTROL Referral tracking key-value pairs]** 新增參數，進一步指定從您的應用程式內容到相關聯產品頁面的反向連結追蹤。

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. 選取這個選項，可針對多個產品頁面建立一個應用程式。針對每個產品頁面篩選產品特定UGC至應用程式。您可以選取一或多個資料夾，將特定系列關聯至應用程式。
   * **[!UICONTROL Select Product folders]**. 選取要用來篩選UGC的頂層產品資料夾。使用 `CTRL/Command + click` 一個以上資料夾。Livefyre會使用資料夾來判斷該資料夾中的哪些產品要顯示在不同頁面上的應用程式中。
   * **[!UICONTROL Show related content]**. 切換此選項可顯示發佈至應用程式的內容，但以不同的產品ID標記。在「應用程式」的產品特定內容顯示後，Livefyre會顯示其他產品與非產品相關內容的內容。Livefyre會先使用相同的產品ID優先排列內容，然後使用其他產品ID將內容發佈至應用程式，然後將內容發佈至不含產品ID的應用程式。

