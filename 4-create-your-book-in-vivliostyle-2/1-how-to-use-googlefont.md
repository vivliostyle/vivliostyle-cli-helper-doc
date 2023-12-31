# Google Fontsの使い方

- 本章から括弧内の数字は[「講師に教わりながら、Vivliostyleで本を作る！ 第2部-2」](https://youtu.be/VnwddnaSsik?si=KlrmYX17cc3VN1wc)の再生時間になります。
- なお、Google Fontsの画面は執筆時点（2023年10月4日）のものであり、セミナーの開催時、そして『CSS組版 Vivliostyle入門』とも異なることをお断りします。

## フォントの選択

- Google Fonts[（https://fonts.google.com/）](https://fonts.google.com/)のカタログページを表示します。**（0:23）**
- 「Filter」（赤丸）ボタンをクリックします。

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-1.png)

- フィルター・ペインが開きます。「Language」メニュー（赤丸）で「Japanese」を選択すると日本語フォントだけにフィルタリングされます。**（1:17）**
- 「Preview」（赤四角）のカラムに任意の文章を入力すると、そのままサンプルテキストとして表示されます。**（1:35）**

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-2.png)

- まず本文に使うフォントをクリックして選択します（赤矢印）。**（2:01）**

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-3.png)

- すると、選択したフォントのウェイトごとのサンプルテキストが一覧できる詳細画面に遷移します。
- 本文用なので、ここでは細目のウェイトを選択します。当該ウェイト右端にあるプラスマーク（赤矢印）をクリックします。**（2:15）**

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-4.png)

- 当該ウェイトが選択され、プラスマークがマイナスマーク（赤四角）に変わりました。
- 画面右上のバッグのアイコン（赤丸）をクリックしてください。**（2:22）**
    - なお、バッグのアイコンについている赤い点は、選択状態のフォントがあることを示すマークです。

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-5.png)

## 選択したフォントのコードをコピー

- すると「Selected family」（赤矢印／選択されたフォント・ファミリー）のペインが開きます。**（2:24）**
- 先ほどクリックしたフォントとそのウェイトが青い文字で表示され（大赤丸）、これが選択されていることを示しています。
    - ここでマイナスマーク（赤四角）をクリックすると選択を解除できます。
- 追加で見出し用のフォントを選択しましょう。画面左上、ブラウザの右矢印「←」（小赤丸）をクリックします。**（2:33）**

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-6.png)

- 前画面に戻りました。見出し用のフォントをクリックして選択します（赤矢印）。**（2:49）**

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-7.png)

- 選択したフォントのウェイトごとのサンプルテキストが一覧できる詳細画面に遷移します。以下の手順でコードをコピーしていきます。コピーした文字列は後で使うために、いずれもエディタ・メモ帳アプリ等にペーストしておいてください。


1. 任意のウェイト右端のプラスマーク（赤矢印）をクリックして選択します（❶）。見出し用なので、ここでは太めのウェイトを選択します。
2. 「Selected family」ペイン中程にある「import」ラジオボタンをクリックします（❷）。**（3:15）**
3. ラジオボタン下に表示されるCSSコードをコピーします（❸）。この時、`<style>`と`</style>`はコピーしないでください。**（3:29）**
4. 「CSS rule to specify families」の下に表示されるコードのうち、本文用として選択したフォント名の文字列を、シングルクォートごとコピーします（❹）。**（4:14）**
5. 見出し用として選択したフォント名の文字列を、シングルクォートごとコピーします（❺）。**（4:15）**

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-8.png)

## スタイルシートにコードをペースト

1. page_settings.cssを開きます。
2. 2行目に、前項手順3でコピーしたコードをペーストします（❶）。**（3:45）**
3. 26行目、`--main-text-font: `に続けて、前項手順4でコピーした本文用フォント名をペーストします（❷）。行末にセミコロン`;`をお忘れなく。**（4:27）**
4. 27行目、`--header-font: `に続けて、前項手順5でコピーした見出し用フォント名をペーストします（❸）。行末にセミコロン`;`をお忘れなく。**（4:41）**
5. ここまでの変更を保存します。

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-9.png)

- プレビューを表示させると、選択したフォントが適用されていることが確認できます。**（4:51）**

![](./images/4-create-your-book-in-vivliostyle-2/1-how-to-use-googlefont/4-1-10.png)

