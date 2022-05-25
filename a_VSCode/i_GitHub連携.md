# Git・GitHubと連携する

### Gitをインストール
* [Windows](https://gitforwindows.org/)
* [macOS](https://git-scm.com/download/mac)

### Gitを設定
```bash
git config --global user.name {名前}
git config --global user.email {メールアドレス}
```

### ローカルリポジトリ初期化
1. VS Codeでフォルダーを開く
2. ターミナルを開く
3. ローカルリポジトリ初期化
```bash
git init
```
4. 「ソース管理」のメニューから、ステージング➡メッセージ➡コミット

### GitHubと連携
1. GitHubでリモートリポジトリを作成
2. ローカルリポジトリをリモートリポジトリに紐づける
3. ローカルリポジトリからリモートリポジトリにプッシュする

#### リモートリポジトリに紐づける
```bash
git remote add origin https://github.com/{ユーザー名}/{リポジトリ名}.git
```

結果確認
```bash
git remote -v
```

#### リモートリポジトリにプッシュする
```bash
git branch -M main
git push -u origin main
```

最初に _fatal: refusing to merge unrelated histories_ エラーが発生する可能性がある。この場合、``git pull``または``git merge``コマンド後ろに **allow-unrelated-histories** スイッチを切り替えることで解決できる。
```bash
git pull origin main --allow-unrelated-histories
```



