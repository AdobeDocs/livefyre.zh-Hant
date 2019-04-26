---
description: 瞭解Livefyre慣例以及Livefyre如何組織內容。
seo-description: 瞭解Livefyre慣例以及Livefyre如何組織內容。
seo-title: 架構
solution: Experience Manager
title: 架構
uuid: 94358e6c-954a-5a52-9bb2-d800 b2933130
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 架構{#architecture}

瞭解Livefyre慣例以及Livefyre如何組織內容。

本節提供Livefyre網路架構的概述。

## 網路與網站概觀

Livefyre透過網路和網站組織使用者和內容。每個網路都可能有一或多個使用者帳戶，而每個網路可能包含一或多個Livefyre網站。Livefyre網站是任意群組的集合。一個系列會對應至您CMS中的一個文章ID。

## 瞭解網路 {#section_hqt_4m4_xz}

具有多個網域的客戶可以使用單一Livefyre網路跨所有網域共用使用者帳戶。想要將不同的使用者帳戶保持為不同網域的客戶，需要個別的Livefyre網路。

組態設定可套用至網站、網路和系列(在上圖中稱為對話)。

>[!NOTE]
>
>有些設定僅適用於網路層級(例如電子郵件通知偏好設定、來自地址的電子郵件，以及電子郵件自訂標誌)。如果您希望這些設定不同於每個網域，您必須使用多個網路。

## 瞭解網站 {#section_vjw_nm4_xz}

網站是任意群組的文章。此群組非常有用，因為它可讓您指派不同的協調者至不同的內容群組。可設定協調者和擁有者來協調內容，並設定網路或網站層級的管理設定。如果您希望某些協調者只看得到某些系列，這些系列可能會設定為獨立的Livefyre網站。

>[!NOTE]
>
>您在自訂網路下可能擁有的網站數量沒有限制。

## 應用程式順序圖表 {#section_mw2_lm4_xz}

無論您想要使用Livefyre提供的端點實作自訂函數，還是只需除錯問題，Livefyre應用程式要求/回應流程的運作方式都有幫助。

![](assets/appsequencediagram.png)

1. 當您的客戶進入您的網站時，請將Livefyre應用程式與網站ID和文章ID實例化。
1. 如果您想要驗證使用者(用於流量評估以及網站保護)，請傳送Livefyre網站資訊和使用者描述檔Token。
1. 傳送Livefyre網站ID和文章ID以初始化應用程式。

   Livefyre會傳回初始內容。

   將此內容傳送至頁面，然後顯示應用程式。

1. 若要更新頁面上顯示的內容，請從您的頁面傳送Livefyre最新的事件ID。如果有任何新內容可供使用，將會傳回。

   使用新內容重新載入頁面，並無限期重復程序。

1. 如果您允許使用者張貼新內容，則會在網站上張貼新內容時觸發事件，將內容張貼至Livefyre。Livefyre會傳回更新的串流，您可用來更新您的網站。
