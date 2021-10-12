---
description: 安裝Livefyre伺服器端工作的程式庫
title: 安裝
exl-id: d74f85be-14c0-4f6d-8f16-b688282c0eb0
source-git-commit: 3091db9d7b9611e26ad65c1432856c9465694e92
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

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

Java庫對以下模組具有依賴性：

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

如需詳細資訊，請參閱Java檔案，或參閱[GitHub](https://github.com/Livefyre/livefyre-java-utils)上的來源。

## NodeJS {#section_swj_pwq_rz}

若要安裝NodeJS程式庫，請執行以下這一行：

`$ npm install livefyre`

NodeJS程式庫與下列模組有相依性：

```
"restler":">=3.2.0", 
"validator":"=3.5.0", 
"jsonwebtoken": ">=5.0.0" 
```

如需詳細資訊，請參閱NodeJs檔案，或查看[GitHub](https://github.com/Livefyre/livefyre-nodejs-utils)上的來源。

連結：[Restler](https://github.com/danwrong/restler), [驗證器](https://www.npmjs.org/package/validator), [jsonwebtoken](https://github.com/auth0/node-jsonwebtoken)。

## PHP {#section_txj_xwq_rz}

若要使用撰寫器安裝PHP程式庫，請將此程式庫新增至您的composer.json :

```
"require": { 
   "livefyre/livefyre-php-utils": "2.0.4" 
}
```

然後使用安裝：

```
composer.phar install 
```

如果您使用撰寫器&#x200B;**not**，請使用取得程式庫的最新版本：

```
git clone https://github.com/Livefyre/livefyre-php-utils 
```

要使用庫，請將以下內容添加到PHP指令碼中：

```
require_once("/path/to/livefyre-php-utils/src/Livefyre.php"); 
```

PHP庫對以下模組具有依賴性：

```
"ext-json": "*", 
"rmccue/requests": ">=1.0" 
"firebase/php-jwt": ">=2.0" 
```

如需詳細資訊，請閱讀PHP檔案，或參閱[GitHub](https://github.com/Livefyre/livefyre-php-utils)上的來源。

連結：[ext-json](https://www.php.net/manual/en/book.json.php), [Requests](https://github.com/rmccue/Requests/), [PHP-JWT](https://github.com/firebase/php-jwt/tree/v2.0.0)

## Python {#section_irk_fxq_rz}

要安裝Python庫，請運行以下行：

`$ pip install livefyre`

Python庫對以下模組具有依賴性：

```
PyJWT >= 1.0.1  
requests >= 2.2.1  
python-dateutil >= 2.2  
enum34 == 1.0  
ordereddict == 1.1 if sys.version_info[:2] < 2.7 
```

如需詳細資訊，請閱讀Python檔案，或查看[GitHub](https://github.com/Livefyre/livefyre-python-utils)上的來源。

連結：[PyJWT](https://github.com/progrium/pyjwt), [Requests](https://github.com/kennethreitz/requests), [Python-Dateutil](https://pypi.python.org/pypi/python-dateutil), [Enum34](https://pypi.python.org/pypi/enum34), [OrderedDict](https://pypi.python.org/pypi/ordereddict)

## 魯比 {#section_fv2_tzq_rz}

要安裝Ruby庫，請將此行添加到應用程式的Gemfile中：

```
gem 'livefyre' 
```

或者自行安裝：

`$ gem install livefyre`

Ruby庫對以下模組具有依賴性：

```
"jwt", '~> 1.4', ">= 1.4.1"  
"rest-client", '~> 1.8', ">= 1.8.0"  
"addressable", '~> 2.3', ">= 2.3.6" 
```

有關詳細資訊，請閱讀Ruby文檔，或查看[GitHub](https://github.com/Livefyre/livefyre-ruby-utils)上的源。

連結：[Ruby JWT](https://github.com/firebase/php-jwt/tree/v2.0.0), [REST客戶端](https://github.com/rest-client/rest-client/), [可定址](https://github.com/sporkmonger/addressable)
