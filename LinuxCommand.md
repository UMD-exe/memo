## 削除ファイルの検索復元コマンド【lsofコマンド】
### 検索
```
lsof | grep '(deleted)'
```

例）
|COMMAND| PID|USER|FD |TYPE |DEVICE|SIZE/OFF|NODE NAME|
|-------|----|----|---|-----|------|-------|----------|
|vin    |1234|user|4u|REG 8,1|12345|5678|/tmp/example.txt (deleted)|


### 復元
```
cp /proc/<PID>/fd/<FD> /path/to/recover_file
```

例）PIDが1234、FDが4の場合、次のコマンドを実行します
```
cp /proc/1234/fd/4 /path/to/recover_file
```

