# mkdocs.balloon.net.eu.org

[<i class="fa-solid fa-link"></i> MkDocs](https://www.mkdocs.org/)  - 公式サイト  
[<i class="fa-brands fa-github"></i> GitHub mkdocs/mkdocs](https://github.com/mkdocs/mkdocs/)

MkDocs の日本語サンプルです。

MkDocs に関する詳細はこちらを参照して下さい。

[🎈 MkDocs | ふうせん🎈 FU-SEN](https://balloon.asia/mkdocs/)

___

## mkdocs コマンド

通常 `mkdocs.yml` があるフォルダで `mkdocs` コマンドを実行します。

Web ブラウザで表示を確認する

```bash
mkdocs serve
```

ビルドして site フォルダを生成する

```bash
mkdocs build
```

Git のリポジトリへデプロイも可能です。

___

## mkdocs.yml

Web サイト（ドキュメント）共通の設定項目です。

```yaml
site_name: mkdocs.balloon.net.eu.org
```

最低限必要な項目は `site_name` ですが、  
公開時は `site_url` など、いくつか項目を追加した方が良いでしょう。

___

## index.md

**site** 内の **index.html** に変換されます。  
通常 Markdown で記載していきます。

[🎈 Markdown | ふうせん🎈 FU-SEN](https://balloon.asia/markdown/)

<strong>HTML タグ</strong> も使用できます。

改行に `\` は使用できません。  
代わりに半角スペース 2 つ、または HTML タグ `<br>` を使用します。

同様に **example.md** は **example.html** へ変換されます。

他のファイルはビルドでそのまま site フォルダへ入ります。  
画像ファイルや `robots.txt` などを入れて下さい。

___

## 検索フォーム

**<i class="fa-solid fa-magnifying-glass"></i> Search** は MkDocs 1.2 より日本語対応しています。  
実際にこのページを日本語検索してみて下さい。

日本語検索を有効にするためには、  
**mkdocs.yml** の `theme` 内に `locale: ja` を追加します。

```yaml
theme:
    locale: ja
```

MkDocs 1.1 以前のバージョンでも Material for MkDocs が日本語対応です。

[<i class="fa-solid fa-link"></i> Material for MkDoc](https://squidfunk.github.io/mkdocs-material/)

___

## Open Graph (OGP) ・ Twitter Card

MkDocs のテーマは対応していません。テーマのカスタムが必要です。

[🎈 MkDocs <i class="fa-solid fa-hashtag"></i> テーマのカスタマイズ | ふうせん🎈 FU-SEN](https://balloon.asia/mkdocs/#%E3%83%86%E3%83%BC%E3%83%9E%E3%81%AE%E3%82%AB%E3%82%B9%E3%82%BF%E3%83%9E%E3%82%A4%E3%82%BA)
