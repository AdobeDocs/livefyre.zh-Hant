---
description: 建立Ping for Pull回應，將更新的使用者資訊傳送至Livefyre。
seo-description: 建立Ping for Pull回應，將更新的使用者資訊傳送至Livefyre。
seo-title: 建立Ping以取得回應
solution: Experience Manager
title: 建立Ping以取得回應
uuid: f90871d5-601f-40dc-b3d2-ab78635e4a88
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# 建立Ping以取得回應{#build-the-ping-for-pull-response}

建立Ping for Pull回應，將更新的使用者資訊傳送至Livefyre。

| 類型 | 屬性 | 說明 |
|--- |--- |--- |
| 需要字 *串* | id | 您的描述檔系統中使用者的使用者ID。 這在您的網路中所有使用者中都必須是唯一的，而且絕不能變更。 |
| 需要字 *串* | display_name | 使用者的顯示名稱。 這會以使用者張貼的Livefyre內容呈現。 |
| 物件 *可選，但建議* | name | 字串以定義使用者的格式化、名字、中間和姓氏。 |
| 字串可 *選，但建議使用* | 電子郵件 | 使用者的電子郵件地址。 用於傳送電子郵件通知。 |
| 字串可 *選，但建議使用* | image_url | 要為使用者顯示的頭像URL。 Livefyre會視需要將上傳的影像縮放為100×100、75×75或50×50像素。 為獲得最佳效果，使用者應上傳100×100像素的方形影像。 為確保在Livefyre中更新頭像影像，請修改每個影像更新的image_url，讓Ping for Pull偵測到影像已變更。 例如，在檔案名稱中附加時間戳記或增加影像變更。 注意： 所有URL都必須具備完整的限定和存取權。 |
| 字串可 *選，但建議使用* | profile_url | 您網站上使用者描述檔頁面的URL。 |
| 字串可 *選，但建議使用* | settings_url | 網頁的URL，使用者可在此設定您網站的使用者設定檔設定。 |
| 陣列可 *選，但建議使用* | 標籤 | 用來指派使用者至使用者群組。 標籤可包含1-63個英數字元和底線字元。 |
| 布林值 *可選，但建議使用* | autofollow_convess | 定義使用者張貼系列後是否希望自動追隨系列。 當追蹤系列時，使用者會在其他使用者參與時收到電子郵件通知。 可能是真或假。 預設為true。 |
| 物件 *可選，但建議* | email_notifications | 定義可用Livefyre電子郵件通知的頻率。 可以為每個通知類型設定不同的頻率。 依預設，不會傳送任何通知。 <br><ul><li> 會立即在列出的事件時發出通知。 </li><li>通常會以批次發出通知。 </li><li> 絕不會傳送活動的電子郵件通知。 </li><li>*注釋*:定義當其他使用者將此使用者追隨的內容張貼至系列時，傳送通知的時間。 </li><li>*回覆*:定義當其他使用者回覆此使用者內容時傳送通知的時間。</li><li>*按贊*:定義當其他使用者按贊此使用者的內容時傳送通知的時間。</li><li>*協調者注釋*:定義當使用者將內容張貼至網路中任何系列時，通知傳送給協調者的時間。</li><li>*協調者_flags*:定義當其他使用者標幟網路中任何系列的內容時，通知傳送給協調者的時間。</li></ul> |
| 字串可 *選* | 位置 | 使用者提交的位置。 |
| 字串可 *選* | 生物 | 使用者提交的自傳。 |
| 陣列可 *選* | 網站 | 使用者提交的網站陣列。 最大值= 2。 |
| 物件選 *用* | display_rules | 定義哪些描述檔屬性可公開顯示給其他使用者。 每個可用參數都採用布林輸入true或false。 可用參數：  <br><ul><li>生物 </li><li> 位置</li><li>  性別 </li><li>nameimage </li><li> remote_profile_url</li></ul> |
| 布林值可 *選* | 協調者 | 定義用戶是否具有跨網路的協調者權限。 |
| 布林值可 *選* | gravatar_disabled | 定義如果未提供image_url，是否停用Livefyre對gravatar的使用。 |

## 範例回應 {#section_uxt_3dd_mz}

```
{
 "id": "1234567890",
 "display_name": "Bob Dole",
 "name": {
   "formatted": "Bob Joseph Dole",
   "first": "Bob",
   "middle": "Joseph",
   "last": "Dole"
 },
   "email": "bob@dole.com",
   "image_url": "https://dole.com/images/bob.jpg",
   "profile_url": "https://site.com/bobdole",
   "settings_url":"https://site.com/settings",
   "tags": ["bob", "dole"],
   "autofollow_conversations": "true",
   "email_notifications": {
      "comments": "never",
      "replies": "immediately",
      "likes": "often",
      "moderator_comments": "immediately",
      "moderator_flags": "immediately" 
 },
  "location": "Washington D.C., USA",
  "bio": "Bob Dole speaks in the third person",
  "websites": ["https://dole.com/blog/", "https://bobdolerocks.com"],
  "display_rules": {
      "bio": "false",
      "location": "false",
      "gender": "false",
      "name": "false",
      "image": "false",
      "remote_profile_url": "false"
  },
  "moderator": "true",
  "gravatar_disabled": "false"
}
```
