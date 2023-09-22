# Theme（スタイル情報の選択）

## 概要

![ ](images/functions-of-the-actions-menu/theme/fig-1.png)

Actionメニューの「Theme」の項目を選択することで、以下のスタイル情報に切り替えることができます。

1. Plain theme
2. Custom theme
3. Book theme for latin font
4. 文庫用のテーマ
5. Slide theme
6. Techbook (技術同人誌) theme
7. Academic theme 

以下では、themeごとにその内容を概説します。使用したサンプルデータの出典は下記の通りです。なお、スクリーンショットは[プレゼンテーション・モード](/ja/functions-of-the-actions-menu/presentation-mode.md)での表示です。

- 1、2、4……銀河鉄道の夜（宮沢賢治、[青空文庫](https://www.aozora.gr.jp/cards/000081/card456.html)）
- 3………[The Project Gutenberg eBook of Alice’s Adventures in Wonderland, by Lewis Carroll](https://www.gutenberg.org/files/11/11-h/11-h.htm)
- 5 ………[Slide theme 付属のslide.md](https://github.com/vivliostyle/themes/blob/master/packages/%40vivliostyle/theme-slide/example/slide.md)
- 6 ………[Markdown を拡張する MDX はドキュメント作成の新たな可能性？](https://github.com/vivliostyle/vivliostyle_doc/tree/gh-pages/ja/vivliostyle-user-group-vol5/content/spring-raining)（spring-raining、[Vivliostyle で本を作ろう Vol.5所収](https://github.com/vivliostyle/vivliostyle_doc/tree/gh-pages/ja/vivliostyle-user-group-vol5/)）
- 7………[Academic theme付属のfet.md](https://github.com/vivliostyle/themes/blob/master/packages/%40vivliostyle/theme-academic/example/fet.md)

## Plain theme

ブラウザのデフォルト設定を使った、シンプルなスタイルです。横組で文字サイズは12ポイント、ページサイズは非定型でウィンドウに追従します。フォントはブラウザの設定で「標準フォント」に指定されたものが使用されます。

![ ](images/functions-of-the-actions-menu/theme/fig-2.png)

Plain themeは手早くプレビューを確認するためのもので出力は想定していません。イメージ通りのスタイルでPDF出力をしたい場合は、後述のVivliostyle公式themeの中から選択するか、自分でCustom themeを作成してください。フォントについては下記も参照してください。

- [Plain themeで使われるフォント](/ja/create-and-save-documents/how-to-specify-fonts.md#plain-themeで使われるフォント)

## Custom theme

### Custom themeの指定方法

ユーザーが作成した任意のtheme（CSSスタイルシート）を利用するには、以下の手順に従います。

1. `vivliostyle.config.js`でthemeのpathを指定する（スクリーンショットの赤線部）
2. `Actionメニュー > Custom theme`を選択する

![ ](images/functions-of-the-actions-menu/theme/fig-3.png)

Custom themeを選択することで、これを適用したPDFファイルが出力できるようになります（→[Export（出力）](/ja/functions-of-the-actions-menu/export.md#export出力)）。themeのpathを指定する記法は下記の通りです。`---`の部分にpathを記述してください。

```js
module.exports = {
  theme: '---',
 }
```

`vivliostyle.config.js`についての詳細は下記をご参照ください。

- [文書のカスタマイズ](/ja/create-and-save-documents/document-customization.md)

### 判型の指定

任意の判型にしたいときは、themeの中で指定します。`@page`ルールにおける`size`プロパティの値として、以下の判型が指定できます。なお、日本での一般的なB5は `JIS-B5` ですのでご注意ください（B4も同様）

- `A5`
- `A4`
- `A3`
- `B5`
- `B4`
- `JIS-B5`
- `JIS-B4`
- `letter`
- `legal`
- `ledger`

記法は下記の通りです。ここではA5判を指定しています。

```css
@page {
   size: A5;
}
```

### トンボと塗り足し（裁ち落とし）の指定

印刷物を指定通りのサイズに裁断したり、多色印刷で各版の刷り位置を合わせるための目印を「トンボ」と言います（アプリケーションによって「トリムマーク」とも）。
トンボを付与するには、Custom themeの中で指定します。

<img src="images/functions-of-the-actions-menu/theme/fig-4.png" alt="トンボと塗り足し（裁ち落とし）の指定" style="max-height: 500px;">


具体的には前述`size`と一緒に、`@page`ルールにおける`marks`プロパティの値として、`crop`と`cross`を指定します。`crop`はページ四隅の位置を示すトンボ、`cross`は上下と左右の中央の位置を示すトンボで、通常は両方とも指定します。

また、ページの端まで色や図版を配置したい場合（つまり用紙の端まで印刷したい場合）、指定されたページサイズの外側を塗り足す領域が必要になります。これを「裁ち落とし」と言い、同じく`@page`ルールで`bleed`プロパティにより指定します。領域の幅を値として指定しますが、デフォルトは6pt（約2.1mm）になっています。日本の印刷業界では3mmが通常なので、これを値として指定します。

```css
@page {
   size: A5;
   marks: crop cross;
   bleed: 3mm;
}
```

より詳細は、下記をご参照ください。

- [Vivliostyle Viewer で CSS 組版ちょっと入門 > トンボをつけるには](https://vivliostyle.github.io/vivliostyle_doc/ja/vivliostyle-user-group-vol1/shinyu/index.html#%E3%83%88%E3%83%B3%E3%83%9C%E3%82%92%E3%81%A4%E3%81%91%E3%82%8B%E3%81%AB%E3%81%AF)

### プレビューとPDF出力でフォントを一致させる

Vivliostyle PubではプレビューとPDF出力とで組版エンジンのある場所が違うため、Custom themeを作成してもなかなかイメージした通りのフォントが表示／出力されなかったり、プレビューとPDFとでページがずれてしまうことが起こり得ます。事前に以下の記事を参照して、プレビューとPDF出力とでフォントが一致するようにCustom themeを作成することをお勧めします。

- [フォントの指定方法](/ja/create-and-save-documents/how-to-specify-fonts.md)
- [クラウドにインストールされているフォント一覧](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウドにインストールされているフォント一覧)
- [クラウド上のVivliostyle CLIにおける代替フォントルール](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウド上のvivliostyle-cliにおける代替フォントルール)

### Vivliostyle公式themeを雛形にする

ゼロからCustom themeを書くには不安がある方は、Vivliostyle公式themeを雛形にして、自分なりにカスタマイズすることをおすすめします。Vivliostyle公式themeリポジトリの[packageディレクトリ](https://github.com/vivliostyle/themes/tree/master/packages/%40vivliostyle)に各themeが格納されているので、以下の手順に従ってください

1. 自分のイメージに近い公式themeの`theme_common.css`というファイルを探してダウンロード
2. Vivliostyle Pubを使って自分のリポジトリにアップロード（→[ファイルのアップロード](/ja/file-and-folder-operations/file-list-pane-operations.md)）
3. Vivliostyle Pubのエディタでカスタマイズ
4. `vivliostyle.comfig.js`をエディタで開いて、Custom themeのpathを指定（本項を参照）
5. `Actionメニュー > Custom theme` を選択（本項を参照）


## Book theme for latin font

英語をはじめとしたラテン文字書籍のためのtheme（CSSスタイルシート）です。横組で文字サイズは`small` （デフォルトの16pxよりも一回り小さい）、ページサイズは非定型でウィンドウサイズに追従します。

![ ](images/functions-of-the-actions-menu/theme/fig-5.png)

これはVivliostyleが [npm packageとして公開](https://www.npmjs.com/package/@vivliostyle/theme-gutenberg)している公式Theme、[@vivliostyle/theme-gutenberg](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-gutenberg)そのものです。以下にその一部を引用します。

```css
html {
  max-width: 90ch;
  margin: auto;
  font-family: Georgia, serif;
}
/* 中略 */
@page {
  font-size: small;
  font-family: Georgia, serif;
  margin: 4rem 10%;
  @top-center {
    color: gray;
    font-variant: small-caps;
  }
}

```

上記でフォントは`Georgia`と`serif`が指定されています。多くのPCには`Georgia`がインストールされているはずです。一方、Vivliostyle PubでPDF出力をおこなうクラウド（前掲図2）にも`Georgia`がインストールされているので、このthemeでは多くの場合プレビューとPDF出力のフォントは一致するでしょう。ただし、フォントのバージョン不一致によりズレが生じる場合もあることにご注意ください（クラウドのフォントは比較的古いバージョンです）。

より詳細は下記をご参照ください。

- [Vivliostyle公式Themeで使われるフォント](/ja/create-and-save-documents/how-to-specify-fonts.md#vivliostyle公式themeで使われるフォント)
- [クラウドにインストールされているフォント一覧](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウドにインストールされているフォント一覧)

## 文庫用のテーマ

縦組で文字サイズは8.5ポイント、ページサイズは148×210mm（A5判タテ）、縦中横や柱にも対応しており、長文の読み物に合います。theme名の「文庫」は読み物の意味で、文庫判（B6判）とは違うことに注意してください。

![ ](images/functions-of-the-actions-menu/theme/fig-6.png)

これはVivliostyleが [npm packageとして公開](https://www.npmjs.com/package/@vivliostyle/theme-bunko)している公式Theme、[@vivliostyle/theme-bunko](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-bunko)そのものです。以下にその一部を引用します。

```css
html {
  writing-mode: vertical-rl;
  orphans: 1;
  widows: 1;
}
/* 中略 */
@page {
  size: 148mm 210mm;
  width: 360pt;
  height: 468pt;
  margin: auto;
  font-size: 8.5pt;
  font-family: "游明朝", "YuMincho", serif;
}
```

上記でフォントは`游明朝`が指定されています。Windows（`游明朝`/`Yu Mincho`）でもMac（`游明朝体`/`YuMincho`）でもプリインストールされているので、プレビューではこれが使用されます（ただし、WindowsとMacではウェイトが若干異なります）。

一方、PDF出力では`Noto Serif CJK JP`に置き換えられます。この結果、プレビューとPDF出力とではズレが発生します（たとえば下記スクリーンショットではプレビューと比べて3行、後にずれています）。より詳細は下記をご参照ください。

![ ](images/functions-of-the-actions-menu/theme/fig-7.png)

- [Vivliostyle公式Themeで使われるフォント](/ja/create-and-save-documents/how-to-specify-fonts.md#vivliostyle公式themeで使われるフォント)
- [クラウド上のVivliostyle CLIにおける代替フォントルール](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウド上のvivliostyle-cliにおける代替フォントルール)

## Slide theme

横組で文字サイズは24ポイント（デフォルトの150%）、ページサイズは210×148mm（A5判ヨコ）、スライド資料に適しています。

![ ](images/functions-of-the-actions-menu/theme/fig-8.png)

これはVivliostyleが [npmパッケージとして公開](https://www.npmjs.com/package/@vivliostyle/theme-slide)している公式Theme、[@vivliostyle/theme-slide](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-slide)そのものです。以下にその一部を引用します。

```css
html {
  font-family: 'Noto', 'YuGothic', 'Yu Gothic', 'Meiryo', sans-serif;
  font-feature-settings: 'palt' on;
  font-size: 150%;
  font-weight: 500;
  line-height: 1.5;
}

@page {
  size: 210mm 148mm;
  margin: 12mm 0 0;
  padding: 0 0 18mm;
  background-position: center bottom;
  background-repeat: no-repeat;
  background-size: contain;
  font-size: 11pt;
  line-height: 1.2;
  /* 中略 */
  }
```

上記でフォントは優先度順に、1. `Noto Sans CJK JP`、2. `游ゴシック`、3. `メイリオ` 4. `sans-serif` と指定されています。プレビューで、ユーザーのPCに1〜3までのフォントがインストールされていない場合は、ブラウザ設定の「Sans Serif フォント」の指定に従います。一方、PDF出力ではすべて`Noto Sans CJK JP`に置き換えられます。

もしもプレビューとPDF出力とでズレが気になる場合、ユーザーのPCに[`Noto Sans CJK JP`](https://fonts.google.com/noto/specimen/Noto+Serif+JP)をインストールすることで改善する可能性があります。

詳細は下記をご参照ください。

- [Vivliostyle公式Themeで使われるフォント](/ja/create-and-save-documents/how-to-specify-fonts.md#vivliostyle公式themeで使われるフォント)
- [プレビューとPDF出力とでフォントを一致させる](/ja/create-and-save-documents/how-to-specify-fonts.md#custom-theme／プレビューとpdf出力とでフォントを一致させる)
- [クラウド上のVivliostyle CLIにおける代替フォントルール](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウド上のvivliostyle-cliにおける代替フォントルール)

なお、見開きではなく、単一ページでプレビューしたい場合は、Vivliostyleのロゴからアクセスできる設定メニューを開き、“Page Spread View” のうち “Single page” のラジオボタンを選択してください。

![ ](images/functions-of-the-actions-menu/theme/fig-9.png)

## Techbook (技術同人誌) theme

横組で文字サイズは12ポイント、ページサイズは182×257mm（B5判タテ）、コードブロックのクラス指定、[脚注の記法](https://vivliostyle.org/ja/make-books-with-create-book/#%E8%84%9A%E6%B3%A8)もサポートされており、技術同人誌に適しています。

![ ](images/functions-of-the-actions-menu/theme/fig-10.png)

これはVivliostyleが [npmパッケージとして公開](https://www.npmjs.com/package/@vivliostyle/theme-techbook)している公式Theme、[@vivliostyle/theme-techbook](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-techbook)そのものです。以下にその一部を引用します。

```css
:root {
  font-family: 'Neue Frutiger World', 'Verdana',  'Hiragino Sans', sans-serif;
  font-weight: 400;
  line-height: 1.7;
}
/* 中略 */
@media print {
  :root {
    widows: 3;
    orphans: 3;
    hyphens: auto;
    font-size: 75%;
  }
/* 中略 */  
}
/* 中略 */
@page {
  size: 182mm 257mm;
  margin-top: 25mm;
  margin-bottom: 33mm;
/* 中略 */
}
```

上記でフォントは優先度順に、1. `Neue Frutiger World`、2. `Verdana`、3. `ヒラギノ角ゴシック`、4. `sans-serif`と指定されています。プレビューで表示される文字は、1〜3の順番でフォントが割り当てられ、どのフォントも当該の文字を表示できない場合はブラウザ設定の「Sans Serif フォント」の指定に従います。たとえば原稿が日本語文の場合、英数字は`Neue Frutiger World`、なければ`Verdana`、仮名や漢字は`ヒラギノ角ゴシック`で表示されます。もしユーザーのPCに`ヒラギノ角ゴシック`がインストールされていなければ、ブラウザ設定の「Sans Serif フォント」が使われます。

一方、PDF出力においては、英数字は`Verdana`、仮名と漢字は`Noto Sans CJK JP`に置き換えられます。こうした結果、プレビューとPDF出力とでページのズレが発生する場合があることにご注意ください。

詳細は下記をご参照ください。

- [Vivliostyle公式Themeで使われるフォント](/ja/create-and-save-documents/how-to-specify-fonts.md#vivliostyle公式themeで使われるフォント)
- [クラウドにインストールされているフォント一覧](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウドにインストールされているフォント一覧)
- [クラウド上のVivliostyle CLIにおける代替フォントルール](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウド上のvivliostyle-cliにおける代替フォントルール)



## Academic theme

横組でページサイズは210×297mm（A4判タテ）、自動で章・節番号がつき、[脚注の記法](https://vivliostyle.org/ja/make-books-with-create-book/#%E8%84%9A%E6%B3%A8)もつかえる、理系の学生レポート向けのスタイルです。

![ ](images/functions-of-the-actions-menu/theme/fig-11.png)

これはVivliostyleが [npmパッケージとして公開](https://www.npmjs.com/package/@vivliostyle/theme-academic)している公式Theme、[@vivliostyle/theme-academic](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-academic)そのものです。以下にその一部を引用します。

```css
@page {
  size: 210mm 297mm;
  margin: 25mm 20mm 25mm 20mm;
/* 中略 */
}
html {
  font-family: 'Hiragino Mincho ProN', serif;
  font-size: 10pt;
  color: #000000;
  line-height: 1.8;
  orphans: 1;
  widows: 1;
}
```

上記でフォントは`ヒラギノ明朝 ProN`と`serif`が指定されています。ユーザーのPCに`ヒラギノ明朝 ProN`がインストールされていれば、これがプレビューで使われます。インストールされていなければ、ブラウザ設定の「Serif フォント」の設定に従います。

一方、PDF出力においてはすべて`Noto Serif CJK JP`に置き換えられます。こうした結果、プレビューとPDF出力とでページのズレが発生することにご注意ください。フォントのしくみについて、詳細は下記をご参照ください。

- [Vivliostyle公式Themeで使われるフォント](/ja/create-and-save-documents/how-to-specify-fonts.md#vivliostyle公式themeで使われるフォント)
- [クラウドにインストールされているフォント一覧](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウドにインストールされているフォント一覧)
- [クラウド上のVivliostyle CLIにおける代替フォントルール](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウド上のvivliostyle-cliにおける代替フォントルール)