---
description: 在您的伺服器上建立唯一Token，用以識別您建立的每個系列。
title: CollectionMeta Token
exl-id: 52edfe75-5ce6-40c9-9afe-c34a3812f1e7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 2%

---

# CollectionMeta Token{#collectionmeta-token}

在您的伺服器上建立唯一Token，用以識別您建立的每個系列。

Livefyre會為您建立的每個系列指派唯一識別碼。 Livefyre會指派標題、URL和其他參數，包括：

## collectionMeta Token參數

| 參數 | 類型 | 說明 |
|--- |--- |--- |
| networkName | 字串（選用） | Livefyre網路的名稱（可從[!UICONTROL Studio] > [!UICONTROL Settings] > [!UICONTROL Integration Settings] > [!UICONTROL Credentials]取得）。 當使用程式庫建立collectionMetaToken時，這是選用的。 |
| networkKey | 字串（選用） | 特定網路的機密金鑰（可從「Studio >設定>整合設定>認證」取得）。 當使用程式庫建立collectionMetaToken時，這是選用的。 |
| siteId | 字串（選用） | 網站的ID（可從[!UICONTROL Studio > Settings > Integration Settings > Credentials]取得）。 使用程式庫建立collectionMetaToken時為選用。 |
| siteKey | 字串（選用） | 站點的密鑰（可從[!UICONTROL Studio > Settings > Integration Settings > Credentials]獲得）。 |
| articleId | 字串（選用） | 系列的唯一ID。 |
| title | 字串（選用） | 您要套用至系列的標題。 通常，這會對應顯示應用程式之頁面的標題。 <br>例如：「整合太有趣了！」<br>注意：標題的字元長度上限為255個字元。標題欄位不支援HTML實體。 請使用UTF-8編碼特殊字元。 |
| url | 字串（選用） | 您要附加至此系列的標準絕對URL。 此URL將用來從Facebook和Twitter分享的內容、電子郵件通知和Livefyre Studio產生回應用程式的連結。 <br>注意：如果在本機測試，請使用有效的基本URL網域(例如：有效： `https://customer.com`;無效： `https://localhost:5995`)。 |
| 標籤 | 字串（選用） | 以逗號分隔的單一關鍵字或片語清單。 使用Studio依標籤搜尋系列。  </br>注意：標籤不能包含空格。如果您希望在UI中顯示空格，請使用底線。 |
| extensions | JSON（選用） | 要傳遞至系列的JSON格式參數集。 |

## Java {#section_orz_m4n_sz}

```
import com.livefyre.Livefyre; 
import com.livefyre.core.Network; 
import com.livefyre.core.Site; 
import com.livefyre.core.Collection; 
  
Network network = Livefyre.getNetwork("networkName", "networkKey"); 
Site site = network.getSite("siteId", "siteKey"); 
Collection collection = site.buildCommentsCollection("title", "articleId", "https://www.example.com"); 
collection.getData().setTags("tags"); 
  
String collectionMetaToken = collection.buildCollectionMetaToken();
```

## NodeJS {#section_kpk_44n_sz}

```
var livefyre = require('livefyre'); 
  
var network = livefyre.getNetwork('networkName', 'networkKey'); 
var site = network.getSite('siteId', 'siteKey'); 
var collection = site.buildCommentsCollection('title', 'articleId', 'https://www.example.com'); 
collection.data.tags = 'tags'; 
  
var collectionMetaToken = collection.buildCollectionMetaToken(); 
```

## PHP {#section_zmd_zbj_tz}

```
$network = Livefyre::getNetwork("networkName", "networkKey"); 
$site = $network->getSite("siteId", "siteKey"); 
$collection = $site->buildCommentsCollection("title", "articleId", "https://www.example.com"); 
$collection->getData()->setTags("tags"); 
  
$collectionMetaToken = $collection->buildCollectionMetaToken();
```

## Python {#section_rdm_prj_tz}

```
from livefyre import Livefyre 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token()
```

## Ruby {#section_l5n_qrj_tz}

```
require 'livefyre' 
  
network = Livefyre.get_network('networkName', 'networkKey') 
site = network.get_site('siteId', 'siteKey') 
collection = site.build_comments_collection('title', 'articleId', 'https://www.example.com') 
collection.data.tags = 'tags' 
  
collection_meta_token = collection.build_collection_meta_token 
```

>[!NOTE]
>
>Livefyre會接收您建立的collectionMeta Token，並結合siteId（提供的Livefyre）和articleId（客戶指定）以判斷其唯一性。
