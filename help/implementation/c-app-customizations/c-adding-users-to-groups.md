---
description: 新增使用者標記至帳戶，新增使用者至群組。
seo-description: 新增使用者標記至帳戶，新增使用者至群組。
seo-title: 新增使用者至群組
solution: Experience Manager
title: 新增使用者至群組
uuid: 3633f2df-8d60-4cdd-b9 a2-3807218c74 a0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 新增使用者至群組{#adding-users-to-groups}

新增使用者標記至帳戶，新增使用者至群組。

「使用者標記」可能會同時針對專屬和企業描述檔系統實施，而且可以透過數種方式新增至帳戶：

* 透過Studio建立擁有者和協調者，將「協調者的使用者標記」指派給帳戶。
* 建立使用者群組，並透過Studio將使用者新增至使用者群組，會自動將使用者標記套用至所選使用者的群組名稱。
* 使用者標記也可以使用 [新增使用者標記HTTP](https://api.livefyre.com/docs#add-user-tag) 呼叫或用於提取的Ping直接套用至帳戶。

>[!NOTE]
>
>API方法、HTTP新增使用者標記呼叫和用於提取方法的Ping方法都會覆寫先前指派給帳戶的任何標記。因此，請選擇一個方法，並在整個程序中使用一致。

## 從Studio的「使用者」頁面新增使用者至群組 {#section_qgq_nbw_xz}

* 按一下 **[!UICONTROL Add Group]** 或任何使用者名稱下方的群組標籤，以開啓群組功能表。
* 捲動清單並尋找您要新增使用者的群組。您可以在下拉式清單頂端的 **[!UICONTROL Search]** 方塊中輸入群組名稱。
* 按一下使用者應加入之群組旁的核取方塊，然後點擊返回。

使用者的描述檔會顯示群組名稱(如果使用者僅在某個群組中)或使用者所屬群組的數目。

## 使用新增使用者標記呼叫將使用者新增至群組 {#section_kn3_gbw_xz}

使用POST請求傳遞使用者的lfToken和您選擇的標籤名稱

例如：

```
curl -XPOST -d 'tag_name=tag&lftoken=eyJhbGciOiAiA_TOKENcGlyZXMiOiAxMzU3OTY3NTAxLjIzn0.KoyXUVCavt-rdvkVXm2qzQTyMAOSp-crQA1uL1ht9WU' 'https://labs.quill.fyre.co/api/v3.0/author/system@`labs.fyre.co`/tag/'
```


如需詳細資訊，請參閱「API參考> [新增使用者標記](https://api.livefyre.com/docs/apis/by-category/user-management#operation=urn:livefyre:apis:quill:operations:api:v3.0:author:tags:method=post)」。

## 使用Ping for Draw新增使用者至群組 {#section_kyj_11w_xz}

使用標籤陣列將使用者指派給使用者群組。(標記可能包含1-63個英數字元和底線字元。)

例如：

```
"tags": ["moderator", "brand_advocate"],
```

## 使用遠端描述檔將使用者新增至群組 {#section_uyn_scv_xz}

新增使用者標記至遠端描述檔，用來同步自訂描述檔系統與Livefyre之間的使用者資料，供特定使用者使用。
