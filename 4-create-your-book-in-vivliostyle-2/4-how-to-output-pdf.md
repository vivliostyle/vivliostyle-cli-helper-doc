# PDFの書き出し方**（21:47）**

1. 編集画面にカーソルを置いた状態で右クリックします（スタイルシート等ではなく、PDFにするテキストの編集画面）。
2. 表示されたサブメニューから「vivliostyle-cli-helper」（赤丸）、ついで「これビルド vivliostyle build (Current File)」（赤矢印）を選択

![](/images/4-create-your-book-in-vivliostyle-2/4-how-to-output-pdf/4-4-1.png)

- **補足：**動画22分前後に、プレビュー表示している時にPDFを出力したい場合、いったん`control`+`c`でプレビューを終了させなければならない旨の説明があります。この問題は修正され、現在はプレビューを閉じるだけで終了できます。
    - [feat: Preview should be terminated when the previewing page is closed #441](https://github.com/vivliostyle/vivliostyle-cli/pull/441)


3 ターミナルのペインを見ると（赤四角）、PDFをビルドしていることが分かります。「🎉 Build successfully」と表示されたら成功です。

![](/images/4-create-your-book-in-vivliostyle-2/4-how-to-output-pdf/4-4-2.png)

- Markdownファイルと同じ階層にPDFファイルが生成されています。開いてみましょう。

![](/images/4-create-your-book-in-vivliostyle-2/4-how-to-output-pdf/4-4-3.png)

- トンボ付きのPDFファイルが生成されました。

![](/images/4-create-your-book-in-vivliostyle-2/4-how-to-output-pdf/4-4-4.png)

