---
description: Livefyre使用PUSH介面來傳送使用者權限變更的外部系統資訊。
seo-description: Livefyre使用PUSH介面來傳送使用者權限變更的外部系統資訊。
seo-title: 將用戶權限發佈到外部系統（可選）
solution: Experience Manager
title: 將用戶權限發佈到外部系統（可選）
uuid: 9c18b20d-3b93-4666-b7de-1ec60318cf88
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 4%

---


# 將用戶權限發佈到外部系統（可選）{#posting-user-permissions-to-external-systems-optional}

Livefyre使用PUSH介面來傳送使用者權限變更的外部系統資訊。

## Livefyre Studio中的使用者類型

| 使用者類型 | 說明 |
|--- |--- |
| 擁有者 | 此使用者是擁有者，可協調內容並指派新的協調者。 |
| admin | 此使用者是協調者，可協調內容。 |
| 成員 | 此用戶被允許列出。 張貼的內容不會透過垃圾訊息或臟話篩選，也不需要在預先協調的串流中核准。 |
| none | 此使用者是標準使用者，沒有特殊權限。 |
| outcast | 此使用者被禁止參與任何對話。 |

若要將使用者權限張貼至外部系統，您必須註冊會以POST要求接收權限資料的URL。

例如：

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| 參數 | 說明 |
|--- |--- |
| networkName | 您的Livefyre提供的網路名稱。 |
| token | 有效的系統Token。 |
| url | 要註冊的URL。 |

已註冊的URL應接受具有下列資料的POST作為內容類型： application/x-www-form-urlencoded.

| 參數 | 說明 |
|--- |--- |
| jid | 從屬關係已更改的用戶的JID。 JID是形式的字串 `user_id@network`。 |
| 學員 | 指派的權限名稱，其必須是下列其中一項：  `{admin | member | none | outcast | owner}` |

如需更新使用者關係設定的詳細資訊，請參閱「新 [增使用者關係API參考」](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post)。
