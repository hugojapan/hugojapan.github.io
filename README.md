**ʕ◔ϖ◔ʔ (工事中)**

[View on GitHub](https://github.com/hugojapan/hugojapan.github.io) | [Main repo](https://github.com/hugojapan/hugoDocs) | [Organization](https://github.com/hugojapan)

Hugo Documentation の和訳・日本語訳プロジェクト



## Table of Contents

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [ドキュメント翻訳プロジェクトについて](#%E3%83%89%E3%82%AD%E3%83%A5%E3%83%A1%E3%83%B3%E3%83%88%E7%BF%BB%E8%A8%B3%E3%83%97%E3%83%AD%E3%82%B8%E3%82%A7%E3%82%AF%E3%83%88%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6)
- [翻訳の優先順位](#%E7%BF%BB%E8%A8%B3%E3%81%AE%E5%84%AA%E5%85%88%E9%A0%86%E4%BD%8D)
- [貢献方法](#%E8%B2%A2%E7%8C%AE%E6%96%B9%E6%B3%95)
  - [初回](#%E5%88%9D%E5%9B%9E)
  - [Netlify deploy preview](#netlify-deploy-preview)
  - [2回目以降](#2%E5%9B%9E%E7%9B%AE%E4%BB%A5%E9%99%8D)
- [注意事項](#%E6%B3%A8%E6%84%8F%E4%BA%8B%E9%A0%85)
- [ライセンス](#%E3%83%A9%E3%82%A4%E3%82%BB%E3%83%B3%E3%82%B9)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->



## ドキュメント翻訳プロジェクトについて

- この organization について
    - 発端 https://github.com/gohugoio/hugoDocs/issues/667
- [hugojapan/ja: Hugo documentation Japanese version](https://github.com/hugojapan/ja)



## 翻訳の優先順位

- ~~Issues で `優先` タグがあるファイルを優先して翻訳してほしいです。~~
- お好きなページの翻訳をお願いします。
- 一部分の翻訳でも構いません。
- 翻訳の訂正なども歓迎します。



## 貢献方法

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
git remote add upstream https://github.com/hugojapan/ja.git
git checkout -b [target]
vim [target.md]
git add [target.md]
git commit -m "translate: [target]"
git push origin [target]
# Pull Request を作成する。
# 必要があれば適宜追加で add, commit, push する。
```

もちろん `hugo server -w` でホットリロードしながらローカルプレビューできます。

`Squash merge` するので自分で切ったブランチのコミットは適当で構いませんが、
こまめにコミットすると複数人でレビューしやすいかもしれません。

作業中に master branch で変更があり、それを自分のブランチに取り込みたい場合は
以下のようにして `rebase` は使わずに `merge` して親ブランチの変更を取り込んでください。

```sh
git checkout master
git pull upstream master
git checkout [target]
git merge master
# commit
git push origin [target]
```

### Netlify deploy preview

- [世界最速のウェブサイト構築フレームワーク | Hugo](https://hugodocsja.netlify.com/)

👆 ここでプレビューを確認できますが `hugojapan/ja` への push がリアルタイムに反映されるわけではありません。
なお、このプレビューサイトは [robots.txt] を設置して検索エンジンによるインデキシングを拒否しています。
よって、このプレビューサイトが検索結果に表示されてしまう心配はありません。

### 2回目以降

```sh
cd content/ja
git checkout master
git pull upstream master
git checkout -b [target]
vim [target.md]
git add [target.md]
git commit -m "translate: [target]"
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



## ライセンス

- [gohugoio/hugoDocs LICENSE](https://github.com/gohugoio/hugoDocs/blob/master/LICENSE.md)



<div align="right"><a href="#table-of-contents">Back to TOC ☝️</a></div>



<!-- Internal References -->
<!-- External References -->
[robots.txt]: https://hugodocsja.netlify.com/robots.txt
