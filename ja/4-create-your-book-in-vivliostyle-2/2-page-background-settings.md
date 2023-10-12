# ページ背景の設定方法

1. page_settings.cssを開きます**（14:31）**
2. 55行目、`@page: left {`以下を編集することで、左ページのスタイルを設定します。
3. 56行目`/* background: url("img/R4_cssbk_smp_pageallbg_l.png"); */`とある行にカーソルを置いた状態で、Macでは`command`+`/`、Windowsでは`Ctrl`+`/`を入力します。

![](./images/4-create-your-book-in-vivliostyle-2/2-page-background-settings/4-2-1.png)

4. コメントアウトが外れました。
  - ソースコードの一部をプログラムとして無効な状態にすることを「コメントアウト」といいます。CSSでは`/*`と`*/`で囲むことでコメントアウトできます。
  - 反対に、有効な状態に戻すことを「コメントアウトを外す」といいます。

![](./images/4-create-your-book-in-vivliostyle-2/2-page-background-settings/4-2-2.png)

5. 56行目を修正していきます。文字列`background`の右端にカーソルを置いた状態で、ハイフン`-`を入力すると、VSCodeのサジェスト機能が働いて、`background-`に続く可能性のあるプロパティ候補が表示されます。
  - 矢印キーでメニュー項目を移動、エンターキーで選択できます。
  - ここでは`background-color`を選択します。

![](./images/4-create-your-book-in-vivliostyle-2/2-page-background-settings/4-2-3.png)

7. つづいて`background-color`の値を指定します。
  - `background-color`の右端にカーソルを置いた状態でコロン`:`を入力すると、VSCodeのサジェスト機能が働いて、`background-color`に続く可能性のある、カラーを示す値の候補が表示されます。
  - 前項と同様に矢印キーでメニュー項目を移動、エンターキーで選択できます。

![](./images/4-create-your-book-in-vivliostyle-2/2-page-background-settings/4-2-4.png)

8. ここでは`#fffaf0`（floralwhite）を選択します。

![](./images/4-create-your-book-in-vivliostyle-2/2-page-background-settings/4-2-5.png)

9. ファイルを保存して、プレビューを表示させてみましょう。なかなかいい感じです。

![](./images/4-create-your-book-in-vivliostyle-2/2-page-background-settings/4-2-6.png)

10. 同じ要領で、70行目、`@page: right {`以下を編集することで、右ページのスタイルを設定できます。同様の手順で`background-color: #fffaf0;`を設定してみてください。