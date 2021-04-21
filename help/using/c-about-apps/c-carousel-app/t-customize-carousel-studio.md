---
description: 變更轉盤應用程式的大小、寬度和互動選項。
title: 使用Studio自訂轉盤
exl-id: f6f681ac-c601-40b9-9e99-bf5495f505f8
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# 使用Studio自訂轉盤{#customize-a-carousel-using-studio}

變更轉盤應用程式的大小、寬度和互動選項。

所有應用程式都會使用&#x200B;**[!UICONTROL App Designer]**&#x200B;中的&#x200B;**[!UICONTROL Style]**&#x200B;和&#x200B;**[!UICONTROL Config]**&#x200B;選項。 如需&#x200B;**[!UICONTROL App Designer]**&#x200B;中所有應用程式的標準&#x200B;**[!UICONTROL Style]**&#x200B;和&#x200B;**[!UICONTROL Config]**&#x200B;選項的詳細資訊，請參閱自訂應用程式。

您可以使用應用程式設計工具中的下列其他選項來自訂轉盤：

* **[!UICONTROL Max Number of Items]**

   設定在轉盤中顯示的項目數。 預設為 50。

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**。僅限電腦螢幕

   * 如果內容大於600像素，則水準顯示
   * 如果內容小於600像素，則垂直顯示
   * **垂直。** 適用於電腦螢幕或行動裝置。在行動裝置中，卡片會縮小以符合螢幕大小。

* **[!UICONTROL Call-to-action button]** 您可以搭配產品目錄使用「行動要求」按鈕，將使用者引導至產品或您的網站，以便採取進一步行動。

   * **[!UICONTROL Call-to-action button]** 切換為開啟，以顯示「動作要求」按鈕。
   * **[!UICONTROL Require rights to display products]** 切換為開啟，要求內容擁有者已授與內容的權限，然後內容才會顯示動作呼叫按鈕。

   >[!NOTE]
   >
   >即使未授與內容的權限，內容也會顯示，但除非授與內容的權限，否則行動要求按鈕不會與內容一起顯示。

   * **[!UICONTROL Show call-to-action in tile]**。選擇是否在方塊上顯示「動作要求」按鈕，而非只在網站訪客點按資訊卡並在較大視窗中開啟內容時顯示「動作要求」按鈕。
   * **[!UICONTROL Call-to-action indication text]** 顯示的文字會提示使用者按一下卡片以開啟動作呼叫模式。
   * **[!UICONTROL Call-to-action header text]** 要在內容模式中「行動要求」按鈕上方標題中顯示的字詞。預設文字為「Shop these products:」。
   * **[!UICONTROL Call-to-action button text]** 要在內容模式的「行動要求」按鈕中顯示的字詞。預設文字為「立即購買：」。
   * **[!UICONTROL Product display options]** 選擇是否要顯示 **[!UICONTROL Photo]** 和 **[!UICONTROL Product name]** 「操作調用」按鈕。

   >[!NOTE]
   >
   >「像片」和「產品」名稱按鈕都會在啟用時反白標示為藍色。

   * **[!UICONTROL Product URL referral tracking]** 切換為開啟，以追蹤從此應用程式到相關產品頁面的反向連結。
   * **[!UICONTROL Referral tracking key-value pairs]** 新增參數，以進一步指定從應用程式內容到相關產品頁面的反向連結追蹤。



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**。選取這個選項，可為多個產品頁面建立一個應用程式。 針對每個產品頁面，將產品特定的UGC篩選至應用程式。 您可以選取一或多個檔案夾，將特定系列與應用程式建立關聯。
   * **[!UICONTROL Select Product folders]**。選取要用來篩選UGC的頂層產品資料夾。 使用CTRL/Command +按一下可選擇多個資料夾。 Livefyre使用資料夾來判斷該資料夾中哪些產品會顯示在不同頁面上的應用程式中。
   * **[!UICONTROL Show related content]**。切換此選項，以顯示已發佈至應用程式，但以不同產品ID標籤的內容。 在顯示應用程式的特定產品內容後，Livefyre會顯示其他產品的內容以及與產品無關的內容。 Livefyre會先將具有相同產品ID的內容排定優先順序，然後將內容發佈至具有其他產品ID的應用程式，接著將內容發佈至沒有產品ID的應用程式。
