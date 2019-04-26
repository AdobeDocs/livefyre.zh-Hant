---
description: 安裝Livefyre伺服器端任務的程式庫
seo-description: 安裝Livefyre伺服器端任務的程式庫
seo-title: 安裝
solution: Experience Manager
title: 安裝
uuid: f60b4cc7-178f-4a16-ba75-f1 d0 d171 c52 f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 安裝{#installation}


## Java {#section_yd3_3zk_rz}

若要安裝Java程式庫，請將此相依性新增至專案的POM：

```
<dependency> 
   <groupId>com.livefyre</groupId> 
   <artifactId>livefyre</artifactId> 
   <version>2.0.3</version> 
</dependency>
```

Java程式庫具有下列模組的相依性：

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

如需詳細資訊，請閱讀Java文件或查看 [GitHub的來源](https://github.com/Livefyre/livefyre-java-utils)。

## NodeJS {#section_swj_pwq_rz}

若要安裝NodeJS程式庫，請執行此行：

`$ npm install livefyre`

NodeJS程式庫具有下列模組的相依性：

```
"restler":">=3.2.0", 
"validator":"=3.5.0", 
"jsonwebtoken": ">=5.0.0" 
```

如需詳細資訊，請閱讀nodeJS文件或查看 [GitHub的來源](https://github.com/Livefyre/livefyre-nodejs-utils)。

連結： [Restler](https://github.com/danwrong/restler)、 [Validator](https://www.npmjs.org/package/validator)、 [jsonWebten](https://github.com/auth0/node-jsonwebtoken).

## PHP {#section_txj_xwq_rz}

若要使用Composer安裝PHP程式庫，請將此項目新增至composer. json：

```
"require": { 
   "livefyre/livefyre-php-utils": "2.0.4" 
}
```

然後使用下列項目安裝：

```
composer.phar install 
```

如果您 **未** 使用Composer，請使用下列項目取得最新版本的程式庫：

```
git clone https://github.com/Livefyre/livefyre-php-utils 
```

若要使用程式庫，請將下列內容新增至您的PHP指令碼：

```
require_once("/path/to/livefyre-php-utils/src/Livefyre.php"); 
```

PHP程式庫具有下列模組的相依性：

```
"ext-json": "*", 
"rmccue/requests": ">=1.0" 
"firebase/php-jwt": ">=2.0" 
```

如需詳細資訊，請閱讀PHP文件或查看 [GitHub的來源](https://github.com/Livefyre/livefyre-php-utils)。

連結： [ext-json](https://php.net/manual/en/book.json.php)， [Requests](https://github.com/rmccue/Requests/)， [PHP-JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)

## Python {#section_irk_fxq_rz}

若要安裝Python程式庫，請執行此行：

`$ pip install livefyre`

Python程式庫具有下列模組的相依性：

```
PyJWT >= 1.0.1  
requests >= 2.2.1  
python-dateutil >= 2.2  
enum34 == 1.0  
ordereddict == 1.1 if sys.version_info[:2] < 2.7 
```

如需詳細資訊，請閱讀Python文件或查看 [GitHub的來源](https://github.com/Livefyre/livefyre-python-utils)。

連結： [PyjWT](https://github.com/progrium/pyjwt)， [Requests](https://github.com/kennethreitz/requests)， [Python-Datetil](https://pypi.python.org/pypi/python-dateutil)， [enum34](https://pypi.python.org/pypi/enum34)， [orderedDict](https://pypi.python.org/pypi/ordereddict)

## Ruby {#section_fv2_tzq_rz}

若要安裝Ruby程式庫，請將此行新增至應用程式的GemFile：

```
gem 'livefyre' 
```

或者自行安裝：

`$ gem install livefyre`

Ruby程式庫具有下列模組的相依性：

```
"jwt", '~> 1.4', ">= 1.4.1"  
"rest-client", '~> 1.8', ">= 1.8.0"  
"addressable", '~> 2.3', ">= 2.3.6" 
```

如需詳細資訊，請閱讀Ruby文件或查看 [GitHub來源](https://github.com/Livefyre/livefyre-ruby-utils)。

連結： [Ruby JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)， [REST Client](https://github.com/rest-client/rest-client/)， [Addressable](https://github.com/sporkmonger/addressable)
