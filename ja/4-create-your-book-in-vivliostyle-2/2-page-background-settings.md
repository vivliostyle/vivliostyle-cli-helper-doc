# ページ背景の設定方法

1. page_settings.cssを開きます**（14:31）**
2. 55行目、`@page: left {`以下を編集することで、左ページのスタイルを設定します。
3. 55行目の行端（矢印）にカーソルを置き、enterキーを押して56行目に空行を作ります。

![](./images/4-create-your-book-in-vivliostyle-2/2-page-background-settings/4-2-1.png)

4. 56行目にプロパティを入力していきます。`background`と入力した後、ハイフン`-`を入力すると、VSCodeのサジェスト機能が働いて、`background-`に続く可能性のあるプロパティ候補が表示されます。**（18:27）**
  - 矢印キーでメニュー項目を移動、エンターキーで選択できます。
  - ここでは`background-color`を選択します。

![](./images/4-create-your-book-in-vivliostyle-2/2-page-background-settings/4-2-2.png)

5. つづいて`background-color`の値（色）を指定します。
  - `background-color`の右端にカーソルを置いた状態でコロン`:`を入力すると、VSCodeのサジェスト機能が働いて、`background-color`に続く可能性のある、値（色）の候補が表示されます。
  - 前項と同様に矢印キーでメニュー項目を移動、エンターキーで選択できます。

![](./images/4-create-your-book-in-vivliostyle-2/2-page-background-settings/4-2-3.png)

6. ここでは`#fffaf0`（floralwhite）を選択します。

![](./images/4-create-your-book-in-vivliostyle-2/2-page-background-settings/4-2-4.png)

7. ファイルを保存して、プレビューを表示させてみましょう。なかなかいい感じです。

![](./images/4-create-your-book-in-vivliostyle-2/2-page-background-settings/4-2-5.png)

8. 同じ要領で、71行目、`@page: right {`以下を編集することで、右ページのスタイルを設定できます。同様の手順で`background-color: #fffaf0;`を設定してみてください。