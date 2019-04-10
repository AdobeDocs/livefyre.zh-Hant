---
description: 關於GDPR適用隱私權要求的常見問題解答(FAQ)。
seo-description: 關於GDPR適用隱私權要求的常見問題解答(FAQ)。
seo-title: 隱私權要求常見問答集
solution: Experience Manager
title: 隱私權要求常見問答集
uuid: 0cd6f0d2-504d-46e9-ac46-070536cda086
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 隱私權要求常見問答集{#privacy-request-faqs}

關於GDPR適用隱私權要求的常見問題解答(FAQ)。

* **網站訪客如何在使用Livefyre應用程式的網站上選擇退出？** 當網站訪客選擇退出時，客戶實作必須指出使用者在實例化應用程式之前已選擇退出的Livefyre。Livefyre已建立使用JavaScript選項完成此動作的方式 `userPrivacyOptOut`。如需如何使用 `userPrivacyOptOut`的詳細資訊，請參閱 [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md)。

   `userPrivacyOptOut` 當標幟設為true時，頁面上的任何應用程式都不會使用Cookie或其他方法將資料傳輸至Livefyre伺服器。Livefyre將不會更新本機儲存空間，內含可用來追蹤網站訪客的資料。如果來源不支援Proxy，則Livefyre會在內容上顯示遮色片，除非使用者按一下視訊並核准來源的潛在追蹤。

   如果您使用Livefyre Identity，使用者可以選擇刪除其描述檔，或建立其使用者帳戶所追蹤的資料報表。

* **如何避免從已選擇退出的網站訪客收集未來內容？**`userPrivacyOptOut` 用於 `livefyre.js` 使用Livefyre應用程式的網頁上。如需詳細資訊， `userPrivacyOptOut`請查看 [userPrivacyOptOut](/help/using/c-settings-other/c-gdpr-compliance/c-userprivacyoptout.md)。

* **如何產生報表並刪除應用程式使用者或社交帳戶擁有者的資料？**[「隱私權請求](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) 」以產生報表並從「應用程式」刪除使用者資料。

* **如何移除訪客的所有內容？** Livefyre不會維護網站訪客的永久性資訊，除非以Cookie的形式唯一識別LiveCount功能。LiveCount是網站訪客的暫時和即時計數。訪客離開或清除Cookie後，不會保留歷史記錄。

   建立 [「隱私權請求](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) 」以刪除帳戶。Livefyre會刪除或讓使用者描述檔和任何相關記錄匿名。

* **如何移除註冊使用者的內容？** 建立 [隱私權請求](../../c-settings-other/c-gdpr-compliance/c-privacy-requests.md#c_privacy_requests) 以刪除帳戶。使用者描述檔和任何相關記錄將會完全銷毀。

   >[!NOTE]
   >
   >此動作無法復原。

* **如何產生目前或前員工所追蹤的資料報表？**[檢視隱私權報告](../../c-settings-other/c-gdpr-compliance/c-view-a-privacy-report.md#c_view_a_privacy_report) ，以產生使用者帳戶所追蹤資料的報表。

* **Livefyre社交串流是否符合規定？** 當使用者從社交網路刪除貼文或推文時，在24小時內，也會從Livefyre中的所有來源刪除內容。這適用於Twitter和Facebook。

