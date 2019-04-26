---
description: 此方法會傳回此系列的URN。執行此方法之前，您必須先執行CreateOrdUpdate()。
seo-description: 此方法會傳回此系列的URN。執行此方法之前，您必須先執行CreateOrdUpdate()。
seo-title: Geturn Collection方法
solution: Experience Manager
title: Geturn Collection方法
uuid: 2f4d7796-2ae5-4b74-a958-40825c6 bff16
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Geturn Collection方法{#geturn-collection-method}

此方法會傳回此系列的URN。執行此方法之前，您必須先執行CreateOrdUpdate()。

## Java範例 {#section_nyl_ycs_rz}

```
collection.getUrn(); 
```

輸出範例：

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## nodeJS範例 {#section_xkd_gds_rz}

```
collection.getUrn(); 
```

輸出範例：

```
<span class="str">"urn:livefyre:network=`example.fyre.co`:site=1:collection=1"</span>
```

## PHP範例 {#section_ghf_gds_rz}

```
$collection->getUrn(); 
```

輸出範例：

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Python範例 {#section_dwg_gds_rz}

```
collection.urn() 
```

輸出範例：

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Ruby範例 {#section_enh_gds_rz}

```
collection.urn
```

輸出範例：

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

