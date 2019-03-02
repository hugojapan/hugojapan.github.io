[View on GitHub](https://github.com/hugojapan/hugojapan.github.io) | [Main repo](https://github.com/hugojapan/hugoDocs) | [Organization](https://github.com/hugojapan)

**ʕ◔ϖ◔ʔ (工事中)**

Hugo Documentation の和訳・日本語訳プロジェクト



## ドキュメント翻訳プロジェクトについて

- この organization について
    - 発端 https://github.com/gohugoio/hugoDocs/issues/667
- [hugojapan/ja: Hugo documentation Japanese version](https://github.com/hugojapan/ja)



## 翻訳の優先順位

Issues で `優先` タグがあるファイルを優先して翻訳してほしいです。



## 方法

- Issue で報告する場合
- Pull Request を作成する場合
    - clone hugoDocs
    - submodule の `ja` で `Draft PR` を作成する、準備ができたら `Ready for review`
    - hugoDocs は確認用、貢献は ja に対して。

### 初回

```sh
# fork
git clone https://github.com/hugojapan/hugoDocs.git
cd hugoDocs
git fetch origin
git checkout -b japanese origin/japanese
git remote add ja-subtree https://github.com/hugojapan/ja.git
git commit -am "Add remote hugojapan/ja"
git subtree add --prefix=content/ja --squash ja-subtree master
```

- `Squash merge` するので自分で切ったブランチのコミットは適当で構いません。
    - こまめにコミットすると複数人でレビューしやすいかも。
    - `rebase` は使わずに `merge` して親ブランチの変更を取り込んでください。



## 注意事項

- 翻訳サービスの出力をそのまま利用しない。
- 英文以上の情報を追加しない。
    - 英文の内容以上の情報を含めるべきと判断した場合は本家に貢献してから。
