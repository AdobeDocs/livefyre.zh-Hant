---
description: 將Livefyre新增至您的原生iOS App。
seo-description: 將Livefyre新增至您的原生iOS App。
seo-title: Livefyre iOS SDK
solution: Experience Manager
title: Livefyre iOS SDK
uuid: bfdef31a-49fc-4b25-b0 c5-300f27067302
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Livefyre iOS SDK{#livefyre-ios-sdk}

將Livefyre新增至您的原生iOS App。

使用這個開放原始碼庫，將Livefyre服務整合到您的原生iOS應用程式中。Livefyre StreamHub iOS SDK可根據絕佳的AffnetNetwork程式庫，圍繞我們常用的API機制提供一個精簡的圖層。

Livefyre也根據此SDK提供兩個iOS範例應用程式：評論串流和評論範例應用程式。

## 將SDK整合在您的專案中成為Cocoa Pod(建議) {#section_qc5_h3v_zz}

將StreamHub-iOS SDK新增至專案最方便的方法就是使用CoCOAPODS。如果您沒有CoCoAPODS，請執行goM安裝cotepod和pod設定。以下是PodFile範例：

```
source 'https://github.com/Livefyre/cocoapods.git' 
source 'https://github.com/CocoaPods/Specs.git' 
  
platform :ios, :deployment_target => '6.0' 
  
pod 'StreamHub-iOS-SDK', '~> 0.3.0'
```

您也需要新增Specs存放庫至您的CoCoAPD安裝(如此會將它複製 `~/.cocoapods/repos` 到目錄)：

```
pod repo add livefyre https://github.com/Livefyre/cocoapods.git
```

在您的應用程式專案根目錄和上面新增的儲存庫中建立PodFile後，執行：

```
pod install
```

這會下載所有相依性並建立檔案MyApp. xcwork，您現在應該使用此工作區，在Xcode中開啓應用程式專案。

## 作為Xcode子專案 {#section_jcm_g3v_zz}

或者，複製存放庫：

```
git clone https://github.com/Livefyre/StreamHub-iOS-SDK.git 
```

接著，將Xcode專案(LFSClient. xcodproj)新增至您的應用程式做為子專案(只要將LFSCLient. xcodproj檔案拖曳至Xcode中的「Project Navigator」(專案導覽器)窗格即可輕鬆完成)。

您也必須對任何相依性([ANetworking](https://github.com/AFNetworking/AFNetworking)、 [JSOKit](https://github.com/escherba/JSONKit))進行相同的動作。

## 一次下載所有內容(不建議) {#section_rpb_f3v_zz}

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
>若要在Xcode中執行測試，您必須在Pods-test-xCTest+ OhthtptpsSuiteLUppodhttps://stackoverflow.com/a/24651704[](https://stackoverflow.com/a/24651704)中新增$(PLATFORM_ DILR)/Developer/Library/Framework至Framework_ Search_ Path。

Livefyre需要Livefyre提供的LFststConfig. plist檔案。

## Xcode文件 {#section_arl_b3v_zz}

您可以瀏覽 [說明文件](https://livefyre.github.com/StreamHub-iOS-SDK/) ，或在您的系統上建立Xcode(需要安裝AppleDoc)的「說明文件」目標。

## 需求 {#section_m5l_13v_zz}

StreamHub iOS SDK版本，因為v0.2.0需要iOS6.0或更新版本。

## 附錄(JSON支援) {#section_pcd_5hv_zz}

對於查看StreamHub-iOS SDK內部架構的使用者，請注意，我們會使用修改版本 [的JSOKit](https://github.com/escherba/JSONKit) 作為預設的JSON剖析器(而非Apple提供的NSjSonalization)。我們必須這麼做，因為Apple提供的剖析器不支援解碼JSON檔案，此檔案包含的整數或浮點數字大於系統可代表的整數或浮點數字。我們修改的JSOKit版本會將很大的數字截斷為對應的系統上限，而不會造成例外狀況。
