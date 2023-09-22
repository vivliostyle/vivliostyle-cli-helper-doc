#  クイックスタートガイド 

## 必要環境 

- Chromeブラウザ（PC版）が動作する環境であること
- GitHubアカウントを既に取得していること（未取得の方はこちら→[GitHubアカウントの取得方法](/ja/advance-preparation/get-an-account#github%E3%82%A2%E3%82%AB%E3%82%A6%E3%83%B3%E3%83%88%E3%81%AE%E5%8F%96%E5%BE%97%E6%96%B9%E6%B3%95)）

## 初期画面

以下のURLにアクセスすると、初期画面が表示されます。

https://vivliostyle-pub-develop.vercel.app/

![](images/readme-first/fig-1.png)

1. ……「Login」ボタンを押して、GitHubアカウントでログインしてください（→[GitHubアカウントの取得方法](/ja/advance-preparation/get-an-account#github%E3%82%A2%E3%82%AB%E3%82%A6%E3%83%B3%E3%83%88%E3%81%AE%E5%8F%96%E5%BE%97%E6%96%B9%E6%B3%95)）
2. ……言語メニューから使用言語を選択することができます（English / 日本語）
3. ……ユーザーガイド（本文書）を表示します



## リポジトリとブランチの選択

ログインしたら、以下の画面でリポジトリを選択してください。リポジトリに複数のブランチがある場合はブランチも選択できます。公開リポジトリは“Public”、非公開は“Private” と表示されます。

![](images/readme-first/fig-2.png)

1. ……GitHubアプリのインストール（→[最初のログインで必要な作業](/ja/advance-preparation/login.md)）
2. ……GitHubアクセス・トークンのリフレッシュ（→[最初のログインで必要な作業](/ja/advance-preparation/login.md)）
3. ……GitHubアカウントのユーザー名（[GitHub > Settings > Public profile](https://github.com/settings/profile)）
4. ……言語メニュー（English / 日本語）
5. ……ユーザーガイド（本文書）の表示
6. ……リポジトリ表示の更新
7. ……リポジトリの選択

いずれかのリポジトリ（ 7 ）をクリックすると、自動的にエディタ／プレビュー画面に遷移します。

## ログアウト／利用者アンケートの送付／不具合のフィードバック

GitHubアカウントのユーザー名をクリックすると、プルダウンメニューが表示されます。ログアウトはメニュー項目の一番下です。これを選択すると、ログアウトして初期画面に戻ります。また、このメニューから利用者アンケートの送付や不具合のフィードバックができます。ぜひご利用ください。

![](images/readme-first/fig-3.png)

1. ……利用者アンケートの送付
2. ……不具合のフィードバック
3. ……ログアウト

## エディタ／プレビュー画面

![](images/readme-first/fig-4.png)

**ペイン境界線の移動**：ファイル一覧ペイン、エディタ・ペイン、プレビュー・ペインの境界線は変更できます。それぞれの区画の境界線上にマウスカーソルを置いてください。左右矢印「↔」の形状に変わったところでマウスボタンをプレスしたまま右か左にドラッグすると、境界線が左右に移動します。

### メニュー・エリア

![](images/readme-first/fig-5.png)

1. ……ユーザー名 / リポジトリ名
2. ……ブランチ切り替えメニュー
3. ……ファイル保存ボタン
4. ……GitHubアカウントのユーザー名（プルダウンメニュー→アンケート送付／フィードバック／ログアウト）
5. ……言語メニュー（English / 日本語）
6. ……ユーザーガイド（本文書）の表示
7. ……ファイル一覧ペインの表示／非表示
8. ……エディタ・ペインの表示／非表示
9. ……プレビュー・ペインの表示／非表示
10. ……Actionメニュー

Actionメニューをプルダウンすると、下記のような操作が可能です。

- Setting（設定）
    - [Presentation mode](/ja/functions-of-the-actions-menu/setting.md#presentation-modeプレゼンテーション・モード)
    - [Auto reload](/ja/functions-of-the-actions-menu/setting.md#auto-reload自動再読み込み)
- Theme（スタイル情報の選択）
    - [Plain theme](/ja/functions-of-the-actions-menu/theme.md#plain-theme)
    - [Custom theme](/ja/functions-of-the-actions-menu/theme.md#custom-theme)
    - [Book theme for latin font](/ja/functions-of-the-actions-menu/theme.md#book-theme-for-latin-font)
    - [文庫用のテーマ](/ja/functions-of-the-actions-menu/theme.md#文庫用のテーマ)
    - [Slide theme](/ja/functions-of-the-actions-menu/theme.md#slide-theme)
    - [ Techbook (技術同人誌) theme](/ja/functions-of-the-actions-menu/theme.md#techbook-技術同人誌-theme)
    -[Academic theme](/ja/functions-of-the-actions-menu/theme.md#academic-theme)
- Add files（ファイルの追加）
    - [Add Image（画像ファイルの追加）](/ja/functions-of-the-actions-menu/add-files.md#add-image画像ファイルの追加)
- Export（出力）
    - [PDF](/ja/functions-of-the-actions-menu/export.md#pdf)
- Help（ヘルプ）
    - [ VFM Spec（Vivliostyle Flavored Markdown仕様の表示）](/ja/functions-of-the-actions-menu/help.md#vfm-specvivliostyle-flavored-markdown仕様の表示)


### ファイル一覧ペイン

![](images/readme-first/fig-6.png)

1. ……リポジトリ内のファイル名を検索
2. ……リポジトリのファイル一覧を再取得
3. ……![](https://github.com/microsoft/vscode-codicons/raw/main/src/icons/arrow-up.svg) リポジトリにファイルをアップロード
4. ……![](https://github.com/microsoft/vscode-codicons/raw/main/src/icons/new-folder.svg) リポジトリにフォルダを新規作成
5. ……![](https://raw.githubusercontent.com/microsoft/vscode-codicons/main/src/icons/new-file.svg) リポジトリにファイルを新規作成
6. ……現在編集中のファイル（**太字**）
7. ……リポジトリ内のファイル一覧


- **アイコン種別一覧**
  - ![](https://raw.githubusercontent.com/astrit/css.gg/master/icons/svg/corner-left-up.svg)……上位フォルダへ移動
  - ![](https://raw.githubusercontent.com/microsoft/vscode-codicons/main/src/icons/folder.svg)……フォルダ
  - ![](https://raw.githubusercontent.com/microsoft/vscode-codicons/main/src/icons/file-media.svg)……画像ファイル
  - ![](https://raw.githubusercontent.com/microsoft/vscode-codicons/main/src/icons/code.svg)……HTMLファイル
  - ![](https://raw.githubusercontent.com/microsoft/vscode-codicons/main/src/icons/symbol-namespace.svg)……CSSファイル
  - ![](https://raw.githubusercontent.com/microsoft/vscode-codicons/main/src/icons/markdown.svg)……Markdownファイル
  - ![](https://raw.githubusercontent.com/microsoft/vscode-codicons/main/src/icons/settings-gear.svg)……vivliostyle.config.js
  - ![](https://raw.githubusercontent.com/microsoft/vscode-codicons/main/src/icons/file.svg)……その他のファイル


各種ファイル操作の詳細は下記をご参照ください。

- [ファイル一覧ペインからの操作](/ja/file-and-folder-operations/file-list-pane-operations.md)



### プレビュー・ペイン

![](images/readme-first/fig-7.png)

1. ……ファイル内の文字列を検索
2. ……ページ移動ボタン（左から先頭ページへ移動、前のページへ移動、後のページへ移動、末尾ページへ移動／単一ページの場合はグレイアウト）
3. ……ページカウンター（現在のページ／総ページ）
4. ……文字サイズ変更（左から小さく、大きく、デフォルト）
5. ……ズーム（左から縮小、拡大、等倍、フィットページ）
6. ……ページ移動スライドバー

## ログの表示 

![](images/readme-first/fig-8.png)

画面下端付近でマウスポインタを動かし、ポインタの形状が上下矢印「↕」に変わったところで、マウスボタンをプレスしたまま上方にドラッグするとログが現れます。