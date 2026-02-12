# 丸八真綿健康保険組合 公式ホームページ

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-success)](https://YOUR-USERNAME.github.io/maruhachi-kenpo/)
[![License](https://img.shields.io/badge/License-Proprietary-red)](LICENSE)

## 📋 プロジェクト概要

丸八真綿健康保険組合の公式ホームページです。健康保険の各種手続き、申請書のダウンロード、健康づくり情報などを提供しています。

## 🌐 公開URL

**GitHub Pages:** `https://YOUR-USERNAME.github.io/maruhachi-kenpo/`

## 📁 ディレクトリ構造

```
maruhachi_kenpo_site/
├── index.html                          # トップページ
│
├── 手続き・申請ページ
│   ├── procedure-family.html           # 扶養家族に関する手続き
│   ├── procedure-certificate.html      # 資格確認書・限度額認定証
│   ├── procedure-injury.html           # 病気・ケガをしたとき
│   ├── procedure-payment.html          # 立て替え払いをしたとき
│   ├── procedure-medical-cost.html     # 医療費が高額になるとき
│   ├── procedure-birth.html            # 出産したとき
│   ├── procedure-death.html            # 亡くなったとき
│   ├── procedure-retirement.html       # 退職したとき
│   └── procedure-checkup.html          # 健診について
│
├── 詳細ページ
│   ├── family-form-info.html           # 被扶養者届の詳細
│   ├── family-status-form-info.html    # 被扶養者状況報告書の詳細
│   ├── family-eligibility.html         # 被扶養者資格について
│   ├── family-documents-search.html    # 必要書類検索
│   ├── limit-certificate-info.html     # 限度額適用認定証の詳細
│   └── medical-expense-application-guide.html  # 療養費申請ガイド
│
├── 申請書類（Excel, PDF）
│   ├── family-form.xlsx                # 被扶養者届（異動届）
│   ├── family-status-form.xlsx         # 被扶養者状況報告書
│   ├── sickness-benefit-application.xlsx      # 傷病手当金支給申請書
│   ├── third-party-injury.xlsx         # 第三者行為による傷病届
│   ├── medical-expense-application-form.xlsx  # 療養費支給申請書
│   ├── acupuncture-massage-application.pdf    # はり・灸・マッサージ用申請書
│   ├── evidence-attachment-sheet.pdf   # 確証添付台紙
│   ├── limit-application-form.xlsx     # 限度額適用認定申請書
│   ├── maternity-allowance-application.xlsx   # 出産手当金請求書
│   ├── childbirth-lump-sum-application.xlsx   # 出産育児一時金請求書
│   ├── burial-expense-application.xlsx # 埋葬料（費）請求書
│   └── succession-of-rights.pdf        # 権利承継届
│
├── セクションページ
│   ├── health/index.html               # 健康づくり関連
│   ├── benefits/index.html             # 保険給付一覧
│   ├── about/index.html                # 当健保組合について
│   ├── contact/index.html              # お問い合わせ
│   └── forms/index.html                # 申請書一覧
│
└── 設定ファイル
    ├── .gitignore                      # Git除外設定
    └── README.md                       # このファイル
```

## 🚀 クイックスタート

### ローカル開発

```bash
# 1. リポジトリをクローン
git clone https://github.com/YOUR-USERNAME/maruhachi-kenpo.git

# 2. ディレクトリに移動
cd maruhachi-kenpo

# 3. ブラウザで開く
# Macの場合
open index.html

# Windowsの場合
start index.html

# Linuxの場合
xdg-open index.html
```

### GitHub Pagesでの公開

1. GitHubリポジトリの **Settings** に移動
2. **Pages** セクションを選択
3. **Source** を `main` ブランチに設定
4. 保存後、数分で `https://YOUR-USERNAME.github.io/maruhachi-kenpo/` で公開

## 🔧 開発ワークフロー

### 新機能の追加

```bash
# 1. 最新のmainブランチを取得
git checkout main
git pull origin main

# 2. 新しいブランチを作成
git checkout -b feature/new-feature-name

# 3. ファイルを編集
# （例）procedure-retirement.htmlを修正

# 4. 変更を確認
git status
git diff

# 5. ステージングに追加
git add procedure-retirement.html

# 6. コミット（わかりやすいメッセージで）
git commit -m "退職時の手続きページに任意継続の説明を追加"

# 7. GitHubにプッシュ
git push origin feature/new-feature-name

# 8. GitHubでPull Requestを作成
# ブラウザでGitHubにアクセスし、「Compare & pull request」をクリック

# 9. レビュー後、mainにマージ
```

### コミットメッセージの例

```
✅ 良い例:
- "出産育児一時金に付加給付金2万円の記載を追加"
- "埋葬費ページに権利承継届のダウンロードボタンを追加"
- "限度額適用認定証ページから不要なリンクを削除"

❌ 悪い例:
- "修正"
- "update"
- "fix bug"
```

## 📝 最近の更新履歴

### 2025年2月12日
- 埋葬費（家族がいない場合）に権利承継届PDFを追加
- 出産育児一時金の支給額に「付加給付金２万円」を追加
- 出生児を被扶養者にする際、扶養家族ページへのリンクを実装

### 2025年2月11日
- 医療費が高額になるときのページを2つのアコーディオンに整理
- 限度額適用認定証申請書（Excel）を追加
- マイナ保険証の説明を追加

### 2025年2月10日
- 立て替え払いページを2つのアコーディオンに整理
- 療養費支給申請書（Excel）と確証添付台紙（PDF）を追加
- はり・灸・マッサージ用申請書（PDF）を追加
- 療養費申請ガイドページを作成

### 2025年2月9日
- 第三者行為による傷病届（交通事故）のExcelファイルと記入見本PDFを追加
- 傷病手当金支給申請書を追加

## 📄 主要な申請書類一覧

| カテゴリ | 申請書類 | ファイル形式 | ファイル名 |
|---------|---------|------------|-----------|
| 扶養家族 | 被扶養者届（異動届） | Excel | family-form.xlsx |
| 扶養家族 | 被扶養者状況報告書 | Excel | family-status-form.xlsx |
| 病気・ケガ | 傷病手当金支給申請書 | Excel | sickness-benefit-application.xlsx |
| 病気・ケガ | 第三者行為による傷病届 | Excel | third-party-injury.xlsx |
| 立て替え払い | 療養費支給申請書 | Excel | medical-expense-application-form.xlsx |
| 立て替え払い | はり・灸・マッサージ用申請書 | PDF | acupuncture-massage-application.pdf |
| 立て替え払い | 確証添付台紙 | PDF | evidence-attachment-sheet.pdf |
| 医療費高額 | 限度額適用認定申請書 | Excel | limit-application-form.xlsx |
| 出産 | 出産手当金請求書 | Excel | maternity-allowance-application.xlsx |
| 出産 | 出産育児一時金請求書 | Excel | childbirth-lump-sum-application.xlsx |
| 死亡 | 埋葬料（費）請求書 | Excel | burial-expense-application.xlsx |
| 死亡 | 権利承継届 | PDF | succession-of-rights.pdf |

## 🎨 デザインガイドライン

### カラーパレット
```css
--primary-color: #0066cc;      /* 青（メイン） */
--background-color: #f5f5f5;   /* ライトグレー */
--accent-color: #ffa000;       /* オレンジ（注意） */
--text-color: #333;            /* ダークグレー */
--white: #ffffff;              /* 白 */
--border-color: #e0e0e0;       /* ボーダー */
```

### タイポグラフィ
```css
font-family: 'Hiragino Kaku Gothic Pro', 'Meiryo', sans-serif;
line-height: 1.8;
```

### レスポンシブブレークポイント
- モバイル: ~768px
- タブレット: 768px~1024px
- デスクトップ: 1024px~

## 🤝 貢献方法

1. このリポジトリをフォーク
2. 新しいブランチを作成 (`git checkout -b feature/amazing-feature`)
3. 変更をコミット (`git commit -m 'Add some amazing feature'`)
4. ブランチにプッシュ (`git push origin feature/amazing-feature`)
5. Pull Requestを作成

### Pull Requestのチェックリスト

- [ ] コードが正しく動作することを確認
- [ ] すべてのリンクが正しく機能することを確認
- [ ] ブラウザの互換性を確認（Chrome, Firefox, Safari, Edge）
- [ ] モバイル表示を確認
- [ ] コミットメッセージがわかりやすい
- [ ] 関連するIssueがあればリンク

## 🐛 バグ報告

バグを見つけた場合は、[Issues](https://github.com/YOUR-USERNAME/maruhachi-kenpo/issues)で報告してください。

**報告に含める情報:**
- 発生した問題の説明
- 再現手順
- 期待される動作
- 実際の動作
- スクリーンショット（あれば）
- ブラウザとバージョン

## 📧 お問い合わせ

- **健康保険組合**: 丸八真綿健康保険組合
- **GitHub Issues**: バグ報告や機能リクエスト
- **Pull Requests**: コード貢献

## 📜 ライセンス

© 丸八真綿健康保険組合 All rights reserved.

このプロジェクトは丸八真綿健康保険組合の所有物です。

## 🙏 謝辞

- いらすとや: イラスト素材の提供
