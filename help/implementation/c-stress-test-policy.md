---
description: 對Livefyre平台執行壓力測試。
title: 壓力測試政策
exl-id: cb87b6ca-4107-46fc-9b1e-dc9399ec6d3a
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# 壓力測試政策{#stress-test-policy}

對Livefyre平台執行壓力測試。

本檔案提供針對Livefyre平台執行壓力測試的指引。 嚴禁客戶在未通知的情況下進行臨機測試。 關於[禁止和允許的活動](#c_stress_test_policy/section_mhs_bfz_vdb)的更多資訊。

>[!NOTE]
>
>壓力測試是選用的。 您無需執行壓力測試，也無需執行壓力測試。 AdobeLivefyre會定期進行壓力測試和驗證，做為發佈程式的一部分。 如果您選擇運行測試，本文檔將概述進行壓力測試的要求和約束。

## 通知 {#section_ihs_bfz_vdb}

您必須在您計劃開始的三週或更久之前，通知您的Livefyre客戶成功專員和Adobe技術顧問有關您計畫的測試。

若要通知Livefyre，請提交下列資訊給您的Livefyre客戶成功專員和Adobe技術顧問：

* 測試的目的和說明
* 您測試的使用案例
* 您計畫在測試中使用的任何Livefyre API清單
* 測試日期、時間和持續時間
* 啟動測試的IP位址

## 要求 {#section_khs_bfz_vdb}

您只能在測試符合下列要求時執行：

* 在開始測試之前，您必須先從Adobe技術顧問獲得明確的書面批准3週以上。
* **您只能對UAT網路執行測試。**
* 您必須針對真實的情境進行測試。 例如，您不得假設您的屬性每天會為&#x200B;*millyns*&#x200B;貼文要求提供服務，因為這並非現實情形。 如果您需要協助來判斷您的藍本是否真實，請洽詢您的Livefyre客戶成功專員或Adobe技術顧問。
* 測試應在太平洋標準時區\(UTC -7\)的工作時間內進行。
* 您可能需要製作測試的資料和推理。

## 治理{#section_mhs_bfz_vdb}

如果您執行下列測試，Livefyre保留隨時終止測試的權利：

* 在生產網路上。
* 未經Adobe技術顧問事先三週或三週以上的明確書面許可。
* 面對不真實的場景。

Livefyre會封鎖對API的存取、停用Livefyre網路，以及拒絕不符合要求的載入測試要求，以終止測試。
