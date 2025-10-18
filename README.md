# GitHub Issues Bulletin Board System

GitHub Issuesを活用したコミュニティ掲示板システムです。

## 📋 概要

このプロジェクトは、GitHub Issuesをバックエンドとして使用するシンプルで美しい掲示板システムです。GitHubリポジトリのIssue機能を活用して、投稿・コメント・管理を行うことができます。

## ✨ 特徴

- **🚀 シンプル設計**: GitHub Issuesをバックエンドに利用
- **📱 モバイル対応**: レスポンシブデザインでスマートフォンにも対応
- **🎨 美しいUI**: モダンなグラデーションデザイン
- **🔄 自動更新**: 5分ごとに投稿を自動で更新
- **📊 統計表示**: 総投稿数、公開中、クローズ済み投稿を表示
- **💬 コメント対応**: GitHub Issuesでのコメント機能をそのまま利用

## 🚀 使い方

### 1. リポジトリの準備

1. GitHubリポジトリを作成（この例では `iwadonchan/my-first-code`）
2. Issues機能を有効化（リポジトリのSettingsから確認）

### 2. 設定

`index.html` 内の `config` オブジェクトを編集：

```javascript
const config = {
    owner: 'YOUR_GITHUB_USERNAME',    // GitHubユーザー名
    repo: 'YOUR_REPOSITORY_NAME',     // リポジトリ名
    maxPosts: 20                      // 表示する最大投稿数
};
```

### 3. デプロイ

- **GitHub Pages**: リポジトリのSettings > Pagesから有効化
- **Vercel**: HTMLファイルをデプロイ
- **Netlify**: ドラッグ＆ドロップでデプロイ

### 4. 投稿の作成

- 掲示板の「新規投稿」ボタンからGitHub Issues作成ページへ
- Issueのタイトルが掲示板の投稿タイトルになります
- Issueの本文が投稿内容になります
- コメントはGitHub Issuesのコメント機能で管理

## 🛠 技術スタック

- **HTML5**: セマンティックなマークアップ
- **CSS3**: モダンなスタイリングとアニメーション
- **JavaScript (ES6+)**: GitHub API連携とDOM操作
- **GitHub API**: Issuesデータの取得
- **Responsive Design**: モバイルファースト設計

## 📁 ファイル構成

```
BBS/
├── index.html      # メインのHTMLファイル
├── issues.json     # サンプルデータ（開発用）
└── README.md       # このファイル
```

## 🎨 デザインの特徴

- **グラデーション背景**: 紫系の美しいグラデーション
- **ガラスモーフィズム**: 半透明のコンテナにぼかし効果
- **ホバーエフェクト**: インタラクティブなアニメーション
- **モバイル対応**: スマートフォンでの最適化表示

## ⚙️ 関数説明

### 主要なJavaScript関数

- `fetchGitHubIssues()`: GitHub APIからIssuesを取得
- `displayPosts()`: 投稿を画面に表示
- `createPostHTML()`: 投稿データをHTMLに変換
- `updateStats()`: 統計情報を更新
- `formatDate()`: 日時を日本語フォーマットに変換

## 🔧 カスタマイズ

### テーマカラーの変更

CSSのカラーコードを編集：

```css
/* ヘッダーのグラデーション */
.header {
    background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
}

/* ボタンの色 */
.btn-primary {
    background: linear-gradient(135deg, #3b82f6 0%, #2563eb 100%);
}
```

### 表示する投稿数の変更

```javascript
const config = {
    maxPosts: 30  // 表示する投稿数を調整
};
```

## 📝 GitHub APIについて

- **認証**: パブリックリポジトリの場合は認証不要
- **レート制限**: 未認証時: 60回/時間、認証時: 5000回/時間
- **CORS対策**: `User-Agent`ヘッダーを追加

## 🌐 デプロイ例

### GitHub Pagesでのデプロイ

1. リポジトリのSettings > Pagesへ
2. Sourceを「Deploy from a branch」に設定
3. Branchを「main」または「master」に設定
4. `https://username.github.io/repository-name/` でアクセス

### Vercelでのデプロイ

```bash
# Vercel CLIをインストール
npm i -g vercel

# デプロイ
vercel --prod
```

## 🐛 トラブルシューティング

### GitHub APIエラーが発生する場合

1. リポジトリが公開（Public）であることを確認
2. リポジトリ名とユーザー名が正しいことを確認
3. Issues機能が有効化されていることを確認

### CORSエラーが発生する場合

- `User-Agent`ヘッダーが正しく設定されているか確認
- リポジトリが存在することを確認

## 📄 ライセンス

このプロジェクトはMITライセンスの下で提供されています。

## 🤝 貢献

Pull RequestやIssueでのご報告を歓迎します。

## 🔗 関連リンク

- **GitHubリポジトリ**: https://github.com/iwadonchan/my-first-code
- **デモサイト**: https://iwadonchan.github.io/my-first-code/
- **GitHub APIドキュメント**: https://docs.github.com/en/rest

---

## 📞 サポート

問題が発生した場合は、以下の点を確認してください：

1. リポジトリが存在し、公開されている
2. Issues機能が有効化されている
3. GitHubユーザー名とリポジトリ名が正しい

それでも問題が解決しない場合は、GitHub Issuesでご報告ください。