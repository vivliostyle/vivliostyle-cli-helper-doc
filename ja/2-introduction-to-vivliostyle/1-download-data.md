# フォントに関する補足情報

## クラウドにインストールされているフォント一覧

PDF出力で使われるクラウドのフォントは、なるべく多くの環境との互換性を確保する目的で、下記のフォントセットをインストールしています。

1. [Noto fonts](https://fonts.google.com/noto)
2. [Microsoft TrueType core fonts](https://packages.ubuntu.com/focal/ttf-mscorefonts-installer)

1は1,000以上の言語と150以上の文字体系に対応し、複数のウェイトと幅、そしてゴシック、明朝、等幅といったスタイルをもつ巨大なフォントファミリーです。2はマイクロソフトによるWeb用の標準フォントのパックです。

このほか、Linuxシステム上での標準的なフォントとして次のものがインストールされています。

- [liberation-fonts](https://packages.ubuntu.com/focal/fonts-liberation)
- [Thai Loma font](https://packages.ubuntu.com/focal/fonts-tlwg-loma-otf)
- [Ubuntu font](https://design.ubuntu.com/font/)
- [urw-base35-fonts](https://github.com/ArtifexSoftware/urw-base35-fonts)

個々の`font-family`名は下記の通りです。これらをCustom theme（スタイル情報）の中で指定することにより、出力するPDFに埋め込むことができます（→[Custom theme／プレビューとPDF出力とでフォントを一致させる](/ja/create-and-save-documents/how-to-specify-fonts.md#custom-theme／プレビューとpdf出力とでフォントを一致させる)）

- `Andale Mono`
- `Arial`
- `Arial Black`
- `C059`
- `Comic Sans MS`
- `Courier New`
- `D050000L`
- `Georgia`
- `Impact`
- `Liberation Mono`
- `Liberation Sans`
- `Liberation Sans Narrow`
- `Liberation Serif`
- `Loma`
- `Nimbus Mono PS`
- `Nimbus Roman`
- `Nimbus Sans`
- `Nimbus Sans Narrow`
- `Noto Color Emoji`
- `Noto Kufi Arabic`
- `Noto Mono`
- `Noto Music`
- `Noto Naskh Arabic`
- `Noto Naskh Arabic UI`
- `Noto Nastaliq Urdu`
- `Noto Sans`
- `Noto Sans Adlam`
- `Noto Sans Adlam Unjoined`
- `Noto Sans Anatolian Hieroglyphs`, `Noto Sans AnatoHiero`
- `Noto Sans Arabic`
- `Noto Sans Arabic UI`
- `Noto Sans Armenian`
- `Noto Sans Avestan`
- `Noto Sans Bamum`
- `Noto Sans Bassa Vah`
- `Noto Sans Batak`
- `Noto Sans Bengali`
- `Noto Sans Bengali UI`
- `Noto Sans Bhaiksuki`
- `Noto Sans Brahmi`
- `Noto Sans Buginese`
- `Noto Sans Buhid`
- `Noto Sans CJK HK`
- `Noto Sans CJK JP`
- `Noto Sans CJK KR`
- `Noto Sans CJK SC`
- `Noto Sans CJK TC`
- `Noto Sans Canadian Aboriginal`, `Noto Sans CanAborig`
- `Noto Sans Carian`
- `Noto Sans Caucasian Albanian`, `Noto Sans CaucAlban`
- `Noto Sans Chakma`
- `Noto Sans Cham`
- `Noto Sans Cherokee`
- `Noto Sans Coptic`
- `Noto Sans Cuneiform`
- `Noto Sans Cypriot`
- `Noto Sans Deseret`
- `Noto Sans Devanagari`
- `Noto Sans Devanagari UI`
- `Noto Sans Display`
- `Noto Sans Duployan`
- `Noto Sans Egyptian Hieroglyphs`, `Noto Sans EgyptHiero`
- `Noto Sans Elbasan`
- `Noto Sans Ethiopic`
- `Noto Sans Georgian`
- `Noto Sans Glagolitic`
- `Noto Sans Gothic`
- `Noto Sans Grantha`
- `Noto Sans Gujarati`
- `Noto Sans Gujarati UI`
- `Noto Sans Gunjala Gondi`
- `Noto Sans Gurmukhi`
- `Noto Sans Gurmukhi UI`
- `Noto Sans Hanifi Rohingya`, `Noto Sans HanifiRohg`
- `Noto Sans Hanunoo`
- `Noto Sans Hatran`
- `Noto Sans Hebrew`
- `Noto Sans Imperial Aramaic`, `Noto Sans ImpAramaic`
- `Noto Sans Indic Siyaq Numbers`
- `Noto Sans Inscriptional Pahlavi`, `Noto Sans InsPahlavi`
- `Noto Sans Inscriptional Parthian`, `Noto Sans InsParthi`
- `Noto Sans Javanese`
- `Noto Sans Kaithi`
- `Noto Sans Kannada`
- `Noto Sans Kannada UI`
- `Noto Sans Kayah Li`
- `Noto Sans Kharoshthi`
- `Noto Sans Khmer`
- `Noto Sans Khmer UI`
- `Noto Sans Khojki`
- `Noto Sans Khudawadi`
- `Noto Sans Lao`
- `Noto Sans Lao UI`
- `Noto Sans Lepcha`
- `Noto Sans Limbu`
- `Noto Sans Linear A`
- `Noto Sans Linear B`
- `Noto Sans Lisu`
- `Noto Sans Lycian`
- `Noto Sans Lydian`
- `Noto Sans Mahajani`
- `Noto Sans Malayalam`
- `Noto Sans Malayalam UI`
- `Noto Sans Mandaic`
- `Noto Sans Manichaean`
- `Noto Sans Marchen`
- `Noto Sans Masaram Gondi`
- `Noto Sans Math`
- `Noto Sans Mayan Numerals`
- `Noto Sans Meetei Mayek`
- `Noto Sans Mende Kikakui`
- `Noto Sans Meroitic`
- `Noto Sans Miao`
- `Noto Sans Modi`
- `Noto Sans Mongolian`
- `Noto Sans Mono`
- `Noto Sans Mono CJK HK`
- `Noto Sans Mono CJK JP`
- `Noto Sans Mono CJK KR`
- `Noto Sans Mono CJK SC`
- `Noto Sans Mono CJK TC`
- `Noto Sans Mro`
- `Noto Sans Multani`
- `Noto Sans Myanmar`
- `Noto Sans Myanmar UI`
- `Noto Sans NKo`, `Noto Sans N'Ko`
- `Noto Sans Nabataean`
- `Noto Sans New Tai Lue`
- `Noto Sans Newa`
- `Noto Sans Ogham`
- `Noto Sans Ol Chiki`
- `Noto Sans Old Hungarian`, `Noto Sans OldHung`
- `Noto Sans Old Italic`
- `Noto Sans Old North Arabian`, `Noto Sans OldNorArab`
- `Noto Sans Old Permic`
- `Noto Sans Old Persian`
- `Noto Sans Old Sogdian`
- `Noto Sans Old South Arabian`, `Noto Sans OldSouArab`
- `Noto Sans Old Turkic`
- `Noto Sans Oriya`
- `Noto Sans Oriya UI`
- `Noto Sans Osage`
- `Noto Sans Osmanya`
- `Noto Sans Pahawh Hmong`
- `Noto Sans Palmyrene`
- `Noto Sans Pau Cin Hau`
- `Noto Sans PhagsPa`
- `Noto Sans Phoenician`
- `Noto Sans Psalter Pahlavi`, `Noto Sans PsaPahlavi`
- `Noto Sans Rejang`
- `Noto Sans Runic`
- `Noto Sans Samaritan`
- `Noto Sans Saurashtra`
- `Noto Sans Sharada`
- `Noto Sans Shavian`
- `Noto Sans Siddham`
- `Noto Sans Sinhala`
- `Noto Sans Sinhala UI`
- `Noto Sans Sogdian`
- `Noto Sans Sora Sompeng`, `Noto Sans SoraSomp`
- `Noto Sans Soyombo`
- `Noto Sans Sundanese`
- `Noto Sans Syloti Nagri`
- `Noto Sans Symbols`
- `Noto Sans Symbols2`
- `Noto Sans Syriac`
- `Noto Sans Tagalog`
- `Noto Sans Tagbanwa`
- `Noto Sans Tai Le`
- `Noto Sans Tai Tham`
- `Noto Sans Tai Viet`
- `Noto Sans Takri`
- `Noto Sans Tamil`
- `Noto Sans Tamil Supplement`
- `Noto Sans Tamil UI`
- `Noto Sans Telugu`
- `Noto Sans Telugu UI`
- `Noto Sans Thaana`
- `Noto Sans Thai`
- `Noto Sans Thai UI`
- `Noto Sans Tibetan`
- `Noto Sans Tifinagh`
- `Noto Sans Tirhuta`
- `Noto Sans Ugaritic`
- `Noto Sans Vai`
- `Noto Sans Wancho`
- `Noto Sans Warang Citi`
- `Noto Sans Yi`
- `Noto Sans Zanabazar Square`, `Noto Sans Zanabazar`
- `Noto Serif`
- `Noto Serif Ahom`
- `Noto Serif Armenian`
- `Noto Serif Balinese`
- `Noto Serif Bengali`
- `Noto Serif CJK JP`
- `Noto Serif CJK KR`
- `Noto Serif CJK SC`
- `Noto Serif CJK TC`
- `Noto Serif Devanagari`
- `Noto Serif Display`
- `Noto Serif Dogra`
- `Noto Serif Ethiopic`
- `Noto Serif Georgian`
- `Noto Serif Gujarati`
- `Noto Serif Gurmukhi`
- `Noto Serif Hebrew`
- `Noto Serif Kannada`
- `Noto Serif Khmer`
- `Noto Serif Lao`
- `Noto Serif Malayalam`
- `Noto Serif Myanmar`
- `Noto Serif Sinhala`
- `Noto Serif Tamil`
- `Noto Serif Tamil Slanted`
- `Noto Serif Tangut`
- `Noto Serif Telugu`
- `Noto Serif Thai`
- `Noto Serif Tibetan`
- `P052`
- `Standard Symbols PS`
- `Times New Roman`
- `Trebuchet MS`
- `URW Bookman`
- `URW Gothic`
- `Ubuntu`
- `Ubuntu Condensed`
- `Ubuntu Mono`
- `Verdana`
- `Webdings`
- `Z003`

なお、 各フォントがサポートするウェイトを含む詳細なリストは、こちらをご参照ください（→[fc-list.sorted](/ja/create-and-save-documents/fc-list.sorted.md)）

## クラウド上のVivliostyle CLIにおける代替フォントルール

PDF出力に際して、前項のリストにないフォントが指定された場合、以下のように代替されます。

| 指定されたフォント                                                                                                                                            | 代替されるフォント      |     | 
| ------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | --- | 
|  Times  |  Times New Roman  |
|  Helvetica  |  Arial  |
|  Courier  | Courier New   |
|  `font-family: fantasy;`  |  Impact  |
|  `font-family: cursive`  |  Comic Sans MS  |
|  `font-family: monospace;`  |  Andale Mono  |
| Source Han Serif<br>Hiragino Mincho ProN<br>Hiragino Mincho Pro<br>YuMincho<br>Yu Mincho<br>MS Mincho<br>MS PMincho                                     | Noto Serif CJK JP |     | 
| Source Han Sans<br>Hiragino Sans<br>Hiragino Kaku Gothic ProN<br>Hiragino Kaku Gothic Pro<br>YuGothic<br>Yu Gothic<br>Meiryo<br>MS Gothic<br>MS PGothic | Noto Sans CJK JP  | 
|  上記以外の欧文フォント  |  Times New Roman  |
|  上記以外の日本語フォント  |  Noto Sans CJK JP  |

- **ご注意**
    - たとえばtheme（スタイルシート）で`font-family: "IPA明朝", serif;`と指定されていた場合、IPA明朝は前項のリストにも上の表にもありませんから、PDF出力ではブラウザ設定「Serif」のフォント（日本語環境では明朝体）が使用されるはずです。しかし、実際にはNoto Sans CJK JPが使用されてしまいます。
    - 上の表で`Noto Serif CJK JP`に代替されるフォント以外の明朝体フォント全てにこの問題が発生します（逆の言い方をすれば、上の表で`Noto Serif CJK JP`に代替されるフォントはこの問題は発生しません）。私たちはこの問題の解決に努めています。詳細は下記をご参照ください。
        - [font-family: serif を指定しても明朝体にならない問題と対策](https://github.com/vivliostyle/vivliostyle-cli/issues/303#issuecomment-1169786479)

## 推奨する有償Webフォントサービスの用途

有償Webフォントサービスは利用規約によって用途を制限しており、Vivliostyle Pubで無条件にこれらのサービスを利用できるわけではありません。

本来、利用規約の解釈は契約者間で解決すべきであり、第三者である私たちが判断できるものではありません。とはいえ、このままではユーザーが安心してVivliostyle PubでWebフォントを使うことはできないでしょう。そこで、各社とコミュニケーションをとりながら、以下の用途を利用規約が許容しているか調査しました。

- Webフォントを使ってプレビューができる
- Webフォントを使ってPDF出力、及びオフセット／オンデマンド印刷ができる
- Webフォントを使って成果物の有償販売ができる

その結果を踏まえ、Webフォントサービスごとに推奨できる用途を選定したのが下記のものです。

|              | [DynaSmart V](https://www.dynacw.co.jp/product/product_dynasmart_detail.aspx?sid=25)           | [DynaSmart T](https://www.dynacw.co.jp/product/product_dynasmart_detail.aspx?sid=43)  | [TypeSquare](https://typesquare.com/ja/)    |[fonts.com](https://www.fonts.com/ja)  | [FONTPLUS](https://fontplus.jp/)※  | [Adobe Fonts](https://fonts.adobe.com/)     |
| ------------ | -------------- | ---------------- | --------------- |  -------------- | ---------------- | --------------- |
| プレビュー | ○                    | ×                      | ×                     | ×                      | ○                   |    ×                 | 
| PDF出力／印刷 |  ○             | ×                      | ×                    | ×                      | ×                   |    ×               | 
| 有償販売     |  ○                    | ×                      | ×                    | ×                      | ×                   |    ×               | 

※……FONTPLUSはプレビューのみ○（ブログでの使用と同じと解釈）。ただし、PDF出力等については個別判断になるので要問い合わせ

より詳細については、以下をご参照ください。

- [VivliostyleでWebフォントを使う 調査編：小形克宏（YouTube）](https://www.youtube.com/watch?v=czVRSsekLjc)
- [VivliostyleでWebフォントを使う：調査編（スライド）](https://vivliostyle.org/viewer/#src=https://github.com/ogwata/slide-20220423-2/blob/main/myslide.html&bookMode=true&spread=false)

## GoogleフォントのうちVivliostyleのPDF出力で “Type 3” にならない日本語フォント一覧

以下は、[Googleフォント](https://fonts.google.com/?subset=japanese)に収録されている日本語フォント50書体のうち、私たちのテストの結果、VivliostyleによるPDF出力で “Type 3” ではなく “TrueType (CID)” として埋め込まれたフォントです。結果として、Noto Sans JapaneseとNoto Serif Japanese を除くすべての日本語フォントでもあります。

一般に “Type 3” としてフォントが埋め込まれたPDFファイルは印刷に不適とされています。一方で “TrueType (CID)” として埋め込まれていれば問題はないとされています。詳細は下記をご参照ください。

- [Actionメニューの機能 > Export（出力）> 補足情報](/ja/functions-of-the-actions-menu/export.md#補足情報)

----------------------------

BIZ UDGothic<br>
BIZ UDMincho<br>
BIZ UDPGothic<br>
BIZ UDPMincho<br>
Dela Gothic One<br>
DotGothic16<br>
Hachi Maru Pop<br>
Hina Mincho<br>
Kaisei Decol<br>
Kaisei HarunoUmi<br>
Kaisei Opti<br>
Kaisei Tokumin<br>
Kiwi Maru<br>
Klee One<br>
Kosugi<br>
Kosugi Maru<br>
M PLUS 1<br>
M PLUS 1 Code<br>
M PLUS 1p<br>
M PLUS 2<br>
M PLUS Rounded 1c<br>
Mochiy Pop One<br>
Mochiy Pop P One<br>
Murecho<br>
New Tegomin<br>
Potta One<br>
Rampart One<br>
Reggae One<br>
RocknRoll One<br>
Sawarabi Gothic<br>
Shippori Antique<br>
Shippori Antique B1<br>
Shippori Mincho<br>
Shippori Mincho B1<br>
Stick<br>
Train One<br>
Yomogi<br>
Yuji Boku<br>
Yuji Mai<br>
Yuji Syuku<br>
Yusei Magic<br>
Zen Antique<br>
Zen Antique Soft<br>
Zen Kaku Gothic Antique<br>
Zen Kaku Gothic New<br>
Zen Kurenaido<br>
Zen Maru Gothic<br>
Zen Old Mincho<br>




