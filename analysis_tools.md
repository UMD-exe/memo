# Autopsy
Autopsyは、BasisTechnologyが提供している統合型のフォレンジックツール。  
統合型ということで、単一のアーティファクトを解析するタイプではなく、HDDやイメージデータまるごと解析するタイプのツールになる。
参考資料：  
[Autopsyのインストールから基礎的な使い方まで](https://muchipopo.com/forensic/autopsy/)  
[Autopsyで迅速なマルウェアのスキャンとディスク内の簡単調査](https://www.slideshare.net/slideshow/cb19-autopsy-by/206640023)  

# MFTECmd
主にNTFSファイルシステムの$MFT（Master File Table）を解析するために使用される。このツールは、$MFTだけでなく、$Boot、$J、$SDS、$LogFileなどの他のNTFSメタデータファイルも解析できる。
MFTECmdは、コマンドラインインターフェースを使用しており、解析結果をJSONやCSV形式で保存することができる。デジタルフォレンジックの調査において、重要なアーティファクトを提供するため、調査官にとって非常に有用なツール。
<details><summary>詳細</summary>  
  
* MFTECmd使用例
```ex
MFTECmd -f "$MFTファイル" --csvf"保存先ファイル名" --fls
```
```ex
MFTECmd -f "$MFTファイル" --de [シーケンス番号-入力]
```

* オプション一覧
 
| オプション | 説明 |
|------------|------|
| `-f` | ファイルを処理する（$MFT, $J, $Boot, $SDS, $LogFileなど） |
| `--json` | JSON形式の結果を保存するディレクトリ |
| `--jsonf` | JSON形式の結果を保存するファイル名 |
| `--csv` | CSV形式の結果を保存するディレクトリ |
| `--csvf` | CSV形式の結果を保存するファイル名 |
| `--body` | Bodyfile形式の結果を保存するディレクトリ |
| `--bodyf` | Bodyfile形式の結果を保存するファイル名 |
| `--bdl` | Bodyfileのドライブレター |
| `--do` | ファイルレコードのオフセットをダンプする |
| `--de` | 入力/シーケンス番号の詳細をダンプする |
| `--fls` | ディレクトリの内容を表示する |
| `--ds` | セキュリティIDの詳細をダンプする |
| `--dt` | カスタム日付/時刻形式 |
| `--sn` | DOSファイル名タイプを含める |
| `--fl` | コンパクトなファイルリストを生成する |
| `--at` | すべてのタイムスタンプを含める |
| `--vss` | ボリュームシャドコピーを処理する |
| `--dedupe` | SHA-1で重複を削除する |
| `--debug` | デバッグ情報を表示する |

参考資料：  
[タイムライン解析によるマルウェア感染原因の特定](https://www.sendai-ctf.org/Library/2018/day1/sendaiCTF2018_Day1_02_lab.pdf)

</details>

# MFTExplorer
主にNTFSファイルシステムの$MFT（Master File Table）を視覚的に解析するために使用される。このツールは、$MFTだけでなく、$Boot、$J、$SDS、$LogFile（近日対応予定）などの他のNTFSメタデータファイルも解析できる。  

# TimelineExplorer
主にCSVやExcelファイルを視覚的に解析するために使用される。このツールは、デジタルフォレンジック調査において、タイムラインデータを効率的に解析するための機能を提供。


[サイバーセキュリティ担当者向け、おすすめツール、サイト、勉強本](https://qiita.com/eguchi7309/items/475e030fd52c013911e8)

***
# tesseract
```
sudo apt-get install tesseract-ocr
```
