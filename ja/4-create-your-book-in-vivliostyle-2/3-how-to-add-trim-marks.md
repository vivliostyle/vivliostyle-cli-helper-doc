# トンボの設定方法**（20:20）**

1. 51行目`/* bleed: 3mm; */`（赤矢印）にカーソルを置いた状態で、Macでは`command`+`/`、Windowsでは`ctrl`+`/`を入力します。
2. 続いて52行目`marks: crop cross;`（青矢印）にカーソルを置いた状態で、Macでは`command`+`/`、Windowsでは`ctrl`+`/`を入力します。

![](/images/4-create-your-book-in-vivliostyle-2/3-how-to-add-trim-marks/4-3-1.png)

3. コメントアウトが外れました。ファイルを保存して、プレビューを表示させてみましょう。

![](/images/4-create-your-book-in-vivliostyle-2/3-how-to-add-trim-marks/4-3-2.png)

4. ファイルを保存して、プレビューを表示させてみましょう。トンボが付きました。
  - bleedプロパティは裁ち落としのサイズを指定するプロパティです。ここでは3ミリに指定しています。**（pp.220-221）**
  - marksプロパティはトンボの種類を指定します。値`crop`はコーナートンボ、値`cross;`はセンタートンボを意味します。**（pp.220-221）**

![](/images/4-create-your-book-in-vivliostyle-2/3-how-to-add-trim-marks/4-3-3.png)


