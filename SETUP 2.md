# Lingua をiPhoneにインストールする手順

## 全体の流れ

1. GitHub アカウントを作成(無料)
2. リポジトリにファイルをアップロード
3. GitHub Pages を有効化 → URL取得
4. iPhone Safariでアクセス → ホーム画面に追加

所要時間: **約20分**

---

## ステップ 1: GitHubアカウント作成

すでにアカウントがある場合はスキップ。

1. https://github.com/signup にアクセス
2. メールアドレス、パスワード、ユーザー名を入力
3. メール認証を完了

---

## ステップ 2: リポジトリ作成

1. ログイン後、画面右上の「+」→「New repository」をクリック
2. 設定:
   - **Repository name**: `lingua` (好きな名前でOK)
   - **Public** を選択(Privateでは無料のGitHub Pagesが使えない)
   - 「**Add a README file**」にチェック
3. 「Create repository」をクリック

---

## ステップ 3: ファイルをアップロード

1. 作成したリポジトリのページで「Add file」→「Upload files」をクリック
2. ZIPファイルを解凍した中身を**ドラッグ&ドロップ**:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`
   - `icon-512.png`
3. 下部の「Commit changes」をクリック

---

## ステップ 4: GitHub Pagesを有効化

1. リポジトリの「Settings」タブをクリック
2. 左メニューの「Pages」をクリック
3. 「Build and deployment」セクション:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main` を選択、フォルダは `/ (root)`
4. 「Save」をクリック
5. 数分待つと、ページ上部に「Your site is live at https://[ユーザー名].github.io/lingua/」と表示される

⚠ 初回は反映まで **5〜10分** かかることがあります。

---

## ステップ 5: iPhoneにインストール

1. **iPhone の Safari** でステップ4のURLにアクセス
   - ⚠ Chrome ではダメ、必ず Safari を使う
2. 画面下の **共有ボタン**(□に↑の矢印)をタップ
3. メニューを下にスクロール →「**ホーム画面に追加**」をタップ
4. 名前を確認(「Lingua」のはず)→ 右上の「**追加**」をタップ
5. ホーム画面にアイコンが表示されたら完了!

---

## 動作確認

ホーム画面のLinguaアイコンをタップして起動:
- ✅ フルスクリーンで起動する(Safari のアドレスバーが消える)
- ✅ アプリのように使える
- ✅ オフラインでも基本機能が動く(音声合成はオンライン推奨)
- ✅ 進捗が保存される(同じ端末内)

---

## トラブルシューティング

**Q: GitHub Pagesにアクセスしても「404」が出る**
- A: 5〜10分待つ。それでも出る場合、Settings → Pages で再度設定を確認

**Q: 音声が再生されない**
- A: 初回起動時に再生ボタンをタップしてください(ブラウザのポリシー)。iPhone のサイレントモードもオフに

**Q: マイクが使えない(Speakingクエスト)**
- A: ⚠ **iOS Safari の Web Speech API はネイティブアプリよりも制限が多く、認識精度が低めです。** 動かない場合は手動で「Check」を押すと自動的にスキップモードになります

**Q: ホーム画面から開いてもSafariが起動する**
- A: manifest.json の `display: standalone` が効くのは「ホーム画面に追加」した場合のみ。共有メニューから「ホーム画面に追加」を選んでください

---

## 後で教材を増やしたいとき

ファイルを更新したい時:
1. GitHub リポジトリで `index.html` を開く
2. 鉛筆アイコン(編集)をクリック
3. 修正してCommit
4. 数分で反映される

新しい問題を追加したい時はClaudeに相談してください。`lessons` オブジェクトに追加する形で拡張できます。
