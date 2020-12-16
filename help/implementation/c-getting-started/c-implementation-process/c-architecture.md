---
description: 瞭解Livefyre慣例，以及Livefyre如何組織內容。
seo-description: 瞭解Livefyre慣例，以及Livefyre如何組織內容。
seo-title: 架構
solution: Experience Manager
title: 架構
uuid: 94358e6c-954a-4a52-9bb2-d800b2933130
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---


# 架構{#architecture}

瞭解Livefyre慣例，以及Livefyre如何組織內容。

本節提供Livefyre網路架構的概觀。

## 網路與網站概觀

Livefyre依網路和網站來組織使用者和內容。 每個網路都可能有一個或多個與其相關聯的使用者帳戶，而每個網路可能包含一或多個Livefyre網站。 Livefyre網站是系列的任意群組。 一個系列會對應至CMS中的一個文章ID。

## 瞭解網路{#section_hqt_4m4_xz}

擁有多個網域的客戶可以使用單一Livefyre網路，在所有網域中共用使用者帳戶。 想要為不同網域保留個別使用者帳戶的客戶，需要個別的Livefyre網路。

組態設定可套用至網站、網路和系列（在上圖中稱為對話）。

>[!NOTE]
>
>有些設定僅適用於網路層級（例如電子郵件通知偏好設定、地址寄送電子郵件，以及電子郵件自訂標誌）。 如果您希望這些設定在每個網域中不同，則必須使用多個網路。

## 瞭解網站{#section_vjw_nm4_xz}

網站是文章的任意群組。 群組可讓您指派不同的協調者給不同的內容群組，因此很實用。 協調者和擁有者可設定為協調內容，並在網路或網站層級設定管理設定。 如果您希望某些協調者只看到某些系列，這些系列可能會設為個別的Livefyre網站。

>[!NOTE]
>
>您在自訂網路下可能擁有的網站數量沒有限制。

## 應用程式順序圖{#section_mw2_lm4_xz}

不論您是想要使用Livefyre提供的端點來建置自訂功能，或只是需要除錯問題，這都有助於瞭解Livefyre應用程式請求／回應流程的運作方式。

![](assets/appsequencediagram.png)

1. 當您的客戶點擊您的網站時，使用網站ID和文章ID實例化Livefyre應用程式。
1. 如果您想要驗證使用者（對於流量評估以及網站保護而言非常有用），請傳送Livefyre網站資訊和使用者設定檔Token。
1. 傳送Livefyre網站ID和文章ID以初始化應用程式。

   Livefyre會傳回初始內容。

   將此內容傳送至頁面，並顯示應用程式。

1. 若要更新頁面上顯示的內容，請從您的頁面傳送最新的事件ID給Livefyre。 如果有新內容可用，則會傳回它。

   使用新內容重新載入頁面，並無限期重複此程式。

1. 如果您允許使用者張貼新內容，則會在網站上張貼新內容時觸發事件，以便將內容張貼至Livefyre。 Livefyre將會傳回更新的串流，您可以用它來更新網站。
