---
description: null
seo-description: null
seo-title: SSL執行
solution: Experience Manager
title: SSL執行
uuid: e64af8c2-3ab6-4034-b385-1e552 d828 c6 e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# SSL執行{#ssl-enforcement}

為確保資料安全無虞，我們淘汰HTTP以取代HTTPS。在2018年月底之前，Adobe Livefyre將會完全停用所有HTTP和不安全的SSL/TLS加密。此Adobe Standard是專為保護您和您的使用者隱私而設計的Adobe Standard。

## 誰受到影響？ {#section_jf2_4yz_kcb}

這可能會影響Livefyre的客戶：

* 從CRM、CMS、WordPress或其他用戶端呼叫伺服器呼叫。
* 行動整合(Android和iOS應用程式)
* 自訂應用程式或自訂程式碼

## 我需要做甚麼？ {#section_unv_dc5_kcb}

1. 所有Livefyre客戶都必須透過HTTPS與所有的API通訊，包括：

   * 伺服器至伺服器整合(CRM、CMS、WordPress等)
   * 行動整合(Android和iOS應用程式)
   * 自訂應用程式(StreamHub SDK或直接編碼)。

1. 伺服器至伺服器和行動HTTP用戶端必須支援TLS1.2
1. Change hostnames from `{*}.<network>.fyre.co` to `<network>.{*}.fyre.co`. 例如，主機名稱 `example.network.fyre.co` 變更 `network.`為範例. fyre. co」。例如：

   * `bootstrap.<network_name>.fyre.co` to `<network_name>.bootstrap.fyre.co`

   * `quill.<network_name>.fyre.co` to `<network_name>.quill.fyre.co`

   * `admin.<network_name>.fyre.co` to `<network_name>.admin.fyre.co`

## 我要如何知道我是否做了變更？ {#section_sqk_5d5_kcb}

您可能已使用HTTPS，但Livefyre建議您再次檢查，尤其是當您有下列情況時：

* 從您的CMS或CRM呼叫伺服器呼叫。
* 自訂程式碼，或使用Javascript或Mobile中自訂應用程式的SDK。
* 如果您的整合超過一年。
* 如果堆疊中的技術早於一年。

即使您已使用HTTPS，您也必須確認您的API用戶端是否支援TLS1.2。

## 我要如何驗證我的API用戶端是否支援TLS1.2？ {#section_nd1_j25_kcb}

負責開發網站的人員可以：

* 識別用戶端軟體。
* 識別版本。
* 閱讀文件以確保API用戶端支援TLS1.2。
* 視需要開啓除錯模式。

## Java支援TLS1.2 {#section_lwn_rwk_ycb}

Java和更新版本的Oracle和OpenJDK JVM已設定為依預設針對所有SSL連線使用TLS1.2。如果您使用Java或更新版本，則無須採取任何額外動作。

Java或更早版本的使用者應參閱有關如何啓用TLS1.2的公開文件。

## 我為何需要變更主機名稱？ {#section_d5q_p25_kcb}

Livefyre `{*}.<network>.fyre.co` 在網域上沒有SSL憑證。只要將URL變更為HTTPS，就會中斷應用程式。

## 我是否必須升級至最新版的Livefyre SDK？ {#section_dw5_s25_kcb}

不行。您可以改為修補程式碼。若要修補程式碼，請修改一些靜態字串並重建程式碼。如果您的HTTP用戶端過期，您將需要升級，或使用不同的HTTP用戶端。

## 這需要多久時間？ {#section_lgd_v25_kcb}

此時間長度取決於您的設定。如果您有簡單實作，應該花少許時間確認。如果您有許多自訂項目，您將需要測試並部署更新的程式碼至您的伺服器或新的應用程式至App Store。為獲得最佳結果，建議您初始審核作品，讓您可以規劃任何期限的工作。

## 完成此工作的時間軸為何？ {#section_kgk_w25_kcb}

Livefyre將在2018年月底之前停用連接埠80(HTTP)，僅支援連線至443(HTTPS)。嘗試使用HTTP的瀏覽器和其他客戶將會失敗。

## 我何時需要完成這項工作？ {#section_rvb_x25_kcb}

所有客戶必須在2018年月底之前使用HTTPS。如果您無法趕上此期限，請與我們的團隊聯絡，來信請寄至prioritysupport@livefyre.com。
