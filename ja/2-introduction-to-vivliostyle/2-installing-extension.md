# 文書のカスタマイズ

文書全体の設定ファイルが`vivliostyle.config.js`です。 pathはリポジトリのルートです

![](/images/create-and-save-documents/document-customization/fig-1.png)

`vivliostyle.config.js`はVivliostyle Pub自身を使って編集でき、編集後に保存すれば文書全体に反映されます。記法は下記`{  }` の内部に次項のような値を記入していくものです

```js
module.exports = {

}
```

## 書名の指定

 `title` で書名を指定できます（値をシングルクォートで括る。以下同じ）

```js
title: '私の本',
```

## 著者名とメールアドレスの指定

 `author`  で著者名を指定できます

```js
author: '尾久綿次郎 <ogwata@example.com>',
```

## 使用言語の指定

`language`で文書で使用する言語を指定できます。英語は  `en`、日本語は `ja`、その他 [ISO 639-1](https://www.loc.gov/standards/iso639-2/php/code_list.php )に規定された2文字コードが指定できます

```js
language: 'ja',
```

## 判型の指定

判型はvivliostyle.comfig.jsではなく、themeで指定してください。詳細は下記をご参照ください。

- [Theme（スタイル情報の選択）> Custom theme > 判型の指定](/ja/functions-of-the-actions-menu/theme#%E5%88%A4%E5%9E%8B%E3%81%AE%E6%8C%87%E5%AE%9A)

## 対象となる文書の指定

`entry: [  ]` の記法により処理の対象となる文書を指定します。複数文書を指定可能で、下記のように指定することで、複数のmarkdownファイルをまとめて1冊の本として出力できるようになります

```js
entry: [
    "Chapter-1.md",
    "Chapter-2.md",
    "Chapter-3.md",
],
```

出力したくないファイルがあれば、行頭に`//`を記入すればコメントアウトになります

## 目次の追加

以下の手順で目次を追加することができます

1. あらかじめ以下のような目次用の markdown ファイルを用意し、ファイル名を `index.md` としてアップロードします（→[ファイルのアップロード](/ja/file-and-folder-operations/file-list-pane-operations.md#ファイルのアップロード)）。他と違って以下はHTML構文なので、指定するのもHTMLファイルであることにご注意ください

```md
# 本のタイトル

<nav id="toc" role="doc-toc">

## 目次

- [記事タイトル1](Chapter-1.html)
- [記事タイトル2](Chapter-2.html)
- [記事タイトル3](Chapter-3.html)

</nav>
```

なお、HTMLのタグがある行とmarkdownの行の間は、必ず空行をいれるよう注意してください。そうしないとエラーになります

2. `vivliostyle.config.js` の `entry` の先頭行に、用意した `index.md` を指定します

```js
entry: [
    "index.md",
    "Chapter-1.md",
    "Chapter-2.md",
    "Chapter-3.md",
],
```

## 奥付の追加

以下の手順で奥付を追加することができます

1. あらかじめ以下のような markdownファイルを用意し、ファイル名を `colophon.md` としてアップロードします（→[ファイルのアップロード](/ja/file-and-folder-operations/file-list-pane-operations.md#ファイルのアップロード)）

```md
<section id="colophon" role="doc-colophon">

## 私が書いた本
20xx年x月x日　初版発行
- 発行　私が書いた本刊行会
- 著者　尾久綿次郎
- 印刷　Sample Printing

© My Book Publishing, 20xx

</section>
```

2. `vivliostyle.config.js` の `entry` の末尾行に、用意した `colophon.md` を指定します

```js
entry: [
    "index.md",
    "Chapter-1.md",
    "Chapter-2.md",
    "Chapter-3.md",
    "colophon.md",
],
```

## まとめ

ここまでの説明をまとめると、`vivliostyle.config.js`の記述は下記のようになります

```js
module.exports = {
	title: '私の本',
	author: '尾久綿次郎 <ogwata@example.com>',
	language: 'ja',
	theme: 'css/style.css',
	entry: [
		"index.md",
		"Chapter-1.md",
		"Chapter-2.md",
		"Chapter-3.md",
		"colophon.md",
	],
}
```