# Markdownファイルの新規作成

## 用意した新規テキストファイルをフォルダにコピーする**（9:45）**

- 新規テキストファイルのコピー先は、作る本が横書きなら「formatE_yoko」直下、縦書きなら「formatE_tate」直下です。

![](/images/3-create-your-book-in-vivliostyle-1/2-create-a-new-markdown-file/3-2-1.png)

## テキストファイルの拡張子を.mdに変更する**（9:57）**

1. エクスプローラーでフォルダ「formatE_yoko」（縦書きなら「formatE_tate」）を選択します。
2. エクスプローラーから先に追加したテキストファイルを見つけ、そのファイルを選択して右クリックします。
3. 表示されたサブメニューから「名前を変更」を選択します。

![](/images/3-create-your-book-in-vivliostyle-1/2-create-a-new-markdown-file/3-2-2.png)

- そのテキストファイルのファイル名が変更可能になりました（赤丸）。ファイル名はそのままに、拡張子だけ`.txt`から`.md`に変更します。

![](/images/3-create-your-book-in-vivliostyle-1/2-create-a-new-markdown-file/3-2-3.png)

- 拡張子が変更されました（赤丸）。

![](/images/3-create-your-book-in-vivliostyle-1/2-create-a-new-markdown-file/3-2-4.png)

## Markdownファイルを開き、プレビューを表示させる

1. エクスプローラーから先に拡張子を変更したMarkdownファイルを選択して開きます。
2. 表示されたサブメニューから「vivliostyle-cli-helper」（赤丸）、ついで「install/update vivliostyle-cli」（赤矢印）を選択します。

![](/images/3-create-your-book-in-vivliostyle-1/2-create-a-new-markdown-file/3-2-5.png)

- プレビューが表示されました。見て分かるように、前節まで書いてきたスタイルシートは適用されていないことにご注意ください。

![](/images/3-create-your-book-in-vivliostyle-1/2-create-a-new-markdown-file/3-2-6.png)

## ファイルの先頭に、`ginga.md`のフロントマターをコピペする**（10:47）**

1. フロントマターから第2章で使った`ginga.md`（赤丸）を選択して開きます。
2. `ginga.md`冒頭の`---`で囲まれた部分（フロントマター）をコピーします（赤四角）。

![](/images/3-create-your-book-in-vivliostyle-1/2-create-a-new-markdown-file/3-2-7.png)

3. 新しいMarkdownファイルを開き（赤丸）、その冒頭に先ほどのコピーした文字列をペーストします（赤四角）。

![](/images/3-create-your-book-in-vivliostyle-1/2-create-a-new-markdown-file/3-2-8.png)

4. 「vivliostyle-cli-helper」でプレビューしてみると（操作は前項「Markdownファイルを開き、プレビューを表示させる」参照）、`ginga.md`のスタイルシートがそのまま新しいMarkdownファイルにも適用されるようになりました。

![](/images/3-create-your-book-in-vivliostyle-1/2-create-a-new-markdown-file/3-2-9.png)
