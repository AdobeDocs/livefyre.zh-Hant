---
description: 建立網路對象。
title: 網路類方法
exl-id: 5a011120-05d0-4768-9038-6a312e8c5dd1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 14%

---

# 網路類方法{#network-class-methods}

建立網路對象。

建立網路對象後，該頁的其餘部分將假定您在會話中具有實例化的網路對象。

## 網路物件

| 參數 | 類型 | 說明 |
|---|---|---|
| *`network`* | 字串 | 您的Livefyre網路。 例如: “`labs.fyre.co`”. |
| *`networkKey`* | 字串 | Livefyre為網路提供的機密金鑰。 |

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
