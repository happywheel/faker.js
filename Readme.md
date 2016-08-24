# faker.js - 在浏览器或者nodejs生成模拟数据
![Faker.js](http://imgur.com/KiinQ.png)

[![Build Status](https://travis-ci.org/Marak/faker.js.svg?branch=master)](https://travis-ci.org/Marak/faker.js)

[![npm version](https://badge.fury.io/js/faker.svg)](http://badge.fury.io/js/faker)

## Demo

[http://marak.com/faker.js/](http://marak.com/faker.js/)

## 托管API微服务

[http://faker.hook.io](http://faker.hook.io/)
 - Supports all Faker API Methods
 - Full-Featured Microservice
 - Hosted by [hook.io](http://hook.io)

```bash
curl http://faker.hook.io?property=name.findName&locale=de
```

## 用法

### 浏览器

    <script src = "faker.js" type = "text/javascript"></script>
    <script>
      var randomName = faker.name.findName(); // Caitlyn Kerluke
      var randomEmail = faker.internet.email(); // Rusty@arne.info
      var randomCard = faker.helpers.createCard(); // random contact card containing many properties
    </script>

### Node.js

    var faker = require('faker');

    var randomName = faker.name.findName(); // Rowan Nikolaus
    var randomEmail = faker.internet.email(); // Kassandra.Haley@erich.biz
    var randomCard = faker.helpers.createCard(); // random contact card containing many properties

## API文档


### Faker.fake()

faker.js contains a super useful generator method `Faker.fake` for combining faker API methods using a mustache string format.

**Example:**

``` js
console.log(faker.fake("{{name.lastName}}, {{name.firstName}} {{name.suffix}}"));
// outputs: "Marks, Dean Sr."
```

This will interpolate the format string with the value of methods `name.lastName()`, `name.firstName()`, and `name.suffix()`

### JSDoc API Browser

[http://marak.github.io/faker.js/](http://marak.github.io/faker.js/)

### API Methods

* address-地址
  * zipCode-邮编
  * city-城市
  * cityPrefix-城市前缀
  * citySuffix-城市后缀
  * streetName-街道名字
  * streetAddress-街道地址
  * streetSuffix-街道前缀
  * streetPrefix-街道后缀
  * secondaryAddress-二级地址
  * county-县
  * country-国家
  * countryCode-国家代码
  * state-州
  * stateAbbr州缩写
  * latitude-纬度
  * longitude-经度
* commerce-电子商务
  * color-颜色
  * department-部门
  * productName-产品名称
  * price-价格
  * productAdjective-产品形容词
  * productMaterial-产品材料
  * product-产品
* company-公司
  * suffixes-后缀
  * companyName-公司名称
  * companySuffix-公司后缀名
  * catchPhrase-标语
  * bs-
  * catchPhraseAdjective标语形容词
  * catchPhraseDescriptor口号描述
  * catchPhraseNoun
  * bsAdjective
  * bsBuzz
  * bsNoun
* date-日期
  * past-过去
  * future-未来
  * between-期间
  * recent-最近
  * month-月份
  * weekday-平日
* fake
 * finance 金融
  * account 账户 
  * accountName 用户名
  * mask 
  * amount
  * transactionType
  * currencyCode 货币代码
  * currencyName 货币名称
  * currencySymbol 货币符号
  * bitcoinAddress 比特币地址
* hacker 黑客
  * abbreviation 缩写
  * adjective 形容词
  * noun 名词
  * verb 动词
  * ingverb 
  * phrase 短语
* helpers 助手
  * randomize 随机化
  * slugify
  * replaceSymbolWithNumber 替换符号编号
  * replaceSymbols 符号替换
  * shuffle 洗牌
  * mustache 
  * createCard
  * contextualCard
  * userCard
  * createTransaction
* image 图片
  * image
  * avatar 头像 
  * imageUrl 图片地址
  * abstract 抽象
  * animals 动物
  * business 业务
  * cats 猫
  * city 城市
  * food 食物
  * nightlife 夜生活
  * fashion 时尚
  * people 人
  * nature 自然
  * sports 运动 
  * technics 工艺
  * transport 运输
* internet 互联网
  * avatar 头像
  * email 电子邮箱
  * exampleEmail 示例邮箱
  * userName 用户名
  * protocol 协议
  * url 网址
  * domainName 域名
  * domainSuffix 域字
  * domainWord 域名后缀
  * ip 
  * userAgent 用户代理
  * color 颜色
  * mac mac地址
  * password 密码
* lorem
  * word 字
  * words 话
  * sentence 句子
  * sentences 
  * paragraph 
  * paragraphs 段落
  * text 文本
  * lines
* name 姓名
  * firstName 名
  * lastName 姓
  * findName 
  * jobTitle 职称
  * prefix 字首
  * suffix 后缀
  * title 标题
  * jobDescriptor
  * jobArea
  * jobType
* phone 电话
  * phoneNumber 电话号码 
  * phoneNumberFormat 电话号码格式
  * phoneFormats 手机号码格式
* random 随机
  * number 数字
  * arrayElement 数组元素
  * objectElement 对象元素
  * uuid
  * boolean 布尔值
  * word 文字
  * words 语句
  * image 图片
  * locale 地区
  * alphaNumeric  字母数字
* system 系统
  * fileName 文件名
  * commonFileName 常见文件名
  * mimeType MIME类型
  * commonFileType 常见文件类型
  * commonFileExt 常见文件扩展名
  * fileType 文件类型
  * fileExt 文件扩展
  * directoryPath 目录路径
  * filePath 文件路径
  * semver


## Localization-本地化

As of version `v2.0.0` faker.js has support for multiple localities.

The default language locale is set to English.

Setting a new locale is simple:

```js
// sets locale to de
faker.locale = "de";
```

 * de
 * de_AT
 * de_CH
 * en
 * en_AU
 * en_BORK
 * en_CA
 * en_GB
 * en_IE
 * en_IND
 * en_US
 * en_au_ocker
 * es
 * es_MX
 * fa
 * fr
 * fr_CA
 * ge
 * id_ID
 * it
 * ja
 * ko
 * nb_NO
 * nep
 * nl
 * pl
 * pt_BR
 * ru
 * sk
 * sv
 * tr
 * uk
 * vi
 * zh_CN
 * zh_TW


### Individual Localization Packages

As of vesion `v3.0.0` faker.js supports incremental loading of locales. 

By default, requiring `faker` will include *all* locale data.

In a production environment, you may only want to include the locale data for a specific set of locales.

```js
// loads only de locale
var faker = require('faker/locale/de');
```

## Tests

    npm install .
    make test

You can view a code coverage report generated in coverage/lcov-report/index.html.

## Projects Built with faker.js

### Fake JSON Schema - 模拟JSON schema

Use faker generators to populate JSON Schema samples.
使用faker生成 数据填充json模型 样本
See: https://github.com/pateketrueke/json-schema-faker/

### CLI

Run faker generators from Command Line.
在命令行中运行faker生成器
See: https://github.com/lestoni/faker-cli

**Want to see your project added here? Let us know!**

### Meteor

#### Meteor Installation

```
meteor add practicalmeteor:faker
```

#### Meteor Usage, both client and server

```js
var randomName = faker.name.findName(); // Rowan Nikolaus
var randomEmail = faker.internet.email(); // Kassandra.Haley@erich.biz
var randomCard = faker.helpers.createCard(); // random contact card containing many properties
```

## Building faker.js

faker uses [gulp](http://gulpjs.com/) to automate it's build process. Running the following build command will generate new browser builds, documentation, and code examples for the project.

```
npm run-script build
```

## Building JSDocs

```
npm run-script doc
```

## Version Release Schedule

faker.js is a popular project used by many organizations and individuals in production settings. Major and Minor version releases are generally on a monthly schedule. Bugs fixes are addressed by severity and fixed as soon as possible.

If you require the absolute latest version of `faker.js` the `master` branch @ http://github.com/marak/faker.js/ should always be up to date and working.

## Maintainer

#### Marak Squires

faker.js - Copyright (c) 2016
Matthew Bergman & Marak Squires
http://github.com/marak/faker.js/

faker.js was inspired by and has used data definitions from:

 * https://github.com/stympy/faker/ - Copyright (c) 2007-2010 Benjamin Curtis
 * http://search.cpan.org/~jasonk/Data-Faker-0.07/ - Copyright 2004-2005 by Jason Kohles

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
"Software"), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


