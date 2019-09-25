---
description: 安裝Livefyre伺服器端工作的程式庫
seo-description: 安裝Livefyre伺服器端工作的程式庫
seo-title: 安裝
solution: Experience Manager
title: 安裝
uuid: f60b4cc7-178f-4a16-ba75-f1d0d171c52f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 安裝{#installation}


## Java {#section_yd3_3zk_rz}

若要安裝Java程式庫，請將此相依性新增至專案的POM:

```
<dependency> 
   <groupId>com.livefyre</groupId> 
   <artifactId>livefyre</artifactId> 
   <version>2.0.3</version> 
</dependency>
```

Java庫與以下模組有相關性：

```
<dependency> 
   <groupId>com.sun.jersey</groupId> 
   <artifactId>jersey-client</artifactId> 
   <version>[1.18.1,)</version> 
</dependency> 
<dependency> 
   <groupId>com.google.code.gson</groupId> 
   <artifactId>gson</artifactId> 
   <version>[2.3,)</version> 
</dependency> 
<dependency> 
   <groupId>com.google.guava</groupId> 
   <artifactId>guava</artifactId> 
   <version>[18.0,)</version> 
</dependency> 
<dependency> 
   <groupId>org.apache.commons</groupId> 
   <artifactId>commons-lang3</artifactId> 
   <version>[3.0.1,)</version> 
</dependency> 
<dependency> 
   <groupId>org.bitbucket.b_c</groupId> 
   <artifactId>jose4j</artifactId> 
   <version>[0.4.1,)</version> 
</dependency> 
```

如需詳細資訊，請閱讀Java檔案或查看 [GitHub上的來源](https://github.com/Livefyre/livefyre-java-utils)。

## NodeJS {#section_swj_pwq_rz}

要安裝NodeJS庫，請運行以下行：

`$ npm install livefyre`

NodeJS庫與以下模組有相關性：

```
"restler":">=3.2.0", 
"validator":"=3.5.0", 
"jsonwebtoken": ">=5.0.0" 
```

如需詳細資訊，請閱讀NodeJs檔案或在 [GitHub上查看來源](https://github.com/Livefyre/livefyre-nodejs-utils)。

連結： [Restler](https://github.com/danwrong/restler)、 [Validator](https://www.npmjs.org/package/validator)、 [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken)。

## PHP {#section_txj_xwq_rz}

若要安裝含Composer的PHP程式庫，請將它新增至您的composer.json:

```
"require": { 
   "livefyre/livefyre-php-utils": "2.0.4" 
}
```

然後使用：

```
composer.phar install 
```

如果您不 **使用** Composer，請使用下列程式庫取得最新版本：

```
git clone https://github.com/Livefyre/livefyre-php-utils 
```

若要使用程式庫，請將下列項目新增至PHP指令碼：

```
require_once("/path/to/livefyre-php-utils/src/Livefyre.php"); 
```

PHP庫具有對以下模組的依賴性：

```
"ext-json": "*", 
"rmccue/requests": ">=1.0" 
"firebase/php-jwt": ">=2.0" 
```

如需詳細資訊，請閱讀PHP檔案或查看 [GitHub上的來源](https://github.com/Livefyre/livefyre-php-utils)。

連結： [ext-json](https://php.net/manual/en/book.json.php)、 [Requests](https://github.com/rmccue/Requests/)、 [PHP-JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)

## Python {#section_irk_fxq_rz}

要安裝Python庫，請運行以下行：

`$ pip install livefyre`

Python庫具有對以下模組的依賴性：

```
PyJWT >= 1.0.1  
requests >= 2.2.1  
python-dateutil >= 2.2  
enum34 == 1.0  
ordereddict == 1.1 if sys.version_info[:2] < 2.7 
```

如需詳細資訊，請閱讀Python檔案或在 [GitHub上查看來源](https://github.com/Livefyre/livefyre-python-utils)。

連結：Py JWT [、](https://github.com/progrium/pyjwt)Requests [、](https://github.com/kennethreitz/requests)Python-Dateutil [、](https://pypi.python.org/pypi/python-dateutil)[](https://pypi.python.org/pypi/enum34)[Enum 34Dict、OrderedOrderedDit](https://pypi.python.org/pypi/ordereddict)

## Ruby {#section_fv2_tzq_rz}

要安裝Ruby庫，請將此行添加到應用程式的Gemfile中：

```
gem 'livefyre' 
```

或自行安裝：

`$ gem install livefyre`

Ruby庫具有下列模組的依賴性：

```
"jwt", '~> 1.4', ">= 1.4.1"  
"rest-client", '~> 1.8', ">= 1.8.0"  
"addressable", '~> 2.3', ">= 2.3.6" 
```

如需詳細資訊，請閱讀Ruby檔案或查看 [GitHub上的來源](https://github.com/Livefyre/livefyre-ruby-utils)。

連結： [Ruby JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)、 [REST客戶端](https://github.com/rest-client/rest-client/)、可 [定址](https://github.com/sporkmonger/addressable)
