# webExploit
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
</details>
参考資料：
[SQL](https://qiita.com/shyamahira/items/9f80d16c3436f9dea753)


## Cookie
### curlでCookieを保存、送信する
```
curl -b "KEY=VALUE" http://localhost
```

<details><summary>詳細</summary> 

例
```
curl 10.6.255.116:3000/orders -b "bakeSaleVolunteer=dHJ1ZQ%3D%3D"
```

参考資料：
[curlでCookieを保存、送信する](https://qiita.com/shyamahira/items/9f80d16c3436f9dea753)
[cookie の取得方法と curl で cookie を送信する方法](https://qiita.com/fmyuk/items/dec3992caa4fd4f574fd)

</details>

# トラバー



錬成環境：
[hacker101](https://ctf.hacker101.com/ctf)

- 教訓
サーバーに入る系の問題で管理者権限が与えられていない場合、 sudo -lを使用すると何をしたらいいのかわかることがある。
