---
description: Livefyre使用PUT介面來傳送有關使用者權限變更的外部系統資訊。
seo-description: Livefyre使用PUT介面來傳送有關使用者權限變更的外部系統資訊。
seo-title: 將使用者權限張貼至外部系統(可選)
solution: Experience Manager
title: 將使用者權限張貼至外部系統(可選)
uuid: 9c18b20d-3b93-4666-b7 de-1ec60318 cf88
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 將使用者權限張貼至外部系統(可選){#posting-user-permissions-to-external-systems-optional}

Livefyre使用PUT介面來傳送有關使用者權限變更的外部系統資訊。

## Livefyre Studio中的使用者類型

| 使用者類型 | 說明 |
|--- |--- |
| 擁有者 | 此使用者是擁有者，而且可以協調內容，並指派新的協調者。 |
| admin | 這位使用者是協調者，可以協調內容。 |
| 會員 | 此使用者已列入白名單。發佈的內容不會通過垃圾郵件或粗話篩選，而且不需要在預先協調的串流中核准。 |
| none | 這位使用者是標準使用者，沒有特殊權限。 |
| excast | 此使用者已被禁止參與任何交談。 |

若要張貼使用者權限至外部系統，您必須註冊接收權限資料作為POST請求的URL。

例如：

```
POST https://{networkName}.quill.fyre.co/?actor_token={token}&push_affiliation_url={url}
```

| 參數 | 說明 |
|--- |--- |
| socialName | 您的Livefyre提供的網路名稱。 |
| Token | 有效的系統代號。 |
| url | 註冊的URL。 |

註冊的URL應該接受具有下列資料的POST，作為內容類型：application/x-www-form-urlencoded.

| 參數 | 說明 |
|--- |--- |
| jid | 變更之使用者的JID。JID是表格 `user_id@network`的字串。 |
| 附屬機構 | 指派權限的名稱，必須屬於下列其中一項： `{admin | member | none | outcast | owner}` |

如需更新使用者關係設定的詳細資訊，請參閱 [新增使用者關係API參考](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:affiliation:add:method=post)。
