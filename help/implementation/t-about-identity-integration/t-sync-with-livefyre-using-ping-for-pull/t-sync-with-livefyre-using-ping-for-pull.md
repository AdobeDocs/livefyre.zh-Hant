---
description: 使用Ping for Draw可讓Livefyre與您的使用者管理系統同步。
seo-description: 使用Ping for Draw可讓Livefyre與您的使用者管理系統同步。
seo-title: 與Livefyre同步，以用於提取
solution: Experience Manager
title: 與Livefyre同步，以用於提取
uuid: 7b 059064-cca-46d7-8055-dfe59 f493 ac1
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# 與Livefyre同步，以用於提取{#sync-with-livefyre-using-ping-for-pull}

使用Ping for Draw可讓Livefyre與您的使用者管理系統同步。

一般來說， ***您只要在*** 網站/應用程式的使用者更新其描述檔(顯示名稱、頭像等)，然後Livefyre ***提取*** 該使用者的更新描述檔時，就會對您進行Ping Livefyre。

![](assets/Ping-for-Pull.png)

針對提取順序進行Ping：

1. 客戶將Ping要求傳送至Livefyre(包括要更新的使用者)。
1. Livefyre確認接收到HTTP200/成功的Ping。
1. Livefyre處理提取請求。
1. Livefyre佇列提取請求。
1. Livefyre會執行提取請求至端點，以擷取更新的使用者資訊。
1. 客戶接收提取回應並驗證。
1. Livefyre會使用提取端點中包含的外部描述檔資訊更新遠端描述檔。

每當使用者更新其描述檔資訊時，Ping Livefyre就會出現。雖然Ping的提取完成時間視網路負載而定，但會在到10分鐘內更新使用者資訊。更新的描述檔變更將會先顯示在Livefyre Studio>使用者中。

更新的描述檔資訊會在兩個事件之後出現在Livefyre應用程式中：

* 使用者登出，然後登入應用程式。在userAuthToken中顯示名稱值優先於Ping for Drag更新。使用者登出/登入會重新整理Token，以更新工作階段。

   若要在更新描述檔資訊時產生新的userAuthToken，請使用SSO AuthDelegate將使用者登出，然後再次在背景中登入。

* 系列更新將會提供更新資訊(每5-10分鐘)。

若要針對您的使用者描述檔系統實施Ping for Drag：

1. [建立提取端點](#t_build_the_pull_endpoint)。

   >[!NOTE]
   >
   >Livefyre程式庫包含同步使用者設定檔的同步使用者設定檔。如果您使用Livefyre程式庫，請略過接下來的兩個步驟。

1. [在Studio中註冊提取端點](#register_the_endpoint_with_studio)。
1. [建立Ping](#t_build_the_ping)。
1. [建立用於提取回應]的Ping。(# reference_ n3 x_ pzb_ mz)
