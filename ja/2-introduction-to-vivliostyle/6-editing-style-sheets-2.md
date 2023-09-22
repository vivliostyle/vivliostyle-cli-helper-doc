# 文書作成の記法

Vivliostyle　Pubの文書はMarkdownという記法で作成します。ここでは主な記法だけ紹介します。詳細は下記を参照してください。

- [特集企画：Create Book で同人誌を作ろう！](https://vivliostyle.org/ja/make-books-with-create-book/#vfm-%E3%81%A7%E5%8E%9F%E7%A8%BF%E3%82%92%E6%9B%B8%E3%81%84%E3%81%A6%E3%81%BF%E3%82%88%E3%81%86)
- [VFM 入門 2021 夏](https://vivliostyle.github.io/vivliostyle_doc/ja/vivliostyle-user-group-vol5/content/akabeko/index.html)
- [Vivliostyle Flavored Markdown](https://vivliostyle.github.io/vfm/#/vfm)

## 見出し

見出しは全部で6段階が用意されています。大見出しの`#`から、一番小さな`######`まで、シャープが増えるほど下位の見出しになります。いずれも半角スペースを空けて見出し文字列を書いてください。

### 記法

```md
# 見出し1 Heading 1

## 見出し2 Heading 2

### 見出し3 Heading 3

#### 見出し4 Heading 4

##### 見出し5 Heading 5

###### 見出し6 Heading 6
```
### Vivliostyle Pub エディタ

![ ](images/create-and-save-documents/notation-for-document-creation/fig-1.png)

### Vivliostyle Pub プレビュー

![ ](images/create-and-save-documents/notation-for-document-creation/fig-2.png)

## リスト

リストの種類は3種類。`*`、`-`、`+`を先頭に書く点（disc）のリスト、数字+ピリオドの数字（decimal）のリスト、そしてチェックボックスです。数字のリストでは、必ずしも順番通りに数字を書く必要はないことにご注意ください。先頭の数字から降順で描画されます。

### 記法

```md
## disc型のリスト

* 打ち揚ぐるボールは高く雲に入りて　又落ち来る人の手の中に（正岡子規）
- 打ち揚ぐるボールは高く雲に入りて　又落ち来る人の手の中に（正岡子規）
+ 打ち揚ぐるボールは高く雲に入りて　又落ち来る人の手の中に（正岡子規）

## decimal型のリスト

1. 打ち揚ぐるボールは高く雲に入りて　又落ち来る人の手の中に（正岡子規）
1. 打ち揚ぐるボールは高く雲に入りて　又落ち来る人の手の中に（正岡子規）
2. 打ち揚ぐるボールは高く雲に入りて　又落ち来る人の手の中に（正岡子規）

checkbox型のリスト

- [ ] 打ち揚ぐるボールは高く雲に入りて　又落ち来る人の手の中に（正岡子規）
- [x] 打ち揚ぐるボールは高く雲に入りて　又落ち来る人の手の中に（正岡子規）
```

### Vivliostyle Pub エディタ

![ ](images/create-and-save-documents/notation-for-document-creation/fig-3.png)

### Vivliostyle Pub プレビュー

![ ](images/create-and-save-documents/notation-for-document-creation/fig-4.png)

## 強調

強調は2種類。`*`で囲むとイタリック体、`**`で囲むと太字になります。HTML記法では前者はem要素、後者はstorong要素と同じです。

### 記法

```md
## 強調

### em要素

「こら、罪人ども。 *この蜘蛛の糸は己のものだぞ。お前たちは一体誰に尋いて、のぼって来た*。
下りろ。下りろ。」と喚きました。その途端でございます。今まで何ともなかった蜘蛛の糸が、
急に犍陀多のぶら下っている所から、ぷつりと音を立てて断れました。

### strong要素

「こら、罪人ども。 **この蜘蛛の糸は己のものだぞ。お前たちは一体誰に尋いて、のぼって来た**。
下りろ。下りろ。」と喚きました。その途端でございます。今まで何ともなかった蜘蛛の糸が、
急に犍陀多のぶら下っている所から、ぷつりと音を立てて断れました。
```

### Vivliostyle Pub エディタ

![ ](images/create-and-save-documents/notation-for-document-creation/fig-5.png)

### Vivliostyle Pub プレビュー


![ ](images/create-and-save-documents/notation-for-document-creation/fig-6.png)

## 取り消し線

`~~`で文字列を囲むと取り消し線（中線）になります。

### 記法

```md
## 取り消し線

「こら、罪人ども。 ~~この蜘蛛の糸は己のものだぞ。お前たちは一体誰に尋いて、のぼって来た。
~~下りろ。下りろ。」と喚きました。その途端でございます。今まで何ともなかった蜘蛛の糸が、
急に犍陀多のぶら下っている所から、ぷつりと音を立てて断れました。
```


### Vivliostyle Pub エディタ

![ ](images/create-and-save-documents/notation-for-document-creation/fig-7.png)

### Vivliostyle Pub プレビュー

![ ](images/create-and-save-documents/notation-for-document-creation/fig-8.png)


## リンク

`[string](URL)`の形式で、「string」の部分をクリッカブルにできます。URLをそのまま書いてもクリッカブルになります。また、TwitterやYouTube等の埋め込み要素も書くことができます。

### 記法

```html
## リンク

[Vivliostyle](https://vivliostyle.org/ja/)は最新 Web 標準技術により、
電子出版や Web 出版のための新しい組版システムを作るオープンソース・プロジェクトです。

https://vivliostyle.org/ja/

<blockquote class="twitter-tweet" data-partner="tweetdeck"><p lang="en" dir="ltr">
We released Vivliostyle CLI v4.1.0 with Vivliostyle.js v2.9.1.<br>✅Support the @ supports CSS at-rule (feature queries)<br>
✅MathJax Content MathML extension is enabled<a href="https://t.co/Me1coX2Hlp">https://t.co/Me1coX2Hlp
</a></p>&mdash; Vivliostyle (@Vivliostyle) <a href="https://twitter.com/Vivliostyle/status/1436735010921332736?ref_src=twsrc%5Etfw">
September 11, 2021</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

```

### Vivliostyle Pub エディタ

![ ](images/create-and-save-documents/notation-for-document-creation/fig-9.png)

### Vivliostyle Pub プレビュー

![ ](images/create-and-save-documents/notation-for-document-creation/fig-10.png)

## ルビ

`{親文字|ルビ}`の形式でルビを書くことができます。いずれも全角記号ではなく半角を使うことにご注意ください。

### 記法


```md
## ルビ

- {打|う}ち{揚|あ}ぐる　ボールは{高|たか}く{雲|くも}に{入|い}りて　{又|また}{落|お}ち{来|きた}る{人|ひと}の{手|て}の{中|なか}に（正岡子規）
- マッチ{擦|す}る　つかのま{海|うみ}に{霧|きり}ふかし　{身捨|みす}つるほどの{祖国|そこく}はありや（寺山修司）
- {友|とも}がみな　われよりえらく{見|み}ゆる{日|ひ}よ　{花|はな}を{買|か}ひ{来|き}て{妻|つま}としたしむ（石川啄木）
- ああ{皐月|さつき}　{仏蘭西|ふらんす}の{野|の}は{火|ひ}の{色|いろ}す　{君|きみ}も{雛罌粟|こくりこ}われも{雛罌粟|こくりこ}（与謝野晶子）
```

### Vivliostyle Pub エディタ

![ ](images/create-and-save-documents/notation-for-document-creation/fig-11.png)

### Vivliostyle Pub プレビュー

![ ](images/create-and-save-documents/notation-for-document-creation/fig-12.png)


## 表組

セルになる文字列を`|`で囲むことにより表組を作成できます。2行目にセル文字列を`|-----|`にした行をはさむことで、1行目をヘッダにすることができます。

### 記法

```md
## 表組

| ヘッダ1 　| ヘッダ2　　　| ヘッダ3 |
| ------　| -------| -----　 |
| コラム1  | コラム2  | コラム3 |
| コラム4  | コラム5  | コラム6 |
```


### Vivliostyle Pub エディタ

![ ](images/create-and-save-documents/notation-for-document-creation/fig-13.png)

### Vivliostyle Pub プレビュー

![ ](images/create-and-save-documents/notation-for-document-creation/fig-14.png)


## 縦中横

残念ながら今はまだ縦中横をMarkdownで表現できません。HTMLのspan要素とtcy属性`<span class="tcy">`と閉じタグ`</span>`で数字を囲みます。

### 記法

```html
## 縦中横

合併で誕生した葉山村ですが、その<span class="tcy">36</span>年後の大正<span class="tcy">14</span>
（<span class="tcy">1</span><span class="tcy">9</span><span class="tcy">2</span><span class="tcy">5
</span>）年<span class="tcy">1</span>月<span class="tcy">1</span>日に「葉山町」になった際も、合併をする
ことはありませんでした。葉山町の範囲は<span class="tcy">3</span><span class="tcy">2</span><span class="tcy">0</span>
年前の葉山村のままであり、同時にそれは江戸期の<span class="tcy">6</span>ヵ村の範囲とも一致しているという、
おそらく日本でも希少な例に属するわけです。
```

### Vivliostyle Pub エディタ

![ ](images/create-and-save-documents/notation-for-document-creation/fig-15.png)

### Vivliostyle Pub プレビュー

![ ](images/create-and-save-documents/notation-for-document-creation/fig-16.png)

## 画像のキャプションとサイズ指定

### 記法

```md
## 画像のキャプションとサイズ指定

![千代ヶ崎砲台跡の塁道から南上空を仰ぎ見る](IMG_5694-2.jpeg){width=100%}
```

### Vivliostyle Pub エディタ

![ ](images/create-and-save-documents/notation-for-document-creation/fig-17.png)

### Vivliostyle Pub プレビュー

![ ](images/create-and-save-documents/notation-for-document-creation/fig-18.png)
