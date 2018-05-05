# _ng5-i18n-multilingual_ Angular5による多言語サイトの構築方法
[![MIT License](http://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE)


_ng5-i18n-multilingual_ はAngular5によって多言語サイトを構築するためのサンプルプログラムです。

_ビデオ解説（英語）_
<https://youtu.be/74OCrD6Ckgg>

_ビデオ解説（日本語）_
<https://youtu.be/AUXpQvqGjeA>

_デモサイト_
<https://ohtsu.github.io/ng5-i18n-multilingual/>

_完全なソースコード_
<https://github.com/Ohtsu/ng5-i18n-multilingual.git>

## 概要
- _ng5-i18n-multilingual_はAngular5で多言語サイトを作成するためのサンプルプログラムです。


## 前提条件

   - Node.js
   - TypeScript2
   - Angular/Cli (for Angular5 or later)


## インストール


このプログラムをインストールするには：

- まずディレクトリを作成し、そこに移動します。

``` bash
$ mkdir mydir
$ cd mydir
```

- GitHubによりクローンを作成します。

``` bash
$ git clone https://github.com/Ohtsu/ng5-i18n-multilingual.git

```

- _ng5-i18n-multilingual_に移動し、npm installを実行します。


``` bash
$ cd ng5-i18n-multilingual
$ npm install 
```

## ローカルサーバーでのチェック

### 英語（デフォルト）版の開始

コマンドラインで以下のように入力してローカル・サーバーを起動します。

```bash
$ ng serve
```

ブラウザで**http://localhost:4200**にアクセスすると、以下のページがブラウザに表示されます。

- ***初期画面***

  <img src = "https://raw.githubusercontent.com/Ohtsu/images/master/ng5-i18n-multilingual/ng5-i18n-multilingual_en_initial_page01.png" width = "640">



### 日本語版の開始

次のようにローカルサーバーを起動します。

``` bash
$ npm run start:ja
```

同様に、**http://localhost:4200**にアクセスすると、以下のページがブラウザに表示されます。

- ***初期画面***

 <img src = "https://raw.githubusercontent.com/Ohtsu/images/master/ng5-i18n-multilingual/ng5-i18n-multilingual_ja_initial_page01.png" width = "640">

### フランス語版の開始

次のようにローカルサーバーを起動します。

``` bash
$ npm run start:fr
```

同様に、**http://localhost:4200**にアクセスすると、以下のページがブラウザに表示されます。

- ***初期画面***

 <img src = "https://raw.githubusercontent.com/Ohtsu/images/master/ng5-i18n-multilingual/ng5-i18n-multilingual_fr_initial_page01.png" width = "640">


## 多言語サイトデータの作成方法

### Package.jsonファイルを変更する

上記のようにローカルサーバーを使用する場合、動的に言語の変更はできません。
実際のサイトでは、URLに基​​づいて言語を変更できます。

これを準備するには、言語ごとに**Base href**を変更する必要があります。以下のように、ビルド時にパラメータを設定する必要があります。

URLは言語ごとに変更されます。


```bash

    "build": "ng build --aot --output-path dist/ --base-href /ng5-i18n-multilingual/",
    "build:ja": "ng build --aot --output-path dist/ja --base-href /ng5-i18n-multilingual/ja/ --i18nFile=src/locale/messages.ja.xlf --i18nFormat=xlf --locale=ja",
    "build:fr": "ng build --aot --output-path dist/fr --base-href /ng5-i18n-multilingual/fr/ --i18nFile=src/locale/messages.fr.xlf --i18nFormat=xlf --locale=fr"

```

```bash
デフォルト      /ng5-i18n-multilingual/
日本語          /ng5-i18n-multilingual/ja/
フランス語      /ng5-i18n-multilingual/fr/
```


ここでは、このプログラムの実行結果としてGitHub Pagesを使用しているため、 **/ng5-i18n-multilingual**を追加しています。したがって、GitHub Pagesを利用する場合は、この部分を独自のリポジトリ名にする必要があります。

GitHub Pagesとは別の独自のサイトを使用している場合は、そのような文字列を追加する必要はありません。

### 多言語のサイトデータを構築する方法

まず、自分のサイトに基づいて**Base href**文字列を変更する必要があります。文字列 `/ng5-i18n-multilingual`を独自の文字列（またはnull）に変更します。

#### コンパイル

次に、以下のようにコンパイルする必要があります。

``` bash
npm run build
npm run build:ja
npm run build:fr
```

## 自分のサーバーにサイトデータをアップロードする

コンパイルが成功すると、プロジェクトのルートディレクトリに `dist`ディレクトリが生成されます。

`dist`ディレクトリにあるすべてのファイルとディレクトリを自分のサーバにアップロードする必要があります。

詳細は以下のビデオをご覧ください。

_ビデオ解説（英語）_
<https://youtu.be/74OCrD6Ckgg>

_ビデオ解説（日本語）_
<https://youtu.be/AUXpQvqGjeA>

## バージョン

   - TypeScript         : 2.4.2
   - @angular/cli       : 1.5.0
   - Node               : 6.11.3



## 参照

- "Internationalization (I18N)",
<https://v2.angular.io/docs/ts/latest/cookbook/i18n.html>

- "Internationalization (I18N) Japanese Translation by mixplace in Qiita",
<https://qiita.com/mixplace/items/3f1e1190e38c14f5297d>


## その他

- 「Angular5用カスタムライブラリの作成: 完全ステップ・バイ・ステップ・ガイド」
<https://www.udemy.com/1450138/learn/v4/content>

- 割引クーポン
<https://www.udemy.com/angular5-l/?couponCode=NG5-CUSLIB-JA-0712>


## 変更ログ

  - 2018.5.4　バージョン0.2をアップロード

## 著作権

copyright 2018 by Shuichi Ohtsu (DigiPub Japan)


## ライセンス

MIT © [Shuichi Ohtsu](mailto:ohtsu@digipub-net.com)
