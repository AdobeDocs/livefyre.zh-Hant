---
description: 建立用於提取回應的Ping回應，將更新的使用者資訊傳送至Livefyre。
seo-description: 建立用於提取回應的Ping回應，將更新的使用者資訊傳送至Livefyre。
seo-title: 建立用於提取回應的Ping
solution: Experience Manager
title: 建立用於提取回應的Ping
uuid: f90871d5-601f-40dc-b3 d2-ab78635 e4 a88
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 建立用於提取回應的Ping{#build-the-ping-for-pull-response}

建立用於提取回應的Ping回應，將更新的使用者資訊傳送至Livefyre。

| Type | 屬性 | 說明 |
|--- |--- |--- |
| *需要字串* | id | 個人資料系統使用者的使用者ID。這對您網路中所有使用者都必須是唯一的，而且絕不能變更。 |
| *需要字串* | display_ name | 使用者的顯示名稱。這會以使用者張貼的Livefyre內容呈現。 |
| 可 *選物件，但建議使用* | name | 字串來定義使用者的格式化、第一、中間和姓氏。 |
| 字串 *選用，但建議使用* | 電子郵件 | 使用者的電子郵件地址。用來傳送電子郵件通知。 |
| 字串 *選用，但建議使用* | image_ url | 要顯示給使用者的頭像URL。Livefyre會視需要將上傳的影像縮放為100×100、75×75或50×50像素。為獲得最佳結果，使用者應上傳一個正方形影像，大小為100×100像素。為了確保在Livefyre中更新頭像，請修改每個影像更新的image_ url，以便Ding for Draw偵測到影像已變更。例如，在檔案名稱加上時間戳記，或增加影像變更。注意：所有URL都必須具備完整資格和存取權。 |
| 字串 *選用，但建議使用* | profile_ url | 網站上使用者設定檔頁面的URL。 |
| 字串 *選用，但建議使用* | settings_ url | 使用者可為您的網站設定使用者設定檔設定的URL。 |
| Array *選用，但建議使用* | 標記 | 用來指派使用者給使用者群組。標記可能包含1-63英數字元和底線字元。 |
| 布林 *值可選，但建議使用* | autofollow_ convertising | 定義使用者在張貼後是否希望自動跟隨系列。在關注系列後，使用者會在其他使用者參與時收到電子郵件通知。可以是true或false。預設為true。 |
| 可 *選物件，但建議使用* | email_ notifications | 定義可用的Livefyre電子郵件通知的頻率。每個通知類型可設定不同的頻率。依預設，不會傳送通知。 <br><ul><li> 立即在列出的事件上發出通知。 </li><li>通常會分批發出通知。 </li><li> 絕不會傳送活動的電子郵件通知。 </li><li>*注釋*：定義當其他使用者將內容張貼至此使用者所關注的系列時，傳送通知的時機。 </li><li>*回覆*：定義當其他使用者回覆此使用者內容時，傳送通知的時機。</li><li>*按贊*：定義當其他使用者按贊此使用者的內容時傳送通知時。</li><li>*協調者_ comments*：定義當使用者將內容張貼至網路中的任何系列時，通知傳送給協調者的時機。</li><li>*協調者_旗標*：定義當其他使用者標幟網路中任何「系列」中的內容時，傳送給協調者的通知。</li></ul> |
| 字串 *選用字串* | location | 使用者提交的位置。 |
| 字串 *選用字串* | bio | 使用者提交的自動攝影。 |
| 陣列 *選用* | 網站 | 使用者提交的網站陣列。最大值=2。 |
| 物件 *選擇性* | display_ rules | 定義其他使用者公開顯示的描述檔屬性。每個可用參數都採用布林輸入true或false。可用參數： <br><ul><li>bio </li><li> location</li><li>  性別 </li><li>nameimage </li><li> remote_ profile_ url</li></ul> |
| *布林選* | 協調者 | 定義使用者是否擁有網路上的協調者權限。 |
| *布林選* | gravar_ disabled | 定義如果未提供image_ url，是否停用Livefyre的使用位置。 |

## 回應範例 {#section_uxt_3dd_mz}

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
