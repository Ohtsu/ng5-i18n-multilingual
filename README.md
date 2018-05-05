

# _ng5-i18n-multilingual_ Angular5 multilingual site sample
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
$ npm run start:fr
```

And you will get the page below in your browser by accessing **http://localhost:4200**.  

  - ***First Page*** 

 <img src="https://raw.githubusercontent.com/Ohtsu/images/master/ng5-i18n-multilingual/ng5-i18n-multilingual_fr_initial_page01.png" width= "640" >


## How to make multilingual site data

### Modify package.json file

When using the above local server, dynamic language change is not possible.
On the actual site, you can change the language based on the URL.

To prepare for this, you need to change **Base href** for each language. It must be set with parameters at build time as follows.

The URL is  changed for each language.

```bash

    "build": "ng build --aot --output-path dist/ --base-href /ng5-i18n-multilingual/",
    "build:ja": "ng build --aot --output-path dist/ja --base-href /ng5-i18n-multilingual/ja/ --i18nFile=src/locale/messages.ja.xlf --i18nFormat=xlf --locale=ja",
    "build:fr": "ng build --aot --output-path dist/fr --base-href /ng5-i18n-multilingual/fr/ --i18nFile=src/locale/messages.fr.xlf --i18nFormat=xlf --locale=fr"

```
```bash
Default   /ng5-i18n-multilingual/
Japanese  /ng5-i18n-multilingual/ja/
French    /ng5-i18n-multilingual/fr/
```

Here we are adding "/ng5-i18n-multilingual" because we use GitHub Pages as the execution result of this program, so we need to add its own repository name.

If you are using your own site, adding such a string is not necessary.

### How to build multilingual site data

At first, you need to change base-href string based on your own site. Change the string `/ng5-i18n-multilingual` to your own string (or null).

#### Compile

Next you need to compile as follows.

```bash
npm run build
npm run build:ja
npm run build:fr
```

## Upload the site data to your own server

If you compilation is successful, you will find `dist` directory in your project root directory.

You need to upload all the files and directories under `dist` directory to your own server.

In more details, please watch the following video.

_Video Explanation(English)_
<https://youtu.be/74OCrD6Ckgg>

_Video Explanation(Japanese)_
<https://youtu.be/AUXpQvqGjeA>

## Version

   - TypeScript         : 2.4.2
   - @angular/cli       : 1.5.0
   - Node               : 6.11.3


## Reference

- "Internationalization (I18N)",
<https://v2.angular.io/docs/ts/latest/cookbook/i18n.html>

- "Internationalization (I18N) Japanese Translation by mixplace in Qiita",
<https://qiita.com/mixplace/items/3f1e1190e38c14f5297d>

## Others

- "Angular5 Custom Library: The definitive, step-by-step guide", 
<https://www.udemy.com/1461368/learn/v4/content>

- Discount coupon
<https://www.udemy.com/angular5-custom-library-the-definitive-step-by-step-guide/?couponCode=CUSTLIB-EN-20180713>


## Change Log

 - 2018.5.4 version 0.2 uploaded

## Copyright

copyright 2018 by Shuichi Ohtsu (DigiPub Japan)


## License

MIT © [Shuichi Ohtsu](mailto:ohtsu@digipub-net.com)
