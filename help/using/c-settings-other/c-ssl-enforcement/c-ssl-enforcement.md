---
description: 'null'
seo-description: 'null'
seo-title: SSL強制
solution: Experience Manager
title: SSL強制
uuid: e64af8c2-3ab6-4034-b385-0e552d828c6e
translation-type: tm+mt
source-git-commit: 7dc3ac6725a27460cecfa6051549da85370ca053

---


# SSL強制{#ssl-enforcement}

為確保您的資料保持安全，我們淘汰HTTP，轉而採用HTTPS。 Adobe Livefyre將於2018年8月底之前完全停用所有HTTP和不安全的SSL/TLS密碼。 此Adobe Standard旨在保護您和您使用者的隱私權。

## 誰受影響？ {#section_jf2_4yz_kcb}

這可能會影響Livefyre客戶，他們已：

* 從其CRM、CMS、WordPress或其他用戶端進行伺服器對伺服器呼叫。
* 行動整合（Android和iOS應用程式）
* 自訂應用程式或自訂程式碼

## 我需要做什麼？{#section_unv_dc5_kcb}

1. 所有Livefyre客戶必須透過HTTPS與所有API通訊，以處理所有流量，包括：

   * 伺服器與伺服器的整合（CRM、CMS、WordPress等）
   * 行動整合（Android和iOS應用程式）
   * 自訂應用程式（串流集線器SDK或直接編碼）。

1. 伺服器對伺服器和行動HTTP用戶端必須支援TLS 1.2
1. 將主機名從更 `{*}.<network>.fyre.co` 改為 `<network>.{*}.fyre.co`。 例如，主機名 `example.network.fyre.co` 稱變 `network.`更為example.fyre.co"。 例如:

   * `bootstrap.<network_name>.fyre.co` 變更為 `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` 變更為 `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` 變更為 `<network_name>.admin.fyre.co`

## 我要如何得知我是否做了變更？ {#section_sqk_5d5_kcb}

您可能已使用HTTPS，但Livefyre建議您重複檢查，尤其是：

* 從CMS或CRM進行伺服器對伺服器呼叫。
* 在Javascript或Mobile中自訂應用程式的自訂程式碼或使用SDK。
* 如果您的整合已推出一年以上。
* 如果您堆疊中的技術超過一年。

即使您已使用HTTPS，您也必須確認您的API用戶端支援TLS 1.2。

## 如何驗證我的API用戶端是否支援TLS 1.2? {#section_nd1_j25_kcb}

負責網站開發的人員可以：

* 識別客戶端軟體。
* 識別版本。
* 閱讀檔案以確保API用戶端支援TLS 1.2。
* 視需要開啟除錯模式。

## TLS 1.2的Java支援 {#section_lwn_rwk_ycb}

針對Java 8和更新版本的Oracle和OpenJDK JVM，依預設會針對所有SSL連線使用TLS 1.2。 如果您使用Java 8或更新版本，則不需要採取任何其他動作。

使用Java 7或更舊版本的使用者應查閱公開檔案，瞭解如何啟用TLS 1.2。

## 我為何需要變更主機名稱？ {#section_d5q_p25_kcb}

Livefyre在網域上沒有SSL憑 `{*}.<network>.fyre.co` 證。 只要將URL變更為HTTPS，就會中斷應用程式。

## 我是否必須升級至最新版的Livefyre SDK? {#section_dw5_s25_kcb}

不會。您可以改用修補程式碼。 若要修補程式碼，請修改部分靜態字串並重建程式碼。 如果您的HTTP用戶端已過時，您也需要升級該用戶端，或使用其他用戶端。

## 要多久？ {#section_lgd_v25_kcb}

這所花費的時間長度取決於您的設定。 如果您有簡單的實作，則確認時間應該很少。 如果您有許多自訂項目，您將需要測試並部署更新的程式碼至您的伺服器，或是新的「應用程式至App Store」。 為獲得最佳效果，我們建議您對工作進行初始審核，以便您能規劃任何長期工作。

## 完成此工作的時間表是什麼？ {#section_kgk_w25_kcb}

Livefyre將於2018年8月底停用服務的連接埠80(HTTP)，並僅支援443(HTTPS)連線。 嘗試使用HTTP的瀏覽器和其他用戶端將會失敗。

## 我何時需要完成這項工作？ {#section_rvb_x25_kcb}

所有客戶必須在2018年7月底前使用HTTPS。 如果您無法達到此期限，請聯絡我們的團隊，來信請寄至prioritysupport@livefyre.com。
