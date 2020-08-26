---
description: 2018年11月15日發行說明。
seo-description: 2018年11月15日發行說明。
seo-title: 發行說明
solution: Experience Manager
title: 發行說明
uuid: 34e64943-dea6-46ac-9fcc-8febeab6aa42
translation-type: tm+mt
source-git-commit: efb031b58f01ec69c8297a808998d25a0015f102
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 7%

---


# 發行說明{#release-notes}

2018年11月15日發行說明。

## 新功能 {#section_syx_mdt_wcb}

此版本的生產版本中已發佈下列新功能：

* **Instagram搜尋和串流的更新。** 您可以使用 *Instagram商業帳戶* :

   * 依使用者執行Instagram社交搜尋（使用者也必須是Instagram商業帳戶）。

   * 從特定Instagram使用者帳戶建立Instagram串流（該帳戶也必須是商業帳戶），包括您自己的帳戶。

   * 使用部分自動化的工作流程，從Instagram要求資產的權限。

   * 如需您需要從Instagram設定和請求權限的Instagram帳戶類型的詳細資訊，請參閱關於 [Instagram帳戶](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md)。

* **自動監控使用權要求回應，以便進行商業帳戶搜尋。** 僅適用於商業帳戶搜尋——可自動監控權限要求的回應並更新Livefyre中的活動記錄。

如需如何申請Instagram帳戶權限的詳細資訊，請參閱「手動傳送Instagram權限請求 [](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md) 」和「傳送部分自動化的Instagram權限請求」 [](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md)。

* **Adobe Target 整合.** 已新增與Adobe Target的整合，讓您可直接將Livefyre應用程式共用至Adobe Target選件程式庫。 如需搭配Adobe Target使用Livefyre的詳細資訊，請參閱 [Target檔案](hhttps://docs.adobe.com/content/help/en/livefyre/using/library/livefyre-target.html)。

## 問題 {#section_ehw_ndt_wcb}

本版本已解決下清單格中的問題。

### 生產版本

| 問題類型 | 元件 | 發行說明 |
|--- |--- |--- |
| 問題 | AppService:Livefyre Identity | 修正按一下時，Studio > [!UICONTROL Reset to Default] 整合設定> Livefyre Identity中「登入模式」下的標誌未重設為預設影像的問題。 |
| 問題 | 庫 | 已修正視訊上傳至「資料庫」，接著以資產詳細資料檢視的問題，此問題無法正確顯示。 |
| 問題 | 串流 | 修正產品無法顯示在串流規則中的問題。 |
| 問題 | 串流 | 修正產品標籤無法用於串流規則的問題。 |
| 增強功能 | Studio | 修正Livefyre Studio中未顯示產品ID的問題。 |
| 問題 | Studio:ModQ | 修正已刪除的內容刪除後仍顯示在ModQ中的問題。 |

### UAT發行

| **問題類型** | **元件** | **發行說明** |
|---|---|---|
| 問題 | 社交元件：轉盤 | 修正IE11和Mozilla Firefox中未回應並複製URL的問題。 |