# 奥付と白紙ページ

## 奥付の作り方

- ginga.mdを開き、最終行を表示させてください。すると奥付用のhtml文があるので（水色テキスト選択部分）、これをコピーします。

![](./images/4-create-your-book-in-vivliostyle-2/6-how-to-make-a-colophon/4-6-1.png)

- 自分が作成したMarkdownファイルを開き、最終行にペーストします。

![](./images/4-create-your-book-in-vivliostyle-2/6-how-to-make-a-colophon/4-6-2.png)

- ファイルを保存して、プレビューを表示させてみましょう。

![](./images/4-create-your-book-in-vivliostyle-2/6-how-to-make-a-colophon/4-6-3.png)

- 奥付の内容は「銀河鉄道の夜」のものですから、これを自分の本に合わせてカスタマイズしましょう。

![](./images/4-create-your-book-in-vivliostyle-2/6-how-to-make-a-colophon/4-6-4.png)

- ファイルを保存して、プレビューを表示させてみましょう。奥付が中途半端な位置にあるのが残念です。

![](./images/4-create-your-book-in-vivliostyle-2/6-how-to-make-a-colophon/4-6-5.png)

- div要素を使ってスタイルを指定し、奥付のブロックを版面（テキストエリア）下端に配置してみましょう。

```html
<div style="float-reference: page; float: block-end;">
</div>
```

![](./images/4-create-your-book-in-vivliostyle-2/6-how-to-make-a-colophon/4-6-6.png)

- いい感じになりました。

![](./images/4-create-your-book-in-vivliostyle-2/6-how-to-make-a-colophon/4-6-7.png)

- **補足：**ここでは奥付のブロックをテキストエリア下端に揃えましたが、同じ記法を使って画像等をテキストエリア下端に揃えることもできます。その場合は画像を指定する行の前後ををdivで包みます。なお、テキストエリア上端に揃えたい場合は`block-start`をお使いください。

```html
<div style="float-reference: page; float: block-end;">

![明治28年に竣工した千代ヶ崎砲台跡](img/IMG_8510.png)

</div>
```


## 白紙ページの入れ方**（24:50）**

- 奥付の前で改ページしてみましょう。このスタイルシートでは、ハイフン3つ`---`で改ページになるよう設定されています（赤丸）。

![](./images/4-create-your-book-in-vivliostyle-2/6-how-to-make-a-colophon/4-6-8.png)

- 奥付の前で改ページできました。

![](./images/4-create-your-book-in-vivliostyle-2/6-how-to-make-a-colophon/4-6-9.png)

![](./images/4-create-your-book-in-vivliostyle-2/6-how-to-make-a-colophon/4-6-10.png)

- **補足：**この方法を使って白紙ページを任意の場所に入れることで、ページ数を調整することもできます。