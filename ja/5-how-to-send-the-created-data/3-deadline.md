# 作業の手順（後半）

## コミッターがGitHubでプルリクエストを作成

1. GitHubリポジトリのトップページに移動し、ブランチ名を確認してから “Contribute”（赤丸／貢献する）をクリック

![](images/multi-user-collaborative-editing/working-procedure-latter-part/fig-1.png)

2. “Open pull request”（赤丸／プルリクエストを開く）をクリック

![](images/multi-user-collaborative-editing/working-procedure-latter-part/fig-2.png)

3. タイトルとコメントを記入して “Create pull request”（赤丸／プルリクエストの作成）をクリック

![](images/multi-user-collaborative-editing/working-procedure-latter-part/fig-3.png)

4. プルリクエストが作成されます。この画面で左上 “Reviewer” のギアマーク（赤丸）をクリックすると、管理者やメンバーにレビュー依頼ができます


- **参考：**[Pull Request レビューをリクエストする](https://docs.github.com/ja/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/requesting-a-pull-request-review)

![](images/multi-user-collaborative-editing/working-procedure-latter-part/fig-4.png)

## 管理者がGitHubでプルリクエストをレビュー、承認、マージ

ここからは、レビューを依頼された管理者の操作です。

1. メールでコミッターからのレビュー依頼を受信したら、プルリクエストの番号をクリック

2. プルリクエストの画面が開きます。自分の名前が “Reviewer”（赤丸）にあることを確認したら、“Files changed”（赤四角／ファイルの変更）をクリック

![](images/multi-user-collaborative-editing/working-procedure-latter-part/fig-6.png)

3. レビュー対象となる変更箇所の一覧画面に遷移するのでレビューを開始しましょう。レビューの方法などは下記を参照してください


- **参考：**[プルリクエストのレビューについて](https://docs.github.com/ja/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/about-pull-request-reviews)
- **参考：**[プルリクエストへコメントする](https://docs.github.com/ja/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/commenting-on-a-pull-request)


![](images/multi-user-collaborative-editing/working-procedure-latter-part/fig-7.png)

4. “Review changes”（赤丸）をクリックすると、コメントの記入、そして ①Comment（コメント）、②Approve（承認）、③Request changes（変更の要請）のどれかがが選択できます。ここでは “Approve” を選びました。“Submit review”（赤丸／レビューを送る）を押すと、コミッターにレビューが届きます

![](images/multi-user-collaborative-editing/working-procedure-latter-part/fig-8.png)


- **参考：**[必須レビューでのプルリクエストの承認](https://docs.github.com/ja/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/approving-a-pull-request-with-required-reviews)


5. Approve（承認）を押したので、さきほどのプルリクエストの画面に戻りました。 “Reviewer” のカラムにある自分の名前の横に「✓」（赤丸）が入って、変更を承認したことが示されています。

![](images/multi-user-collaborative-editing/working-procedure-latter-part/fig-9.png)

6. 問題がないことが確認できたので、デフォルトブランチにマージしましょう。“Conform merge”（赤丸／統合）をクリック

![](images/multi-user-collaborative-editing/working-procedure-latter-part/fig-10.png)

7. ごくろうさまでした。デフォルトブランチへのマージが成功しました。“Pull request successfully merged and closed”（プルリクエストは正常にマージされ、クローズされました）。ついでに “Delete branch”（赤丸）を押して、不要になったブランチを削除しておきましょう

![](images/multi-user-collaborative-editing/working-procedure-latter-part/fig-11.png)
