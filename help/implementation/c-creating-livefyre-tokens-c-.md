---
description: 瞭解如何使用「C#」語言產生Livefyre Token。
seo-description: 瞭解如何使用「C#」語言產生Livefyre Token。
seo-title: 建立Livefyre Tokens'C#'
solution: Experience Manager
title: 建立Livefyre Tokens'C#'
uuid: c5e05625-8550-4b51-9211-134600e20ec7
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# 建立Livefyre Tokens C\# {#creating-livefyre-tokens-c}

瞭解如何使用 ``C#`` 語言產生 Livefyre 權杖。

您可以利用舊版文件和範例程式碼 `C#.NET` 來編寫方法來建立Token。

若要參照Livefyre的官方程式庫，請使用 [Java Library](https://github.com/Livefyre/livefyre-java-utils) 做為 `C#` 開發人員的起點。

您也可以考慮從命令列使用 [Node. js Library](https://github.com/Livefyre/livefyre-nodejs-utils) 來產生參考Token，並熟悉方法結構。

* [跳至系列中繼標記](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-collectionMeta-token)
* [跳至Auth Token](https://gist.github.com/gibron/56cb9c7060bf4816c4c5#the-auth-token)

## 相依性 {#section_c15_fnh_xz}

* 您需要專案中 [的JWT nutget套件](https://www.nuget.org/packages/JWT) 才能產生Token。
* 此頁面上的程式碼範例使用 [NewTonSoft JSON](https://www.nuget.org/packages/newtonsoft.json/) 套件。

## CollectionMeta Token {#section_dzt_4mh_xz}

當您將Comments嵌入頁面時，CollectionMeta Token會傳遞至Livefyre，並為您的新系列提供必要中繼資料。此外，您還會建立此資料的MD5 `checksum` ，Livefyre會檢查中繼資料是否已變更。(例如，如果您的文章的標題或URL已編輯)。

此代號由您的 `Site Key`技術帳戶經理在Livefyre提供給您。

另請參閱:

* Official CollectionMeta Token Docs
* [範例Gist](https://gist.github.com/pcolombo/dbbea020618c521a2bd5)

1. 建立包含系列中繼資料的Diconary。我們只會新增這個步驟中的一些必要欄位，在新增articleID之前，我們想要建立此物件的核取總和。

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

   * **必要標題****：系列的標題，通常是文章的標題。最大長度為255個字元。不支援html實體。請使用UTF-8編碼特殊字元。
   * **需要url****：文章的標準URL。這會用於留言共用和社交同步功能，以及管理控制面板中的文章連結。如果在本機測試，請注意Livefyre不會接受'localhost'做為網域。
   * **標記***可選*：您要在Livefyre儀表板中新增至系列的逗號分隔標籤清單。標記不能包含空格。如果您希望空間出現在管理控制面板中，請使用底線。
   * **類型***可選*：一個字串，用以指出要建立哪一種系列。有效值為：

      * `reviews`
      * `sidenotes`
      * `ratings`
      * `counting`
      * `livecomments`
      * `liveblog`
      * `livechat`
      如果未指定，則會預設建立LiveComplients系列。


1. JSON會編碼此字典，並產生md結帳的總和。

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

1. 將 **articleID** 新增至字典。**checksum** 不會進入collectionMeta Token，但應作為Consepfig js物件中的seap參數傳送。

   ```
       meta.Add("articleId", "article-abcde00001"); 
   ```

   * **需要articleID****：您的Livefyre網站內系列的唯一識別碼。通常，您的CMS中使用的唯一articleID。(例如您的WordPress貼文ID)此值不應變更。Livefyre透過結合SiteID和ArticleId來識別獨特的系列。

1. 使用Livefyre提供的網站金鑰，產生字典的JWT Token。請注意，您必須指定正確的雜湊演算法，因為JWT套件預設不會使用HS256。

   ```
       string token = JWT.JsonWebToken.Encode(meta, siteSecret, JWT.JwtHashAlgorithm.HS256);
   ```

## 使用者驗證Token {#section_g1d_43h_xz}

使用者驗證Token可用來將使用者簽署至Livefyre。當使用者登入您的網站時，網站會產生使用者驗證Token，該Token會傳遞至頁面上的Livefyre Widget。(如需驗證程序的詳細資訊，請參閱遠端描述檔)。

此代號需要您的網路名稱(網路. fyre. co)，並使用Livefyre的技術帳戶管理員提供給您的網路金鑰進行簽署。

另請參閱:

* 官方Auth Token文件
* [範例Gist](https://gist.github.com/pcolombo/7d7403172c28734c87e2)

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

   * **網域：** 您的網路名稱(由Livefyre提供)。e. g mynetwork. fyre. co
   * **user_ id：** 您網站設定檔系統中使用者的唯一使用者ID。必須僅為英數字元(A-Z、a-z、0-9)。如果您的系統使用者ID包含無效的charaacters，請考慮傳送使用者ID的md雜湊，或其基本64編碼版本。(請讓您的帳戶管理員知道您是否這麼做)。
   * **過期：** 代號過期的日期(在Epoch時間)。這應符合您網站登入的作業時間，因此Livefyre的登入狀態會與您網站的登入狀態保持同步。
   * **display_ name：** 描述檔系統中使用者的顯示名稱，因為該名稱應該顯示在留言流中。

1. 使用Livefyre提供的網路金鑰，產生字典的JWT Token。請注意，您必須指定正確的雜湊演算法，因為JWT套件預設不會使用HS256。

   ```
          string token = JWT.JsonWebToken.Encode(payload, networkKey, JWT.JwtHashAlgorithm.HS256);
   ```
