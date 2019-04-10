---
description: 建立網路物件。
seo-description: 建立網路物件。
seo-title: 網路類別方法
solution: Experience Manager
title: 網路類別方法
uuid: 4130beda-dd09-49ae-aafb-f6 b956 e30 b51
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 網路類別方法{#network-class-methods}

建立網路物件。

當您建立網路物件後，頁面的其餘部分會假設您的作業中已有個體化的網路物件。

## 網路物件

| 參數 | Type | 說明 |
|---|---|---|
| *`network`* | 字串 | 您的Livefyre網路。例如：`labs.fyre.co`。 |
| *`networkKey`* | 字串 | Livefyre為網路提供的秘密金鑰。 |

## Java {#section_myk_dzs_kbb}

```
import com.livefyre.Livefyre; 
  
Network network = Livefyre.getNetwork(network, networkKey); 
```

## NodeJS {#section_nyk_dzs_kbb}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork(network, networkKey); 
```

## PHP {#section_oyk_dzs_kbb}

```
use Livefyre\Livefyre; 
  
$network = Livefyre::getNetwork(network, networkKey); 
```

## Python {#section_pyk_dzs_kbb}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network(network, networkKey) 
```

## Ruby {#section_qyk_dzs_kbb}

```
require 'livefyre' 
  
network = Livefyre.get_network(network, networkKey) 
```
