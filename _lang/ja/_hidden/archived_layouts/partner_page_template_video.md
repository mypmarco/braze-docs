---
nav_title: ビデオ付きパートナーページ

page_order: 4

#Required
description: "これはGoogle検索の説明です。160文字を超えると切り捨てられる。"
page_type: partner
tool:
  - Dashboard
  - Docs
  - Canvas
  - Campaigns
  - Segments
  - Templates
  - Media
  - Location
  - Currents
  - Reports

platform:
  - iOS
  - Android
  - Web
  - API

channel:
  - Content Cards
  - Email
  - News Feed
  - In-App Messages
  - Push
  - SMS
  - Webhooks
  
noindex: true
#ATTENTION: remove noindex and this alert from template

---

# \[パートナー名]

{% multi_lang_include video.html id="XY5uXoKIvFY" align="right" %}

> パートナーページテンプレートへようこそ。ここには、自分のパートナーページを作成するために必要なものがすべて用意されています。この最初のセクションでは、最初の段落でパートナーを 1～2 文で説明します。また、そのパートナーのメインサイトへのリンクも含めてください。

第2段落では、Braze とこのパートナーの関係を詳しく説明します。この段落では、Brazeとこのパートナーがどのように協力し、Brazeユーザーとその顧客との絆を深めるかを説明する。Brazeユーザーがこのパートナーやそのサービスと統合したり、活用したりするときに発生する「昇格」について説明する。

## 必要条件または前提条件

このセクションでは、パートナーと連携してパートナーのサービスを使用するために必要な条件について説明します。この情報を伝える最良の方法は、「知る必要がある」情報の技術的でない重要な詳細、例えば、あなたの統合が追加のセキュリティチェックやクリアランスの対象となるかどうかなどを、手短に説明する段落を設けることである。次に、この連携の技術的な要件をチャートで説明します。

{% alert important %}
以下の要件は、Brazeが必要とする典型的な要件である。以下の表にあるような、帰属するタイトル、由来、リンク、言い回しを使用することを推奨する。それぞれの要件が何をするために使われるのかがわかるように、必ず説明を調整すること。
{% endalert %}

| 必要条件 | Origin | アクセス | 説明 |
|---|---|---|---|
|BrazeワークスペースREST APIキー | Braze プラットフォーム | **設定**>**アプリ設定**ページ | この説明は、ワークスペース REST API キーを使って行う作業を説明するものです。 |
|Braze APIエンドポイント | Braze プラットフォーム | [リストされたエンドポイント]({{site.baseurl}}/developer_guide/rest_api/basics/#endpoints)を確認するか、[サポートチケット]({{site.baseurl}}/braze_support/)を登録します。 | 説明保留。 |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

## \[統合の種類] 統合

ここで、統合をステップに分解する。段落が長過ぎないようにしてください。これらは、マーケターと開発者が統合を運用するために使用する技術ドキュメントです。このセクションの唯一の目標は、Brazeユーザーが仕事をこなすのに役立つ説明的な文書を書くことである。セクションタイトルの「統合のタイプ」とは、これがサイド・バイ・サイド統合なのか、サーバー間統合なのか、Out-of-the Boxなのかを示すことを意味する。これにより、このパートナーと統合する方法が複数ある場合、複数の統合セクションを持つことができる。

これがカレントの統合である場合、このページはカレントセクションに配置され、カレントのその場所にリダイレクトする対応するナビページが構築されるべきである。

### ステップ1:これはステップ1の簡単な説明である。

必要に応じてコードも含めて、これを分解すればいい。複数の異なるコードセットを提供できるので、統合のために1種類の方法だけを提供する必要がないことに注意してください。

### ステップ2:このステップでは画像を説明します。

ドキュメントに画像を配置するオプションがあるので、画像を注意して配置することをお勧めします。

### コードサンプル

技術的なコンセプトを説明しているのであれば、そのことをここに記し、コードサンプルを示す。

```html
<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
</head>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

ユーザーがコードサンプルから調整しなければならないかもしれないパラメータや要素を定義しておくこと。多くのユーザーはただコピー＆ペーストするだろう。

| 可変 | 説明 |
| -------- | ----------- |
| ページタイトル | ページのタイトルは何でもいい。これを持っていなければならない。 |
| 初めての見出し | 大文字で書くことをお勧めする。これもオプションである。 |
{: .reset-td-br-1 .reset-td-br-2}


### ステップ3:ステップの数

メッセージコンポーザーにLiquidを挿入する場合は特にそうだ。

## カスタマイズ

これは**オプション**のセクションです。ここでは、2つのパートナー間の統合をカスタマイズする具体的な方法を説明することができる。

## この統合を使う

これは、統合の使い方を説明するもので、読者がいくつかのボタンを押す必要があるのか、統合後に何もする必要がないのかを知らせる。

### ステップ1:これはステップ1の簡単な説明である。

典型的なステップバイステップのやり方だ。

### コードサンプル

技術的なコンセプトを説明しているのであれば、そのことをここに記し、コードサンプルを示す。

```html
<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
</head>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

ユーザーがコードサンプルから調整しなければならないかもしれないパラメータや要素を定義しておくこと。多くのユーザーはただコピー＆ペーストするだろう。

| 可変 | 説明 |
| -------- | ----------- |
| ページタイトル | ページのタイトルは何でもいい。これを持っていなければならない。 |
| 初めての見出し | 大文字で書くことをお勧めする。これもオプションである。 |
{: .reset-td-br-1 .reset-td-br-2}


## ユースケース

これはドキュメンテーションの重要な部分となる可能性があります。これは任意であるが、典型的な、あるいは斬新な統合の使用例を概説するのに良い場所である。これは、リレーションシップを売り込んだり、アップセルしたりする方法として使うことができる。コンテキストやアイデアを提供し、最も重要なのは、統合の能力を可視化する方法である。
