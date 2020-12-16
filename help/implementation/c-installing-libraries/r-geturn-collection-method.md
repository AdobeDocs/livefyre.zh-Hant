---
description: 此方法會傳回此集合的URN。 您必須先執行createOrUpdate()，才能執行此方法。
seo-description: 此方法會傳回此集合的URN。 您必須先執行createOrUpdate()，才能執行此方法。
seo-title: getUrn收集方法
solution: Experience Manager
title: getUrn收集方法
uuid: 2f4d7796-2ae5-4b74-a958-40825c6bff16
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# getUrn Collection Method{#geturn-collection-method}

此方法會傳回此集合的URN。 您必須先執行createOrUpdate()，才能執行此方法。

## Java示例{#section_nyl_ycs_rz}

```
collection.getUrn(); 
```

輸出範例：

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## NodeJS示例{#section_xkd_gds_rz}

```
collection.getUrn(); 
```

輸出範例：

```
<span class="str">"urn:livefyre:network=`example.fyre.co`:site=1:collection=1"</span>
```

## PHP示例{#section_ghf_gds_rz}

```
$collection->getUrn(); 
```

輸出範例：

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Python示例{#section_dwg_gds_rz}

```
collection.urn() 
```

輸出範例：

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

## Ruby示例{#section_enh_gds_rz}

```
collection.urn
```

輸出範例：

```
"urn:livefyre:network=`example.fyre.co`:site=1:collection=1" 
```

