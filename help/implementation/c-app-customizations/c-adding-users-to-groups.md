---
description: 新增使用者標籤至帳戶，以新增使用者至群組。
title: 新增使用者至群組
exl-id: 6e799c77-e815-40c2-ae06-bbd076df9fe7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 1%

---

# 新增使用者至群組{#adding-users-to-groups}

新增使用者標籤至帳戶，以新增使用者至群組。

使用者標籤可用於專有和企業描述檔系統，並可透過下列幾種方式新增至帳戶：

* 透過Studio建立擁有者和協調者會指派「協調者」使用者標籤給帳戶。
* 建立使用者群組，並透過Studio將使用者新增至使用者群組，會自動將具有群組名稱的使用者標籤套用至選取的使用者。
* 使用[新增使用者標籤HTTP](https://api.livefyre.com/docs#add-user-tag)呼叫或Ping for Pull，使用者標籤也可以直接套用至帳戶。

>[!NOTE]
>
>API方法、HTTP新增使用者標籤呼叫和Ping for Pull方法都會覆寫先前透過其他方式指派給帳戶的任何標籤。 因此，請選擇一種方法，並在整個流程中一致使用。

## 從Studio {#section_qgq_nbw_xz}的「使用者」頁面將使用者新增至群組

* 按一下任何使用者名稱下方的&#x200B;**[!UICONTROL Add Group]**&#x200B;或群組標籤，以開啟群組功能表。
* 捲動清單並尋找您要新增使用者的群組。 您可以在下拉式清單頂端的&#x200B;**[!UICONTROL Search]**&#x200B;方塊中輸入群組名稱。
* 按一下應新增使用者之群組旁的核取方塊，然後點擊傳回。

使用者的設定檔會顯示群組的名稱（如果使用者僅在一個群組中）或使用者所屬的群組數目。

## 使用「新增使用者標籤」呼叫{#section_kn3_gbw_xz}將使用者新增至群組

將使用者的LFToken和您選取的標籤名稱與POST要求一併傳遞

例如：

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


如需詳細資訊，請參閱「API參考> [新增使用者標籤」。](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post)

## 使用Ping for Pull {#section_kyj_11w_xz}將用戶添加到組

使用標籤陣列將用戶分配給用戶組。 （標籤可能包含1-63個英數字元和底線字元。）

例如：

```
"tags": ["moderator", "brand_advocate"],
```

## 使用遠程配置式將用戶添加到組{#section_uyn_scv_xz}

將使用者標籤新增至「遠端設定檔」，用於為特定使用者在自訂設定檔系統與Livefyre之間同步使用者資料。
