---
description: 建立採用Livefyre架構的Android應用程式。
title: Android SDK
exl-id: 54ea6537-5f27-4174-af25-d17257f23e48
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 1%

---

# Android SDK{#android-sdk}

建立採用Livefyre架構的Android應用程式。

使用此程式庫，將Livefyre服務整合至您的原生Android應用程式。 [Livefyre StreamHub Android SDK](https://github.com/Livefyre/StreamHub-Android-SDK)根據Gradle/Android Studio開發環境，針對我們常用的API機制提供精簡的圖層。

Livefyre也提供以此SDK為基礎的[Reviews](https://github.com/Livefyre/StreamHub-iOS-Reviews-App)範例應用程式。

此Livefyre Android SDK可同時用於Eclipse和Android Studio。

>[!NOTE]
>
>在安裝Livefyre Android SDK之前，您必須在您的環境中安裝[Android SDK](https://developer.android.com/sdk/index.html)。 您也必須包含一些額外的Android SDK套件，如「Android開發人員檔案>」所述。
>[新增SDK套件](https://developer.android.com/sdk/installing/adding-packages.html)

使用Android SDK Manager（可從Android Studio或Eclipse工具列取得）來安裝所有建議的套件。 請確定也包含Android支援儲存庫。

## Eclipse {#section_dtm_slv_zz}

若要在Eclipse中將Livefyre Android SDK新增至您的專案：

1. 從GitHub取得最新的[StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK)。
1. 從現有專案開始或建立新專案。
1. 若要將StreamHub-Android-SDK匯入您的工作區，請前往&#x200B;**[!UICONTROL File > Import > General > Existing Project into Workspace]**。
1. 瀏覽並選取StreamHub-Android-SDK;它現在應該會顯示在套件檔案總管中。
1. 在您的專案上按一下滑鼠右鍵，然後選取&#x200B;**[!UICONTROL Properties,]**，然後選取「Android」標籤。
1. 在「程式庫」區段下，選取&#x200B;**[!UICONTROL Add button,]**，然後從程式庫清單中選取「StreamHub-Android-SDK」。
1. 按一下&#x200B;**[!UICONTROL Apply]**&#x200B;和&#x200B;**[!UICONTROL OK]**。

## Android Studio {#section_vpw_klv_zz}

若要將Livefyre Android SDK新增至Android Studio的專案：

1. 從GitHub取得最新的[StreamHub-Android-SDK](https://github.com/Livefyre/StreamHub-Android-SDK)。
1. 從現有專案開始或建立新專案。
1. 在您的專案上按一下滑鼠右鍵，然後選取&#x200B;**[!UICONTROL Open Module Settings]**。
1. 選擇窗口左上角的&#x200B;**[!UICONTROL +]**&#x200B;按鈕。
1. 選擇&#x200B;**[!UICONTROL Import Existing Project.]**（在新版Android studio中，您可在&#x200B;**[!UICONTROL More Modules]**&#x200B;下找到&#x200B;**[!UICONTROL Import Existing Project]**。）

1. 瀏覽並選取StreamHub-Android-SDK。

Android Studio可能會要求您將SDK轉換為Gradle版本；如果發生這種情況，請選擇&#x200B;**[!UICONTROL next]**，然後選擇&#x200B;**[!UICONTROL finish]**。

前往相依項下的&#x200B;**專案資料夾>應用程式資料夾> build.gradle**&#x200B;檔案，以新增下列相依項：

```
dependencies {   compile project(':streamHubAndroidSDK') } 
```

請確定以下行位於&#x200B;**專案資料夾> settings.gradle**&#x200B;檔案中：

```
include ':streamHubAndroidSDK' 
```

>[!NOTE]
>
>您可以從Config.java中自訂設定。

## 客戶 {#section_yfq_blv_zz}

StreamHub Android SDK公開數個可用來要求Livefyre API端點的用戶端類別：

* **AdminClient** 為使用者資訊、金鑰和其他中繼資料交換使用者驗證Token。

* **BootstrapClient** 取得特定系列的最新內容和中繼資料。

* **StreamClient** 輪詢系列的串流，以擷取新、更新和刪除的內容。

* **WriteClientPost** 、標幟和贊系列中的內容。
