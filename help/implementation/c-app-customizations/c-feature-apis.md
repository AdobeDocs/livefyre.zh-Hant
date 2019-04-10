---
description: 使用功能API自動化程序
seo-description: 使用功能API自動化程序
seo-title: 功能API
title: 功能API
uuid: eac3a156-1b60-4ffa-8b6f-e451 eb03 da77
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 功能API{#feature-apis}

使用功能API自動化程序

使用功能API將內容的特色自動化。例如，建立即時部落格或留言應用程式時，請先功能由選定協調者張貼來調整對話，並建立串流內的一致性。

Livefyre提供功能和Unfeature API。

## 功能 {#section_jpw_nqw_xz}

**資源**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/feature/<commentId>/?lftoken=<base64userToken>
```

輸入您所選協調者的使用者Token。

**貼文資料**

```
{value: <number>} 
```

此值將用於排序精選內容，最大到最小(10將在精選內容清單中的1之前顯示)。此值預設 **為** 目前的持續時間，因此精選的註解通常會被排序最新到最舊。

**回應範例**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>資料欄位尚未使用。

## 取消功能 {#section_knh_mqw_xz}

**資源**

```
POST: https://{networkName}.quill.fyre.co/api/v3.0/collection/<collectionId>/unfeature/<commentId>/?lftoken=<base64userToken>
```

輸入您所選協調者的使用者Token。

**回應範例**

```
{"status": "ok", "code": 200, "data": null} 
```

>[!NOTE]
>
>資料欄位尚未使用。

