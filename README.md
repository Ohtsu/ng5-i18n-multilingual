

# _ng5-i18n-multilingual_ Angular5 internationalization sample
[![MIT License](http://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE)


_ng5-i18n-multilingual_ is a sample program for making multilingual sites by Angular5.

_Video Explanation(English)_
<https://youtu.be/74OCrD6Ckgg>

_Video Explanation(Japanese)_
<https://youtu.be/AUXpQvqGjeA>

_Demo Site_
<https://ohtsu.github.io/ng5-i18n-multilingual/>

_Full Source Code_
<https://github.com/Ohtsu/ng5-i18n-multilingual.git>

## Overview 
   - _ng5-i18n-multilingual_ is a sample program for making multilingual sites by Angular5.


## Prerequisite

   - Node.js
   - TypeScript2
   - Angular/Cli (for Angular5 or later)


## Installation


To install this program:

   - Make your own directory and change into it.

```bash
$ mkdir mydir
$ cd mydir
```
   - Make the clone as follows.

```bash
$ git clone https://github.com/Ohtsu/ng5-i18n-multilingual.git 
```

   - Change into _ng5-i18n-multilingual_ and run "npm install".

```bash
$ cd ng5-i18n-multilingual
$ npm install 
```

## Check by local server

### Start English (default) version


```bash
$ ng serve
```
And you will get the page below in your browser by accessing **http://localhost:4200**.  

  - ***First Page*** 

  <img src="https://raw.githubusercontent.com/Ohtsu/images/master/ng5-i18n-multilingual/ng5-i18n-multilingual_en_initial_page01.png" width= "640" >



### Start Japanese version 
Start the local server as follows. 

```bash
$ npm run start:ja
```

And you will get the page below in your browser by accessing **http://localhost:4200**.  

  - ***First Page*** 

 <img src="https://raw.githubusercontent.com/Ohtsu/images/master/ng5-i18n-multilingual/ng5-i18n-multilingual_ja_initial_page01.png" width= "640" >

### Start French version 
Start the local server as follows. 

```bash
$ npm run start:ja
```

And you will get the page below in your browser by accessing **http://localhost:4200**.  

  - ***First Page*** 

 <img src="https://raw.githubusercontent.com/Ohtsu/images/master/ng5-i18n-multilingual/ng5-i18n-multilingual_fr_initial_page01.png" width= "640" >


## How to make multilingual site date

```bash

    "build": "ng build --aot --output-path dist/ --base-href /ng5-i18n-multilingual/",
    "build:ja": "ng build --aot --output-path dist/ja --base-href /ng5-i18n-multilingual/ja/ --i18nFile=src/locale/messages.ja.xlf --i18nFormat=xlf --locale=ja",
    "build:fr": "ng build --aot --output-path dist/fr --base-href /ng5-i18n-multilingual/fr/ --i18nFile=src/locale/messages.fr.xlf --i18nFormat=xlf --locale=fr"

```



## Version

   - TypeScript         : 2.4.2
   - @angular/cli       : 1.5.0
   - Node               : 6.11.3


## Reference

- "Internationalization (I18N)",
<https://v2.angular.io/docs/ts/latest/cookbook/i18n.html>

- "Internationalization (I18N) Japanese Translation by mixplace in Qiita",
<https://qiita.com/mixplace/items/3f1e1190e38c14f5297d>

- "Angular5 Custom Library: The definitive, step-by-step guide", 
<https://www.udemy.com/1461368/learn/v4/content>


## Change Log

 - 2018.5.4 version 0.1 uploaded

## Copyright

copyright 2018 by Shuichi Ohtsu (DigiPub Japan)


## License

MIT © [Shuichi Ohtsu](mailto:ohtsu@digipub-net.com)
