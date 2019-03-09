# **ʕ◔ϖ◔ʔ (工事中)**

[View on GitHub](https://github.com/hugojapan/hugojapan.github.io) | [Main repo](https://github.com/hugojapan/hugoDocs) | [Organization](https://github.com/hugojapan)


Hugo Documentation の和訳・日本語訳プロジェクト



## ドキュメント翻訳プロジェクトについて

- この organization について
    - 発端 https://github.com/gohugoio/hugoDocs/issues/667
- [hugojapan/ja: Hugo documentation Japanese version](https://github.com/hugojapan/ja)



## 翻訳の優先順位

- ~~Issues で `優先` タグがあるファイルを優先して翻訳してほしいです。~~Issues
- お好きなページの翻訳をお願いします。
- 1ページの一部分の翻訳でも構いません。
- 翻訳の訂正なども歓迎します。



## 方法

- Issue で報告する場合
- Pull Request を作成する場合
    - clone hugoDocs
    - submodule の `ja` で `Draft PR` を作成する、準備ができたら `Ready for review`
    - hugoDocs は確認用、貢献は ja に対して。

### 初回

```sh
# fork hugojapan/hugoDocs
git clone https://github.com/[your_github_id]/hugoDocs.git
cd hugoDocs
# fork hugojapan/ja
git submodule add https://github.com/[your_github_id]/ja.git content/ja
cd content/ja
git checkout -b [target]
vim [target.md]
git add [target.md]
git commit -m "translate: target"
git push origin [target]
# Pull Request を作成する。
# 必要があれば適宜追加で add, commit, push する。
```

- `Squash merge` するので自分で切ったブランチのコミットは適当で構いません。
    - こまめにコミットすると複数人でレビューしやすいかも。
    - `rebase` は使わずに `merge` して親ブランチの変更を取り込んでください。

### Netlify deploy preview

- [世界最速のウェブサイト構築フレームワーク | Hugo](https://hugodocsja.netlify.com/)

👆 ここでプレビューを確認できますが `hugojapan/ja` への push がリアルタイムに反映されるわけではありません。
なお、このプレビューサイトは [robots.txt] を設置して検索エンジンによるインデキシングを拒否しています。
よって、このプレビューサイトが検索結果に表示されてしまう心配はありません。

### 2回目以降

```sh
cd content/ja
git remote add upstream https://github.com/hugojapan/ja.git
git checkout master
git pull upstream master
git checkout -b [target]
vim [target.md]
git add [target.md]
git commit -m "translate: target"
git push origin [target]
# Pull Request を作成する。
# 必要があれば適宜追加で add, commit, push する。
```



## 注意事項

- 翻訳サービスの出力をそのまま利用しない。
    - ライセンスに引っかかる可能性があるので。
    - まだまだ人間の手直しが必要な品質であることがほとんど。
    - 参考にする程度にしてほしい。
- 英文以上の情報を追加しない。
    - 英文の内容以上の情報を含めるべきと判断した場合は本家に貢献してから。



[robots.txt]: https://hugodocsja.netlify.com/robots.txt
