#  はじめに 

## このドキュメントの目的 

この文書は、2023年8月26日に開催された、第1回Vivliostyleハンズオンセミナー（協力：欧文印刷株式会社）[『講師に教わりながら、Vivliostyleで本を作る！』](https://vivliostyle.org/ja/hands-on/1/)のフォローアップ用教材として制作された。

おもにセミナー後の復習として活用してただくために制作したが、とくにオススメするのは以下のアーカイブ動画を視聴しながら読み進めることだ（リーダー罫の右側は対応する本ドキュメントの章）。

1. [講師に教わりながら、Vivliostyleで本を作る！第1部](https://youtu.be/NdwVgr83q7Y)……第1章
2. [講師に教わりながら、Vivliostyleで本を作る！ 第2部-1](https://youtu.be/SrlJI5rKTbo)……第2章
3. [講師に教わりながら、Vivliostyleで本を作る！ 第2部-2](https://youtu.be/VnwddnaSsik)……第3章

なお、他にも以下の2本の動画を公開しているが、これらはハンズオンではないので、この文書の対象から外している。

4. [MyBooksPOD のご紹介／印刷しやすい原稿の作成方法（松尾孝行：欧文印刷株式会社）](https://youtu.be/kIiUlq5JHvw)
5. [講師に教わりながら、Vivliostyleで本を作る！ 第2部-3](https://youtu.be/DStotKNSyfE)

この文書の目的はもう一つある。今までとかく導入のしにくさを指摘されてきたVivliostyle CLIだが、[vivliostyle-cli-helper](https://marketplace.visualstudio.com/items?itemName=Libroworks.vivliostyle-cli-helper)を使えば、驚くほど簡単に使い始められることを伝えたかった。この文書にざっと目を通すだけでも、vivliostyle-cli-helperを使うメリットが納得できるはずだ。

ただし、動画を一緒に見ればさらに理解が進むと言うだけで、動画は必須ではない。この文書だけでも十分にvivliostyle-cli-helperの操作を理解することができるだろう。

なお、vivliostyle-cli-helperは、セミナーで講師を務めた[大津雄一郎氏（リブロワークス）](https://libroworks.co.jp/?author=2)によるフリーウェアです。

## このドキュメントの読み方

H3見出しの横、カッコで括った数字は対応する動画の時間だ。これを目安にすれば、対応する動画部分を見ながら読み進められるだろう。

また、動画だけでなく、適宜該当する[『CSS組版 Vivliostyle入門』（リブロワークス、C&R研究所、2023年）](https://libroworks.co.jp/?p=6956)、のページ番号も掲載している。当日のセミナーでは時間の都合で書籍を作るためのすべての指定については説明しきれなかった。足りない部分は単行本で補っていただこうという意図もある。

本文書に掲載したスクリーンショットはMacで撮影したものだが、Windows、Linuxでも同様の画面になるはずだ。万が一相違している場合は、お手数だが以下までご一報いただければ幸いだ。他にも疑問、質問などを知らせてもらえると、一同大変喜びます。

- [Vivliostyle Slack (#q-and-a)](https://join.slack.com/t/vivliostyle/shared_invite/enQtNzc1NjE4ODk1ODI5LWQxZjM4YTZjMmQ0ZTUyNmUyOGZlMzIwZjQ5OWYwYjkyZDZmOTIwNGMwOWU5NDc0NjE5OTAyMmVhZTRhYTAyNWQ)
