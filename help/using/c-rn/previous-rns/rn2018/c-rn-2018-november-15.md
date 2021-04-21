---
description: 2018年11月15日發行說明。
title: 發行說明
exl-id: 3f904022-b770-4f35-a3b0-790e15748763
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 6%

---

# 發行說明{#release-notes}

2018年11月15日發行說明。

## 新功能 {#section_syx_mdt_wcb}

此版本的生產版本中已發佈下列新功能：

* **instagram搜尋與串流的更新。** 您可以使用 *Instagram商* 務帳戶：

   * 依使用者執行Instagram社交搜尋(使用者必須是Instagram企業帳戶)。

   * 從特定的Instagram使用者帳戶（帳戶也必須是商業帳戶）建立Instagram串流，包括您自己的帳戶。

   * 使用部分自動化的工作流程，向Instagram索取資產的權利。

   * 有關您需要設定和請求Instagram權利的Instagram帳戶類型的資訊，請參閱[關於Instagram帳戶](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md)。

* **自動監控使用權要求回應，以便進行商業帳戶搜尋。** 僅適用於商業帳戶搜尋——可自動監控權限要求的回應並更新Livefyre中的活動記錄。

有關如何請求Instagram帳戶權限的詳細資訊，請參閱[手動發送Instagram權限請求](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md)和[發送部分自動的Instagram權限請求](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md)。

* **Adobe Target 整合.** 已新增與Adobe Target的整合，讓您可直接將Livefyre應用程式分享到您的Adobe Target選件程式庫。如需搭配Adobe Target使用Livefyre的詳細資訊，請參閱[ Target檔案](hhttps://docs.adobe.com/content/help/en/livefyre/using/library/livefyre-target.html)。

## 問題 {#section_ehw_ndt_wcb}

本版本已解決下清單格中的問題。

### 生產版本

| 問題類型 | 元件 | 發行說明 |
|--- |--- |--- |
| 問題 | AppService:Livefyre Identity | 修正按一下[!UICONTROL Reset to Default]後，在Studio中的「登入模式」>「整合設定」>「Livefyre身分識別」下未將標誌重設為預設影像的問題。 |
| 問題 | 庫 | 已修正視訊上傳至「資料庫」，接著以資產詳細資料檢視的問題，此問題無法正確顯示。 |
| 問題 | 串流 | 修正產品無法顯示在串流規則中的問題。 |
| 問題 | 串流 | 修正產品標籤無法用於串流規則的問題。 |
| 增強功能 | Studio | 修正Livefyre Studio中未顯示產品ID的問題。 |
| 問題 | Studio:ModQ | 修正已刪除的內容刪除後仍顯示在ModQ中的問題。 |

### UAT發行

| **問題類型** | **元件** | **發行說明** |
|---|---|---|
| 問題 | 社交元件：轉盤 | 修正IE11和Mozilla Firefox中未回應並複製URL的問題。 |
