# Privacy Policy / プライバシーポリシー

**Last updated / 最終更新日: 2026-09-23**

---

## 日本語

### 1. はじめに

Tachometer Lite（Mac App Store 版。インストール後のアプリ名は Tachometer）および Tachometer Plus（Developer ID 版。以下あわせて「本アプリ」）は、ユーザーのプライバシーを尊重します。本ポリシーは、本アプリがどのような情報を取り扱うか、または扱わないかを明示するものです。

### 2. 収集する情報

**本アプリは、いかなる個人情報も収集しません。**

具体的には以下のいずれも行いません:

- ユーザーアカウントの作成・管理
- 氏名・メールアドレス・電話番号などの個人情報の取得
- 位置情報の取得
- アプリ使用状況や利用統計の収集
- クラッシュレポートの自動送信
- 広告 ID・追跡 ID の収集
- 連絡先・カレンダー・写真など macOS の機密データへのアクセス

### 3. 本アプリが読み取るシステム情報について

本アプリは計器の針を振らせるために、お使いの Mac の以下の指標を約 1〜4 秒ごとに読み取ります。いずれも**集計済みの数値**です。App Store 版は macOS が提供する公開 API だけを使います。Developer ID 版は、これに加えて消費電力・GPU・Neural Engine・温度を、macOS の IOKit を通じてハードウェアの計測値（SMC・IOReport）から読み取ります。

- ネットワークインターフェイスの送受信バイト数（`getifaddrs` / `SCDynamicStoreCopyValue`）
- ディスクの読み書きバイト数（IOKit の `IOBlockStorageDriver` 統計）
- 物理メモリの空き容量とメモリ負荷（`host_statistics64` / メモリプレッシャー通知）
- CPU 使用率（`host_processor_info`）
- Mac 全体の消費電力、GPU・Neural Engine の稼働状況（Developer ID 版のみ）
- CPU・GPU の温度（Developer ID 版のみ）

本アプリが扱うのは、これらの**数値だけ**です。

- **通信の中身を見ることはありません。** 読み取るのはインターフェイスを通過したバイト数の合計のみで、通信先・URL・パケットの内容は一切参照しません。
- **ファイルの中身を見ることはありません。** 読み取るのはディスクドライバの読み書きバイト数の合計のみで、ファイル名・パス・内容にはアクセスしません。
- **どのアプリが何をしているかを識別しません。** 本アプリが見るのはシステム全体の合計値だけです。
- 取得した数値は針の表示とピーク値の学習にのみ使い、**記録・保存・外部送信は行いません**。

### 4. ローカルに保存されるデータ

本アプリは、以下の情報をお使いの Mac 上（UserDefaults / サンドボックスコンテナ）のみに保存します。これらは外部に送信されません。

- 各計器の表示 / 非表示
- 計器ウインドウの位置と、表示しているディスプレイの識別子
- ウインドウの置き方（常に最前面 / 壁紙に貼り付ける）、照明（自動 / Day / Night）、シンボルの種類、システムモニターの並べ方
- ピーク学習の期間設定と、学習したピーク値
- 「画面下端で呼び出す」の有効 / 無効
- 設定の移行を済ませたかどうかの印（アップデート時に一度だけ行う処理のため）

これらのデータは、本アプリをアンインストールすることで削除されます。

### 5. ネットワーク通信

**本アプリはインターネット通信を行いません。**

- 外部サーバーへのデータ送信なし
- 外部 API の呼び出しなし
- アップデートチェックなし（App Store 版は Apple の更新機構、Developer ID 版は Homebrew または手動更新のみ）

App Store 版は App Sandbox 下で動作し、ネットワークアクセスの権限（`com.apple.security.network.client`）自体を要求していません。

### 6. 第三者サービス

本アプリは、Google Analytics、Firebase、その他のアナリティクスや広告 SDK を一切利用していません。

### 7. 児童のプライバシー

本アプリは特定の年齢層を対象としたものではなく、また 13 歳未満の児童から意図的に個人情報を収集することはありません。

### 8. プライバシーポリシーの変更

本ポリシーは予告なく改定される場合があります。変更がある場合、本ページの「最終更新日」を更新します。

### 9. お問い合わせ

ご質問・ご意見は GitHub Discussions または Email までお願いします:

- GitHub Discussions: https://github.com/EVAtiter/tachometer-release/discussions
- Email: info@slack-kingdom.com

---

## English

### 1. Introduction

Tachometer Lite (Mac App Store edition; the installed app is named Tachometer) and Tachometer Plus (Developer ID edition) — together, "the App" — respect user privacy. This policy outlines what information the App handles and does not handle.

### 2. Information We Collect

**The App does not collect any personal information.**

Specifically, the App does NOT:

- Create or manage user accounts
- Collect names, email addresses, phone numbers, or any other personal data
- Access location data
- Collect usage statistics or analytics
- Automatically send crash reports
- Collect advertising or tracking identifiers
- Access sensitive macOS data such as Contacts, Calendar, or Photos

### 3. About the System Metrics the App Reads

To move the gauge needles, the App reads the following metrics from your Mac about every 1 to 4 seconds. All of them are **aggregate numbers**. The App Store edition uses only public macOS APIs. The Developer ID edition additionally reads power, GPU and Neural Engine activity, and temperatures from hardware sensors (SMC and IOReport) through macOS IOKit.

- Bytes sent and received on network interfaces (`getifaddrs` / `SCDynamicStoreCopyValue`)
- Bytes read from and written to disks (IOKit `IOBlockStorageDriver` statistics)
- Free physical memory and memory pressure (`host_statistics64` / memory pressure notifications)
- CPU utilization (`host_processor_info`)
- Whole-Mac power draw, GPU and Neural Engine activity (Developer ID edition only)
- CPU and GPU temperatures (Developer ID edition only)

These **numbers are the only thing the App handles**.

- **It never inspects the content of your network traffic.** It reads only the total byte counters of an interface — never destinations, URLs, or packet contents.
- **It never inspects the content of your files.** It reads only the total byte counters of the disk driver — never file names, paths, or contents.
- **It does not identify which app is doing what.** The App only sees system-wide totals.
- The values are used solely to drive the needles and to learn peak values. They are **never recorded, stored, or transmitted**.

### 4. Locally Stored Data

The App stores the following information only on your Mac (UserDefaults / sandbox container). None of it is transmitted externally.

- Which gauges are shown or hidden
- Gauge window positions and the identifier of the display they appear on
- Window placement (Always on Top / Pin to Wallpaper), lighting (auto / day / night), symbol set, and System Monitor layout
- Peak-learning window setting and the learned peak values
- Whether "Quick Reveal" (reveal at the bottom edge of the screen) is enabled
- A marker recording that one-time settings migrations have been completed

This data is deleted when the user uninstalls the App.

### 5. Network Communication

**The App does not communicate over the internet.**

- No data transmission to external servers
- No external API calls
- No update checks (the App Store edition updates through Apple's mechanisms; the Developer ID edition through Homebrew or manual download)

The App Store edition runs under App Sandbox and does not even request the network access entitlement (`com.apple.security.network.client`).

### 6. Third-Party Services

The App does not use Google Analytics, Firebase, or any other analytics or advertising SDKs.

### 7. Children's Privacy

The App is not directed at any specific age group and does not knowingly collect personal information from children under 13.

### 8. Changes to This Policy

This policy may be revised without prior notice. When changes are made, the "Last updated" date at the top of this page will be updated.

### 9. Contact

For questions or feedback, please use GitHub Discussions or Email:

- GitHub Discussions: https://github.com/EVAtiter/tachometer-release/discussions
- Email: info@slack-kingdom.com
