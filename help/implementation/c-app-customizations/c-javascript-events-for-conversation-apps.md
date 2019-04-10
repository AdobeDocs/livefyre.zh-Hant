---
description: 可用於繫結對話應用程式 (如 Comments、Chat、Live Blog、Reviews 和 Sidenotes) JavaScript
  的事件。
seo-description: 可用於繫結對話應用程式 (如 Comments、Chat、Live Blog、Reviews 和 Sidenotes) JavaScript
  的事件。
seo-title: 對話應用程式的Javascript事件
solution: Experience Manager
title: 對話應用程式的Javascript事件
uuid: cce112b5-7c3a-4721-9854-fc8471 f3 d5 d0
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 對話應用程式的Javascript事件{#javascript-events-for-conversation-apps}

可用於繫結對話應用程式 (如 Comments、Chat、Live Blog、Reviews 和 Sidenotes) JavaScript 的事件。

## 對話應用程式與活動矩陣 {#section_y4j_x4m_ybb}

以下是對話應用程式可用事件的矩陣。an X表示該事件適用於應用程式，N/A表示該事件不適用於應用程式，而無標記表示該事件無法用於該應用程式：

### 對話應用程式事件

| Events | 注釋 | 聊天室 | LiveBlog | 評論 | Sitents | 民調問答 | 趨勢分析 |
|---|---|---|---|---|---|---|---|
| Init | X | X | X | X | X |  |  |
| 載入 | X | X | X | X |  |  |  |
| 檢視 | X | X | X | X |  |  |  |
| 貼文 | X | X | X | X |  | N/A | N/A |
| 已張貼 | X | X | X | X | X | N/A | N/A |
| Twitter回覆 | X | X | X | N/A | N/A | N/A | N/A |
| Twitter贊 | X | X | X | N/A | N/A | N/A | N/A |
| LF like | X | X | X | X | N/A | N/A | N/A |
| LF收回贊 | X | X | X | X | N/A | N/A | N/A |
| 分享貼文 | X | X |  | X | N/A | N/A | N/A |
| 共用按鈕 | X | X | X | X |  | N/A | N/A |
| 分享Twitter | X | X | X | X | X | N/A | N/A |
| 分享Facebook | X | X | X | X | X | N/A | N/A |
| 共用URL | X | X | X | X |  | N/A | N/A |
| ExpandReprections | X | N/A | X | X | N/A | N/A | N/A |
| 收合回覆 | X | N/A | X | X | N/A | N/A | N/A |
| 旗標按鈕 | X | X | X | X | N/A | N/A | N/A |
| 旗標 | X | X | X | X | X | N/A | N/A |
| 標幟取消 | X | X | X | X | N/A | N/A | N/A |
| 關注點 | X | N/A | X | X | N/A | N/A | N/A |
| 取消關注 | X | N/A | X | X | N/A | N/A | N/A |
| 詳細資訊 | X | X | X | X | N/A | N/A | N/A |
| ModalView |  | N/A | N/A | N/A | N/A | N/A | N/A |
| Twitter回推 | X | X | X | N/A | N/A | N/A | N/A |
| 貼文按鈕點擊 | N/A | N/A | N/A | N/A | N/A | N/A | N/A |
| 評論計數已更新 | X | X | X | X | N/A | N/A | N/A |
| 使用者登入 |  |  |  |  |  | N/A | N/A |
| 使用者登出 |  |  |  |  |  | N/A | N/A |
| 註解功能 |  | N/A |  |  | N/A | N/A | N/A |
| 註解功能 |  | N/A |  |  | N/A | N/A | N/A |
| 投票意見 | N/A | N/A | N/A | X | X | N/A | N/A |
| 民調問答選擇 | N/A | N/A | N/A | N/A | N/A |  | N/A |
| 選取趨勢項目 | N/. A | N/A | N/A | N/A | N/A | N/A |  |
| 網路ID |  |  |  |  |  |  |  |
| 應用程式ID | X | X | X | X |  |  |  |
| 上下文ID | X | X | X | X |  |  |  |
| 應用程式類型 | X | X | X | X |  |  |  |
| 內容類型 | X | X | X | X |  |  |  |
| 發佈至應用程式的日期 |  |  |  |  |  |  |  |
| 登入使用者應用程式 |  |  |  |  |  |  |  |

