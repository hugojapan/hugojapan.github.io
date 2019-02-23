# Hugo 日本語ドキュメント (工事中)


## ドキュメント翻訳プロジェクトについて

- この organization について
    - 発端 https://github.com/gohugoio/hugoDocs/issues/667
- [hugojapan/ja: Hugo documentation Japanese version](https://github.com/hugojapan/ja)


## 翻訳の優先順位

Issues で `優先` タグがあるファイルを優先して翻訳してほしいです。


## 方法

- Issue で報告する場合
- Pull Request を作成する場合
    - `Draft` で作成する、準備ができたら `Ready for review`

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


## 注意事項

- 翻訳サービスの出力をそのまま利用しない。
- 英文以上の情報を追加しない。
    - 英文の内容以上の情報を含めるべきと判断した場合は本家に貢献してから。
