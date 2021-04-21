---
description: 使用Ping for Pull可讓Livefyre與您的使用者管理系統保持同步。
title: 使用Ping for Pull與Livefyre同步
exl-id: 01b5851d-9dc0-44dc-9c0d-0c467502450d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 使用Ping for Pull{#sync-with-livefyre-using-ping-for-pull}與Livefyre同步

使用Ping for Pull可讓Livefyre與您的使用者管理系統保持同步。

一般而言，只要您的網站／應用程式的使用者更新其設定檔（顯示名稱、頭像等），您就能&#x200B;***Ping*** Livefyre，而Livefyre ***Tellack***&#x200B;則會提取該使用者的更新設定檔。

![](assets/Ping-for-Pull.png)

Ping提取序列：

1. 客戶傳送Ping要求給Livefyre（包括要更新的使用者）。
1. Livefyre確認收到Ping with HTTP 200/Success。
1. Livefyre處理Pull請求。
1. Livefyre佇列Pull請求。
1. Livefyre會執行對端點的「提取」請求，以擷取更新的使用者資訊。
1. 客戶收到拉式回應並驗證。
1. Livefyre會使用納入端點中的外部描述檔資訊來更新遠端描述檔。

每當使用者更新其描述檔資訊時，Ping Livefyre。 雖然Ping for Pull完成時間會視網路負載而異，但會在1到10分鐘內更新使用者資訊。 更新的描述檔變更會先顯示在Livefyre Studio >使用者中。

在發生兩個事件後，更新的描述檔資訊將會出現在您的Livefyre應用程式中：

* 使用者登出，然後再登入應用程式。 userAuthToken中的顯示名稱值優先於Ping for Pull更新。 使用者登出／登入會重新整理Token以更新工作階段。

   若要在更新描述檔資訊時產生新的userAuthToken，請使用SSO authDelegate，在背景再次登出您的使用者。

* 系列的引導程式更新將帶入更新資訊（最多每5-10分鐘）。

要為用戶配置檔案系統實施Ping for Pull，請執行以下操作：

1. [構建拉式端點](#t_build_the_pull_endpoint)。

   >[!NOTE]
   >
   >Livefyre程式庫包含syncUser方法，可讓您的使用者描述檔保持最新狀態。 如果您使用Livefyre程式庫，請略過接下來的兩個步驟。

1. [在Studio中註冊拉入端點](#register_the_endpoint_with_studio)。
1. [建立Ping](#t_build_the_ping)。
1. [建立Ping以提取回應]。(#reference_n3x_pzb_mz)
