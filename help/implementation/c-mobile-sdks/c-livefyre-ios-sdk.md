---
description: 將Livefyre新增至您的原生iOS應用程式。
title: Livefyre iOS SDK
exl-id: 961c41dc-fee8-480c-a189-a20a689e705f
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Livefyre iOS SDK{#livefyre-ios-sdk}

將Livefyre新增至您的原生iOS應用程式。

使用此開放原始碼程式庫，將Livefyre服務整合至您的原生iOS應用程式。 Livefyre StreamHub iOS SDK根據絕佳的AFNetworking程式庫，在常見API機制周圍提供精簡層。

Livefyre也提供以此SDK為基礎的兩個iOS範例應用程式：評論資料流和評論範例應用程式。

## 將SDK整合至您的專案，為Cocoa Pod（建議使用） {#section_qc5_h3v_zz}

將StreamHub-iOS SDK新增至專案最方便的方式是使用CocoaPods。 如果您沒有CocoaPods，請執行gem install cocoapods和pod setup。 以下是範例Podfile:

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

您還需要將規格儲存庫添加到CocoaPod安裝中（這會將其克隆到`~/.cocoapods/repos`目錄）:

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

在您的應用程式專案根目錄中建立Podfile後，以及上方新增的存放庫，請執行：

```
pod install
```

這會下載所有相依性並建立檔案MyApp.xcworkspace，您應從現在開始使用此檔案，在Xcode中開啟您的應用程式專案。

## 作為Xcode子專案 {#section_jcm_g3v_zz}

或者，複製存放庫：

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

接下來，將Xcode項目(LFSClient.xcodeproj)作為子項目添加到應用程式中（只需將LFSClient.xcodeproj檔案拖到Xcode的「項目導航器」窗格中即可輕鬆完成）。

您也需要對任何相依性([AFNetworking](https://github.com/AFNetworking/AFNetworking)、[JSONKit](https://github.com/escherba/JSONKit))執行相同操作。

## 一次下載所有內容（不建議使用） {#section_rpb_f3v_zz}

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
>若要在Xcode 6中執行測試，您必須將$(PLATFORM_DIR)/Developer/Library/Frameworks新增至Pods-test-XCTest+OHHTTPStubSuiteCleanUp pod[https://stackoverflow.com/a/24651704](https://stackoverflow.com/a/24651704)中的FRAMEWORK_SEARCH_PATHS。

您需要來自Livefyre的LFSTestConfig.plist檔案，Livefyre可應要求提供。

## Xcode檔案 {#section_arl_b3v_zz}

您可以瀏覽[documentation](https://github.com/Livefyre/StreamHub-iOS-SDK)，或在系統上的Xcode中（需要安裝appledoc）建立「Documentation」目標。

## 要求 {#section_m5l_13v_zz}

StreamHub iOS SDK 0.2.0版以來的版本需使用iOS 6.0或更新版本。

## 附錄（JSON支援） {#section_pcd_5hv_zz}

若是查看StreamHub-iOS SDK內部檔案的使用者，請注意，我們使用經修改的[JSONKit](https://github.com/escherba/JSONKit)版本作為預設JSON剖析器(而非Apple提供的NSJSONSerialization)。 我們必須這麼做，因為Apple提供的剖析器不支援解碼JSON檔案，這些檔案包含的整數或浮點數大於系統可表示的整數或浮點數。 我們修改的JSONKit會將非常大的數字截斷到相應的系統最大值，而不是引發異常。
