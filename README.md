**ʕ◔ϖ◔ʔ (工事中)**

[View on GitHub] | [Main repo] | [Organization]

Hugo Documentation の和訳・日本語訳プロジェクト



## Table of Contents

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [ドキュメント翻訳プロジェクトについて](#%E3%83%89%E3%82%AD%E3%83%A5%E3%83%A1%E3%83%B3%E3%83%88%E7%BF%BB%E8%A8%B3%E3%83%97%E3%83%AD%E3%82%B8%E3%82%A7%E3%82%AF%E3%83%88%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6)
- [翻訳の優先順位](#%E7%BF%BB%E8%A8%B3%E3%81%AE%E5%84%AA%E5%85%88%E9%A0%86%E4%BD%8D)
- [注意事項](#%E6%B3%A8%E6%84%8F%E4%BA%8B%E9%A0%85)
- [貢献方法](#%E8%B2%A2%E7%8C%AE%E6%96%B9%E6%B3%95)
  - [初回](#%E5%88%9D%E5%9B%9E)
  - [Netlify deploy preview](#netlify-deploy-preview)
  - [2回目以降](#2%E5%9B%9E%E7%9B%AE%E4%BB%A5%E9%99%8D)
- [ライセンス](#%E3%83%A9%E3%82%A4%E3%82%BB%E3%83%B3%E3%82%B9)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->



## ドキュメント翻訳プロジェクトについて

以下の Issue で提案しました。

- [Translation project for Japanese users · Issue #667 · gohugoio/hugoDocs](https://github.com/gohugoio/hugoDocs/issues/667)

実際に Pull Request を出していただくのは以下の Repository です。

- [hugojapan/ja](https://github.com/hugojapan/ja)

以下の Repository はローカルプレビュー用です。

- [hugojapan/hugoDocs](https://github.com/hugojapan/hugoDocs)



## 翻訳の優先順位

- ~~Issues で `優先` タグがあるファイルを優先して翻訳してほしいです。~~
- お好きなページの翻訳をお願いします。
- 一部分の翻訳でも構いません。
- 翻訳の訂正なども歓迎します。



## 注意事項

翻訳サービスの出力をそのまま利用しないでください。

- ライセンスに引っかかる可能性がある
- まだまだ人間の手直しが必要な品質であることがほとんど
- 参考にする程度で利用してほしい

英文以上の情報を追加しないようにしてください。

- 英文の内容以上の情報を含めるべきと判断した場合は本家に貢献してから
- 良い改善であれば他言語でも共有すべき



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
npm install # node 実行環境が無い方はスキップしても構いません。
git checkout -b [target]
vim [target.md]
git add [target.md]
git commit -m "translate: [target]"
git push origin [target]
# Pull Request を作成する。
# 必要があれば適宜追加で add, commit, push する。
```

もちろん `hugo server -w` でホットリロードしながらローカルプレビューできます。

- http://localhost:1313/

コミットする際に textlint による日本語のチェックが自動で実行されます。
また、個別のファイルに対して `npm run lint [target].md` で日本語のチェックができます。
textlint のルールについて改善案があれば [Issue][Issues hugojapan/ja] を出してください。

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

- [世界最速のウェブサイト構築フレームワーク - Hugo]

👆 ここでプレビューを確認できますが `hugojapan/ja` への push がリアルタイムに反映されるわけではありません。
(`hugojapan/ja` の `master` への merge をトリガーにして `hugojapan/hugoDocs` の `japanese` で submodule を自動 update させる予定。
[Clone hugojapan/ja once a day at japanese branch · Issue #7 · hugojapan/ja](https://github.com/hugojapan/ja/issues/7))

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



## ライセンス

- [gohugoio/hugoDocs LICENSE](https://github.com/gohugoio/hugoDocs/blob/master/LICENSE.md)



<div align="right"><a href="#table-of-contents">Back to TOC ☝️</a></div>



<!-- Internal References -->
[View on GitHub]: https://github.com/hugojapan/hugojapan.github.io

<!-- External References -->
[Main repo]: https://github.com/hugojapan/ja
[Organization]: https://github.com/hugojapan
[Issues hugojapan/ja]: https://github.com/hugojapan/ja/issues
[世界最速のウェブサイト構築フレームワーク - Hugo]: https://hugodocsja.netlify.com/
[robots.txt]: https://hugodocsja.netlify.com/robots.txt
