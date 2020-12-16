---
description: 設定憑證，讓您的使用者可以將內容分享至各種社交網路。
seo-description: 設定憑證，讓您的使用者可以將內容分享至各種社交網路。
seo-title: 啟用社交共用
solution: Experience Manager
title: 啟用社交共用
uuid: f584a0ae-46c7-48c1-aea4-36da9f1e259b
translation-type: tm+mt
source-git-commit: d77b633b9892e3ea4aaec860317887f1fdf66830
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%

---


# 啟用社交共用{#enabling-social-sharing}

設定憑證，讓您的使用者可以將內容分享至各種社交網路。

若要允許使用者跨社交媒體網站分享內容，請實作Livefyre的「社交分享」功能，並建立OAuth系統，為這些網站提供適當的驗證。 透過此系統，當使用者選擇透過社交媒體分享內容時，Livefyre會代表使用者行事。

>[!NOTE]
>
>不同的提供者有不同的OAuth需求。 請洽詢您的供應商，以取得與其實作OAuth相關的資訊。

## 必要的社交憑證{#section_gff_cjm_b1b}

如果您使用自訂使用者識別系統，您必須提供您的社交認證，讓使用者能夠從Livefyre應用程式分享到Twitter、Facebook或LinkedIn。

>[!NOTE]
>
>使用Janrain Engage的客戶只需提供其Engage Domain和Engage API金鑰。

使用「管理控制台」的「整合設定」面板，輸入或更新下列社交憑證。

### 必要憑證：

* **** Facebook用戶端ID用戶端密碼OAuth代理重新導向
* **** LinkedInAPI金鑰API密碼
* **** TwitterAccess Token存取Token密碼API金鑰API密碼

## Twitter {#section_qp5_1yl_b1b}

Twitter認證可從「Twitter應用程式儀表板」取得。 要查找這些憑據，請執行以下操作：

* 開啟[Twitter的應用程式開發頁面](https://dev.twitter.com/apps)作為應用程式擁有者，尋找您的應用程式，然後按一下標題。
* 向下捲動至「您的存取Token」，並從「存取Token」和「存取Token密碼」擷取值。

您必須：

* 在Twitter應用程式中輸入回呼URL欄位的值。 雖然此欄位可能是簡單的預留位置，但不能保留為空白。
* 將「應用程式類型」設定為具有&#x200B;**read**&#x200B;和&#x200B;**write**&#x200B;訪問權。
* 確認Twitter應用程式網站URL與Livefyre核心應用程式位於相同的主機網域。

>[!NOTE]
>
>所有顯示Twitter內容的應用程式都必須遵循其顯示要求。 如需詳細資訊，請參閱[Twitter顯示准則](https://dev.twitter.com/terms/display-requirements)。

## LinkedIn {#section_lfz_zxl_b1b}

LinkedIn憑證可從LinkedIn應用程式API金鑰的「OAuth金鑰」區段取得。

* 從LinkedIn的「開發人員」頁面[https://developer.linkedin.com/](https://developer.linkedin.com/)登入您的帳戶。
* 將滑鼠指標暫留在右上角的名稱上，然後從下拉式選單中選取「API金鑰」。
* 按一下「應用程式」標題。
* 從「OAuth金鑰」區段擷取API金鑰和密碼金鑰值

## Facebook {#section_zyb_gpl_b1b}

您的「開發人員應用程式」頁面提供Facebook認證。

* 開啟[Facebook的開發人員應用程式頁面](https://developers.facebook.com/apps)作為應用程式擁有者，尋找您的應用程式，然後按一下標題。
* 擷取應用程式ID和應用程式密碼的值。 若是「應用程式密碼」，您可能需要按一下「顯示」按鈕才能顯示。

共用至Facebook需要您設定重新導向頁面，以接受Facebook請求並遵循[Facebook](https://developers.facebook.com/docs/reference/dialogs/oauth/)所要求的網域慣例。 頁面必須托管在您的網域上，Facebook才能確認請求來自合法來源。

### Facebook重新導向

代管頁面應包含下列程式碼：

### Ruby

這是使用Ruby和Rails執行Facebook OAuth重新導向的範例。

```ruby
require "base64" 
  
class Controller < ActionController::Base 
   def base64url_decode(str) 
      str.gsub! '-_', '+/' 
      Base64.decode64(str.ljust(str.length+str.length%4, '=')) 
   end 
  
   def index 
      lfoauth = params[:lfoauth] 
      if not lfoauth 
         render :status => :forbidden, :text => 'Missing lfoauth.' 
      end 
  
      redirect = base64url_decode lfoauth 
  
      match = /^(http:\/\/|https:\/\/)?([^\/?]+)/i.match(redirect) 
      host = match[2] 
  
         if not host.include? 'fyre.co' 
      render :status => :forbidden, :text => 'Invalid host.' 
         end 
  
         sep = (redirect.include? '?') ? '&' : '?' 
      params.delete :lfoauth 
  
         rdir = redirect + sep + params.to_query 
      redirect_to rdir 
   end 
end
```

### Python

這是使用Python和Django進行Facebook OAuth重新導向的範例。

```python
import base64, re 
from django.views.decorators.http import require_GET 
from django.http.response import HttpResponseRedirect, HttpResponseBadRequest 
  
def base64url_decode(st): 
    return base64.b64decode(re.sub("-_","+/", st).ljust(len(st)+len(st)%4, '=')) 
  
@require_GET 
def handle_lfoauth(request): 
    lfoauth = request.GET.get('lfoauth', None) 
    import pdb; pdb.set_trace() 
    if not lfoauth: 
        return HttpResponseBadRequest('Missing lfoauth.') 
     
    redirect = base64url_decode(lfoauth) 
     
    match = re.match(r"^(http:\/\/|https:\/\/)?([^\/?]+)", redirect, re.IGNORECASE) 
    host = match.group(2) 
     
    # validate the destination to secure this proxy 
    if not 'fyre.co' in host: 
        return HttpResponseBadRequest('Invalid host.') 
     
    # if params were included in the uri already, append with &, otherwise ? 
    sep = '&' if '?' in redirect else '?' 
     
    # remove lfoauth from query param 
    dict_ = request.GET.copy() 
    dict_.pop('lfoauth') 
  
    # attach remaining param to redirect 
    rdir = redirect + sep + dict_.urlencode() 
  
    # this does the actual redirection 
    return HttpResponseRedirect(rdir)
```

### NodeJS

這是使用NodeJS和Sail/Express進行Facebook OAuth重新導向的範例。

```nodejs
/* 
 * 
 */ 
var S = require('string'), 
     querystring = require('querystring'); 
  
var base64UrlDecode = function(str) { 
     var temp = S(str.replace('-_', '+/')).padRight(str.length+(str.length%4), '=').s 
     return new Buffer(temp, 'base64').toString('utf8'); 
} 
  
module.exports = { 
  index: function(req, res) { 
     var lfoauth = req.param('lfoauth'); 
  
     if (typeof lfoauth === 'undefined') { 
        res.send(400, 'Missing lfoauth.'); 
     } 
  
     var redirect = base64UrlDecode(lfoauth); 
  
     var match = redirect.match(/^(http:\/\/|https:\/\/)?([^\/?]+)/i); 
     var host = match[2] 
  
     if (host.indexOf('fyre.co') <= -1) { 
        res.send(400, 'Invalid host.'); 
     } 
  
     var sep = redirect.indexOf('?') > -1 ? '&' : '?'; 
  
     delete req.query['lfoauth']; 
     var rdir = redirect + sep + querystring.stringify(req.query); 
  
     res.redirect(rdir); 
  }, 
  
  _config: {} 
};
```

### Java

這是使用Java和Spring控制器執行Facebook OAuth重新導向的範例。

```java
/* 
 *  
 */ 
import java.util.Collection; 
import java.util.HashMap; 
import java.util.Map; 
import java.util.regex.Matcher; 
import java.util.regex.Pattern; 
  
import org.apache.commons.codec.binary.Base64; 
import org.apache.commons.lang.StringUtils; 
import org.jboss.resteasy.spi.BadRequestException; 
import org.springframework.stereotype.Controller; 
import org.springframework.web.bind.annotation.RequestMapping; 
import org.springframework.web.bind.annotation.RequestParam; 
import org.springframework.web.servlet.View; 
import org.springframework.web.servlet.view.RedirectView; 
  
@Controller 
public class RedirectController { 
    @RequestMapping("/fbredirect") 
    public View facebook(@RequestParam Map<string,object> allRequestParams) { 
        if (!allRequestParams.containsKey("lfoauth")) { 
            throw new BadRequestException("Missing lfoauth."); 
        } 
             
        String redirect = base64UrlDecode((String) allRequestParams.get("lfoauth")); 
  
        Pattern p = Pattern.compile("^(http:\\/\\/|https:\\/\\/)?([^\\/?]+)", Pattern.CASE_INSENSITIVE); 
        Matcher m = p.matcher(redirect); 
        if (!m.find() || !m.group(2).contains("fyre.co")) { 
            throw new BadRequestException("Invalid host."); 
        } 
         
        Map<string, object=""> params = new HashMap<string, object="">(allRequestParams); 
        params.remove("lfoauth"); 
        String rdir = redirect + (redirect.contains("?") ? '&' : '?') + mapToQueryString(params); 
         
        return new RedirectView(rdir); 
    } 
     
    private String base64UrlDecode(String str) { 
        return new String(Base64.decodeBase64(StringUtils.rightPad(str.replaceAll("-_", "+/"), str.length()+(str.length()%4), '='))); 
    } 
     
    private String mapToQueryString(Map<string, object=""> map) { 
        String queryparam = ""; 
        for (String key : map.keySet()) { 
            if (map.get(key) instanceof Collection) { 
                for (Object item : (Collection) map.get(key)) { 
                    queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, item.toString())); 
                } 
            } else { 
                queryparam = queryparam.concat(String.format("%1$s=%2$s&", key, map.get(key).toString())); 
            } 
        } 
        return StringUtils.removeEnd(queryparam, "&"); 
    } 
}
```

### PHP

```php
<?php 
/* 
Purpose: Provide a landing page for the last step of successful oAuth 
         that is on the correct (Facebook approved) domain. 
  
Location: This file should be hosted on the same domain as your  
          Facebook App's "site url". 
  
Input Parameters:  
    - (GET) lfoauth: This should be a url-safe base64-encoded URL that  
      is the "real" final redirection URL. Livefyre sets this. 
  
      For testing purposes, this can be set to a url-safe base64-encoded  
      URL of your choosing, but the domain name must end in .fyre.co in  
      order to be considered valid. 
  
    - (GET) [all other parameters]: Any other parameters should simply  
      be passed thru on the redirection URL. If the decoded URL from "lfoauth"  
      includes querystring parameters, then the additional parameters included  
      with the initial request should be appended with "&..." 
  
Output: The response should indicate that the browser redirect (302) to the  
        "real" URL which is encoded in the "lfoauth" parameter. 
  
*/ 
  
function base64url_decode($data) { 
  return base64_decode(str_pad(strtr($data, '-_', '+/'), strlen($data) % 4, '=', STR_PAD_RIGHT)); 
} 
  
if (isset($_GET['lfoauth'])) { 
    // Warning: If implemented with non-PHP, b64 may fail because we have  
    // stripped padding (trailing ='s), to comply with Facebook parameters.   
    // The decode needs to be non-strict in this sense. 
  
    $rdir = base64url_decode($_GET['lfoauth']); 
  
    // validate the destination to secure this proxy 
    preg_match("/^(https?:\/\/)?([^\/?]+)/i", $rdir, $domain_only);    
    $host = $domain_only[2]; 
    if (!strstr($host,'fyre.co')) { 
        echo "Error - this redirection is not allowed! ".$host; 
        exit; 
    } 
  
    // if params were included in the uri already, append with &, otherwise ? 
    $sep = strstr($rdir,'?') ? '&' : '?'; 
  
    // don't include this in the params we add to the redirect url 
    unset($_GET['lfoauth']); 
  
    // assemble a new querystring from the remaining inbound GET params 
    $rdir = $rdir.$sep.http_build_query($_GET); 
  
    // this does the actual redirection, PHP's implementation is weird 
    header('Location: '.$rdir); 
} 
?>
```

## 配置「貼文至」提供者{#section_rdk_dpl_b1b}

依預設，Facebook、LinkedIn和Twitter的「貼文至」按鈕會顯示在Livefyre核心應用程式上。 使用postToButtons參數來設定在內嵌Livefyre應用程式時，會出現哪些提供者。

```
var convConfig = {}; // Ignoring other options for this example 
convConfig.postToButtons = ['tw', 'fb', 'li']; // Or any subset of these 
fyre.conv.load(networkConfig, [convConfig], function() {}); 
```

`postToButtons` 是具有以下任意子集的陣列：

* tw:Twitter
* fb:Facebook
* 李：LinkedIn
