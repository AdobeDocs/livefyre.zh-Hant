---
description: 有關GDPR適用隱私權要求的常見問答集(FAQ)解答。
seo-description: 有關GDPR適用隱私權要求的常見問答集(FAQ)解答。
seo-title: 隱私權要求常見問答集
solution: Experience Manager
title: 隱私權要求常見問答集
uuid: 0cd6f0d2-504d-46e9-ac46-070536cda086
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 1%

---


# 隱私權要求常見問答{#privacy-request-faqs}

有關GDPR適用隱私權要求的常見問答集(FAQ)解答。

* **在使用Livefyre應用程式的網站上，網站訪客如何選擇不受追蹤？** 當網站訪客退出時，客戶實作必須向Livefyre指出使用者已退出，然後再執行個體化應用程式。Livefyre已建立方式來使用JavaScript選項`userPrivacyOptOut`進行此作業。 如需如何使用`userPrivacyOptOut`的詳細資訊，請參閱[userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md)。

   當`userPrivacyOptOut`標幟設為true時，頁面上的任何應用程式都不會使用Cookie或其他方法將資料傳輸至Livefyre伺服器。 Livefyre則不會使用可用於追蹤網站訪客的資料來更新本機儲存空間。 如果來源不支援Proxy，則Livefyre會在內容上顯示遮色片，除非使用者點按視訊並核准來自該來源的潛在追蹤。

   如果您使用Livefyre Identity，使用者可以選擇刪除其個人資料，或建立其使用者帳戶所追蹤資料的報表。

* **如何防止從已選擇退出的網站訪客收集未來內容？** 在使 `userPrivacyOptOut` 用 `livefyre.js` Livefyre應用程式的網頁上使用。如需`userPrivacyOptOut`的詳細資訊，請參閱[userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md)。

* **如何產生報表並刪除「應用程式使用者」或社交帳戶擁有者的資料？** [隱私](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) 權要求，以產生報告並從應用程式刪除使用者資料。

* **如何移除訪客的所有內容？** Livefyre不會維護網站訪客的永續性資訊，但是會以Cookie的形式來唯一識別網站訪客，以利用Livecount功能。livecount是網站訪客的即時暫時計數。 訪客離開或清除Cookie後，不會保留任何歷史記錄。

   建立[隱私權要求](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests)以刪除帳戶。 Livefyre會刪除或讓使用者描述檔和任何相關記錄變成匿名。

* **如何移除註冊使用者的內容？** 建立隱 [私權](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) 要求以刪除帳戶。用戶配置檔案和所有相關記錄將被完全銷毀。

   >[!NOTE]
   >
   >此動作無法復原。

* **如何產生目前或前任員工的資料追蹤報表？** [檢視隱私權](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) 報表，以產生使用者帳戶所追蹤資料的報表。

* **Livefyre社交串流是否符合規範？** 當使用者從其社交網路刪除貼文或推文時，24小時內，內容也會從Livefyre的所有來源刪除。這適用於Twitter和Facebook。

