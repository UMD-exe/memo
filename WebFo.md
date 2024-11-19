

# ブラウザフォレンジック
ブラウザのメタデータはどこでも残るのでフォレンジック対象としては興味深いということだと思う
NirSoftのフォレンジックツール群がとても役に立つ
Freeware Web Browser Tools Package
## IE
Internet Explorer
IE 8-11 （Windows7） C:¥Users¥【ユーザー名】¥AppData¥Local¥Microsoft¥Windows¥Temporary Internet Files¥Content.IE5
IE 11（Windows8 以降） C:¥Users¥【ユーザー名】¥AppData¥Local¥Microsoft¥Windows¥INetCache

## Chrome
- ログ
- C:¥Users¥【ユーザー名】¥AppData¥Local¥Google¥Chrome¥User Data¥Default¥Cache
  - 保存されている認証情報
- C:¥Users¥【ユーザー名】¥AppData¥Local¥Google¥Chrome¥User Data¥Default¥Login DataをDB Browser for SQLiteで開いて確認
  - nirsoftにも解析ツールはあるが、パスワードが暗号化されていると見れなくなる
  - パスワードが暗号化されている場合はDPAPIが使われている
    - mimikatzを起動して
```
dpapi::chrome /in:"C:\Users\eric\Downloads\Seized\AppData\Local\Google\Chrome\User Data\Default\Login Data" /masterkey:138f089556f32b87e53c5337c47f5f34746162db7fe9ef47f13a92c74897bf67e890bcf9c6a1d1f4cc5454f13fcecc1f9f910afb8e2441d8d3dbc3997794c630みたいに復号
```

    - 副産物にAESキーが得られる
    - Local Stateというファイルも持っている場合は、追加でstate:"Local Stateへのパス"を追加すると別の情報が得られるかも

## FireFox
- Firefox 32.0以降  
  - C:¥Users¥【ユーザー名】¥AppData¥Local¥Mozilla¥Firefox¥Profiles ¥【プロファイル名】.default¥cache2  
  - Firefoxは、一時ファイル（キャッシュ）としてダウンロードしたファイルの末尾に、HTTPリクエスト/レスポンスの情報を追記する。バイナリエディタで確認することで、ダウンロード元URLを特定することが可能  
- .mozillaにfirefoxの情報が入ってる  
  - firefoxの履歴情報はplaces.sqliteに入っているから、これを覗けば中身が見られる  
  - Ubuntu 22だと~/snap/firefox/common/.mozilla/firefox/にプロファイルがおいてあるかも  
- メモリから認証情報が抜けるかも  
  - psでPIDを手に入れてprocdump64.exeを被害者環境に入れて.\procdump64.exe -accepteula -ma [PID]で持ってくる。  
  - stringsで文字列を探してgrep passwordで認証情報っぽいもが無いか探してみよう  

### 解析ツール
- https://github.com/Busindre/dumpzilla
  - python3 dumpzilla.py ./Firefox/Profiles/br873ssy.default-release/
  - 履歴情報などを抜く
