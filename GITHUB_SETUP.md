# GitHub セットアップガイド

## ステップ1: GitHubアカウントの準備

1. [GitHub](https://github.com/)にアクセス
2. アカウントを作成（既にある場合はログイン）

## ステップ2: 新しいリポジトリを作成

1. GitHubの右上の「+」→「New repository」をクリック
2. 以下の情報を入力：
   - **Repository name**: `maruhachi-kenpo`
   - **Description**: 丸八真綿健康保険組合 公式ホームページ
   - **Public/Private**: プライベートを推奨
   - **Initialize this repository with**: チェックを入れない

3. 「Create repository」をクリック

## ステップ3: ローカルでGitを初期化

ターミナル（コマンドプロンプト）で以下を実行：

```bash
# 1. プロジェクトディレクトリに移動
cd maruhachi_kenpo_site

# 2. Gitリポジトリを初期化
git init

# 3. すべてのファイルをステージング
git add .

# 4. 初回コミット
git commit -m "Initial commit: 丸八真綿健保サイト"

# 5. デフォルトブランチをmainに変更
git branch -M main

# 6. リモートリポジトリを追加（YOUR-USERNAMEを自分のユーザー名に変更）
git remote add origin https://github.com/YOUR-USERNAME/maruhachi-kenpo.git

# 7. GitHubにプッシュ
git push -u origin main
```

### GitHubの認証

初めてpushする際、認証を求められます：

**方法1: Personal Access Token（推奨）**
1. GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. 「Generate new token」をクリック
3. Scopeで「repo」にチェック
4. トークンをコピー
5. pushの際、パスワードの代わりにトークンを使用

**方法2: SSH Key**
```bash
# SSH鍵を生成
ssh-keygen -t ed25519 -C "your-email@example.com"

# 公開鍵をコピー
cat ~/.ssh/id_ed25519.pub

# GitHubのSettings → SSH and GPG keys → New SSH keyに追加
```

## ステップ4: GitHub Pagesを有効化

1. GitHubリポジトリのページで「Settings」をクリック
2. 左サイドバーの「Pages」をクリック
3. Source:
   - **Source**: Deploy from a branch
   - **Branch**: main
   - **Folder**: / (root)
4. 「Save」をクリック
5. 数分後、`https://YOUR-USERNAME.github.io/maruhachi-kenpo/`で公開

## ステップ5: 動作確認

```bash
# サイトにアクセス
https://YOUR-USERNAME.github.io/maruhachi-kenpo/
```

## 日常の作業フロー

### 新しい変更を加える場合

```bash
# 1. 最新のmainを取得
git checkout main
git pull origin main

# 2. 新しいブランチを作成
git checkout -b feature/update-birth-page

# 3. ファイルを編集
# （例）procedure-birth.htmlを修正

# 4. 変更を確認
git status
git diff

# 5. 変更をステージング
git add procedure-birth.html

# 6. コミット
git commit -m "出産ページに新しい情報を追加"

# 7. GitHubにプッシュ
git push origin feature/update-birth-page

# 8. GitHubでPull Requestを作成

# 9. レビュー後、mainにマージ
```

### 緊急の修正の場合

```bash
# mainブランチで直接修正
git checkout main
git add .
git commit -m "緊急修正: リンク切れを修正"
git push origin main
```

## トラブルシューティング

### エラー: "fatal: remote origin already exists"

```bash
git remote remove origin
git remote add origin https://github.com/YOUR-USERNAME/maruhachi-kenpo.git
```

### エラー: "Updates were rejected because the remote contains work"

```bash
git pull origin main --rebase
git push origin main
```

### GitHub Pagesが更新されない

1. Actions タブで deployment の状態を確認
2. Settings → Pages でSourceが正しく設定されているか確認
3. ブラウザのキャッシュをクリア（Ctrl+Shift+R / Cmd+Shift+R）

## 便利なGitコマンド

```bash
# 変更履歴を見る
git log --oneline

# 特定のファイルの変更履歴
git log -- procedure-birth.html

# 変更を元に戻す（コミット前）
git checkout -- ファイル名

# 直前のコミットを修正
git commit --amend

# ブランチ一覧
git branch -a

# 不要なブランチを削除
git branch -d feature/old-feature
```

## 次のステップ

1. ✅ GitHubリポジトリ作成
2. ✅ 初回コミット
3. ✅ GitHub Pages有効化
4. ⏭️ README.mdを更新（YOUR-USERNAMEを実際のユーザー名に変更）
5. ⏭️ Issuesでタスク管理を開始
6. ⏭️ ブランチ戦略で並行作業

## 質問がある場合

- [GitHub Docs](https://docs.github.com/)
- [Git公式ドキュメント](https://git-scm.com/doc)
