# 見出し周りの装飾**（12:33）**

## 新規画像を`css`フォルダ直下の`img`フォルダにコピー

- 用意したアイコン用の新規画像を`formatE_yoko`＞`css`＞`img`に入れます（赤丸）。**（15:15）**

![](/images/3-create-your-book-in-vivliostyle-1/3-decoration-around-headings/3-3-1.png)

## `css`フォルダ内の`main.css`を開く**（16:15）**

![](/images/3-create-your-book-in-vivliostyle-1/3-decoration-around-headings/3-3-2.png)

## main.css87行目の`h2::before {`以下を書き換える**（16:41）**

- `h2::before`をふくむ赤四角部分は、H2見出しのスタイルを定義している部分です。ここを書き換えることで、H2見出しを装飾していきます。
- まず、89行目`background: url("…");`のうち、`"`と`"`に囲まれた部分のpathを、表示させたい画像のpathに書き換えてみましょう。

![](/images/3-create-your-book-in-vivliostyle-1/3-decoration-around-headings/3-3-3.png)

- pathを新しい画像ファイルのpathに書き換えました。「vivliostyle-cli-helper」でプレビューさせてみましょう。**（17:05）**

![](/images/3-create-your-book-in-vivliostyle-1/3-decoration-around-headings/3-3-4.png)

- H2見出しの先頭にアイコンのように画像ファイルが表示されます。試しにもう少し大きくしてみましょう。

![](/images/3-create-your-book-in-vivliostyle-1/3-decoration-around-headings/3-3-5.png)

- 92行目の`block-size:`の値を`24mm`から`40mm`に変更してみる（赤四角）。
    - **補足**：`block-size:`は、当該イラストを含むブロックの、書字方向がヨコの場合はタテの、タテの場合はヨコのサイズを指定するプロパティです。**（17:44）**

![](/images/3-create-your-book-in-vivliostyle-1/3-decoration-around-headings/3-3-6.png)

- プレビューすると以下のように少し大きくなりました。でも大きすぎですね。

![](/images/3-create-your-book-in-vivliostyle-1/3-decoration-around-headings/3-3-7.png)

- 先の`block-size:`の値を`24mm`に戻します。
- 93行目の`inline-size:`の値を`24mm`から`40mm`に変更します（赤四角）。
    - **補足**：`inline-size:`は、当該イラストを含むブロックの、書字方向がヨコの場合はヨコの。タテの場合はヨコのサイズを指定するプロパティです。**（17:44）**

![](/images/3-create-your-book-in-vivliostyle-1/3-decoration-around-headings/3-3-8.png)

- プレビューさせると、今度のサイズはしっくりきます。

![](/images/3-create-your-book-in-vivliostyle-1/3-decoration-around-headings/3-3-9.png)

- つぎに位置を変更してみましょう。
- 93行目の`inset-inline-start:`の値を`-20mm`から`-30mm`に変更します（赤四角）。
    - **補足**
        - この`inset-inline-start:`は当該イラストを含む**インライン方向**の、先頭のオフセット（書字方向がヨコの場合はヨコの、タテの場合であればタテの距離）を指定するプロパティです。**（17:58）**
        - もう一つの`inset-block-start:`は、当該イラストを含む**ブロック方向**における先頭のオフセット（書字方向がヨコの場合はタテの、タテの場合であればヨコの距離）を指定するプロパティです。**（17:58）**

![](/images/3-create-your-book-in-vivliostyle-1/3-decoration-around-headings/3-3-10.png)

- 指定したオフセットが大きすぎて、見出しからだいぶ離れてしまいました。

![](/images/3-create-your-book-in-vivliostyle-1/3-decoration-around-headings/3-3-11.png)

- `inset-inline-start:`の値を`-17mm`に変更します（赤四角）。

![](/images/3-create-your-book-in-vivliostyle-1/3-decoration-around-headings/3-3-12.png)

- 今度はヨコの位置はうまくいきました。しかし、タテの位置が少しだけ上すぎるようです。

![](/images/3-create-your-book-in-vivliostyle-1/3-decoration-around-headings/3-3-13.png)

- `inset-block-start:`の値を`2mm;`に変更します（赤四角）。

![](/images/3-create-your-book-in-vivliostyle-1/3-decoration-around-headings/3-3-14.png)

- 失敗。タテの位置が下すぎになってしまいました。

![](/images/3-create-your-book-in-vivliostyle-1/3-decoration-around-headings/3-3-15.png)

- 今度は`inset-block-start:`の値を`-2mm;`に変更します（赤四角）。

![](/images/3-create-your-book-in-vivliostyle-1/3-decoration-around-headings/3-3-16.png)

- ようやくいい感じになりました。

![](/images/3-create-your-book-in-vivliostyle-1/3-decoration-around-headings/3-3-17.png)

- devツールの表示を確認してみましょう。イラスト画像の本来の位置はオレンジ色の部分に該当し、ここからのタテとヨコのオフセット量をそれぞれ値として指定しています。

![](/images/3-create-your-book-in-vivliostyle-1/3-decoration-around-headings/3-3-18.png)