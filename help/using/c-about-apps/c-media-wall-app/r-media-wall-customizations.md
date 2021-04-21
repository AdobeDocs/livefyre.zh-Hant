---
description: 變更媒體塗鴉牆應用程式的大小、寬度和互動選項。
title: 介質牆定制
exl-id: bc34d8da-9e14-4226-b38d-128889bc31cc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 0%

---

# 介質牆定制{#media-wall-customizations}

變更媒體塗鴉牆應用程式的大小、寬度和互動選項。



「媒體牆」會將即時影像和其他內容串流至即時社交牆，以視覺化方式呈現事件周圍的所有活動。

如果啟用，使用者可以直接將文字、影像或視訊張貼至此應用程式。 支援的檔案類型包括:

* 影像：JPEG、GIF、PNG
* 影片：Quicktime/MOV、MP4、MPEG、WebM
* 音訊：WAV、WAVE、X-MS-WMA、FLAC、OGG、MPEG

* **[!UICONTROL Items to load]**

   設定顯示的內容項目初始數。

* **[!UICONTROL Load content with animation.]** 開啟這個選項，以載入具有動畫的頁面上的媒體塗鴉牆。關閉此選項可在沒有動畫的頁面上載入媒體塗鴉牆。
* **[!UICONTROL Number of columns.]** 設定介質牆的列數。無論視窗或瀏覽器大小，欄數都維持不變。 如果您選取「自動」，欄數會調整以顯示螢幕大小的最佳欄數。
* **[!UICONTROL Fit content to width]**。當此選項關閉時，內容會裁切成正方形。 將此選項切換為開啟，以顯示卡片中的整個影像，不論是否填滿整個卡片。
* **[!UICONTROL Include content modal]**

   可讓使用者按一下串流中的像片，在重疊的快顯視窗中開啟像片。

* **[!UICONTROL Require rights]**。啟用此選項可僅顯示權限請求狀態為「已授權」的內容。
* **[!UICONTROL Hide social branding when rights granted]** 開啟此選項，在授與內容權限時，移除原始社交媒體網路(Twitter或Instagram)的標誌。

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**。選擇您是否允許使用者使用上傳按鈕張貼文字、像片或影片。
   * **[!UICONTROL Require Media]**。切換為開啟，要求使用者僅使用「上傳按鈕」上傳像片或視訊內容。
   * 您可以編輯下列「上傳按鈕」欄位的預設文字：

      * **[!UICONTROL Upload Button Text]**。「上傳」按鈕的文字。 預設文字是「您在想什麼？」
      * **[!UICONTROL Comment Modal Title]**。模式網站訪客用於張貼內容的標題。 預設文字為「張貼您的留言」。
      * **[!UICONTROL Comment Modal Button]**。按鈕網站訪客點按以張貼內容的文字。 預設文字為「張貼您的留言」。

* **[!UICONTROL Call-to-action button]** 您可以搭配產品目錄使用「行動要求」按鈕，將使用者引導至產品或您的網站，以便採取進一步行動。

   * **[!UICONTROL Call-to-action button]** 切換為開啟，以顯示「動作要求」按鈕。
   * **[!UICONTROL Require rights to display products]** 切換為開啟，要求內容擁有者已授與內容的權限，然後內容才會出現「動作要求」按鈕。

      >[!NOTE]
      >
      >即使未授與內容的權限，內容仍會顯示，但「行動要求」按鈕不會與內容一起顯示，除非授與內容的權限。

   * **[!UICONTROL Call-to-action header text]** 要在內容模式中「行動要求」按鈕上方標題中顯示的字詞。預設的措辭為「購買這些產品：」。
   * **[!UICONTROL Call-to-action button text]** 要在內容模式的「行動要求」按鈕中顯示的字詞。預設文字為「立即購買：」。
   * **[!UICONTROL Product display options]** 選擇是否要使用「行動要求」按鈕顯示像片和產品名稱。

      >[!NOTE]
      >
      >「像片」和「產品」名稱按鈕都會在啟用時反白標示為藍色。

   * **[!UICONTROL Product URL referral tracking]** 切換為開啟，以追蹤從此應用程式到相關產品頁面的反向連結。
   * **[!UICONTROL Referral tracking key-value pairs]** 新增參數，以進一步指定從應用程式內容到相關產品頁面的反向連結追蹤。

* **[!UICONTROL Product page filter]**。
   * **[!UICONTROL Filter UGC by Product ID]**。選取這個選項，可為多個產品頁面建立一個應用程式。 針對每個產品頁面，將產品特定的UGC篩選至應用程式。 您可以選取一或多個檔案夾，將特定系列與應用程式建立關聯。
   * **[!UICONTROL Select Product folders]**。選取要用來篩選UGC的頂層產品資料夾。 使用CTRL/Command +按一下可選擇多個資料夾。 Livefyre使用資料夾來判斷該資料夾中哪些產品會顯示在不同頁面上的應用程式中。
   * **[!UICONTROL Show related content]**。切換此選項，以顯示已發佈至應用程式，但以不同產品ID標籤的內容。 在顯示應用程式的特定產品內容後，Livefyre會顯示其他產品的內容以及與產品無關的內容。 Livefyre會先將具有相同產品ID的內容排定優先順序，然後將內容發佈至具有其他產品ID的應用程式，接著將內容發佈至沒有產品ID的應用程式。

您可以使用下列項目來自訂媒體塗鴉牆：

* **[!UICONTROL Style]** 和 **[!UICONTROL Config]** 中所有應用程式的選項 **[!UICONTROL App Designer]**。如需&#x200B;**[!UICONTROL App Designer]**&#x200B;中所有應用程式的標準&#x200B;**[!UICONTROL Style]**&#x200B;和&#x200B;**[!UICONTROL Config]**&#x200B;選項的詳細資訊，請參閱自訂應用程式。

* 整合工具。 如需如何使用整合工具自訂媒體塗鴉牆的詳細資訊，請參閱[媒體塗鴉牆整合](/help/implementation/c-app-integrations/c-media-wall-integration.md)。
