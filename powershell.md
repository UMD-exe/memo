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

例）
```
PS C:\work> # 平文データ
PS C:\work> $plainText = "YourSensitiveData"
PS C:\work>
PS C:\work> # セキュアストリングに変換
PS C:\work> $secureString = ConvertTo-SecureString $plainText -AsPlainText -Force
PS C:\work>
PS C:\work> # セキュアストリングをBase64エンコードで文字列化
PS C:\work> $encryptedText = ConvertFrom-SecureString -SecureString $secureString -Key (1..32)
PS C:\work>
PS C:\work> # 暗号化された文字列をファイルに保存
PS C:\work> Set-Content -Path "encrypted.txt" -Value $encryptedText
PS C:\work> # 暗号化された文字列を読み込み
PS C:\work> $encryptedText = Get-Content -Path "encrypted.txt"
PS C:\work>
PS C:\work> # セキュアストリングに変換
PS C:\work> $secureString = ConvertTo-SecureString -String $encryptedText -Key (1..32)
PS C:\work>
PS C:\work> # セキュアストリングをプレーンテキストに変換
PS C:\work> $plainText = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secureString))
PS C:\work>
PS C:\work> Write-Output $plainText
YourSensitiveData
```
