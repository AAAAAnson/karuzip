# Karuzip（かるジップ）

**軽い・安心・広告なしの解凍/圧縮ソフト（Windows）**

Karuzip は、ZIP・7z・RAR などをドラッグ＆ドロップや右クリックでかんたんに解凍／圧縮できる、日本語対応の無料 Windows アプリです。広告・バンドルソフト・テレメトリは一切ありません。

**公式サイト: https://karuzip.com**

> このリポジトリは Karuzip の**配布専用**です（インストーラの公開・更新履歴・不具合報告のため）。アプリ本体のソースコードは含みません。

## ダウンロード

**→ [最新版をダウンロード](https://github.com/AAAAAnson/karuzip/releases/latest)**（現在 v1.3.0）

- 公式サイトから: https://karuzip.com/download/Karuzip-Setup.exe （常に最新版）
- **Microsoft Store 版**: https://apps.microsoft.com/detail/9N9KD93CM84T
  （Microsoft の署名が付くため **SmartScreen の警告が出ません**。Windows 11 向け）

対応: Windows 11 / 10（64bit）／ サイズ: 約 7.4 MB

### 初回起動時の警告について（SmartScreen）

公式サイト・GitHub で配布しているインストーラは現在**コード署名なし**のため、初回起動時に Windows の SmartScreen が「WindowsによってPCが保護されました」と青い画面で警告を表示することがあります。これはウイルスを検出したという意味ではなく、利用実績の少ない新しいアプリへの注意表示です。［詳細情報］→［実行］で起動できます。

警告を出したくない場合は、上記の **Microsoft Store 版**をご利用ください。

くわしい解説: https://karuzip.com/smartscreen.html

ご不安な場合は、配布ファイルの SHA-256 ハッシュをご確認ください（v1.3.0 は各リリースページにも記載しています）:

```powershell
Get-FileHash .\Karuzip_1.3.0_x64-setup.exe -Algorithm SHA256
# 3091F7D826CC6D932662326315DDE3C24C7050F5B652924FD8D65A42C43FA751
```

## 特長

- ドラッグ＆ドロップでかんたんに解凍・圧縮
- **解凍は 320 種類の拡張子に対応**（うち動作検証済み 230 種類、実機ファイルでの検証済み 12 種類）。ZIP・7z・RAR・tar・gz ほか
- 圧縮は ZIP・7z・tar・gz ほかに対応（**RAR の作成は行いません**。下記ライセンス参照）
- パスワード付き（暗号化）書庫の解凍と作成に対応（7z はファイル名も暗号化）
- **日本語ファイル名の文字化けに対応**。文字コードを手動で切り替えることもできます（自動 / UTF-8 / CP932 / GBK / Big5）
- 分割書庫（`.zip.001` / `.part1.rar` など）の解凍と作成に対応
- 右クリックメニューから直接「ここに解凍」「Karuzip で圧縮」（Windows 11 の Store 版は一次メニューに 6 項目）
- 大きな書庫でも件数つきの進捗表示、必要なファイルだけを選んで解凍することも可能
- 書庫の中身を解凍せずに一覧・検索、破損チェック（テスト）
- 自動更新に対応（v1.0.2 以降）
- 広告・バンドルソフトなし、個人情報の収集・送信なし

## ドキュメント

- [使い方ガイド（実際の画面つき）](https://karuzip.com/tsukaikata.html)
- [更新履歴](https://karuzip.com/koushin-rireki.html)
- [安全性について](https://karuzip.com/anzen.html)
- [ZIP の文字化けはなぜ起きるのか](https://karuzip.com/zip-mojibake.html)
- [運営者情報・お問い合わせ](https://karuzip.com/operator.html)

不具合のご報告・ご要望は、このリポジトリの [Issues](https://github.com/AAAAAnson/karuzip/issues) か support@karuzip.com までお願いします。

## プライバシー

Karuzip は広告を表示せず、利用者の個人情報を収集・送信しません（アプリからの通信は自動更新の確認のみです）。

## ライセンス

本体は無償で提供されます（[LICENSE](LICENSE)）。

Karuzip は解凍・圧縮エンジンとして、以下のソフトウェアを**改変せず**同梱・使用しています。第三者ライセンスの全文は [licenses/](licenses/) を参照してください（同じものがインストール先の `licenses` フォルダーにも入っています）。

| 同梱ソフトウェア | ライセンス | ソースコード |
|---|---|---|
| **7-Zip 25.01** | 主に GNU LGPL、一部 BSD および unRAR 制限（[全文](licenses/7-Zip-License.txt)／[日本語](licenses/7-Zip-License-ja.txt)） | https://www.7-zip.org/download.html （`7z2501-src.7z`） |
| **unar / lsar 1.8.1** | GNU LGPL 2.1（[全文](licenses/unar-LGPL-2.1.txt)） | 対応する XADMaster / universal-detector の commit を [licenses/unar-NOTICE.txt](licenses/unar-NOTICE.txt) に記載 |
| **Foundation.1.0.dll**（Cocotron 由来、unar が使用） | MIT（[全文・来歴](licenses/Foundation-MIT.txt)） | MIT のためソース提供義務なし。判明している来歴は同ファイルに記載 |

RAR は **解凍のみ** に対応します（[unRAR ライセンス](licenses/unRAR-LICENSE.txt)により RAR 形式の作成は行いません）。
