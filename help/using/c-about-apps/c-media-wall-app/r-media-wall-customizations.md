---
description: 變更Media塗鴉牆應用程式的大小、寬度和互動選項。
seo-description: 變更Media塗鴉牆應用程式的大小、寬度和互動選項。
seo-title: 媒體塗鴉牆自訂
solution: Experience Manager
title: 媒體塗鴉牆自訂
uuid: 79aid92-3937-4bb4-a6 a6-b090 fb39 afb0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 媒體塗鴉牆自訂{#media-wall-customizations}

變更Media塗鴉牆應用程式的大小、寬度和互動選項。



媒體牆會將即時影像和其他內容串流化至即時社交塗鴉牆，視覺化事件周圍的所有活動。

如果已啓用，使用者可以直接將文字、影像或視訊張貼至此應用程式。支援的檔案類型包括：

* 影像：JPEG，GIF，PNG
* 影片：Quicktime/MOV、MP4、MPEG、WebM
* 音訊：WAV、WAVE、X-MS-WMA、FAC、OGG、MPEG

* **[!UICONTROL Items to load]**

   設定顯示的初始內容項目。

* **[!UICONTROL Load content with animation.]** 開啓此選項，在含有動畫的頁面上載入媒體塗鴉牆。關閉這個選項，在沒有動畫的頁面上載入媒體塗鴉牆。
* **[!UICONTROL Number of columns.]** 設定媒體塗鴉牆的欄數。不論視窗或瀏覽器大小，欄數都相同。如果您選取「自動」，欄數會調整，以顯示螢幕大小的最佳化欄數。
* **[!UICONTROL Fit content to width]**. 當此選項關閉時，內容會被裁切至方形。切換此選項以顯示卡片中的整個影像，不論是否填滿整個卡片。
* **[!UICONTROL Include content modal]**

   可讓使用者按一下串流中的像片，以在覆蓋的快顯視窗中開啓。

* **[!UICONTROL Require rights]**. 啓用此選項，只顯示權限請求狀態為「已授予」的內容。
* **[!UICONTROL Hide social branding when rights granted]** 切換此選項，以移除原始社交媒體網路(Twitter或Instagram)上的標誌，以供內容片段授予權限。

* **[!UICONTROL Upload Button]**

   * **[!UICONTROL Allow user posts]**. 選擇是否允許使用者使用上傳按鈕張貼文字、像片或影片。
   * **[!UICONTROL Require Media]**. 切換為要求使用者只上傳使用「上傳按鈕」的像片或視訊內容。
   * 您可以編輯下列「上傳按鈕」欄位的預設文字：

      * **[!UICONTROL Upload Button Text]**. 上傳按鈕的文字。預設文字是「您的想法？」
      * **[!UICONTROL Comment Modal Title]**. 用來張貼內容的模型網站的標題。預設文字為「貼文您的留言」。
      * **[!UICONTROL Comment Modal Button]**. 訪客點按以張貼內容的按鈕網站文字。預設文字為「貼文您的留言」。

* **[!UICONTROL Call-to-action button]** 您可以使用產品目錄的「呼叫動作」按鈕，將使用者導向產品或網站，以進行進一步的動作。

   * **[!UICONTROL Call-to-action button]** 切換切換至開啓以顯示「呼叫動作」按鈕。
   * **[!UICONTROL Require rights to display products]** 將切換切換為要求內容擁有者已授與內容權限，然後內容的「呼叫動作」按鈕會顯示內容。

      >[!NOTE]
      >
      >即使內容未授與權限，內容仍會顯示，但除非授予內容的權限，否則「呼叫動作」按鈕不會與內容一起顯示。

   * **[!UICONTROL Call-to-action header text]** 要顯示在內容模型中「呼叫收貨人」按鈕上方標題上方的字詞。預設字詞為「Shop these products：「.
   * **[!UICONTROL Call-to-action button text]** 要顯示在內容模型中「呼叫收貨人」按鈕中的字詞。預設文字為「立即購買：「.
   * **[!UICONTROL Product display options]** 選擇要使用「呼叫動作」按鈕顯示像片和產品名稱。

      >[!NOTE]
      >
      >像片和產品名稱按鈕在啓用時都會反白顯示。

   * **[!UICONTROL Product URL referral tracking]** 切換切換至開啓，以追蹤從此應用程式到相關聯產品頁面的反向連結。
   * **[!UICONTROL Referral tracking key-value pairs]** 新增參數，進一步指定從您的應用程式內容到相關聯產品頁面的反向連結追蹤。

* **[!UICONTROL Product page filter]**.
   * **[!UICONTROL Filter UGC by Product ID]**. 選取這個選項，可針對多個產品頁面建立一個應用程式。針對每個產品頁面篩選產品特定UGC至應用程式。您可以選取一或多個資料夾，將特定系列關聯至應用程式。
   * **[!UICONTROL Select Product folders]**. 選取要用來篩選UGC的頂層產品資料夾。使用CTRL/Command+按一下可選取多個資料夾。Livefyre會使用資料夾來判斷該資料夾中的哪些產品要顯示在不同頁面上的應用程式中。
   * **[!UICONTROL Show related content]**. 切換此選項可顯示發佈至應用程式的內容，但以不同的產品ID標記。在「應用程式」的產品特定內容顯示後，Livefyre會顯示其他產品與非產品相關內容的內容。Livefyre會先使用相同的產品ID優先排列內容，然後使用其他產品ID將內容發佈至應用程式，然後將內容發佈至不含產品ID的應用程式。

您可以使用下列項目來自訂媒體塗鴉牆：

* **[!UICONTROL Style]** 以及所有應用程式中的 **[!UICONTROL Config]** 選項 **[!UICONTROL App Designer]**。如需所有應用程式中所有應用程式之標準 **[!UICONTROL Style]** 和 **[!UICONTROL Config]** 選項的詳細資訊，請參閱自訂應用程式 **[!UICONTROL App Designer]**。

* 整合工具。如需使用整合工具自訂媒體塗鴉牆的詳細資訊，請參閱 [「媒體塗鴉牆整合](/help/implementation/c-app-integrations/c-media-wall-integration.md) 」。

