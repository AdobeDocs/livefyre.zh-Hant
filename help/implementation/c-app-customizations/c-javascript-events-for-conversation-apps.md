---
description: 可用於繫結對話應用程式 (如 Comments、Chat、Live Blog、Reviews 和 Sidenotes) JavaScript 的事件。
seo-description: 可用於繫結對話應用程式 (如 Comments、Chat、Live Blog、Reviews 和 Sidenotes) JavaScript 的事件。
seo-title: 對話應用程式的Javascript事件
solution: Experience Manager
title: 對話應用程式的Javascript事件
uuid: cce112b5-7c3a-4721-9854-fc8471f3d5d0
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 73%

---


# 對話應用程式的Javascript事件{#javascript-events-for-conversation-apps}

可用於繫結對話應用程式 (如 Comments、Chat、Live Blog、Reviews 和 Sidenotes) JavaScript 的事件。

## 對話應用程式和事件矩陣{#section_y4j_x4m_ybb}

以下是對話應用程式可用事件的矩陣。 X表示該事件適用於應用程式，N/A表示該事件不適用於應用程式，而無標籤表示該事件不適用於該應用程式：

### 對話應用程式事件

| 事件 | 意見 | 聊天室 | Liveblog | 評論 | Siesors | 民調 | 趨勢分析 |
|---|---|---|---|---|---|---|---|
| 初始化 | X | X | X | X | X |  |  |
| 載入 | X | X | X | X |  |  |  |
| 檢視 | X | X | X | X |  |  |  |
| 貼文 | X | X | X | X |  | 不適用 | 不適用 |
| 已張貼 | X | X | X | X | X | 不適用 | 不適用 |
| Twitter 回覆 | X | X | X | 不適用 | 不適用 | 不適用 | 不適用 |
| Twitter贊 | X | X | X | 不適用 | 不適用 | 不適用 | 不適用 |
| LF like | X | X | X | X | 不適用 | 不適用 | 不適用 |
| LF不同 | X | X | X | X | 不適用 | 不適用 | 不適用 |
| 在貼文時分享 | X | X |  | X | 不適用 | 不適用 | 不適用 |
| 共用按鈕 | X | X | X | X |  | 不適用 | 不適用 |
| 分享Twitter | X | X | X | X | X | 不適用 | 不適用 |
| 分享Facebook | X | X | X | X | X | 不適用 | 不適用 |
| 共用URL | X | X | X | X |  | 不適用 | 不適用 |
| 展開回覆 | X | 不適用 | X | X | 不適用 | 不適用 | 不適用 |
| 收合回覆 | X | 不適用 | X | X | 不適用 | 不適用 | 不適用 |
| 標幟按鈕 | X | X | X | X | 不適用 | 不適用 | 不適用 |
| 標幟 | X | X | X | X | X | 不適用 | 不適用 |
| 標籤取消 | X | X | X | X | 不適用 | 不適用 | 不適用 |
| 關注 | X | 不適用 | X | X | 不適用 | 不適用 | 不適用 |
| 取消關注 | X | 不適用 | X | X | 不適用 | 不適用 | 不適用 |
| 請求更多 | X | X | X | X | 不適用 | 不適用 | 不適用 |
| ModalView |  | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 |
| Twitter回推 | X | X | X | 不適用 | 不適用 | 不適用 | 不適用 |
| 「貼文」按鈕按一下 | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 |
| 注釋計數已更新 | X | X | X | X | 不適用 | 不適用 | 不適用 |
| 使用者登入 |  |  |  |  |  | 不適用 | 不適用 |
| 用戶已登出 |  |  |  |  |  | 不適用 | 不適用 |
| 注釋精選 |  | 不適用 |  |  | 不適用 | 不適用 | 不適用 |
| 注釋未精選 |  | 不適用 |  |  | 不適用 | 不適用 | 不適用 |
| 評論投票 | 不適用 | 不適用 | 不適用 | X | X | 不適用 | 不適用 |
| 民調問答選擇 | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 |  | 不適用 |
| 已選取趨勢項目 | N/.A | 不適用 | 不適用 | 不適用 | 不適用 | 不適用 |  |
| 網路ID |  |  |  |  |  |  |  |
| 應用程式 ID | X | X | X | X |  |  |  |
| 內容ID | X | X | X | X |  |  |  |
| 應用程式類型 | X | X | X | X |  |  |  |
| 內容類型 | X | X | X | X |  |  |  |
| 發佈日期至應用程式 |  |  |  |  |  |  |  |
| 登入使用者應用程式 |  |  |  |  |  |  |  |

