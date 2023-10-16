# 画像の指定方法

## 挿絵として画像を入れる方法**（26:25、p.106）**

1. 新規イラスト画像を、Markdownファイルと同じ階層の`img`フォルダにコピーします。**（27:50）**
    - フォルダ名が同じ、`css`フォルダの中の`img`フォルダと間違わないでください。

![](/images/4-create-your-book-in-vivliostyle-2/5-how-to-include-illustrations/4-5-1.png)

2. Markdownファイルの、画像を入れたい箇所に以下のような記法で指定します。**（27:58）**
    - `![キャプション](画像ファイルのpath)`

```css
![明治28年に竣工した千代ヶ崎砲台跡](img/IMG_8510.png)
```

- **補足：** キャプションの入れ方については動画**28:41**を、サイズ指定については動画**28:21**を参照してください。

![](/images/4-create-your-book-in-vivliostyle-2/5-how-to-include-illustrations/4-5-2.png)

3. 以下のようにプレビューされます。**（28:12）**

![](/images/4-create-your-book-in-vivliostyle-2/5-how-to-include-illustrations/4-5-3.png)

4. HTMLファイルをみてみましょう**（29:11）**。figure要素として画像が、figcaption要素としてキャプションがパースされていることが確認できます（水色でテキスト選択された部分）。
    - **補足：** vivliostyle-cli-helperは、プレビューやPDFビルドのためにHTMLファイルを生成します。上記で見ているのはこのHTMLファイルです。ファイル名は先頭に`.`を付けたランダムな英数字が使われています。これは一時的に作られたテンポラリファイルであり、時間がたつと自動的に削除されるのでご注意ください。

![](/images/4-create-your-book-in-vivliostyle-2/5-how-to-include-illustrations/4-5-4.png)

## figure要素を自分で指定する方法**（31:41）**

1. 複数の画像を続けて配置する場合を考えてみましょう。直感的には以下のように、前項で説明された画像ファイルを指定する記法を2つ続ければよいように思えます。

![](/images/4-create-your-book-in-vivliostyle-2/5-how-to-include-illustrations/4-5-5.png)

2. ではファイルを保存して、プレビューを表示させてみましょう。
    - 上下に2枚連続して収まったのはよいのですが、すこしずれてしまって体裁が悪いですね。しかもキャプションがありません。

![](/images/4-create-your-book-in-vivliostyle-2/5-how-to-include-illustrations/4-5-6.png)

5. プレビューのために生成されたHTMLファイルを確認してみると、2つの画像ファイルがp要素に囲まれていることが分かります。
    - p要素（段落要素）はコンテンツ（この場合は画像）をインライン方向（この場合はヨコ）に順次配置します。
    - しかしこの場合は画像ファイルのサイズが大きいのでインライン方向に配置しようとしても版面に収まらず、強制的に次行に折り返す形で上下に配置されたわけです。
    - ただし、2つの画像は結果として上下に配置されただけなのでずれてしまいました。
    - また、figure要素にならないので、キャプションをパースするfigcaption要素も付加されないので、キャプションがなくなってしまったのです。

![](/images/4-create-your-book-in-vivliostyle-2/5-how-to-include-illustrations/4-5-7.png)

6. では、下記のように自分で画像ファイルの前後にfigureタグを付けてみたらどうでしょう？

![](/images/4-create-your-book-in-vivliostyle-2/5-how-to-include-illustrations/4-5-8.png)

7. きれいに上下に、そして版面に揃って配置されました。ただし、キャプションはないままです。

![](/images/4-create-your-book-in-vivliostyle-2/5-how-to-include-illustrations/4-5-9.png)

8. HTMLファイルを確認すると、2つの画像をパースする2つのimgタグが、figure要素に包まれていることが分かります。
    - ただし、figcaption要素はありません。

![](/images/4-create-your-book-in-vivliostyle-2/5-how-to-include-illustrations/4-5-10.png)

9. では、それぞれの画像に`{width=219}`として画像の幅が219pxになるように指定してみましょう。

![](/images/4-create-your-book-in-vivliostyle-2/5-how-to-include-illustrations/4-5-11.png)

10. 画像の幅は版面のギリギリ半分未満である219pxになったため、インライン方向（この場合はヨコ）に配置されました。

![](/images/4-create-your-book-in-vivliostyle-2/5-how-to-include-illustrations/4-5-12.png)

11. HTMLを確認してみましょう。上記8.のHTMLに幅を表す`width="219"`の属性が付加されていることが確認できます。

![](/images/4-create-your-book-in-vivliostyle-2/5-how-to-include-illustrations/4-5-13.png)

- **補足：** その他、2つの画像をfigureタグで囲まずに1行空けて指定するとどうなるか、同じく幅をぞれぞれ`{width=219}`とした上で1行空けずに指定するとどうなるか、その時キャプションはどうなるか、またHTMLはどのようにパースされるかなど、いろいろなパターンを試してみると面白いでしょう。