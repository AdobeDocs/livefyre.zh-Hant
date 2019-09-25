---
description: 2018年11月1日發行說明。
seo-description: 2018年11月1日發行說明。
seo-title: 2018 年 11 月 1 日
solution: Experience Manager
title: 2018 年 11 月 1 日
uuid: ed1a3bf1-b3f1-4746-8462-07283723ba62
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 2018 年 11 月 1 日{#november}

2018年11月1日發行說明。

## 新功能 {#section_syx_mdt_wcb}

此版本的生產版本中已發佈下列新功能：

* 視訊智慧型標籤

   運用Adobe Sensei支援的最新電腦視覺技術，在您將視訊內容儲存至資料庫時自動標籤視訊內容。 智慧型標籤可協助您更有效率地管理UGC，同時建立超精確的組織規則（串流），以根據視訊中的內容（而非僅是文字）收集內容，為您節省大量的心力來協調不想要的內容。

   功能詳細資訊：

   * 智慧型標籤會自動新增至從「資料庫」中的社交搜尋、串流和上傳的視訊檔案所取得的視訊。 在個別視訊的資產詳細資料中檢視標籤
   * 以。MP4、.MOV和AVI格式標籤視訊
   * 將視訊標籤為高達60秒或50MB
   * 智慧標籤有兩類套用至視訊：功能（動物、物件、地點等）和動作（跑步、走路、唱歌等）
   For more information see [Smart Tags](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags)

* Instagram速率限制

   Instagram已將任何使用Instagram API（包括Livefyre）的公司，每小時每個Token可發出5,000個請求，變更為每小時每Token發出200個請求。 這稱為速率 *限制*。 如需詳細資訊，請參 [閱Instagram速率限制](/help/using/c-streams/c-instagram-rate-limiting.md)。

* 資料庫中的音訊檔案

   您現在可以從程式庫面板對音訊檔案執行下列功能：

   * 搜尋
   * 預覽
   * 匯入
   * 依音訊檔案篩選
   * 將檔案拖放至設計人員

## 問題 {#section_ehw_ndt_wcb}

本版本的生產版本未解決任何新問題。 請參 [閱上節](#c_rn/section_syx_mdt_wcb)。

## UAT發行 {#section_EE91B0C9313E45C5B4CBD59CFBCCFCFE}

下表中的問題已在此版本的UAT版本中解決。

| **問題類型** | **元件** | **發行說明** |
|---|---|---|
| 增強功能 | GDPR | Analytics中前客戶的所有資料都將被刪除。 |
| 錯誤 | 庫 | 已修正視訊上傳至「資料庫」，接著以資產詳細資料檢視的問題，此問題無法正確顯示。 |
| 錯誤 | 馬賽克 | 修正Mosaic將Instagram轉盤上最後一段內容顯示為縮圖而非卡片的問題。 |
| 錯誤 | 社交搜尋 | 修正Instagram社交搜尋無法如預期般運作的問題。 |

