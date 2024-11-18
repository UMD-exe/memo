## AESのパスワード復号
### 導入
- 必要なもの
ConvertTo-SecureString(PowerShell 3.0以降で利用可能)

- Installation method
1. コマンドレットの正しい入力を確認する コマンドが正しく入力されているか確認
```
ConvertTo-SecureString -String "YourPasswordHere" -AsPlainText -Force
```

2. 実行ポリシーの確認 スクリプトが実行できるように、実行ポリシーを確認
```
Set-ExecutionPolicy RemoteSigned
```

3. 必要なモジュールのインポート
```
Import-Module Microsoft.PowerShell.Security
```


