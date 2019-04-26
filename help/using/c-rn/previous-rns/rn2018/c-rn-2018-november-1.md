---
description: 2018年11月日發行的發行說明。
seo-description: 2018年11月日發行的發行說明。
seo-title: 2018年11月日
solution: Experience Manager
title: 2018年11月日
uuid: ed1a3bf1-b3 f1-4746-8462-072823ba62
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 2018年11月日{#november}

2018年11月日發行的發行說明。

## 新特性 {#section_syx_mdt_wcb}

此發行版本中發行了下列新功能：

* 視訊智慧標記

   運用Adobe Sensei提供的藝術電腦願景技術，在將視訊內容儲存至資料庫時，自動標記視訊內容。「智慧標記」可協助您更有效地管理UGC，但也能建立超級精確的組織規則(串流)，以根據視訊中的內容收集內容，而不僅是文字，讓您更能協調不想要的內容。

   功能詳細資訊：

   * 智慧標記會自動新增至從Social搜尋、串流和上傳的視訊檔案中所取得的影片中。檢視個別視訊資產詳細資料中的標記
   * 標記. MP4、. MOV和AVI格式中的視訊
   * 標記視訊高達60秒或50MB
   * 兩種智慧標籤類別適用於視訊：功能(動物、物件、地點等)和動作(執行、行走、唱歌等)
   如需詳細資訊，請參閱 [智慧標記](/help/using/c-features-livefyre/c-smart-tags/c-smart-tags.md#c_smart_tags)

* Instagram比率限制

   Instagram已變更任何使用Instagram API(包括Livefyre)的公司，可從每個代號每小時要求到200個要求每個代號要求一小時的要求數。這稱為 *比率限制*。如需詳細資訊，請參閱 [Instagram比率限制](/help/using/c-streams/c-instagram-rate-limiting.md)。

* 程式庫中的音訊檔案

   您現在可以從程式庫面板對音訊檔案執行下列功能：

   * 搜尋
   * 預覽
   * 匯入
   * 依音訊檔案篩選
   * 將檔案拖放至設計人員

## 問題 {#section_ehw_ndt_wcb}

此發行版本中未解決新的問題。請參閱 [上述章節](#c_rn/section_syx_mdt_wcb)。

## UAT版本 {#section_EE91B0C9313E45C5B4CBD59CFBCCFCFE}

下列表格中的問題已在此版本的UAT版本中獲得解決。

| **問題類型** | **元件** | **發行說明** |
|---|---|---|
| 增強功能 | GDPR | 將刪除Analytics中舊客戶的所有資料。 |
| Bug | Library | 已修正上傳至「資料庫」的視訊，然後在資產詳細資料中檢視的問題無法正確顯示的問題。 |
| Bug | Mosaic | 修正Mosaic會將Instagram轉盤中的最後一部分內容顯示為縮圖，而非卡片的問題。 |
| Bug | 社交搜尋 | 已修正Instagram社交搜尋無法如預期運作的問題。 |

