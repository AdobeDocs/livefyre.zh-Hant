---
description: 建立由Livefyre提供支援的Android應用程式。
seo-description: 建立由Livefyre提供支援的Android應用程式。
seo-title: Android SDK
solution: Experience Manager
title: Android SDK
uuid: 68793fa-9ea1-4890-b36 d-b631 f1 c6 f7 de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Android SDK{#android-sdk}

建立由Livefyre提供支援的Android應用程式。

使用此資料庫將Livefyre服務整合到您的原生Android應用程式中。[Livefyre StreamHub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) 可根據Gradle/Android Studio開發環境，以我們常用的API機制為基礎，提供一個精簡的圖層。

Livefyre也根據此SDK提供 [評論](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) 範例應用程式。

此Livefyre Android SDK可用於Eclipse和Android Studio。

>[!NOTE]
>
>在安裝Livefyre Android SDK之前，您必須在環境中安裝 [Android SDK](https://developer.android.com/sdk/index.html) 。如Android Developer docs>所述，您也必須包含一些額外的Android SDK套件。
>[新增SDK套件](https://developer.android.com/sdk/installing/adding-packages.html)

使用Android SDK Manager(從Android Studio或Eclipse工具列取得)來安裝所有建議的套件。請確定也包含Android支援存放庫。

## Eclipse {#section_dtm_slv_zz}

若要在Eclipse中新增Livefyre Android SDK至您的專案：

1. 從GitHub取得最新 [的StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) 。
1. 從現有專案開始，或建立新專案。
1. 若要將StreamHub-Android-SDK匯入工作區 **[!UICONTROL File > Import > General > Existing Project into Workspace]**，請前往。
1. 瀏覽並選擇StreamHub-Android-SDK；現在應該會顯示在套件總管中。
1. 在專案上按一下滑鼠右鍵，然後選取 **[!UICONTROL Properties,]** 「Android」索引標籤。
1. 在「Library」(資料庫)區段下方，選取 **[!UICONTROL Add button,]** 「StreamHub-Android-SDK(從資料庫清單中選取)」。
1. 按一下 **[!UICONTROL Apply]** 和 **[!UICONTROL OK]**。

## Android Studio {#section_vpw_klv_zz}

若要在Android Studio中新增Livefyre Android SDK至您的專案：

1. 從GitHub取得最新 [的StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK) 。
1. 從現有專案開始，或建立新專案。
1. 在專案上按一下滑鼠右鍵，然後選取 **[!UICONTROL Open Module Settings]**。
1. 選取視窗左上角的 **[!UICONTROL +]** 按鈕。
1. 選取 **[!UICONTROL Import Existing Project.]** (在新版本Android工作室中，您可以找到 **[!UICONTROL Import Existing Project]****[!UICONTROL More Modules]**)。

1. 瀏覽並選擇StreamHub-Android-SDK。

Android Studio可能會要求您將SDK轉換為gradle版本；如果發生這種 **[!UICONTROL next]****[!UICONTROL finish]**情況，請選取。

前往 **專案檔案夾> app檔案夾> build. gradle** 檔案underend相ies以新增下列相依性：

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

請確定下列行位於 **您的專案檔案夾> settings. gradle** 檔案中：

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>您可以自訂Config. java中的設定。

## 客戶 {#section_yfq_blv_zz}

StreamHub Android SDK顯示幾個client類別，可用來請求Livefyre API端點：

* **SocialClient** 交換使用者驗證Token以取得使用者資訊、金鑰和其他中繼資料。

* **BootstraPCLient** 取得關於特定系列的最近內容和中繼資料。

* **StreamClient** 輪詢系列的串流以擷取新的、更新和刪除的內容。

* **WriteClient** 貼文、標幟和贊系列中的內容。

