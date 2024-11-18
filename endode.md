### base64一括

# base64 ライブラリをインポートして、Base64デコード機能を利用
```
import base64

# 入力ファイルと出力ファイルのパスを指定
input_file = 'Base64.txt'  
output_file = 'decoded_output.txt'

# 入力ファイルを読み込み、Base64デコードして出力ファイルに書き込み
# with ステートメントを使用して、入力ファイルを読み込み、出力ファイルに書き込み
with open(input_file, 'r') as infile, open(output_file, 'w') as outfile:

# 入力ファイルを行ごとに読み込み、各行をデコードして出力ファイルに書き込み
    for line in infile:
        try:
            # 改行文字を除去し、Base64デコード
            decoded_line = base64.b64decode(line.strip()).decode('utf-8')
            # 出力ファイルに書き込み
            outfile.write(decoded_line + '\n')

# デコード時にエラーが発生した場合、その行をスキップし、エラーメッセージを表示
        except (UnicodeDecodeError, base64.binascii.Error) as e:
            print(f"エラー: {e} 行: {line.strip()}")

print("デコード完了！出力ファイル: ", output_file)

```
