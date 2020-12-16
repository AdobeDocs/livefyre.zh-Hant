---
description: 變更地圖應用程式的大小、寬度和互動選項。
seo-description: 變更地圖應用程式的大小、寬度和互動選項。
seo-title: 功能卡自訂
solution: Experience Manager
title: 功能卡自訂
uuid: dd43c076-027f-42c8-be2e-7d863d4e3976
translation-type: tm+mt
source-git-commit: a014b5cd618672934843f1adf20d6b2cc504e2d8
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---


# 功能卡自訂{#feature-card-customizations}

變更地圖應用程式的大小、寬度和互動選項。

<!-- 
r_feature_card_customization.dita
 -->

功能卡應用程式僅包含標準自訂：** [!UICONTROL Theme]**、品牌色彩、字型系列和字型大小。

您可以使用下列功能自訂功能卡：

* **[!UICONTROL Style]** 和 **[!UICONTROL Config]** 中所有應用程式的選項 **[!UICONTROL App Designer]**。如需&#x200B;**[!UICONTROL App Designer]**&#x200B;中所有應用程式的標準&#x200B;**[!UICONTROL Style]**&#x200B;和&#x200B;**[!UICONTROL Config]**&#x200B;選項的詳細資訊，請參閱自訂應用程式。

* 整合工具。 如需如何使用整合工具自訂應用程式的詳細資訊，請參閱應用程式整合。
* **[!UICONTROL Call-to-action button]** 您可以搭配產品目錄使用「行動要求」按鈕，將使用者引導至產品或您的網站，以便採取進一步行動。

   * **[!UICONTROL Call-to-action button]** 切換為開啟，以顯示「動作要求」按鈕。
   * **[!UICONTROL Require rights to display products]** 切換為開啟，要求內容擁有者已授與內容的權限，然後內容才會出現「動作要求」按鈕。

      >[!NOTE]
      >
      >即使未授與內容的權限，內容仍會顯示，但「行動要求」按鈕不會與內容一起顯示，除非授與內容的權限。

   * **[!UICONTROL Call-to-action header text]** 要在內容模式中「行動要求」按鈕上方標題中顯示的字詞。預設的措辭為「購買這些產品：」。
   * **[!UICONTROL Call-to-action button text]** 自訂「行動要求」按鈕上的文字。預設文字為「立即購買」。
   * **[!UICONTROL Product display options]** 選擇是否要顯示 **[!UICONTROL Photo]** 和 **[!UICONTROL Product name]** 「操作調用」按鈕。
   * **[!UICONTROL Product URL referral tracking]** 切換為開啟，以追蹤從此應用程式到相關產品頁面的反向連結。
   * **[!UICONTROL Referral tracking key-value pairs]** 新增參數，以進一步指定從應用程式內容到相關產品頁面的反向連結追蹤。

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**。選取這個選項，可為多個產品頁面建立一個應用程式。 針對每個產品頁面，將產品特定的UGC篩選至應用程式。 您可以選取一或多個檔案夾，將特定系列與應用程式建立關聯。
   * **[!UICONTROL Select Product folders]**。選取要用來篩選UGC的頂層產品資料夾。 使用`CTRL/Command + click`選擇多個資料夾。 Livefyre使用資料夾來判斷該資料夾中哪些產品會顯示在不同頁面上的應用程式中。
   * **[!UICONTROL Show related content]**。切換此選項，以顯示已發佈至應用程式，但以不同產品ID標籤的內容。 在顯示應用程式的特定產品內容後，Livefyre會顯示其他產品的內容以及與產品無關的內容。 Livefyre會先將具有相同產品ID的內容排定優先順序，然後將內容發佈至具有其他產品ID的應用程式，接著將內容發佈至沒有產品ID的應用程式。

