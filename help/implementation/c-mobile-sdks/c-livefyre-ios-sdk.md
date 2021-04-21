---
description: 將Livefyre新增至原生iOS應用程式。
title: Livefyre iOS SDK
exl-id: 961c41dc-fee8-480c-a189-a20a689e705f
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Livefyre iOS SDK{#livefyre-ios-sdk}

將Livefyre新增至原生iOS應用程式。

使用此開放原始碼程式庫，將Livefyre服務整合至您的原生iOS應用程式。 Livefyre StreamHub iOS SDK以優異的AFNetworking程式庫為基礎，提供我們常見API機制的精簡層。

Livefyre也提供兩個以此SDK為基礎的iOS範例應用程式：注釋串流和評論範例應用程式。

## 將SDK整合至您的專案中，做為Cocoa Pod（建議）{#section_qc5_h3v_zz}

將StreamHub-iOS SDK新增至專案最方便的方式是使用CocoaPods。 如果您沒有CocoaPods，請執行寶石安裝Cocoapods和Pod設定。 以下是Podfile範例：

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

您還需要將系統需求儲存庫添加到CocoaPod安裝中（這將將其克隆到`~/.cocoapods/repos`目錄）:

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

在應用程式專案根目錄中建立您的播客檔案後，請執行下列動作：

```
pod install
```

這會下載所有相依項並建立檔案MyApp.xcworkspace，您應從現在開始使用它，以Xcode開啟您的應用程式專案。

## 作為Xcode子項目{#section_jcm_g3v_zz}

或者，克隆儲存庫：

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

接著，將Xcode專案(LFSClient.xcodeproj)新增至您的應用程式做為子專案（只需將LFSClient.xcodeproj檔案拖曳至Xcode的「專案導覽器」窗格，即可輕鬆完成）。

您也需要對任何相依性([AFNetworking](https://github.com/AFNetworking/AFNetworking)、[JSONKit](https://github.com/escherba/JSONKit))執行相同操作。

## 一次下載所有內容（不建議）{#section_rpb_f3v_zz}

```
cd ~/dev 
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
cd StreamHub-iOS-SDK 
git submodule init 
git submodule update 
pod repo add livefyre https://github.com/Livefyre/cocoapods.git 
pod install 
cd examples/CommentStream 
pod install 
open CommentStream.xcworkspace
```

>[!NOTE]
>
>若要在Xcode 6中執行測試，您必須在Pods-test-XCTest+OHHTTPStubSuiteCleanUp pod[https://stackoverflow.com/a/24651704](https://stackoverflow.com/a/24651704)中將$(PLATFORM_DIR)/Developer/Library/Frameworks新增至FRAMEWORK_SEARCH_PATHS。

您需要Livefyre的LFSTestConfig.plist檔案，Livefyre會在要求時提供此檔案。

## Xcode檔案{#section_arl_b3v_zz}

您可以瀏覽[documentation](https://livefyre.github.com/StreamHub-iOS-SDK/)，或在系統上的Xcode中建立&quot;Documentation&quot;目標（需要安裝appledoc）。

## 要求 {#section_m5l_13v_zz}

自v0.2.0以來的StreamHub iOS SDK版本需要iOS 6.0或更新版本。

## 附錄（JSON支援）{#section_pcd_5hv_zz}

若是查看StreamHub-iOS SDK內部軟體的使用者，請注意，我們使用已修改的[JSONKit](https://github.com/escherba/JSONKit)版本作為預設JSON剖析器（而非Apple提供的NSJSONSerialization）。 我們必須這麼做，因為Apple提供的剖析器不支援解碼包含整數或浮點數的JSON檔案，這些數字大於系統可以表示的整數。 我們修改的JSONKit版本會將非常大的數字截斷到相應的系統最大值，而不是拋出異常。
