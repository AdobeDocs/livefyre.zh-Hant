---
description: 用來為您網站上的Livefyre提供動力的核心Livefyre程式庫。
seo-description: 用來為您網站上的Livefyre提供動力的核心Livefyre程式庫。
seo-title: Livefyre.js
solution: Experience Manager
title: Livefyre.js
uuid: 7b3eca57-d5e8-416d-badf-a9c51d10dadd
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---


# Livefyre.js {#livefyre-js}

用來為您網站上的Livefyre提供動力的核心Livefyre程式庫。

`Livefyre.js` 是核心程式庫，您可以安裝在每個啟用Livefyre的網頁上。它定義全域`window.Livefyre`物件和單一公用方法`Livefyre.require`，可用來載入其他Livefyre JavaScript程式庫，以協助[內嵌Livefyre應用程式](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)、[整合驗證提供者與Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md)等。

## 新增至您的網站{#section_cst_twg_xz}

將下列`<script>`標籤新增至您的網頁或網站範本。 如果可能，請將它新增至HTML檔案的`<head>`區段，以便快速載入。

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>此指令碼將內嵌一個稱為Livefyre.js偵測器的很小(~1 Kb)檔案，隨後會透過您的網頁存取通訊協定（HTTP或HTTPS）載入最新版的Livefyre.js。

## Livefyre.require {#section_ipq_hwg_xz}

`Livefyre.require` 是自訂的JavaScript模組載入器， [例如curl.](https://github.com/cujojs/curl) jsor  [RequireJS](https://requirejs.org/)。它可用來載入Livefyre發佈的大部分套件，並提供方便且直覺的整合路徑。

可通過`Livefyre.require`訪問的包使用[語義版本控制](https://semver.org/)版本控制。 特定版本或一系列版本都需要套件，讓您的網頁可自動受益於新的錯誤修正功能。 這可讓您在網站上整合Livefyre時有彈性。 版本釘選有三個層級，可搭配`Livefyre.require`使用。

* **package-name#1:** 釘到主要版本v1。您將會取得所有可維持回溯相容API的新更新。 請釘選主要版本，以接收該版本的錯誤修正和次要功能增強。
* **package-name#1.1：將** Pin釘到次要版本v1.1。您會取得此次次要版本的所有錯誤修正。如果套件的預設行為或功能範圍發生變更，可能導致網頁上出現新的意外行為，Livefyre工程將一律會加入次要版本的套件。 如果您想要收到自動錯誤修正，但沒有其他功能或預設行為變更，請釘選次要版本。
* **package-name#1.1.1：針** 對修補程式1.1.1版。即使有錯誤修正，此內嵌的行為也不會變更。如果您的網站有大量CSS自訂設定，且這些設定依賴可能變更的封裝標籤結構，或者您有其他理由希望您執行的Livefyre版本不會有任何變更，請釘選修補程式版本。

使用`Livefyre.require`的範例整合可能如下所示：

```
<!-- First add Livefyre.js to the page --> 
<script src="https://cdn.livefyre.com/Livefyre.js"></script> 
  
<!-- Then load up all the desired Livefyre packages and Do Stuff in the callback --> 
<script> 
Livefyre.require([ 
    'lfawesome#1', 
    'lfsuperawesome#2.1.2' 
], function (LFAwesome, LFSuperAwesome) { 
    var greatness = new LFAwesome(); 
    // etc.. 
}); 
</script>
```

## 可用包{#section_ygd_dwg_xz}

想知道哪些Livefyre JavaScript套件可透過`Livefyre.require`取得？ 您隨時可以在這裡找到支援套件及其最新版本的最新清單：[packages.html](https://cdn.livefyre.com/packages.html)。

## 測試軟體包的搶鮮版{#section_pgm_dpg_xz}

有時，您可能會想要測試即將推出的Livefyre套件版本，以確定它可在您的網站上運作，或接受測試您要求開發的功能。 除了包含「語義版本」範圍外，還可以指定搶鮮版UAT環境。

例如，以下需要`fyre.conv`的UAT版本、「注釋」、「即時部落格」和「聊天」應用程式。

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
