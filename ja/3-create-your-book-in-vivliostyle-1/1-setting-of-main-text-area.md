# 本文領域の設定方法

## Markdownファイルを開く

- lesson2＞formatE_tate＞ginga.md（赤丸）を開く

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-1.png)

## カーソルをエディター部分に置いた状態で右クリック

- 表示されたサブメニューから「vivliostyle-cli-helper」（赤丸）、ついで「これプレビューvivliostyle preview (Current File)」（赤矢印）を選択

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-2.png)

- ブラウザーが自動的に起動して「sample1.md」をCSS組版したプレビューが表示されます。

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-3.png)

## スタイルシートを開く

- lesson2＞formatE_tate＞css＞page_settings.cssを開く

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-4.png)

- ここからスタイルシートの中の本文領域に関わるプロパティを書き換えて、それぞれの役割を確認していきましょう
- 13行目、`:root {`以下が本文領域に関わる指定です
- まず、`--line-height:`の値を`40Q`に書き換えて、プレビューを確認してみましょう

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-5.png)

- この時プレビューは以下のようになります。行送りが広くなったことが確認できます
- つまり、`--line-height:`は行送りを指定するプロパティです

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-6.png)

- つぎに`--line-height:`の値を`24Q`に戻した上で、`--letters-per-line:`を40に減らしてみましょう

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-7.png)

- 1行当たりの文字数が減ったことが確認できます。
- つまり、`--letters-per-line:`は字詰めを指定するプロパティです

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-8.png)

- つぎに`--lines-per-page:`の値を15に減らしてみる

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-9.png)

- 

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-10.png)

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-11.png)

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-12.png)

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-13.png)

![](/images/3-create-your-book-in-vivliostyle-1/1-setting-of-main-text-area/3-1-14.png)
