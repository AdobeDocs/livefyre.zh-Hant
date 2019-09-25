---
description: 建立採用Livefyre架構的Android應用程式。
seo-description: 建立採用Livefyre架構的Android應用程式。
seo-title: Android SDK
solution: Experience Manager
title: Android SDK
uuid: 68793fa9-3ea1-4890-b36d-b631f1c6f7de
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Android SDK{#android-sdk}

建立採用Livefyre架構的Android應用程式。

使用此程式庫，將Livefyre服務整合至您的原生Android應用程式。 Livefyre [StreamHub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK) ，以Gradle/Android studio開發環境為基礎，針對我們常用的API機制提供精簡的層。

Livefyre也提供以此SDK [為基礎的](https://github.com/Livefyre/StreamHub-iOS-Reviews-App) 「評論」範例應用程式。

此Livefyre Android SDK可同時用於Eclipse和Android Studio。

>[!NOTE]
>
>在安裝Livefyre Android SDK之前，您必須先在您的 [環境中安裝Android SDK](https://developer.android.com/sdk/index.html) 。 您也必須包含一些額外的Android SDK套件，如「Android開發人員檔案&gt;」所述。
>[新增SDK套件](https://developer.android.com/sdk/installing/adding-packages.html)

使用Android SDK Manager（可從Android studio或Eclipse工具列取得）來安裝所有建議的套件。 Be certain to also include the Android Support Repository.

## Eclipse {#section_dtm_slv_zz}

若要在Eclipse中將Livefyre Android SDK新增至您的專案：

1. 從GitHub取得 [最新的StreamHub-Android](https://github.com/Livefyre/StreamHub-Android-SDK) -SDK。
1. 從現有專案開始或建立新專案。
1. 若要將StreamHub-Android-SDK匯入您的工作區，請至 **[!UICONTROL File > Import > General > Existing Project into Workspace]**。
1. 瀏覽並選取StreamHub-Android-SDK;它現在應該會顯示在套件檔案總管中。
1. 在專案上按一下滑鼠右鍵，然後選 **[!UICONTROL Properties,]** 取「Android」標籤。
1. 在「程式庫」區段下，選 **[!UICONTROL Add button,]** 取「程式庫」清單中的「StreamHub-Android-SDK」。
1. 按一下 **[!UICONTROL Apply]** 和 **[!UICONTROL OK]**。

## Android Studio {#section_vpw_klv_zz}

若要將Livefyre Android SDK新增至Android studio的專案：

1. 從GitHub取得 [最新的StreamHub-Android](https://github.com/Livefyre/StreamHub-Android-SDK) -SDK。
1. 從現有專案開始或建立新專案。
1. 在您的專案上按一下滑鼠右鍵，然後選取 **[!UICONTROL Open Module Settings]**。
1. 選擇 **[!UICONTROL +]** 窗口左上角的按鈕。
1. 選 **[!UICONTROL Import Existing Project.]** 取(在新版Android Studio中，您可在下 **[!UICONTROL Import Existing Project]** 方找 **[!UICONTROL More Modules]**&#x200B;到)。

1. 瀏覽並選取StreamHub-Android-SDK。

Android studio可能會要求您將SDK轉換為Gradle版本；如果發生此情況，請選 **[!UICONTROL next]** 擇 **[!UICONTROL finish]**。

移至相 **依項下的專案資料夾&gt;應用程式資料夾&gt; build.gradle** 檔案，以新增下列相依項：

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

請確定下列行位於您的專 **案資料夾&gt; settings.gradle** 檔案中：

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>您可以從Config.java中自訂設定。

## 客戶 {#section_yfq_blv_zz}

StreamHub Android SDK公開數個可用來要求Livefyre API端點的用戶端類別：

* **AdminClient** 針對使用者資訊、金鑰和其他中繼資料交換使用者驗證Token。

* **BootstrapClient** 取得特定系列的最新內容和中繼資料。

* **StreamClient** 輪詢系列的串流，以擷取新、更新和刪除的內容。

* **WriteClient** Post、標幟和贊系列中的內容。

