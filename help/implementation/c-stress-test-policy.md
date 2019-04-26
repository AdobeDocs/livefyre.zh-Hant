---
description: 對Livefyre平台執行壓力測試。
seo-description: 對Livefyre平台執行壓力測試。
seo-title: 壓力測試政策
solution: Experience Manager
title: 壓力測試政策
uuid: f2d49b55-f4 fc-485f-9aea-a17 ce64813 ee
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 壓力測試政策{#stress-test-policy}

對Livefyre平台執行壓力測試。

本文件提供對Livefyre平台執行壓力測試的指引。嚴禁未經通知的客戶進行臨機測試。詳細瞭解 [禁止和允許的活動](#c_stress_test_policy/section_mhs_bfz_vdb)。

>[!NOTE]
>
>壓力測試是選擇性的。您不需要或預期執行壓力測試。Adobe Livefyre會在發行過程中進行定期壓力測試和驗證。如果您選擇執行測試，此文件將說明執行壓力測試的需求和限制。

## 通知 {#section_ihs_bfz_vdb}

在計劃開始之前，您必須先通知Livefyre客戶成功專家和Adobe技術顧問三周以上計劃的測試。

若要通知Livefyre，請向Livefyre客戶成功專員和Adobe技術顧問提交下列資訊：

* 測試用途與說明
* 您要測試的使用案例
* 您打算在測試中使用的任何Livefyre API清單
* 測試日期、時間和時間長度
* 您將啓動測試的IP位址

## 需求 {#section_khs_bfz_vdb}

您只能在符合下列需求時執行測試：

* 您必須先收到Adobe技術顧問的明確書面核准，才能開始測試。
* **您只能在UAT網路上執行測試。**
* 您必須測試實際案例。例如，您不會假設您的屬性每天都能提供 *數百萬* 個貼文請求，因為這不是實際情況。如果您需要協助判斷藍本是否真實，請洽詢您的Livefyre客戶成功專員或Adobe技術顧問。
* 測試應在太平洋標準時區\(UTC-7\)的營業時間進行。
* 您可能需要製作資料以及測試的推理。

## 治理 {#section_mhs_bfz_vdb}

Livefyre保留在執行測試時隨時終止測試的權利：

* 在生產網路上。
* 若未事先明確向Adobe技術顧問提出明確的書面核准，則會提前三周或更久。
* 解決非真實案例。

Livefyre會封鎖對API的存取、停用Livefyre Networks，並在不符合要求的情況下進行負載測試請求，以終止測試。
