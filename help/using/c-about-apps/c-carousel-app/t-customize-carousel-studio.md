---
description: 變更轉盤應用程式的大小、寬度和互動選項。
seo-description: 變更轉盤應用程式的大小、寬度和互動選項。
seo-title: 使用Studio自訂轉盤
solution: Experience Manager
title: 使用Studio自訂轉盤
uuid: 24f080fc-37fb-40d4-8c1a-a502 ee8 ac978
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 使用Studio自訂轉盤{#customize-a-carousel-using-studio}

變更轉盤應用程式的大小、寬度和互動選項。

所有應用程式使用 **[!UICONTROL Style]** 和 **[!UICONTROL Config]** 選項 **[!UICONTROL App Designer]**。如需所有應用程式中所有應用程式之標準 **[!UICONTROL Style]** 和 **[!UICONTROL Config]** 選項的詳細資訊，請參閱自訂應用程式 **[!UICONTROL App Designer]**。

您可以使用App Designer中的下列其他選項來自訂轉盤：

* **[!UICONTROL Max Number of Items]**

   設定在轉盤中顯示的項目數。預設值為50。

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. 僅適用於電腦螢幕

   * 如果內容大於600像素，則會水平顯示
   * 如果內容小於600像素，則會垂直顯示
   * **垂直。** 適用於電腦螢幕或行動裝置。在行動裝置中，卡片會符合螢幕大小。

* **[!UICONTROL Call-to-action button]** 您可以使用產品目錄的「呼叫動作」按鈕，將使用者導向產品或網站，以進行進一步的動作。

   * **[!UICONTROL Call-to-action button]** 切換切換至開啓以顯示行動收視按鈕。
   * **[!UICONTROL Require rights to display products]** 將切換切換為要求內容擁有者已授予內容權限，在內容針對內容顯示呼叫動作按鈕之前。
   >[!NOTE]
   >
   >即使內容未授與權限，內容仍會顯示，但除非授予內容的權限，否則呼叫動作按鈕將不會與內容一起顯示。

   * **[!UICONTROL Show call-to-action in tile]**. 選擇是否在圖標上顯示呼叫動作按鈕，而不是只在網站訪客點按資訊卡並開啓較大視窗中的內容時，顯示呼叫動作按鈕。
   * **[!UICONTROL Call-to-action indication text]** 要顯示的文字，提示使用者按下卡片以開啓呼叫動作模式。
   * **[!UICONTROL Call-to-action header text]** 要顯示在內容模型中「呼叫收貨人」按鈕上方標題上方的字詞。預設文字為「Shop these products：「.
   * **[!UICONTROL Call-to-action button text]** 要顯示在內容模型中「呼叫收貨人」按鈕中的字詞。預設文字為「立即購買：「.
   * **[!UICONTROL Product display options]** 選擇是否要顯示和 **[!UICONTROL Photo]****[!UICONTROL Product name]** 使用「呼叫動作」按鈕。
   >[!NOTE]
   >
   >像片和產品名稱按鈕在啓用時都會反白顯示。

   * **[!UICONTROL Product URL referral tracking]** 切換切換至開啓，以追蹤從此應用程式到相關聯產品頁面的反向連結。
   * **[!UICONTROL Referral tracking key-value pairs]** 新增參數，進一步指定從您的應用程式內容到相關聯產品頁面的反向連結追蹤。



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. 選取這個選項，可針對多個產品頁面建立一個應用程式。針對每個產品頁面篩選產品特定UGC至應用程式。您可以選取一或多個資料夾，將特定系列關聯至應用程式。
   * **[!UICONTROL Select Product folders]**. 選取要用來篩選UGC的頂層產品資料夾。使用CTRL/Command+按一下可選取多個資料夾。Livefyre會使用資料夾來判斷該資料夾中的哪些產品要顯示在不同頁面上的應用程式中。
   * **[!UICONTROL Show related content]**. 切換此選項可顯示發佈至應用程式的內容，但以不同的產品ID標記。在「應用程式」的產品特定內容顯示後，Livefyre會顯示其他產品與非產品相關內容的內容。Livefyre會先使用相同的產品ID優先排列內容，然後使用其他產品ID將內容發佈至應用程式，然後將內容發佈至不含產品ID的應用程式。
