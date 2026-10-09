# pdf-r2l-script-linux

PDFを右綴じ(R2L)かつ見開き(右始まり)にする、Linux 用の GUI アプリです。
(English) A Linux GUI app that changes the binding direction of PDFs (R2L). Source: https://github.com/INORIA/pdf-r2l-script (reimplemented in Rust).

## インストール / Install
`sudo apt install ./pdf-r2l-script-linux_*.deb` でインストールします(Debian/Ubuntu系)。他のディストリビューションは `pdf-r2l-script-linux-x86_64.tar.gz` を展開して実行してください。

## 使い方 / Usage
PDFを選択またはドラッグ&ドロップし、「変換して保存…」。ライセンスはアプリ内の「ライセンス / License」ボタンと
同梱の LICENSES.txt に英語・日本語併記で記載しています。

## 開発 / Build
```
cargo test
cargo build --release
```
パッケージ(dmg/deb)は GitHub Actions(`.github/workflows/release.yml`、`v*` タグで発火)で作成します。
依存を変えたら `scripts/gen-third-party.ps1 > licenses/third-party.txt` の後に `sh scripts/build-licenses.sh`。

## LICENSE
MIT。詳細・第三者ライセンスは [LICENSES.txt](LICENSES.txt)。
