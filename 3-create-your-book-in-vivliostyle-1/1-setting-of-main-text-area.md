# 本文領域の設定方法

- 本章から括弧内の数字は[「講師に教わりながら、Vivliostyleで本を作る！ 第2部-1」](https://youtu.be/SrlJI5rKTbo?si=-thEgFbKQJM2TI6H)の再生時間になります。

## Markdownファイルを開く

- lesson2＞formatE_tate＞ginga.md（赤丸）を開く**（2:11）**

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-1.png)

## カーソルをエディター部分に置いた状態で右クリック**（2:27）**

- 表示されたサブメニューから「vivliostyle-cli-helper」（赤丸）、ついで「これプレビューvivliostyle preview (Current File)」（赤矢印）を選択

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-2.png)

- ブラウザーが自動的に起動して「sample1.md」をCSS組版したプレビューが表示されます。

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-3.png)

## スタイルシートを開く**（3:50）**

- lesson2＞formatE_tate＞css＞page_settings.css（赤丸）を開く

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-4.png)

## 本文領域の指定

- ここからスタイルシートの中の本文領域に関わるプロパティを書き換えて、それぞれの役割を確認していきましょう
- 13行目、`:root {`以下が本文領域に関わる指定です
- まず、`--line-height:`の値を`40Q`に書き換えて、プレビューを確認してみましょう**（4:18）**
    - **補足** この時、接頭辞`--`は[変数（カスタムプロパティ）](https://developer.mozilla.org/ja/docs/Web/CSS/Using_CSS_custom_properties)であることを表します。これはユーザーによって定義された（カスタマイズされた）再利用可能なプロパティです。**もう具体的に詳しく、プロパティとの違いの説明が必要**

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-5.png)

- この時プレビューは以下のようになります。行送りが極端に広くなったことが確認できます**（4:36）**
- つまり、`--line-height:`は行送りの指定です

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-6.png)

- つぎに`--line-height:`の値を`24Q`に戻した上で、`--letters-per-line:`を40に減らしてみましょう**（5:20）**

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-7.png)

- この時プレビューは以下のようになります。1ページ当たりの行数が減ったことが確認できます。
- つまり、`--letters-per-line:`は1行の字詰めの指定です**（5:39）**

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-8.png)

- つぎに`--lines-per-page:`を`15`に減らしてみましょう。

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-9.png)

- 1ページ当たり15行になったことが確認できます。
- つまり、`--lines-per-page:`は1ページの行数の指定です

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-10.png)

- つぎに`--page-margin-top:`を`30mm`に増やしてみましょう**（6:52）**

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-11.png)

- 上側マージンが30㎜に増えたことが確認できます。

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-12.png)

- つぎに`--page-margin-xshift:`を`4mm`に変更してみましょう**（7:36）**

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-13.png)

- ノド側のマージンが広がった（ノド側に本文領域がシフトした）ことがわかります。

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-14.png)
