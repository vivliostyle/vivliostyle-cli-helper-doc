# Google Fontsの使い方

## Google Fontsでフォントを選択

- [Google Fonts](https://fonts.google.com/)のカタログページを表示します。
- 「Filter」（赤丸）ボタンをクリックします。

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-1.png)

- フィルター・ペインが開きます。「Language」メニュー（赤丸）で「Japanese」を選択すると日本語フォントだけにフィルタリングされます。
- 「Preview」（赤四角）のカラムに任意の文章を入力すると、そのままサンプルテキストとして表示されます。

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-2.png)

- まず本文に使うフォントをクリックして選択します（赤矢印）。

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-3.png)

- すると、選択したフォントのウェイトごとのサンプルテキストが一覧できる詳細画面に遷移します。
- 本文用なので、ここでは細目のウェイトを選択します。当該ウェイト右端にあるプラスマーク（赤矢印）をクリックします。

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-4.png)

- 当該ウェイトが選択され、プラスマークがマイナスマーク（赤四角）に変わりました。
- 画面右上のバッグのアイコン（赤丸）をクリックしてください。
    - なお、バッグのアイコンについている赤い点は、選択状態のフォントがあることを示すマークです。

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-5.png)

## コードをスタイルシートにコピー

- すると「Selected family」（赤矢印／選択されたフォント・ファミリー）のペインが開きます。
- 先ほどクリックしたフォントとそのウェイトが青い文字で表示され（大赤丸）、これが選択されていることを示しています。
    - ここでマイナスマーク（赤四角）をクリックすると選択を解除できます。
- 追加で見出し用のフォントを選択しましょう。画面左上、ブラウザの右矢印「←」（小赤丸）をクリックします。

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-6.png)

- 前画面に戻りました。見出し用のフォントをクリックして選択します（赤矢印）。

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-7.png)

- 選択したフォントのウェイトごとのサンプルテキストが一覧できる詳細画面に遷移します。以下の手順でコードをコピーしていきます。コピーした文字列は後で使うために、いずれもエディタ・メモ帳アプリ等にペーストしておいてください。


1. 任意のウェイト右端のプラスマーク（赤矢印）をクリックして選択します。見出し用なので、ここでは太めのウェイトを選択します。
2. 「Selected family」ペイン中程にある「import」ラジオボタンをクリックします。
3. ラジオボタン下に表示されるCSSコードをコピーします。この時、`<style>`と`</style>`はコピーしないでください。
4. 「CSS rule to specify families」の下に表示されるコードのうち、本文用として選択したフォント名の文字列を、シングルクォートごとコピーします。
5. 見出し用として選択したフォント名の文字列を、シングルクォートごとコピーします。

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-8.png)

1. page_settings.cssを開きます。
2. 2行目に、前項手順3でコピーしたコードをペーストします。
3. 26行目、`--main-text-font: `に続けて、前項手順4でコピーした本文用フォント名の文字列をペーストします。行末にセミコロン`;`をお忘れなく。
4. 27行目、`--header-font: `に続けて、前項手順5でコピーした見出し用フォント名の文字列をペーストします。行末にセミコロン`;`をお忘れなく。

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-9.png)

- プレビューを表示させると、選択したフォントが適用されていることが確認できます。

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-10.png)

