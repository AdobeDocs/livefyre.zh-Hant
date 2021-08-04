---
description: 2018年11月15日發行的發行說明。
title: 發行說明
exl-id: 3f904022-b770-4f35-a3b0-790e15748763
source-git-commit: beb224fdccf68c98fc3eff62b0867f22fa52902b
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 6%

---

# 發行說明{#release-notes}

2018年11月15日發行的發行說明。

## 新特性 {#section_syx_mdt_wcb}

此版本的生產版本中發行了下列新功能：

* **instagram搜尋和資料流的更新。** 您可以使用Instagram *商業* 帳戶：

   * 依使用者執行Instagram社交搜尋(使用者也必須是Instagram商業帳戶)。

   * 從特定的Instagram使用者帳戶（帳戶也必須是商業帳戶）建立Instagram資料流，包括您自己的帳戶。

   * 使用部分自動化的工作流程，從Instagram請求資產的權限。

   * 如需您需要設定哪種類型的Instagram帳戶，以及向Instagram要求權限的詳細資訊，請參閱[關於Instagram帳戶](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md)。

* **自動監控以業務帳戶為基礎的搜尋的使用權要求回應。** 僅適用於以商業帳戶為基礎的搜尋 — 可自動監控權限要求的回應以及更新Livefyre中的活動記錄。

如需如何要求Instagram帳戶權限的詳細資訊，請參閱[手動傳送Instagram權限要求](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md)和[傳送部分自動化的Instagram權限要求](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md)。

* **Adobe Target 整合.** 新增與Adobe Target的整合，讓您直接將Livefyre應用程式共用至Adobe Target選件資料庫。如需有關搭配Adobe Target使用Livefyre的詳細資訊，請參閱[Target檔案](https://experienceleague.adobe.com/docs/livefyre/using/library/livefyre-target.html)。

## 問題 {#section_ehw_ndt_wcb}

此版本已解決下表中的問題。

### 生產版本

| 問題類型 | 元件 | 發行說明 |
|--- |--- |--- |
| 問題 | AppService:Livefyre Identity | 修正按一下[!UICONTROL Reset to Default]時，未將Studio > Integration Settings > Livefyre Identity中Login Modal底下的標誌重設為預設影像的問題。 |
| 問題 | 庫 | 修正上傳至程式庫、然後以資產詳細資料檢視的影片無法正確顯示的問題。 |
| 問題 | 資料流 | 修正串流規則無法顯示產品的問題。 |
| 問題 | 資料流 | 修正串流規則無法使用產品標籤的問題。 |
| 增強功能 | Studio | 修正Livefyre Studio中未顯示產品ID的問題。 |
| 問題 | 工作室：ModQ | 修正已刪除的內容在刪除後仍顯示在ModQ中的問題。 |

### UAT版本

| **問題類型** | **元件** | **發行說明** |
|---|---|---|
| 問題 | 社交元件：輪播 | 修正「共用」連結未如IE11和Mozilla Firefox中預期回應並複製URL的問題。 |
