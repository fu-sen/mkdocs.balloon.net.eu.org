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

## mkdocs-bootswatch テーマ

[<i class="fa-brands fa-github"></i> GitHub mkdocs/mkdocs-bootswatch](https://github.com/mkdocs/mkdocs-bootswatch)

Bootswatch 4 系のテーマを使用できます。  
2022年6月 現在 Bootswatch 5 が最新ですが、MkDocs テーマではまだ非対応です。

```yaml
theme:
    name: cosmo
```

`nav_style` でヘッダ部分の表示を変更できます。`light` ・ `dark` があります。

```
theme:
    name: cerulean
    nav_style: dark
```

テーマ毎の細かい表示は Bootswatch を確認して下さい。

[<i class="fa-brands fa-bootstrap"></i> Bootswatch / Bootstrap 4](https://bootswatch.com/4/)

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

## サイズ最小化（Minify）

[<i class="fa-brands fa-github"></i> GitHub byrnereese/mkdocs-minify-plugin](https://github.com/byrnereese/mkdocs-minify-plugin)

`mkdocs-minify-plugin` を使用し、`plugin` に項目を追加します。

```yaml
plugins:
    - minify:
        minify_html: true
        minify_js: true
        minify_css: true
```

___

## Open Graph (OGP) ・ Twitter Card

MkDocs のテーマは対応していません。テーマのカスタムが必要です。

[🎈 MkDocs <i class="fa-solid fa-hashtag"></i> テーマのカスタマイズ | ふうせん🎈 FU-SEN](https://balloon.asia/mkdocs/#%E3%83%86%E3%83%BC%E3%83%9E%E3%81%AE%E3%82%AB%E3%82%B9%E3%82%BF%E3%83%9E%E3%82%A4%E3%82%BA)

___

## Cloudflare Pages

mkdocs.balloon.net.eu.org は Cloudflare Pages を用いています。

[<i class="fa-brands fa-cloudflare"></i> Cloudflare Pages](https://pages.cloudflare.com/)  
[🎈<i class="fa-brands fa-github"></i> GitHub fu-sen/CloudflarePages-MkDocs](https://github.com/fu-sen/CloudflarePages-MkDocs)

Cloudflare Pages 側で Git 連携を用いて MkDocs をビルドする場合は  
次を追加する必要があります。

- **requirements.txt** - `mkdocs` とインストールするプラグインを指定します。
- **runtime.txt** - Python のバージョン。

ダイレクトアップロード（ドラッグ＆ドロップ または wrangler）では  
ビルド動作を行いません。別途ビルド作業が必要です。

[<i class="fa-brands fa-github"></i> Wiki - Mkdocs Deployments | GitHub mkdocs/mkdocs](https://github.com/mkdocs/mkdocs/wiki/Mkdocs-Deployments)

Netlify・Vercel などを用いてのビルドも可能です。  
また GitHub Actions を用いてビルド作業を行う事もできます。
