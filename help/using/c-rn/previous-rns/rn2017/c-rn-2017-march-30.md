---
description: 2017年3月30日發行說明。
title: 2017 年 3 月 30 日
exl-id: 44c73ff9-8bc1-49c9-b720-aff425e5cd28
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 6%

---

# 2017 年 3 月 30 日{#march}

2017年3月30日發行說明。

## 生產版本

| 問題類型 | 元件 | 發行說明 |
|---|---|---|
| 錯誤 | 社交搜尋 | 修正Social搜尋中已儲存的Youtube資產無法發佈的錯誤。 |
| 增強功能 | 社交同步 | 已過時的Twitter社交同步。 |
| 增強功能 | Storify 2 | 已新增增強功能，在找不到任何結果時，在「Facebook主題」搜尋中顯示「找不到結果」訊息。 |
| 增強功能 | 串流 | 已將SAFE規則的摘要規則新增至「Twitter串流」頁面的底部。 |
| 錯誤 | 串流 | 已新增增強功能，在提供已排除的作者時，在「Twitter串流規則」上以可見方式停用「已驗證的使用者」核取方塊。 |
| 錯誤 | 串流 | 修正允許在Twitter規則中使用ANDing關鍵字和位置篩選器的錯誤。 |
| 錯誤 | Studio | 修正套用「功能標籤」時無法正確儲存的錯誤。 |

## UAT發行

| 問題類型 | 元件 | 發行說明 |
|---|---|---|
| 錯誤 | 應用程式內容 | 已變更「更多資訊」的行為，如此一來，如果指定內容上有多個匿名標幟事件，則一律會顯示最早的事件。 |
| 錯誤 | 庫 | 修正「資料庫」使用主題標籤搜尋時斷時續失敗的錯誤。 |
| 錯誤 | 地圖 | 已修正「地圖」中支援iOS裝置叢集中大量內容的錯誤。 |
| 增強功能 | 馬賽克 | 新增功能：設定Mosaic應用程式以按一下內容卡上的任意位置，以在設計人員中依動畫類型`none`開啟模式，若透過SDK實例化則依`cardAnimation: 'off'`開啟模式。 |
| 錯誤 | 馬賽克 | 已修正讓使用者在Designer中成功變更Mosaic應用程式的錯誤。 |
| 增強功能 | 權限請求 | 新增稱為「請求失敗」的新權限請求狀態，以在權限請求訊息無法傳送時反白顯示。 |
| 增強功能 | 設定 | 新增客戶在「設定」中建立垃圾訊息協調規則的能力。 |
| 增強功能 | 社交搜尋 | 修正VK.com貼文無法透過URL Social搜尋顯示的錯誤。 |
| 增強功能 | 社交搜尋 | 從Studio搜尋Instagram內容時，如果搜尋是因為過期的InstagramAPI Token，現在會顯示錯誤訊息。 |
| 錯誤 | 串流 | 修正「應用程式不接受新內容」橫幅錯誤顯示在「串流規則」頁面上的錯誤。 |
| 增強功能 | 串流 | 已將新建立的串流規則的預設值修改為「套用安全規則」（如果適用）。 |
| 增強功能 | 串流（先前稱為組織規則） | 已從「Twitter串流／組織」規則移除「葡萄樹」唯一選項，因為「葡萄樹」現在會顯示為Twitter影片。 |
| 錯誤 | Studio Shell | 已修正錯誤，如此當https://明確附加在URL之前時，Livefyre Studio就會載入。 |
