#  はじめに 

## 必須環境

- このドキュメントで説明されている操作を再現するための前提条件を以下に示す。
    - 以下のソフトウェアがインストールされていること
        - [Node.js（v16以上）](https://nodejs.org/ja)
        - [VSCode（最新版）](https://azure.microsoft.com/ja-jp/products/visual-studio-code)
    - インターネットに接続していること

## このドキュメントの目的 

[一般社団法人ビブリオスタイル](https://vivliostyle.org/ja/)は、2023年8月26日に第1回Vivliostyleハンズオンセミナー（協力：欧文印刷株式会社）[『講師に教わりながら、Vivliostyleで本を作る！』](https://vivliostyle.org/ja/hands-on/1/)を開催した。そのアーカイブ動画はYouTubeで公開している。

1. [講師に教わりながら、Vivliostyleで本を作る！第1部](https://youtu.be/NdwVgr83q7Y)
2. [講師に教わりながら、Vivliostyleで本を作る！ 第2部-1](https://youtu.be/SrlJI5rKTbo)
3. [講師に教わりながら、Vivliostyleで本を作る！ 第2部-2](https://youtu.be/VnwddnaSsik)
4. [MyBooksPOD のご紹介／印刷しやすい原稿の作成方法（松尾孝行：欧文印刷株式会社）](https://youtu.be/kIiUlq5JHvw)
5. [講師に教わりながら、Vivliostyleで本を作る！ 第2部-3](https://youtu.be/DStotKNSyfE)

動画を見直して感じたことは、[vivliostyle-cli-helper](https://marketplace.visualstudio.com/items?itemName=Libroworks.vivliostyle-cli-helper)というVSCode機能拡張がとてもよく出来ていることだ。今まで玄人受けはしても、とかく導入しにくさを指摘されてきたVivliostyle CLIだが、これによってコマンドラインでタイプしなくとも使えるようになった。この点、セミナーで講師も務めてくださった作者の[大津雄一郎（リブロワークス）](https://libroworks.co.jp/?author=2)氏に、改めて感謝したい。

ただしその反面、セミナーではCSSやHTMLの基礎などは既に知っている前提で、細かな作業の説明がしばしば省略されている。もしやこの点が、初めて使うユーザを混乱させないだろうか。

そこで、上記動画に沿いつつ、セミナーでは省略された手順もしつこく再現した文書を制作し、これをフォローアップ用教材としてセミナー受講者に提供することにしたのがこのドキュメントである。

もちろん、対象はセミナー受講者に留まらない。Vivliostyle CLIを手軽に使い始めたいと考えた人なら誰でも、このドキュメントに目を通すことで（手元のPCで再現すればなおさら）vivliostyle-cli-helperの使い方とそのメリットが納得できるだろう。

## このドキュメントの読み方

このドキュメントの構成と動画の対応関係を以下に示す。なお、上記4と5の動画はハンズオンではないので、このドキュメントの対象から外している。

- 第2章……[講師に教わりながら、Vivliostyleで本を作る！第1部](https://youtu.be/NdwVgr83q7Y)
- 第3章……[講師に教わりながら、Vivliostyleで本を作る！ 第2部-1](https://youtu.be/SrlJI5rKTbo)
- 第4章、第5章……[講師に教わりながら、Vivliostyleで本を作る！ 第2部-2](https://youtu.be/VnwddnaSsik)

それぞれの文書中で、**カッコで括った太字の数字**は対応する動画の再生時間を示している。これを目安にすれば、動画を確認しながら読み進められるだろう。

また、動画だけでなく、セミナーの教科書となった[『CSS組版 Vivliostyle入門』（リブロワークス、C&R研究所、2023年）](https://libroworks.co.jp/?p=6956)の、**対応するページ番号**も掲載している。当日のセミナーでは時間の都合もあり、書籍を作るためのすべての指定については説明しきれなかった。足りない部分は単行本で補っていただこうという意図もある。

このドキュメントに掲載したスクリーンショットはMacで撮影したものだが、Windows、Linuxでも同様の画面になるはずだ。万が一相違している場合は、お手数だが以下までご一報いただければ幸いだ。他にも疑問、質問、感想などを知らせてもらえると、制作者一同、大変喜びます。

- [Vivliostyle Slack (#q-and-a)](https://join.slack.com/t/vivliostyle/shared_invite/enQtNzc1NjE4ODk1ODI5LWQxZjM4YTZjMmQ0ZTUyNmUyOGZlMzIwZjQ5OWYwYjkyZDZmOTIwNGMwOWU5NDc0NjE5OTAyMmVhZTRhYTAyNWQ)