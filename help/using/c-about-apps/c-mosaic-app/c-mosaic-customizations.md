---
description: 變更Mosaic應用程式的大小、寬度和互動選項。
seo-description: 變更Mosaic應用程式的大小、寬度和互動選項。
seo-title: 馬賽克自訂
solution: Experience Manager
title: 馬賽克自訂
uuid: 4e226d68-f517-4922-bc25-655d524 d7 d52
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 馬賽克自訂{#mosaic-customizations}

變更Mosaic應用程式的大小、寬度和互動選項。

所有應用程式使用 **[!UICONTROL Style]** 和 **[!UICONTROL Config]** 選項 **[!UICONTROL App Designer]**。如需所有應用程式中所有應用程式標準 **[!UICONTROL Style]** 和 **[!UICONTROL Config]** 選項的詳細資訊，請參閱自訂應用程式。 **[!UICONTROL App Designer.]**

您可以使用App Designer中的下列其他選項來自訂Mosaic：

* **[!UICONTROL Content interaction]**. 設定將新內容載入頁面的樣式：

   * **[!UICONTROL Hover Fade]** 當網站訪客將滑鼠停留在內容上方時，將淡化到資訊卡的另一邊。
   * **[!UICONTROL Hover Flip]** 當網站訪客將滑鼠停留在內容上方時，就會翻轉至卡片的另一側。
   * **[!UICONTROL Click]** 在網站訪客點按內容時顯示資訊卡的另一側。

* **[!UICONTROL Number of Tiles to Load]**. 以Mosaic載入的拼貼數目。這會影響輸出顯示。除非您選擇正確的圖格數目以對應容器寬度，否則Mosaic不會顯示在網格中。您可能需要調整這些格線，才能正確顯示。
* **[!UICONTROL Hide social branding when rights granted]** 切換此選項，以移除原始社交媒體網路(Twitter或Instagram)上的標誌，以供內容片段授予權限。

* **[!UICONTROL Call-to-action button]** 您可以使用產品目錄的「呼叫動作」按鈕，將使用者導向產品或網站，以進行進一步的動作。

   * **[!UICONTROL Call-to-action button]** 切換切換至開啓以顯示「呼叫動作」按鈕。

   * **[!UICONTROL Require rights to display products]** 將切換切換為要求內容擁有者已授與內容權限，然後內容的「呼叫動作」按鈕會顯示內容。

      >[!NOTE]
      >
      >即使內容未授與權限，內容仍會顯示，但除非授予內容的權限，否則「呼叫動作」按鈕不會與內容一起顯示。

   * **[!UICONTROL Show call-to-action in tile]**. 選擇是否在「幻燈片」方塊上顯示呼叫動作按鈕，而不是只在網站訪客點按卡片並開啓較大視窗中的內容時，才顯示呼叫動作按鈕。
   * **[!UICONTROL Call-to-action indication text]** 要顯示的文字，提示使用者按一下卡片以開啓「呼叫動作」模式。

   * **[!UICONTROL Call-to-action header text]** 要顯示在內容模型中「呼叫收貨人」按鈕上方標題上方的字詞。預設字詞為「Shop these products：「.

   * **[!UICONTROL Call-to-action button text]** 自訂「呼叫動作」按鈕上的文字。預設文字為「立即購買」。

   * **[!UICONTROL Product display options]** 選擇是否要顯示和 **[!UICONTROL Photo]****[!UICONTROL Product name]** 使用「呼叫動作」按鈕。

   * **[!UICONTROL Product URL referral tracking]** 切換切換至開啓，以追蹤從此應用程式到相關聯產品頁面的反向連結。

   * **[!UICONTROL Referral tracking key-value pairs]** 新增參數，進一步指定從您的應用程式內容到相關聯產品頁面的反向連結追蹤。

* **[!UICONTROL Product page filter]**.

   * **[!UICONTROL Filter UGC by Product ID]**. 選取這個選項，可針對多個產品頁面建立一個應用程式。針對每個產品頁面篩選產品特定UGC至應用程式。您可以選取一或多個資料夾，將特定系列關聯至應用程式。
   * **[!UICONTROL Select Product folders]**. 選取要用來篩選UGC的頂層產品資料夾。使用CTRL/Command+按一下可選取多個資料夾。Livefyre會使用資料夾來判斷該資料夾中的哪些產品要顯示在不同頁面上的應用程式中。
   * **[!UICONTROL Show related content]**. 切換此選項可顯示發佈至應用程式的內容，但以不同的產品ID標記。在「應用程式」的產品特定內容顯示後，Livefyre會顯示其他產品與非產品相關內容的內容。Livefyre會先使用相同的產品ID優先排列內容，然後使用其他產品ID將內容發佈至應用程式，然後將內容發佈至不含產品ID的應用程式。

如 [需如何使用Livefyre. js自訂Mosaic的](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) 詳細資訊，請參閱Mosaic選項。
