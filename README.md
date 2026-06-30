# Karuzip（かるジップ）

**軽い・安心・広告なしの解凍/圧縮ソフト（Windows）**

Karuzip は、ZIP・7z・RAR などをドラッグ＆ドロップや右クリックでかんたんに解凍／圧縮できる、日本語対応の無料 Windows アプリです。広告・バンドルソフト・テレメトリは一切ありません。

> このリポジトリは Karuzip の**配布専用**です（インストーラの公開・更新履歴・不具合報告のため）。アプリ本体のソースコードは含みません。

## ダウンロード

**→ [最新版をダウンロード](https://github.com/AAAAAnson/karuzip/releases/latest)**

直リンク: `https://github.com/AAAAAnson/karuzip/releases/latest/download/Karuzip_1.0.0_x64-setup.exe`

- 対応: Windows 11 / 10（64bit）
- サイズ: 約 3.3 MB

### 初回起動時の警告について（SmartScreen）

新しいソフトのため、初回起動時に Windows の SmartScreen が「WindowsによってPCが保護されました」と青い画面で警告を表示することがあります。これはウイルスを検出したという意味ではなく、利用実績の少ない新しいアプリへの注意表示です。［詳細情報］→［実行］で起動できます。

ご不安な場合は、各リリースに記載の SHA-256 ハッシュで配布ファイルの同一性をご確認ください:

```powershell
Get-FileHash .\Karuzip_1.0.0_x64-setup.exe -Algorithm SHA256
```

## 特長

- ドラッグ＆ドロップ／右クリックメニューからかんたん解凍・圧縮
- ZIP・7z での圧縮、ZIP・7z・RAR・tar・gz ほか主要形式の解凍
- パスワード付き（暗号化）ZIP・7z の解凍と作成に対応
- 広告・バンドルソフトなし、個人情報の収集・送信なし

## プライバシー

Karuzip は広告を表示せず、利用者の個人情報を収集・送信しません。

## ライセンス

本体は無償で提供されます（[LICENSE](LICENSE)）。

Karuzip は圧縮・解凍エンジンとして **7-Zip 25.01** を改変せず同梱・使用しています（主に GNU LGPL、一部に BSD ライセンスおよび unRAR 制限）。第三者ライセンスの全文は [licenses/](licenses/) を参照してください。

- 7-Zip 公式ライセンス全文: [licenses/7-Zip-License.txt](licenses/7-Zip-License.txt)
- 7-Zip 25.01 ソースコード: https://www.7-zip.org/download.html （`7z2501-src.7z`）

RAR は **解凍のみ** に対応します（unRAR ライセンスにより RAR 形式の作成は行いません）。
