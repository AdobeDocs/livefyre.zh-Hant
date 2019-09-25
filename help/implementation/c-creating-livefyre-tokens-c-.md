---
description: 瞭解如何使用「C#」語言產生Livefyre Token。
seo-description: 瞭解如何使用「C#」語言產生Livefyre Token。
seo-title: 建立Livefyre Token 'C#'
solution: Experience Manager
title: 建立Livefyre Token 'C#'
uuid: c5e05625-8550-4b51-9211-134600e20ec7
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Creating Livefyre Tokens C\# {#creating-livefyre-tokens-c}

瞭解如何使用 ``C#`` 語言產生 Livefyre Token。

您可以運用舊版檔案和范常式式碼來 `C#.NET` 編寫方法來建立Token。

若要參考Livefyre的官方資料庫，請使用 [Java資料庫](https://github.com/Livefyre/livefyre-java-utils) ，做為開發人員的 `C#` 起點。

您也可以考慮從命令行使用 [Node.js庫](https://github.com/Livefyre/livefyre-nodejs-utils) ，為自己生成參考Token，並熟悉方法結構。

* [跳至系列Meta Token](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [跳至驗證Token](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## 相依性 {#section_c15_fnh_xz}

* 您需要專案 [中的JWT nuget套件](https://www.nuget.org/packages/JWT) ，才能產生Token。
* 本頁的程式碼範例使用 [Newtonsoft JSON套件](https://www.nuget.org/packages/newtonsoft.json/) 。

## CollectionMeta Token {#section_dzt_4mh_xz}

當您在頁面上內嵌「注釋」時，CollectionMeta Token會傳遞至Livefyre，並為我們的系統提供新系列的必要中繼資料。 此外，您還將建立此資料的MD5 `checksum` ,Livefyre會檢查此資料，以查看中繼資料是否已變更。 （例如，您文章的標題或URL已編輯）。

此代號會與您簽署， `Site Key`由Livefyre的Technical帳戶管理員提供給您。

另請參閱:

* 正式系列中繼Token檔案
* [示例Gist](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. 建立包含系列中繼資料的字典。 我們只會在此步驟中新增一些必要欄位，因為我們想在新增articleId之前，先建立此物件的校驗和。

   ```
       // Site Key provided by Livefyre 
       string siteSecret = "ABCDE1234"; 
   
       var meta = new Dictionary<string, object>() { 
           {"title", "Kings win the Stanley Cup"}, 
           {"url", "https://www.website.com/kings-win-stanley-cup"}, 
           {"tags", "sports, hockey, stanley_cup"}, 
           {"type", "livecomments"} 
       };
   ```

   * **需要** 標題 **: 系列的標題，通常是您文章的標題。 最大長度為255個字元。 不支援html實體。 請使用UTF-8編碼特殊字元。
   * **url必** 要 **: 您文章的標準URL。 此功能會用於留言分享和社交同步功能，以及從「管理控制面板」連結至您的文章。 如果在本機測試，請注意，Livefyre不會接受「localhost」做為網域。
   * **標籤***可選*: 您要新增至Livefyre控制面板中系列的逗號分隔標籤清單。 標籤不能包含空格。 如果您希望有空格出現在「管理」控制面板中，請使用底線。
   * **可選** 類型 **: 指示要建立之系列類型的字串。 有效值為:

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`
      如果未指定，則預設會建立LiveComments系列。


1. JSON會編碼此字典，並產生其md5總和。

   ```
          var metaStr = JsonConvert.SerializeObject(meta); 
       byte[] hash; 
   
       using (var md5 = MD5.Create()) 
       { 
           hash = md5.ComputeHash(Encoding.UTF8.GetBytes(metaStr)); 
       } 
   
       StringBuilder sBuilder = new StringBuilder(); 
   
       // Loop through each byte of the hashed data  
       // and format each one as a hexadecimal string  
       for (int i = 0; i < hash.Length; i++) 
       { 
           sBuilder.Append(hash[i].ToString("x2")); 
       } 
   ```

1. 將articleId **新增至** 「字典」。 checksum **不會** 進入collectionMeta Token，但應以convConfig js物件中的個別參數傳送。

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **articleId必** 要 **: Livefyre網站中系列的唯一識別碼。 通常是CMS中使用的唯一articleId。 （例如您的WordPress貼文ID）此值永遠不應變更。 Livefyre可結合siteId和articleId來識別唯一的系列。

1. 使用Livefyre提供給您的網站金鑰，產生字典的已簽署JWT Token。 請注意，您必須指定正確的雜湊演算法，因為JWT套件預設不使用HS256。

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## 使用者驗證Token {#section_g1d_43h_xz}

使用者驗證Token可用來將使用者登入Livefyre。 當使用者登入您的網站時，網站會產生一個使用者驗證Token，此Token會傳遞至頁面上的Livefyre介面工具集。 （有關驗證過程的詳細資訊，請參閱遠程配置檔案。）

此Token需要您的網路名稱(network.fyre.co)，並與您的網路金鑰簽署，該金鑰由Livefyre的技術客戶經理提供給您。

另請參閱:

* 正式驗證Token檔案
* [示例Gist](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

1. 建立包含必要資訊的字典。

   ```
       string networkKey = "ABCDEF1234"; 
   
       var payload = new Dictionary<string, object>() {  
               { "domain", "mynetwork.fyre.co" }, 
               { "user_id", "user-00001" }, 
               { "expires", DateTime.Now.AddDays(7).Ticks }, 
               { "display_name", "johndoe" } 
           }; 
   ```

   * **** 域：網路名稱（由Livefyre提供）。例如mynetwork.fyre.co
   * **** user_id:您網站描述檔系統中使用者的唯一使用者ID。 只能是英數字元(A-Z、a-z、0-9)。 如果您的系統使用者ID包含無效字元，請考慮傳送Livefyre和使用者ID的md5雜湊，或是它的base64編碼版本。 （如果您這麼做，請讓客戶經理知道。）
   * **** 過期：代號過期的日期（以紀元時間表示）。 這應符合您網站上登入的作業時間，如此Livefyre的登入狀態就會與您網站的登入狀態保持同步。
   * **** display_name:使用者在您的描述檔系統中的顯示名稱，應該顯示在注釋串流中。

1. 使用Livefyre提供給您的網路金鑰，產生字典的已簽署JWT Token。 請注意，您必須指定正確的雜湊演算法，因為JWT套件預設不使用HS256。

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
