# Export（出力）

## PDF

Actionメニューで「Export（出力）> PDF」を選ぶとPDFが出力されます。その際、出力されるファイルは、プレビューとは無関係に`vivliostyle.config.js`の内容にもとづき処理されます。このため、もし`vivliostyle.config.js`がなければPDFは出力されません。初めてPDFを出力する際は、まず以下を参考に`vivliostyle.config.js`をルートに作成し、その中で出力するファイル名を指定してください。

- [文書のカスタマイズ](/ja/create-and-save-documents/document-customization.md)

関連情報として、下記もご参照ください。

- [フォントの指定方法 > フォントを利用するしくみ](/ja/create-and-save-documents/how-to-specify-fonts.md#フォントを利用するしくみ)
- [ Theme（スタイル情報の選択）> Custom theme](/ja/functions-of-the-actions-menu/theme.md#custom-theme)）

複数あるMarkdownファイルのうち、特定のものだけをPDF出力したい場合は、vivliostyle.config.jsで出力したいファイルだけを指定するか、出力しないファイルをコメントアウトしてください。詳細は下記をご参照ください。

- [文書のカスタマイズ > 対象となる文書の指定](/ja/create-and-save-documents/document-customization.md#対象となる文書の指定)


1. 「Actionメニュー > PDF」を選択します

![](images/functions-of-the-actions-menu/export/fig-1.png)

2. すると、画面下端に「ビルドを開始しました」とメッセージが表示されます

![](images/functions-of-the-actions-menu/export/fig-2.png)

3. しばらく待つと、「以下のリンクをクリックして表示してください View  PDF」と表示されるので、「View  PDF」の部分をクリックしてください

![](images/functions-of-the-actions-menu/export/fig-3.png)

この表示は一定時間が経過すると消えます。再度確認したい場合は、ログ表示から「View  PDF」のリンクを確認できます

- [クイックスタートガイド >  ログの表示](/ja/readme-first/quick-start-guide-and-required-environment.md#ログの表示)


4. ブラウザのPDF閲覧画面に遷移します。ウィンドウ左上の下向き矢印「↓」（赤丸）をクリックするとファイルダイアログが開き、PDFがダウンロードできます

![](images/functions-of-the-actions-menu/export/fig-4.png)

## トンボをつける方法

トンボ付きのPDFファイルを作成するには、カスタムスタイルシートに以下のような記述を追加してください。

```css
@page {
  marks: crop cross;
  bleed: 3mm;
}
```

ただし、上記を追加すると、出力だけでなくプレビューにもトンボがつきますのでご注意ください（時期未定ながら、Actionメニューからトンボ付きPDFを出力できるよう改修する予定です）。


## 印刷会社への入稿

Vivliostyle Pubで出力したPDFファイルを、実際に印刷・製本できるサービスがあります。

- [mybooksPOD](https://pod.mybooks.jp/)

上記は[欧文印刷株式会社](https://obun.jp/)によるサービスで、ユーザーが作成したPDFファイルを、1部から印刷・製本できます。利用を希望するユーザーは上記ページにあるフォームに記入して、印刷したいPDFファイルをアップロードしてください。折り返しメールで見積額が送られてくるので、OKなら正式に発注してください。利用に当たっては、下記の点にご注意ください。

- PDFファイルにトンボがない場合は、印刷会社が付与します
- 現在のVivliostyle Pubは表紙の作成機能がないため、別途ユーザーが用意するか、印刷会社に制作依頼することになります
- 具体的な利用の流れはこちらを参考にしてください→[Vivliostyle Pubで作成したPDFファイルを印刷するサービスが開始](https://vivliostyle.org/ja/blog/2022/09/07/service-to-print-pdfs/)
- このサービスの詳細は欧文印刷株式会社にお問い合わせください。

## 補足情報

- VivliostyleによるPDF出力には、以下の2つの問題が指摘されています
    - [Vivliostyle CLI: 出力したPDFの文字がK100にならないケースがある #276 ](https://github.com/vivliostyle/vivliostyle-cli/issues/276)
    - Vivliostyle.js: PDFを出力するとフォントがType 3フォントに変換されて埋め込まれる
        - [please use CID instead of Type3 #437](https://github.com/vivliostyle/vivliostyle.js/issues/437)
        - [the reversed string is returned on Preview.app when selecting PDF contents which uses Type3 #439](https://github.com/vivliostyle/vivliostyle.js/issues/439)
- このうちK100にならない問題は、大部数を均一な品質で印刷することを求められる商業印刷（オフセット印刷）で版ずれやブロッキングなど印刷トラブルになる可能性があり、解決策を検討中です
- ただし、少部数の同人誌印刷（トナー印刷）では商業印刷ほどの品質を求めるケースは少なく、あまり問題にはならないと考えています。たとえば、出力したPDFを以下のような外部サイトでグレイスケールに変換することで解決できる可能性が高いでしょう
    - [DeftPDF（Sictec Infotech, Inc.）](https://deftpdf.com/ja/grayscale-pdf)  
- つぎにType 3フォントに変換される問題ですが、一般に商業印刷ではType 3フォントは不適とされており、この問題も早い解決が望まれます
- とはいえ、原因はVivliostyle.jsではなく外部のライブラリ（Chromium）にあるので、解決は当該ライブラリのアップデートを待つしかありません
- それでも、以下のような回避方法はあります
    - アドビの有償ソフト[Adobe Acrobat Pro DC](https://www.adobe.com/jp/products/acrobat-pro-cc.html)を使ってPDF/x規格に変換する
        -  [PDF から PDF/X、PDF/A または PDF/E への変換（アドビ）](https://helpx.adobe.com/jp/acrobat/using/pdf-x-pdf-a-pdf.html)
    - Type 3フォントに変換されないようTrueTypeフォントを指定する。たとえば下記リストを参照して無償のWebフォントサービス、Googleフォントを利用するのも一案
        - [GoogleフォントのうちVivliostyleのPDF出力で “Type 3” にならない日本語フォント一覧](/ja/create-and-save-documents/additional-information-on-fonts.md#googleフォントのうちvivliostyleのpdf出力で-type-3-にならない日本語フォント一覧)
    - Vivliostyle Pubは使わず、[Create Book](https://github.com/vivliostyle/create-book)で [Vivliostyle CLI](https://github.com/vivliostyle/vivliostyle-cli)の`--press-ready`オプションを使ってPDF/x-1a準拠のPDFをビルドする
        - なお、上記オプションによりPDF/x-1aを作成した場合、フォントがアウトライン化されてテキスト属性を失い、検索などができなくなることがあります。このオプションは印刷データ作成用で、PDFを頒布する用途には向かないことにご注意ください。詳細は下記を参照してください。
            - [Create Book > 4色印刷用PDFファイル の生成](https://docs.vivliostyle.org/#/ja/create-book#4%E8%89%B2%E5%8D%B0%E5%88%B7%E7%94%A8pdf%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB-%E3%81%AE%E7%94%9F%E6%88%90)
- もっとも、この問題も商業印刷では問題になっても、少部数の同人誌印刷ではあまり問題にはならない可能性があります
    - 私たちのテストではVivliostyle CLIから`build`コマンド、つまりVivliostyle PubでのPDF出力と同じ環境で出力したPDF（A5判、281ページ、1.01GB）が、オンデマンド印刷機[bizhub PRESS 1085（コニカミノルタ）](https://www.konicaminolta.jp/business/products/graphic/ondemand_print/color/bizhub_press_c1100_c1085/index.html)で印刷できました
        - このPDFはType 3フォントが埋め込まれており、通常のオフセット印刷では不適とされる可能性が高いデータです
    - 他にも同じPDFを使って、RIPワークフロー[EQUIOS（SCREENグラフィックソリューションズ）](https://www.screen.co.jp/ga/product/category/workflow)から中間データへの変換に成功しています
    - いずれにしても、どんな場合でも見た目通り印刷できる保証はないのが正直なところです。印刷会社とよくコミュニケーションをとった上で入稿されることをお勧めします
