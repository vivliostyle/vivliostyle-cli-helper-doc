# フォントの指定方法

## フォントを利用するしくみ

フォントは themeの中で指定されます（→[ Theme（スタイル情報の選択）](/ja/functions-of-the-actions-menu/theme.md)）。組版エンジンであるVivliostyle.jsは、themeにしたがってフォントを操作し、レイアウトや組版をします。以下の図1はプレビューのしくみを図式化したものです。

<img src="images/create-and-save-documents/how-to-specify-fonts/fig-1.jpg" alt="図1 プレビューにおけるフォントの利用" style="max-height: 500px;">

ここで注意してほしいのは、プレビューのために組版をおこなうVivliostyle.js（赤い四角）は、ユーザーのPC上のフロントエンドにあるということです。したがってVivliostyle.jsと同じユーザーのPCにある**フォント1**、及びWebフォントサービスの**フォント3**がプレビューで利用できるわけです。

次に、PDF出力のしくみを図式化したのが図2です。PDF出力のために組版をおこなうVivliostyle.js（赤い四角）はクラウド上のバックエンドにあります。

<img src="images/create-and-save-documents/how-to-specify-fonts/fig-2.jpg" alt="図2 PDF出力におけるフォントの利用" style="max-height: 500px;">

したがってVivliostyle.jsと同じクラウドにある**フォント2**、及びWebフォントサービスの**フォント3**がPDF出力で利用できるわけです。

ここまでの説明をまとめてみましょう。プレビューとPDF出力は、それぞれ別の組版エンジン、Vivliostyle.js（図1、図2の赤い四角）が担当します。その際、それぞれの組版エンジンは以下の3つの場所にあるフォントを使用します。

- ユーザーのPCにあるローカルフォント（図1：**フォント1**）
- クラウドにインストールされたフォント（図2：**フォント2**）
- Webフォントサービスのフォント（図1、図2：**フォント3**）

プレビューを担当するユーザーのPC上のVivliostyle.jsは、ローカルフォント（図1：**フォント1**）、及びWebフォントサービスのフォント（図1、図2：**フォント3**）を使います。

一方、PDF出力を担当するクラウド上のVivliostyle.jsは、クラウドにインストールされたフォント（図2：**フォント2**）、及びWebフォントサービスのフォント（図1、図2：**フォント3**）を使います。

このようなしくみなので、プレビューで使われるフォントとPDF出力で使われるフォントが、いつでも無条件に一致するのは、Webフォントサービスのフォント（図1、図2：**フォント3**）だけです。プレビューではクラウドにインストールされたフォント（図2：**フォント2**）は使えず、PDF出力ではユーザーのPCにインストールされたローカルフォント（図1：**フォント1**）は使えません。

例えば、プレビューで使ったローカルフォント（図1：**フォント1**）がクラウドになかった場合、PDF出力ではクラウドにインストールされたフォントのうち、似たものに置き換えられます（→[ クラウド上のVivliostyle CLIにおける代替フォントルール](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウド上のvivliostyle-cliにおける代替フォントルール)）。その結果、プレビューとPDF出力のフォントが不一致になり、ページのズレが発生することにご注意ください。

本節ではActionメニューの項目に沿いながら、3種類のフォントを使い分ける方法について説明していきます。その中で、プレビューとPDF出力のフォントを一致させる方法についても触れます。

## Plain themeで使われるフォント

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-3.png)

Plain themeは最小の手間で素早くプレビューを確認するためのものです。他と違って特定のtheme（スタイル情報）があるのではなく、ブラウザのデフォルト設定にしたがいます。たとえばフォントはブラウザ設定の「標準フォント」が参照されます。これは、前掲図1の分類では**フォント1**（ユーザーのPCにあるローカルフォント）に当たります。

このthemeの目的上、出力は想定されていません。PDF出力そのものは可能ですが、Plain themeで使われたブラウザのデフォルト設定は[クラウド上のVivliostyle CLIにおける代替フォントルール](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウド上のvivliostyle-cliにおける代替フォントルール)に従って置き換えられます。イメージ通りのスタイルでプレビューやPDF出力をしたい場合は、後述のVivliostyle公式themeの中から選択するか、Custom themeを作成してください。

Plain themeについては、以下もご参照ください。

- [ Theme（スタイル情報の選択） >  Plain theme](/ja/functions-of-the-actions-menu/theme.md#plain-theme)

## Vivliostyle公式Themeで使われるフォント

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-4.png)

Actionメニューから、以下のthemeを選択した場合、npm package管理システム上のVivliostyle公式Themeが使用されます。ぞれぞれのthemeの詳細は、リンク先を参照してください。

- [Book theme for latin font](/ja/functions-of-the-actions-menu/theme.md#book-theme-for-latin-font)
- [文庫用のテーマ](/ja/functions-of-the-actions-menu/theme.md#文庫用のテーマ)
- [Slide theme](/ja/functions-of-the-actions-menu/theme.md#slide-theme)
- [Techbook (技術同人誌) theme](/ja/functions-of-the-actions-menu/theme.md#techbook-技術同人誌-theme)
- [Academic theme](/ja/functions-of-the-actions-menu/theme.md#academic-theme) 

プレビューにおいて、これらのthemeで使用されるのはユーザーのPCにあるローカルフォント（前掲図1の**フォント1**）です。したがってthemeで指定されたフォントがユーザーのPCにインストールされている必要があります。もしそれらのフォントがインストールされていなければ、`font-family:`の設定に従って`sans-serif`ないしは`serif`に代替されます。

一方、PDF出力ではクラウドにインストールされたフォント（前掲図2の**フォント2**）が使用されます。もし公式themeで指定されているフォントがクラウドになければ、[クラウド上のVivliostyle CLIにおける代替フォントルール](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウド上のvivliostyle-cliにおける代替フォントルール)に従って別のフォントで代替されます。それぞれの公式themeでどのようなフォントが指定されているか、そしてクラウド上にどのようなフォントがインストールされているのかは下記をご参照ください。

- [ Theme（スタイル情報の選択）](/ja/functions-of-the-actions-menu/theme.md)
- [クラウドにインストールされているフォント一覧](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウドにインストールされているフォント一覧)

こうした代替処理によりフォントが不一致になった場合、プレビューとPDFとでページがずれることにご注意ください。（→[Custom theme／プレビューとPDF出力とでフォントを一致させる](/ja/create-and-save-documents/how-to-specify-fonts.md#custom-theme／プレビューとpdf出力とでフォントを一致させる)）

## Custom theme／プレビューとPDF出力とでフォントを一致させる

Custom themeを作成することで、それにもとづいたプレビューとPDF出力ができます。この時プレビューで使用されるのはユーザーのPCにあるローカルフォント（前掲図1の**フォント1**）です。一方、PDF出力で使用されるのはクラウドにインストールされたフォント（前掲図2の**フォント2**）です。

ここで問題になるのは、Custom themeで指定したフォントが、ユーザーのPCかクラウドにしかインストールされていなかった時です。その場合は似たフォントが代替使用されるので、プレビューとPDF出力でフォントが不一致になります。フォントが異なるので、プレビューとPDF出力とでページのズレが発生します。

しかし、クラウドにあるフォントをPCにもインストールし、これをCustom themeで指定すればプレビューとPDF出力とでフォントを一致でき、ページのズレは発生しません。では、[クラウドにインストールされているフォント](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウドにインストールされているフォント一覧)のうち、どのフォントをPCにインストールすれば間違いないのでしょう？

Vivliostyle Pubでは、世界中の言語や文字体系に対応し豊富なウェイトとスタイルをもつ[Noto fonts](https://fonts.google.com/noto)全てを、クラウドにインストールしています。そのうちの日本語ゴシック体フォントである[`Noto Sans CJK JP`](https://github.com/googlefonts/noto-cjk/tree/main/Sans)、および日本語明朝体フォントである[`Noto Serif CJK JP`](https://github.com/googlefonts/noto-cjk/tree/main/Serif)を、ユーザーのPCにもインストールするのが最も効率的で効果的です。以下、本項では`Noto Sans CJK JP`を使ってプレビューとPDF出力をする方法を説明します。

------------------------

1. あらかじめPCに`Noto Sans CJK JP`をインストールしておきます。

2. Vivliostyle Pubで、以下のような内容のスタイルシート（Custom theme）をアップロードします（→[ファイルのアップロード](/ja/file-and-folder-operations/file-list-pane-operations.md)）。すでにある場合は下記を参考に書き換えてください

```css
@charset "UTF-8";

html {
  writing-mode: vertical-rl;
  font-family: 'Noto Sans CJK JP', sans-serif;
  font-style: normal;
  text-align: justify;
  text-spacing: space-first allow-end ideograph-alpha ideograph-numeric;
  line-height: 2;
  orphans: 1;
  widows: 1;
}

p {
  font-weight: 300;
  margin: 0;
  text-indent: 1em;
  hanging-punctuation: first allow-end;
}
h1 {
  font-weight: 900;
}
h2 {
  font-weight: 700; 
}

@page {
  size: 148mm 210mm;
  width: 360pt;
  height: 468pt;
  margin: auto;
  font-size: 8.5pt;
}
@page :left {
  @top-left {
    writing-mode: horizontal-tb;  
    content: counter(page) "　" env(doc-title);
    margin-left: 7pt;
    margin-top: 8.5mm;
  }
}
@page :right {
  @top-right {
    writing-mode: horizontal-tb;
    content: counter(page);
    margin-right: 7pt;
    margin-top: 8.5mm;
   }
}
```

上記はCustom themeの一例です。ルート要素の`font-family`として`Noto Sans CJK JP`を指定し、本文（`p`）に`font-weight: 300;`、大見出し（`h1`）に`font-weight: 900;`、小見出し（`h2`）に`font-weight: 700;`と、同じデザインで複数の太さを指定し分けています。またページ設定（`@page`）として判型はA5判タテ、幅360pt、高さ468pt、フォントサイズ8.5ptを指定しています。

3. 設定ファイル`vivliostyle.config.js`の中で、Custom themeのあるpathを指定します（→[Custom theme](/ja/functions-of-the-actions-menu/theme.md#custom-theme)）。`entry: `にはPDF出力するファイル名を記述します。

```js
module.exports = {
  title: '私の本',
  author: '尾久綿次郎',
  theme: 'css/style.css',
  entry: [
    'chapter-2.md',
    ]
}
```

`vivliostyle.config.js`についての詳細は下記をご参照ください。

- [文書のカスタマイズ](/ja/create-and-save-documents/document-customization.md)


4. Actionメニューから「Custom theme」を選択します。themeが切り替わらない場合は、ブラウザをリロードさせてください

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-5.png)

5. プレビューで`Noto Sans CJK JP`が使用されるようになりました

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-6.png)

6. Actionメニューから[Export（出力） > PDF](/ja/functions-of-the-actions-menu/export.md#pdf)を選択すると、Custom themeを適用したPDFが出力されます。プレビューと同じ`Noto Sans CJK JP`が、同じ文字サイズ、行長、行送りにより使用されていることを確認してください   

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-7.png)

Custom themeについての詳細は下記をご参照ください。

- [Custom theme](/ja/functions-of-the-actions-menu/theme.md#custom-theme)

- **補足情報**
    - Noto fontsは多種多様なバリエーションがあり、なかなか目的のフォントが見つからない可能性があります。 下記リポジトリにあるリンクのうち **“Variable OTC”** をダウンロードするとよいでしょう。
        - [`Noto Sans CJK JP`](https://github.com/googlefonts/noto-cjk/tree/main/Sans)
        - [`Noto Serif CJK JP`](https://github.com/googlefonts/noto-cjk/tree/main/Serif)
    - リンクは “OTC”（54.3MB）と “TTF”（57.1MB）の2つあります。どちらも単一フォントパッケージに複数のフォントファイルを内蔵させる「フォントコレクション」と呼ばれる形式であり、Vivliostyle Pubで使う場合は “OTC”と “TTF” のどちらを使っても同じです。
    - “Variable OTC” をインストールすることで、日本語（JP）、繁体字（TC）、簡体字（SC）、香港（HK）、韓国語（KR）の5つの言語用フォントがインストールされます。
    - 本項で説明した方法以外にも、Webフォントサービス（図1、図2：**フォント3**）を利用することで、同様にプレビューとPDF出力とでフォントを一致させることができます（次項以降参照）

## Custom theme／Googleフォントの使用

Webフォント（前掲図1／図2の**フォント3**）を利用すると、プレビューとPDF出力でフォントを一致させることができます。本項では無償のWebフォントサービス、[Googleフォント](https://fonts.google.com/)をVivliostyle Pubで使用する方法を説明します。

1. まず[Googleフォント](https://fonts.google.com/)でフォント選択し、つぎにStylesで使いたい太さを “Select this style” 右横にある(+)　をクリックして選択します。ここでは、しっぽり明朝 Regular 400、Noto Sans Japanese Bold 700、Noto Sans Japanese Medium 900を選択しました

すると、画面右ペインに選択したフォント／スタイルの読み込み用コードが表示されるので、これをコピーします。また、「CSS rules to specify families」から`font-family`のコードもコピーします

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-8.png)

2. 下記のようにGoogleフォントの読み込み用コードや`font-family`のコードを記入したCustom themeをアップロードします（→[ファイルのアップロード](/ja/file-and-folder-operations/file-list-pane-operations.md)）。すでにスタイルシート（Custom theme）がある場合は下記を参考に書き換えてください

```css
@charset "UTF-8";

@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@700;900&family=Shippori+Mincho&display=swap');

html{
writing-mode: vertical-rl;
font-family: 'Shippori Mincho', serif;
font-style: normal;
text-align: justify;
text-spacing: space-first allow-end ideograph-alpha ideograph-numeric;
line-height: 2;
}

p {
  font-weight: 400;
  text-indent: 1em;
  hanging-punctuation: first allow-end;
}

h1 {
font-family: 'Noto Sans JP', sans-serif;  
font-weight: 900; 
}

h2 {
font-family: 'Noto Sans JP', sans-serif;
font-weight: 700; 
}

@page {
  size: 148mm 210mm;
  width: 360pt;
  height: 468pt;
  margin: auto;
  font-size: 8.5pt;
}
@page :left {
  @top-left {
    writing-mode: horizontal-tb;  
    content: counter(page) "　" env(doc-title);
    margin-left: 7pt;
    margin-top: 8.5mm;
  }
}
@page :right {
  @top-right {
    writing-mode: horizontal-tb;
    content: counter(page);
    margin-right: 7pt;
    margin-top: 8.5mm;
   }
}
```

Googleフォントでは、読み込みコードとして`link`要素と`@import`の2種類を用意していますが、どちらも外部スタイルシートを読み込むもので機能的には同一です。ここでは複数のMarkdownファイルにWebフォントを適用できるメリットを重視し、スタイルシート（Custom theme）に`@import`の読み込みコードをペーストすることにします（HTMLファイルで使うため前後に`style`要素が入っていますが、それらは取り除いてください）

それから、具体的なフォント名を指定する`font-family`のコードもCustom themeにペーストします。ここではルート要素にしっぽり明朝 Regular 400を、`h1`にNoto Sans Japanese Bold 900を、`h2`にNoto Sans Japanese Medium 700を指定しました

3. 設定ファイル`vivliostyle.config.js`の中で、Custom themeのpathを指定します（→[Custom theme](/ja/functions-of-the-actions-menu/theme.md#custom-theme)）。`entry: `にはPDF出力するファイル名を記述します

```js
module.exports = {
  title: '私の本',
  author: '尾久綿次郎',
  theme: 'css/style.css',
  entry: [
    'chapter-2.md',
    ]
}
```

4. ActionメニューでCustom themeを選択し、プレビューにWebフォントが適用されたことを確認します。themeが切り替わらない場合は、ブラウザをリロードさせてください

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-9.png)

5. Actionメニューで「Export（出力） > PDF」を選択すると、WebフォントでPDF出力ができます（→[Export（出力）> PDF](/ja/functions-of-the-actions-menu/export.md#pdf)）。プレビューと同じフォントが、同じ文字サイズ、行長、行送りでPDF出力されたことを確認します

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-10.png)

- **補足情報**
    - この記事では複数のMarkdownファイルにWebフォントを適用するためスタイルシート（Custom theme）に`@import`をペーストしましたが、特定のMarkdownファイルにだけWebフォントを適用したい場合は、当該ファイルの先頭に読み込みコード（`link`要素、及び`style`要素で囲った`@import`のどちらか）をペーストします。その際、忘れずにスタイルシートの方で`font-family`を指定してください
    - [bunny.net](https://fonts.bunny.net/)によりGoogleフォントと同じフォントが無償で利用可能です
        - このサービスはGoogleフォントと互換性を維持した上で（つまり同じフォントをホスティングした上で）、EUの[GDPR（一般データ保護規則）](https://www.jetro.go.jp/world/europe/eu/gdpr/)をクリアするためにユーザーのトラッキングをしないことを明示しています（[bunny.net > about](https://fonts.bunny.net/about)）
        - 使い方は簡単で、Googleフォントで取得した読み込み用コードのうち、`googleapis.com`の部分を`bunny.net`に置き換えるだけ
        - もしくは、[bunny.net](https://fonts.bunny.net/)でフォントを選択し、画面右上の「Font+」をクリックして読み込みコードを取得し、スタイルシート（Custom theme）かMarkdownにペーストします

## Custom theme／有償Webフォントサービスの使用      

Googleフォントは無償で利用できるメリットがありますが、デメリットは読み込みスピードが多少落ちることです。短い文章なら問題なくとも、原稿がとても長い場合は遅さが気になるかもしれません。そうした場合は、有償Webフォントサービスの利用を検討するとよいでしょう。本項ではダイナコムウェア社の[DynaSmart V](https://www.dynacw.co.jp/product/product_dynasmart_detail.aspx?sid=25)を例にとり、これをVivliostyle Pubで利用する方法を説明します。なお、以下ではすでに同社のアカウントを取得している前提ですすめます。

1. DynaFont OnlineのマイページからVivliostyle Pubのドメイン名`vivliostyle-pub-develop.vercel.app`を登録した上で、利用したいフォントのJavaScriptコード（script要素）と`font-family`を取得します。詳細は下記ページが参考になるでしょう

    - [DFO JavaScript Generator（ダイナコムウェア）](https://dfo.dynacw.co.jp/service/JS_Gen.aspx)

ここでは本文書体としてＤＦ華康明朝体 StdN W3 OpenType、`h1`にＤＦ金剛黒体 Pro-6N Semibold OpenType、`h2`にＤＦ金剛黒体 Pro-6N Ultrabold OpenTypeを利用することにします

2. Markdownファイルの先頭に取得したJavaScriptコードをペーストします（この段階ではまだフォントは変更されていません）

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-11.png)

3. 取得した`font-family`を記入した以下のようなスタイルシート（Custom theme）をアップロードします（→[ファイルのアップロード](/ja/file-and-folder-operations/file-list-pane-operations.md)）。すでにCustom themeがある場合は、下記を参考に書き換えてください

```css
@charset "UTF-8";

html{
writing-mode: vertical-rl;
font-family: 'DFMinchoPPro6N-W3', serif;
font-style: normal;
text-align: justify;
text-spacing: space-first allow-end ideograph-alpha ideograph-numeric;
line-height: 2;
}

p {
  font-weight: 400;
  text-indent: 1em;
  hanging-punctuation: first allow-end;
}

h1 {
font-family: 'DFKingGothicJP16N-Ultrabold', sans-serif; 
}

h2 {
font-family: 'DFKingGothicJP16N-Semibold', sans-serif; 
}

@page {
  size: 148mm 210mm;
  width: 360pt;
  height: 468pt;
  margin: auto;
  font-size: 8.5pt;
}
@page :left {
  @top-left {
    writing-mode: horizontal-tb;  
    content: counter(page) "　" env(doc-title);
    margin-left: 7pt;
    margin-top: 8.5mm;
  }
}
@page :right {
  @top-right {
    writing-mode: horizontal-tb;
    content: counter(page);
    margin-right: 7pt;
    margin-top: 8.5mm;
   }
}
```

4. 設定ファイル`vivliostyle.config.js`の中で、Custom themeのあるpathを指定します（→[Custom theme](/ja/functions-of-the-actions-menu/theme.md#custom-theme)）。`entry: `にはPDF出力するファイル名を記述します

```js
module.exports = {
  title: '私の本',
  author: '尾久綿次郎',
  theme: 'css/style.css',
  entry: [
    'chapter-2.md',
    ]
}
```

5. Actionメニューから「Custom theme」を選択します。themeが切り替わらない場合は、ブラウザをリロードさせてください

6. プレビューでＤＦ華康明朝体、ＤＦ金剛黒体が使用されるようになりました

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-12.png)

7.  Actionメニューから「Export（出力）> PDF」を選択すると、Custom themeを適用したPDFが出力されます（→[Export（出力）> PDF](/ja/functions-of-the-actions-menu/export.md#pdf)）。プレビューと同じＤＦ華康明朝体、ＤＦ金剛黒体が、同じ文字サイズ、行長、行送りにより使用されていることを確認してください   

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-13.png)

- **補足情報**
    - 有償Webフォントサービスの読み込みスピードが速いのは、**動的サブセッティング**という方式を採用しているからです。これは収容文字数が膨大になる東アジア言語のWebフォントで有効性を発揮する技術です
    - 大容量のフォントファイルはネットワークに依存するWebフォントに不向きです。そこでレンダリング前にコンテンツをパースし、そこに含まれている文字だけからなる小容量のサブセット・フォントを作成し、これをWebサーバに送ってレンダリングします。常にサブセットの内容が異なるのでこの名前があります
    - これに対してGoogleフォントが採用しているのは**静的サブセッティング**です。この方式ではコンテンツとは無関係に、使用頻度ごとに小容量のサブセット・フォントに分割しておきます。Webサーバーから文字を要求されると、その文字が含まれたサブセット・フォントを送ってレンダリングします。サブセットの内容は固定されているのでこの名前があります。前者と比べれば効率は悪くなりがちで、読み込みスピードは前者に軍配が上がります
    - このように使い勝手に優れる有償Webフォントサービスですが、利用規約によって用途を制限されている点に注意が必要です。Vivliostyle Pubで無条件にこれらのサービスが利用できるわけではないのです
    - こうした状況をうけ、Vivliostyle Pubで安心して有償Webフォントサービスを利用してもらうために、サービスごとに推奨する用途を選定しました。どうかご参照ください
       - [推奨する有償Webフォントサービスの用途](/ja/create-and-save-documents/additional-information-on-fonts.md#推奨する有償webフォントサービスの用途)
