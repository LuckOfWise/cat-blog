# OneSignal プッシュ通知設定

## GitHub Secrets 設定

このワークフローを有効にするために、以下のGitHub Secretsを設定する必要があります：

### 必要なSecrets

1. **ONESIGNAL_API_KEY**
   - OneSignal の REST API Key
   - OneSignal Dashboard > Settings > Keys & IDs > REST API Key から取得
   - 形式: `Basic xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`

2. **ONESIGNAL_APP_ID** 
   - アプリケーションID（既に設定済み）
   - 値: `573400b8-97dd-4b8f-b416-760352a8739b`

### Secretsの設定方法

1. GitHubリポジトリページに移動
2. **Settings** > **Secrets and variables** > **Actions** に移動
3. **New repository secret** をクリック
4. 上記のSecretを追加

### ワークフローの動作

- `main` ブランチに新しい投稿（`content/posts/*.md`）がプッシュされた時のみ通知が送信されます
- OneSignal Secretsが設定されていない場合は、エラーを出さずにスキップされます
- 通知は日本語で「🐾 新しいラムネの記事だにゃ！」として送信されます
- 通知をクリックすると新しい投稿のURLに移動します

### トラブルシューティング

通知が送信されない場合：
1. GitHub Actions のログを確認
2. OneSignal の Delivery タブで配信状況を確認  
3. Secretsが正しく設定されているか確認