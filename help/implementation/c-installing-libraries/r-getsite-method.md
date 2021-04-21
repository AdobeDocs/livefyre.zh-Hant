---
description: 傳回新的Site物件。
title: getSite網路方法
exl-id: 88782da9-88c6-4e60-9a23-e46d68675d59
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 0%

---

# getSite Network Method{#getsite-network-method}

傳回新的Site物件。
變數|類型|說明|
|— |— |— |
|siteId|String|Livefyre提供的ID，用於系列所屬的網站或應用程式。 例如：303617。  |
|siteKey|String|Livefyre為siteId提供的機密金鑰。  |

## Java示例{#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## NodeJS示例{#section_xkd_gds_rz}

```
var site = network.getSite(siteId, siteKey); 
```

## PHP示例{#section_ghf_gds_rz}

```
$site = $network->getSite(siteId, siteKey);
```

## Python示例{#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## Ruby示例{#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```
