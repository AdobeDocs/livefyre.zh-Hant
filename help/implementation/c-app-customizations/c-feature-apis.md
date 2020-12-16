---
description: 使用功能API自動化程式
seo-description: 使用功能API自動化程式
seo-title: 功能API
title: 功能API
uuid: eac3a156-0b60-4ffa-8b6f-e451eb03da77
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---


# 功能API{#feature-apis}

使用功能API自動化程式

使用功能API，將內容的特色流程自動化。 例如，建立即時部落格或留言應用程式時，功能所有由所選協調者張貼的內容，以引導對話，並建立串流內的一致性。

Livefyre提供功能與非功能API。

## 功能 {#section_jpw_nqw_xz}

**資源**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

輸&#x200B;入所選協調者的使用者Token。

**貼文資料**

```
{value: <number>} 
```

此值將用來排序精選內容，從最大到最小（10會在精選內容清單的1之前顯示）。 此值預設為大紀元時間的&#x200B;**now**，因此，精選的註解通常會最新至最舊。

**範例回應**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>資料欄位尚未使用。

## 取消功能{#section_knh_mqw_xz}

**資源**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

輸入所選協調者的使用者Token。

**範例回應**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>資料欄位尚未使用。

