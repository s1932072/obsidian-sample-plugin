## サンプルプラグイン

これはObsidianのサンプルプラグインです。

このプロジェクトでは型チェックとドキュメンテーションにTypescirptを利用しています。リポジトリはTypesciprtの定義フォーマット上の最新のプラグインAPI(obsidian.d.ts)に基づいており、APIが何を行っているかを記述するTSDocsコメントを含んでいます。

**ノート:** Obsidian APIは依然としてアーリーアルファであり、常に変更の可能性があることに注意してください。

このサンプルプラグインではプラグインAPIのいくつかの基本的な機能のデモンストレーションを行います。
- `styles.css` を利用してデフォルトスタイルカラーをredに変更
- クリック時に通知を表示するリボンアイコンの追加
- モーダルを開く"Open Sample Modal"コマンドを追加
- 設定ページにプラグイン設定タブを追加
- グローバルclickイベント登録とコンソールへの'click'アウトプット
- 'setInterval'をコンソールに記録するグローバルインターバルでの登録

## プラグイン開発は初めて?

新規プラグイン開発のためのクイックスタートガイド

- ｢Use this template｣ボタンをクリックしてこのリポジトリをテンプレートとしてコピーしてください
- リポジトリをローカルの開発用フォルダへとクローンしてください。kのフォルダは`.obsidian/plugins/your-plugin-name` folder`に置いておくと開発に便利です。
- NodeJSをインストールして、リポジトリの元で`npm i`コマンドを実行します。
- プラグイン用に`main.ts`から`main.js`へとコンパイルするために`npm run dev`を実行します。
- `main.ts`(または新しく`.ts`ファイルを作成し)へ変更を加えます。これらの変更は自動的に`main.js`へとコンパイルされます。
- Obsidianをリロードしてプラグインの最新バージョンをロードします。
- 設定ウィンドウにてプラグインを有効化してください。
- ObsidianのAPIをアップデートするにはリポジトリフォルダにてコマンドラインから`npm update`を実行してください。


### 新規リリース方法

- `1.0.1`といったバージョン番号と最新リリースに必要な最小のObsidianのバージョン番号に合わせて `manifest.json` をアップデートしてください。
- `version.json` ファイルについては、"プラグインの新規バージョン": "Obsidianの最小バージョン" を追記して、Obsidianの古いバージョンでも互換性のプラグインがダウンロードできるようにアップデートしてください。
- 最新バージョン番号を"Tag version"として使って新しいGithubリリースを作成します。その際にプレフィックスに `v` をつけないで正確なバージョン番号を記載してください。例として次のリンクを確認してください。https://github.com/obsidianmd/obsidian-sample-plugin/releases
- `manifest.json`, `main.js`, `styles.css` の3つのファイルをバイナリファイルとしてアップロード
- リリースを公開します。

### プラグインをコミュニティのプラグインリストに追加する

- 最初のバージョンを公開
- `README.md` ファイルをリポジトリのルートに配置
- https://github.com/obsidianmd/obsidian-releases にプラグインを追加してプルリクエストを作成する

### 使い方

- このリポジトリをclone
- `npm i` または `yarn` で依存関係をインストール
- `npm run dev` でウォッチモードでコンパイルを開始

### 手動インストールの方法

- `main.js`, `styles.css`, `manifest.json`の3つのファイルを保管庫の`VaultFolder/.obsidian/plugins/your-plugin-id/`にコピー&ペーストする。
  

### APIドキュメント

https://github.com/obsidianmd/obsidian-api を確認してください。
