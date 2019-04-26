---
description: 用來提升網站上Livefyre能力的核心Livefyre庫。
seo-description: 用來提升網站上Livefyre能力的核心Livefyre庫。
seo-title: Livefyre. js
solution: Experience Manager
title: Livefyre. js
uuid: 7b3a57-d5 e8-416d-badf-a9 c51 d10 dd
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Livefyre. js {#livefyre-js}

用來提升網站上Livefyre能力的核心Livefyre庫。

`Livefyre.js` 是您可在每個啓用Livefyre網頁上安裝的核心程式庫。它定義全域 `window.Livefyre` 物件和單一公開方法， `Livefyre.require`可用來載入其他Livefyre JavaScript程式庫，以協助 [內嵌Livefyre應用程式](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)、 [整合驗證提供者與Livefyre](/help/implementation/t-about-identity-integration/t-about-identity-integration.md) 等。

## 新增至您的網站 {#section_cst_twg_xz}

將下列 `<script>` 標記新增至您的網頁或網站範本。如果可行，請將它新增至HTML文件 `<head>` 的區段，以便快速載入。

```
<script src="//cdn.livefyre.com/Livefyre.js"></script>
```

>[!NOTE]
>
>此指令碼會內嵌一個非常小的(~1KB)檔案，稱為Livefyre. js scout，隨後將會載入最新版Livefyre. js，並透過該通訊協定存取您的網頁(HTTP或HTTPS)。

## Livefyre需求 {#section_ipq_hwg_xz}

`Livefyre.require` 是自訂JavaScript模組載入器，例如 [currll. js](https://github.com/cujojs/curl) 或 [必要JS](https://requirejs.org/).它可用來載入Livefyre發佈的大部分套件，並提供方便直覺式的整合路徑。

透過 `Livefyre.require`[「語義版本修訂](https://semver.org/)」來序列化可存取的封裝。套件可以在特定版本或各版本的版本中使用，因此您的網頁可以自動受益於新的錯誤修正功能。這可讓您在整合網站上的Livefyre時彈性。您可使用三種版本的版本釘選 `Livefyre.require`。

* **package-name#1：** 釘選至主要版本v1。您將取得所有維護向後相容API的新更新。釘選至主要版本，以收到該版本的錯誤修正和次要功能增強功能。
* **package-name#1.1：** 釘到次要版本v1.1。您將會收到這個次要版本的所有錯誤。如果您的預設行為或功能範圍變更的方式可能造成網頁上新的非預期行為，Livefyre Engineering永遠會撞上次要版本的套裝。如果您想要接收自動錯誤修正，但沒有其他功能或變更預設行為，請釘選至次要版本。
* **package-name1.1.1：** 釘選以修補版本v1.1.1。即使有錯誤修正，此內嵌的行為永遠不會改變。如果您的網站有廣泛的CSS自訂功能，而您的網站會視套件的標記結構而定，或您有其他理由偏好您執行的Livefyre版本不會改變，則請釘選至修補版本。

使用的範例整合 `Livefyre.require` 如下：

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

## 可用套件 {#section_ygd_dwg_xz}

請注意，哪些Livefyre JavaScript套件可供 `Livefyre.require`使用？您隨時可以在這裡找到最新的支援套件清單及其最新版本： [packages.html](https://cdn.livefyre.com/packages.html)。

## 測試套件的測試發行版本 {#section_pgm_dpg_xz}

有時您可能會想要測試即將推出的Livefyre套件版本，以確定它能在您的網站上運作，或測試正在依您要求開發的功能。除了包含「語義版本」範圍外，也可以指定預先發佈UAT環境。

例如，下列需要UAT版本 `fyre.conv`、留言、即時部落格和聊天應用程式。

```
Livefyre.require(['fyre.conv#uat'], callback); 
```
