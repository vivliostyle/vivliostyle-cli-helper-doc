# スタイルシートの編集②

## 新しく「sample2.css」を開く

![](/images/2-introduction-to-vivliostyle/6-editing-style-sheets-2/2-6-1.png)

## ページサイズを指定する

![](/images/2-introduction-to-vivliostyle/6-editing-style-sheets-2/2-6-2.png)

- 1行目以降に以下のように記述します（そのままコピー・アンド・ペーストしてもよいでしょう）

```css
@charset "utf-8";

@page {
  size: 148mm 210mm;
  }
```

- 記述したらメニューバーから「ファイル＞保存」を選んでファイルを保存します
- ファイルを保存すると、プレビューが更新され、再びページ表示になっています

![](/images/2-introduction-to-vivliostyle/6-editing-style-sheets-2/2-6-3.png)

## 本文領域を指定する

![](/images/2-introduction-to-vivliostyle/6-editing-style-sheets-2/2-6-4.png)

- 3行目に以下のように記述します。この指定は、これ以降はサイズの基準を、border（要素の枠線）にするというものです。

```css

* {
  box-sizing: border-box;
  }

```

- 10行目以降に以下のように記述します

```css
@page:left {
  margin-block: 15mm; margin-inline: 16mm 18.25mm;
  }
@page: right {
  margin-block: 15mm; margin-inline: 18.25mm 16mm;
  }
:root {
  font-size: 13Q;
  line-height: 24Q,
  font-family: "Noto Sans JP";
  font-weight: 400;
  text-spacing: auto;
  widows: 1;
  orphans: 1;
  }

p {
  font-size: 13Q;
  line-height: 24Q;
  text-align: justify;
  text-indent: 1em;
  margin-block: 0;
  }
```

- ファイルを保存すると、プレビューが更新され、指定したとおりの文字サイズ（font-size）、行送り（line-height）、行末の揃え方（text-align）、フォント（font-family）、ウェイト（font-weight）、和欧間隔（text-spacing）、ウィドウ（widows）、オーファン（オーファン）、行頭インデント（text-indent）、上下のマージン（margin-block）など、記述した指定が適用されています

![](/images/2-introduction-to-vivliostyle/6-editing-style-sheets-2/2-6-5.png)

## H2見出しの指定をする

![](/images/2-introduction-to-vivliostyle/6-editing-style-sheets-2/2-6-6.png)

- 35行目以降に以下のように記述します

```css
h2 {
  break-before: page;
  font-size: 40q;
  line-height: 54Q;
  }
```

- ファイルを保存すると、プレビューが更新され、H2見出しの直前で改行され（break-before: page）、指定したとおりの文字サイズ（font-size）、行送り（line-height）が適用されています

![](/images/2-introduction-to-vivliostyle/6-editing-style-sheets-2/2-6-7.png)

![](/images/2-introduction-to-vivliostyle/6-editing-style-sheets-2/2-6-8.png)