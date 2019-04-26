---
description: null
seo-description: null
seo-title: 幻燈片自訂
solution: Experience Manager
title: 幻燈片自訂
uuid: 99f8b697-4aa3-4813-bcac-d0 e0 bdee252 d
translation-type: tm+mt
source-git-commit: bd989c97ae5cf06a5ac3deec215f865b0fe95d16

---


# 幻燈片自訂{#filmstrip-customizations}

所有應用程式使用 **[!UICONTROL Style]** 和 **[!UICONTROL Config]** 選項 **[!UICONTROL App Designer]**。如需所有應用程式中所有應用程式標準 **[!UICONTROL Style]** 和 **[!UICONTROL Config]** 選項的詳細資訊，請參閱自訂應用程式。 **[!UICONTROL App Designer.]**

您可以使用App Designer中的下列其他選項來自訂檔案投影片：

* **[!UICONTROL Content fit]**. 選擇 **[!UICONTROL crop]** 裁切內容以填滿卡片，或 **[!UICONTROL Aspect Ratio]** 在卡片中顯示整個影像，不論是否填滿整個卡片。
* **[!UICONTROL Tile Size]**. 以像素為單位輸入圖格大小。
* **[!UICONTROL Show Notifications]**. 選擇是否要在新內容串流至幻燈片應用程式時顯示通知。
* **[!UICONTROL Require rights]**. 啓用此選項，只顯示權限請求狀態為「已授予」的內容。
* **[!UICONTROL Hide social branding when rights granted]** 切換此選項，以移除原始社交媒體網路(Twitter或Instagram)上的標誌，以供內容片段授予權限。
* **[!UICONTROL Call-to-action button]** 您可以使用產品目錄的呼叫動作按鈕，將使用者導向產品或網站，以進行進一步的動作。

   * **[!UICONTROL Call-to-action button]** 切換切換至開啓以顯示行動收視按鈕。
   * **[!UICONTROL Require rights to display products]** 將切換切換為要求內容擁有者已授予內容權限，在內容針對內容顯示呼叫動作按鈕之前。

      >[!NOTE]
      >
      >即使內容未授與權限，內容仍會顯示，但除非授予內容的權限，否則呼叫動作按鈕將不會與內容一起顯示。

   * **[!UICONTROL Show call-to-action in tile]**. 選擇是否在「幻燈片」方塊上顯示呼叫動作按鈕，而不是只在網站訪客點按卡片並開啓較大視窗中的內容時，才顯示呼叫動作按鈕。
   * **[!UICONTROL Call-to-action indication text]** 要顯示的文字，提示使用者按下卡片以開啓呼叫動作模式。
   * **[!UICONTROL Call-to-action header text]** 要顯示在內容模型中呼叫動作按鈕上方標題上方的字詞。預設文字為「Shop these products：「.
   * **[!UICONTROL Call-to-action button text]** 要顯示在內容模型中呼叫動作按鈕中的字詞。預設文字為「立即購買：「.
   * **[!UICONTROL Product display options]** 選擇是否要顯示和 **[!UICONTROL Photo]****[!UICONTROL Product name]** 使用呼叫動作按鈕。

      >[!NOTE]
      >
      >像片和產品名稱按鈕在啓用時都會反白顯示。

   * **[!UICONTROL Product URL referral tracking]** 切換切換至開啓，以追蹤從此應用程式到相關聯產品頁面的反向連結。
   * **[!UICONTROL Referral tracking key-value pairs]** 新增參數，進一步指定從您的應用程式內容到相關聯產品頁面的反向連結追蹤。

* **[!UICONTROL Embed App in multiple pages]**.

   * **[!UICONTROL Filter UGC by Product ID]**. 選取這個選項，可針對多個產品頁面建立一個應用程式。針對每個產品頁面篩選產品特定UGC至應用程式。您可以選取一或多個資料夾，將特定系列關聯至應用程式。
   * **[!UICONTROL Select product folders]**. 選取要用來篩選UGC的頂層產品資料夾。使用CTRL/Command+按一下可選取多個資料夾。Livefyre會使用資料夾來判斷該資料夾中的哪些產品要顯示在不同頁面上的應用程式中。
   * **[!UICONTROL Show related content]**. 切換此選項可顯示發佈至應用程式的內容，但以不同的產品ID標記。在「應用程式」的產品特定內容顯示後，Livefyre會顯示其他產品與非產品相關內容的內容。Livefyre會先使用相同的產品ID優先排列內容，然後使用其他產品ID將內容發佈至應用程式，然後將內容發佈至不含產品ID的應用程式。

如 [需如何使用Livefyre. js自訂檔案捲動的詳細資訊](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) ，請參閱幻燈片選項。

