---
description: 變更Mosaic應用程式的大小、寬度和互動選項。
seo-description: 變更Mosaic應用程式的大小、寬度和互動選項。
seo-title: 馬賽克自訂
solution: Experience Manager
title: 馬賽克自訂
uuid: 4e226d68-f517-4922-bc25-655d524d7d52
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# 馬賽克自訂{#mosaic-customizations}

變更Mosaic應用程式的大小、寬度和互動選項。

所有應用程式都會使用&#x200B;**[!UICONTROL App Designer]**&#x200B;中的&#x200B;**[!UICONTROL Style]**&#x200B;和&#x200B;**[!UICONTROL Config]**&#x200B;選項。 如需&#x200B;**[!UICONTROL App Designer.]**&#x200B;中所有應用程式的標準&#x200B;**[!UICONTROL Style]**&#x200B;和&#x200B;**[!UICONTROL Config]**&#x200B;選項的詳細資訊，請參閱自訂應用程式

您可以在App Designer中使用下列其他選項來自訂Mosaic:

* **[!UICONTROL Content interaction]**。設定將新內容載入頁面的樣式：

   * **[!UICONTROL Hover Fade]** 當網站訪客將滑鼠暫留在內容上時，淡入資訊卡的另一面。
   * **[!UICONTROL Hover Flip]** 以在網站訪客將滑鼠暫留在內容上時，翻轉至資訊卡的另一側。
   * **[!UICONTROL Click]** 以在網站訪客點按內容上的滑鼠時，顯示資訊卡的另一側。

* **[!UICONTROL Number of Tiles to Load]**。Mosaic中要載入的拼貼數。 這會影響輸出顯示。 除非您選擇正確的拼貼數目以對應容器寬度，否則馬賽克不會顯示在格線中。 您可能需要調整這些項目，以便網格能夠正確顯示。
* **[!UICONTROL Hide social branding when rights granted]** 開啟此選項，在授與內容的權限時，移除原始社交媒體網路（Twitter或Instagram）的標誌。

* **[!UICONTROL Call-to-action button]** 您可以搭配產品目錄使用「行動要求」按鈕，將使用者引導至產品或您的網站，以便採取進一步行動。

   * **[!UICONTROL Call-to-action button]** 切換為開啟，以顯示「動作要求」按鈕。

   * **[!UICONTROL Require rights to display products]** 切換為開啟，要求內容擁有者已授與內容的權限，然後內容才會出現「動作要求」按鈕。

      >[!NOTE]
      >
      >即使未授與內容的權限，內容仍會顯示，但「行動要求」按鈕不會與內容一起顯示，除非授與內容的權限。

   * **[!UICONTROL Show call-to-action in tile]**。選擇是否在幻燈片表徵圖上顯示「動作要求」按鈕，而不是只在網站訪客點按資訊卡並在較大視窗中開啟內容時顯示「動作要求」按鈕。
   * **[!UICONTROL Call-to-action indication text]** 顯示的文字會提示使用者按一下卡片以開啟「動作要求」模式。

   * **[!UICONTROL Call-to-action header text]** 要在內容模式中「行動要求」按鈕上方標題中顯示的字詞。預設的措辭為「購買這些產品：」。

   * **[!UICONTROL Call-to-action button text]** 自訂「行動要求」按鈕上的文字。預設文字為「立即購買」。

   * **[!UICONTROL Product display options]** 選擇是否要顯示 **[!UICONTROL Photo]** 和 **[!UICONTROL Product name]** 「操作調用」按鈕。

   * **[!UICONTROL Product URL referral tracking]** 切換為開啟，以追蹤從此應用程式到相關產品頁面的反向連結。

   * **[!UICONTROL Referral tracking key-value pairs]** 新增參數，以進一步指定從應用程式內容到相關產品頁面的反向連結追蹤。

* **[!UICONTROL Product page filter]**。

   * **[!UICONTROL Filter UGC by Product ID]**。選取這個選項，可為多個產品頁面建立一個應用程式。 針對每個產品頁面，將產品特定的UGC篩選至應用程式。 您可以選取一或多個檔案夾，將特定系列與應用程式建立關聯。
   * **[!UICONTROL Select Product folders]**。選取要用來篩選UGC的頂層產品資料夾。 使用CTRL/Command +按一下可選擇多個資料夾。 Livefyre使用資料夾來判斷該資料夾中哪些產品會顯示在不同頁面上的應用程式中。
   * **[!UICONTROL Show related content]**。切換此選項，以顯示已發佈至應用程式，但以不同產品ID標籤的內容。 在顯示應用程式的特定產品內容後，Livefyre會顯示其他產品的內容以及與產品無關的內容。 Livefyre會先將具有相同產品ID的內容排定優先順序，然後將內容發佈至具有其他產品ID的應用程式，接著將內容發佈至沒有產品ID的應用程式。

如需如何使用Livefyre.js自訂Mosaic的詳細資訊，請參閱[Mosaic選項](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)。
