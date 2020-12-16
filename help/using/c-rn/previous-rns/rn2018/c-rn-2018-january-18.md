---
description: 2018年1月18日發行說明。
seo-description: 2018年1月18日發行說明。
seo-title: 2018 年 1 月 18 日
solution: Experience Manager
title: 2018 年 1 月 18 日
uuid: 8141f431-c154-4c8f-bbcd-b7c712fe5f7d
translation-type: tm+mt
source-git-commit: 35feb87bb82d1f298496717a65f1972cf4e71104
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 8%

---


# 2018 年 1 月 18 日{#january}

2018年1月18日發行說明。

## 生產版本

| **問題類型** | **元件** | **發行說明** |
|---|---|---|
| 錯誤 | 應用程式 | 修正使用jpeg檔案時，無法正確呈現Avatar的錯誤。 |
| 錯誤 | ModQ | 修正S1客戶允許依ModQ中的「系列」篩選的錯誤。 |
| 錯誤 | 串流 | 已修正當語言篩選器設為「無」時，串流規則中斷的錯誤。 |
| 錯誤 | 串流 | 已修正無法儲存Youtube串流規則的錯誤。 |
| 錯誤 | 串流 | 修正使用者在串流規則中建立格式錯誤的地理項目並儲存這些項目的錯誤，這會導致串流失敗。 現在，使用者無法再儲存格式不良的地理標籤。 |
| 錯誤 | Studio | 修正部分使用者無法登入Livefyre的問題。 |

## UAT發行

| **問題類型** | **元件** | **發行說明** |
|---|---|---|
| 錯誤 | 庫 | 安全性錯誤修正。 現在，所有驗證呼叫都是使用HTTPS通訊協定，而非HTTP進行。 |
| 增強功能 | 智慧標籤 | 串流內容現在會自動由Adobe Sensei標籤為智慧型，因為它會儲存至資料夾或發佈至應用程式。 |
| 錯誤 | 串流 | 修正Instagram串流規則無法識別日文字元的問題。 |
| 增強功能 | 串流 | 客戶現在可以使用邏輯運算子(ANY、ALL、NOT)，在串流中建立詳細的智慧標籤篩選，以組織更精確的內容。 例如，如果我使用#himalyas主題標籤，我可以選擇只顯示包含&quot;snowy&quot; &quot;mountains&quot;的影像。 |
| 錯誤 | Studio | 修正名稱中顯示特殊字元為HTML的錯誤。 |

