# 貢献ガイドライン

丸八真綿健康保険組合のホームページプロジェクトへの貢献をありがとうございます！

## 🚀 はじめに

### 環境セットアップ

1. リポジトリをフォーク
2. ローカルにクローン
```bash
git clone https://github.com/YOUR-USERNAME/maruhachi-kenpo.git
cd maruhachi-kenpo
```

3. ブラウザで `index.html` を開いて動作確認

## 📋 貢献の種類

### 1. バグ修正

1. Issueで既存のバグを確認するか、新しいバグを報告
2. ブランチを作成: `git checkout -b fix/bug-description`
3. 修正を実施
4. テストして動作確認
5. コミット: `git commit -m "Fix: バグの説明"`
6. Pull Requestを作成

### 2. 新機能の追加

1. Issueで機能を提案
2. 承認後、ブランチを作成: `git checkout -b feature/feature-name`
3. 実装
4. テスト
5. コミット: `git commit -m "Feature: 機能の説明"`
6. Pull Requestを作成

### 3. 申請書の追加

1. Issue「申請書追加」テンプレートを使用
2. ブランチを作成: `git checkout -b form/form-name`
3. ファイルを追加
4. HTMLページに統合
5. コミット: `git commit -m "Form: 申請書名を追加"`
6. Pull Requestを作成

### 4. ドキュメントの改善

1. ブランチを作成: `git checkout -b docs/description`
2. ドキュメントを更新
3. コミット: `git commit -m "Docs: ドキュメントの説明"`
4. Pull Requestを作成

## 📝 コーディング規約

### HTML

```html
<!-- 良い例 -->
<div class="container">
    <h1 class="page-title">タイトル</h1>
    <p>本文</p>
</div>

<!-- 悪い例 -->
<div class=container>
<h1>タイトル</h1><p>本文</p></div>
```

- インデント: 4スペース
- クラス名: kebab-case（例: `page-title`）
- セマンティックなHTMLを使用
- アクセシビリティを考慮

### CSS

```css
/* 良い例 */
.page-title {
    font-size: 2rem;
    color: #0066cc;
    margin-bottom: 20px;
}

/* 悪い例 */
.page-title{font-size:2rem;color:#0066cc;margin-bottom:20px;}
```

- インデント: 4スペース
- プロパティは改行して記述
- カラーコードは小文字
- セミコロンを必ず付ける

### JavaScript

```javascript
// 良い例
function toggleAccordion(element) {
    const accordionItem = element.parentElement;
    accordionItem.classList.toggle('active');
}

// 悪い例
function toggleAccordion(element){
const accordionItem=element.parentElement;
accordionItem.classList.toggle('active');}
```

- インデント: 4スペース
- セミコロンを使用
- 変数名: camelCase
- const/let を使用（var は避ける）

## 🔍 コミットメッセージ

### フォーマット

```
<type>: <subject>

<body>
```

### Type の種類

- **Feature**: 新機能
- **Fix**: バグ修正
- **Form**: 申請書の追加
- **Docs**: ドキュメント更新
- **Style**: コードスタイルの変更（動作に影響なし）
- **Refactor**: リファクタリング
- **Test**: テストの追加・修正
- **Chore**: ビルドプロセスやツールの変更

### 例

```bash
# 良い例
git commit -m "Feature: 出産ページに付加給付金の説明を追加"
git commit -m "Fix: 限度額認定証ページのリンク切れを修正"
git commit -m "Form: 埋葬費に権利承継届を追加"

# 悪い例
git commit -m "修正"
git commit -m "update"
git commit -m "fix bug"
```

## ✅ Pull Request のチェックリスト

Pull Request を作成する前に、以下を確認してください：

- [ ] コードが正しく動作する
- [ ] すべてのブラウザで動作確認（Chrome, Firefox, Safari, Edge）
- [ ] モバイル表示を確認
- [ ] すべてのリンクが正しく機能する
- [ ] 新しいファイルが `.gitignore` に含まれていない
- [ ] コミットメッセージが明確
- [ ] Pull Request の説明が詳細
- [ ] 関連する Issue をリンク

## 🧪 テスト

### ブラウザテスト

以下のブラウザで動作確認してください：
- Google Chrome（最新版）
- Mozilla Firefox（最新版）
- Safari（最新版）
- Microsoft Edge（最新版）

### レスポンシブテスト

以下のデバイスサイズで確認してください：
- モバイル: 375px, 414px
- タブレット: 768px, 1024px
- デスクトップ: 1280px, 1920px

### リンクチェック

```bash
# すべてのHTMLファイルでリンクをチェック
grep -r "href=\"" *.html | grep -v "http" | cut -d'"' -f2 | sort -u
```

## 🐛 バグ報告

バグを見つけた場合：

1. Issueテンプレート「バグ報告」を使用
2. 以下の情報を含める：
   - 問題の説明
   - 再現手順
   - 期待される動作
   - 実際の動作
   - スクリーンショット
   - 環境情報（OS, ブラウザ）

## 💡 質問・サポート

- **GitHub Discussions**: 一般的な質問や議論
- **Issues**: バグ報告や機能リクエスト
- **Pull Requests**: コード貢献

## 📜 ライセンス

このプロジェクトに貢献することで、あなたの貢献が丸八真綿健康保険組合の所有物となることに同意したものとみなされます。
