---
description: 2018年11月15日發行的發行說明。
seo-description: 2018年11月15日發行的發行說明。
seo-title: 發行說明
solution: Experience Manager
title: 發行說明
uuid: 34e64943-dea6-46ac-9fc-9feeab6 aa42
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 發行說明{#release-notes}

2018年11月15日發行的發行說明。

## 新特性 {#section_syx_mdt_wcb}

此發行版本中發行了下列新功能：

* **Instagram搜尋與串流更新。** 您可以使用 *Instagram商業帳戶* 來：

   * 依使用者執行Instagram社交搜尋(使用者必須是Instagram的商業帳戶)。

   * 從特定Instagram使用者帳戶建立Instagram串流(帳戶也必須是商務帳戶)，包括您自己的帳戶。

   * 使用部分自動化工作流程從Instagram取得資產的權限。

   * 如需有關您需要設定和請求Instagram權限的Instagram帳戶類型的詳細資訊，請參閱 [關於Instagram帳戶](/help/using/c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md)。

* **自動監控商業帳戶型搜尋的使用權限請求回應。** 僅適用於商業帳戶型搜尋—可自動監視權限要求的回應並更新Livefyre中的活動記錄。

如需如何申請Instagram帳戶權限的詳細資訊，請參閱 [「傳送Instagram權限請求」，](/help/using/c-how-requesting-rights-works/c-send-instagram-manual-rights-request.md)[以及「傳送部分自動化Instagram權限請求](/help/using/c-how-requesting-rights-works/c-send-an-instagram-rights-request-from-the-library.md)」。

* **Adobe Target整合。** 已新增與Adobe Target的整合，可讓您直接將Livefyre應用程式共用至Adobe Target選件庫。如需使用Livefyre搭配Adobe Target的詳細資訊，請參閱 [Target文件](https://marketing.adobe.com/resources/help/en_US/livefyre/livefyre-target.html)。

## 問題 {#section_ehw_ndt_wcb}

下列表格中的問題已解決。

### 生產版本

| 問題類型 | 元件 | 發行說明 |
|--- |--- |--- |
| 期刊 | AppService：Livefyre身份識別 | 修正點按的問題 [！UICCOHTROL重設為預設] 值未將標誌重設為「Studio>整合設定> Livefyre Identity」(「整合設定>「整合設定」>「Livefyre Identity」)下的標誌。 |
| 期刊 | Library | 已修正上傳至「資料庫」的視訊，然後在資產詳細資料中檢視的問題無法正確顯示的問題。 |
| 期刊 | 串流 | 修正產品無法在串流規則中顯示的問題。 |
| 期刊 | 串流 | 修正產品標記無法用於串流規則的問題。 |
| 增強功能 | Studio | 修正Livefyre Studio中無法顯示產品ID的問題。 |
| 期刊 | Studio：ModQ | 已修正刪除的內容刪除後仍以ModQ顯示的問題。 |

### UAT版本

| **問題類型** | **元件** | **發行說明** |
|---|---|---|
| 期刊 | Social元件：轉盤 | 修正共用連結未如IE11和Mozilla Firefox般回應及複製URL的問題。 |