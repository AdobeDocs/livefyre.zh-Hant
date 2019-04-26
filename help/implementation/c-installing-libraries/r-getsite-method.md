---
description: 傳回新的網站物件。
seo-description: 傳回新的網站物件。
seo-title: getSite Network方法
solution: Experience Manager
title: getSite Network方法
uuid: 67de781e-5240-4be5-9e93-c614828 e0 bb5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# getSite Network方法{#getsite-network-method}

傳回新的網站物件。
|變數|類型|說明|
|—|—|—|
| SiteID|字串|Collection所屬之網站或應用程式的Livefyre提供ID。例如：303617.|
| SiteKey|字串|Livefyre為SiteID提供的秘密金鑰。|

## Java範例 {#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## nodeJS範例 {#section_xkd_gds_rz}

```
var site = network.getSite(siteId, siteKey); 
```

## PHP範例 {#section_ghf_gds_rz}

```
$site = $network->getSite(siteId, siteKey);
```

## Python範例 {#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## Ruby範例 {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

