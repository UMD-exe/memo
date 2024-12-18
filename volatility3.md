## options
| プラグイン                                | 説明                                                                                  |
|----------------------------------------|-------------------------------------------------------------------------------------|
| `configwriter.ConfigWriter`            | 自動マジックを実行し、設定を出力ディレクトリに出力します。                                    |
| `layerwriter.LayerWriter`              | 自動マジックを実行し、レイヤーが指定されていない場合は生成されたレイヤーをリストします。レイヤー名が指定されている場合は、そのレイヤーを書き出します。 |
| `linux.bash.Bash`                      | メモリからBashコマンド履歴を復元します。                                                      |
| `linux.check_afinfo.Check_afinfo`      | ネットワークプロトコルの操作関数ポインターを検証します。                                          |
| `linux.check_syscall.Check_syscall`    | システムコールテーブルにフックがないかチェックします。                                              |
| `linux.elfs.Elfs`                      | すべてのプロセスのメモリマップされたELFファイルをリストします。                                         |
| `linux.lsmod.Lsmod`                    | 読み込まれているカーネルモジュールをリストします。                                                |
| `linux.lsof.Lsof`                      | すべてのプロセスのメモリマップをリストします。                                                 |
| `linux.malfind.Malfind`                | 潜在的に注入されたコードが含まれるプロセスメモリ範囲をリストします。                                      |
| `linux.proc.Maps`                      | すべてのプロセスのメモリマップをリストします。                                                 |
| `linux.pslist.PsList`                  | 特定のLinuxメモリイメージに存在するプロセスをリストします。                                         |
| `linux.pstree.PsTree`                  | 親プロセスIDに基づいてプロセスをツリー形式でリストします。                                           |
| `mac.bash.Bash`                        | メモリからBashコマンド履歴を復元します。                                                      |
| `mac.check_syscall.Check_syscall`      | システムコールテーブルにフックがないかチェックします。                                              |
| `mac.check_sysctl.Check_sysctl`        | sysctlハンドラーにフックがないかチェックします。                                               |
| `mac.check_trap_table.Check_trap_table`| machトラップテーブルにフックがないかチェックします。                                              |
| `mac.ifconfig.Ifconfig`                | 読み込まれているカーネルモジュールをリストします。                                                |
| `mac.lsmod.Lsmod`                      | 読み込まれているカーネルモジュールをリストします。                                                |
| `mac.lsof.lsof`                        | すべてのプロセスのオープンファイルディスクリプタをリストします。                                         |
| `mac.malfind.Malfind`                  | 潜在的に注入されたコードが含まれるプロセスメモリ範囲をリストします。                                      |
| `mac.netstat.Netstat`                  | すべてのプロセスのネットワーク接続をリストします。                                                |
| `mac.proc_maps.Maps`                   | 潜在的に注入されたコードが含まれるプロセスメモリ範囲をリストします。                                      |
| `mac.psaux.Psaux`                      | プログラムのコマンドライン引数を復元します。                                                 |
| `mac.pslist.PsList`                    | 特定のMacメモリイメージに存在するプロセスをリストします。                                          |
| `mac.pstree.PsTree`                    | 親プロセスIDに基づいてプロセスをツリー形式でリストします。                                           |
| `mac.tasks.Tasks`                      | 特定のMacメモリイメージに存在するプロセスをリストします。                                          |
| `mac.trustedbsd.trustedbsd`            | 悪意のあるtrustedbsdモジュールがないかチェックします。                                         |
| `timeliner.Timeliner`                  | 時間関連情報を提供するすべての関連プラグインを実行し、結果を時間順に並べます。                               |
| `windows.bigpools.BigPools`            | 大きなページプールをリストアップします。                                                 |
| `windows.cachedump.Cachedump`          | メモリからlsaシークレットをダンプします。                                                |
| `windows.callbacks.Callbacks`          | カーネルコールバックおよび通知ルーチンをリストします。                                             |
| `windows.cmdline.CmdLine`              | プロセスのコマンドライン引数をリストします。                                                  |
| `windows.crashinfo.Crashinfo`          | Windowsのクラッシュダンプの情報をリストします。                                               |
| `windows.devicetree.DeviceTree`        | 特定のWindowsメモリイメージにおけるドライバと付属デバイスに基づくツリーをリストします。                     |
| `windows.dlllist.DllList`              | 特定のWindowsメモリイメージに読み込まれているモジュールをリストします。                                   |
| `windows.driverirp.DriverIrp`          | 特定のWindowsメモリイメージ内のドライバのIRPをリストします。                                        |
| `windows.drivermodule.DriverModule`    | 読み込まれたドライバがルートキットによって隠されているかどうかを判断します。                                   |
| `windows.driverscan.DriverScan`        | 特定のWindowsメモリイメージに存在するドライバをスキャンします。                                       |
| `windows.dumpfiles.DumpFiles`          | Windowsのメモリサンプルからキャッシュされたファイルの内容をダンプします。                                 |
| `windows.envars.Envars`                | プロセス環境変数を表示します。                                                      |
| `windows.filescan.FileScan`            | 特定のWindowsメモリイメージに存在するファイルオブジェクトをスキャンします。                                  |
| `windows.getservicesids.GetServiceSIDs`| プロセストークンのSIDをリストします。                                              |
| `windows.getsids.GetSIDs`              | 各プロセスを所有するSIDを表示します。                                                 |
| `windows.handles.Handles`              | プロセスのオープンハンドルをリストします。                                                  |
| `windows.hashdump.Hashdump`            | メモリからユーザーハッシュをダンプします。                                                |
| `windows.info.Info`                    | 解析中のメモリサンプルのOSおよびカーネルの詳細を表示します。                                           |
| `windows.joblinks.JobLinks`            | プロセスのジョブリンク情報を表示します。                                                 |
| `windows.ldrmodules.LdrModules`        | 特定のWindowsメモリイメージに読み込まれているモジュールをリストします。                                   |
| `windows.lsadump.Lsadump`              | メモリからlsaシークレットをダンプします。                                                |
| `windows.malfind.Malfind`              | 潜在的に注入されたコードが含まれるプロセスメモリ範囲をリストします。                                      |
| `windows.mbrscan.MBRScan`              | 潜在的なマスターブートレコード（MBR）をスキャンして解析します。                                       |
| `windows.memmap.Memmap`                | メモリマップを表示します。                                                      |
| `windows.mftscan.MFTScan`              | 特定のWindowsメモリイメージに存在するMFT FILEオブジェクトをスキャンします。                          |
| `windows.modscan.ModScan`              | 特定のWindowsメモリイメージに存在するモジュールをスキャンします。                                      |
| `windows.modules.Modules`              | 読み込まれているカーネルモジュールをリストします。                                                |
| `windows.mutantscan.MutantScan`        | 特定のWindowsメモリイメージに存在するミューテックスをスキャンします。                                     |
| `windows.netscan.NetScan`              | 特定のWindowsメモリイメージに存在するネットワークオブジェクトをスキャンします。                                 |
| `windows.netstat.NetStat`              | 特定のWindowsメモリイメージに存在するネットワーク追跡構造を走査します。                                 |
| `windows.poolscanner.PoolScanner`      | 汎用プールスキャナプラグインです。                                                   |
| `windows.privileges.Privs`             | プロセストークンの特権をリストします。                                                  |
| `windows.pslist.PsList`                | 特定のWindowsメモリイメージに存在するプロセスをリストします。                                        |
| `windows.psscan.PsScan`                | 特定のWindowsメモリイメージに存在するプロセスをスキャンします。                                        |
| `windows.pstree.PsTree`                | 親プロセスIDに基づいてプロセスをツリー形式でリストします。                                           |
| `windows.registry.certificates.Certificates`| レジストリの証明書ストアにある証明書をリストします。                                           |
| `windows.registry.hivelist.HiveList`   | 特定のメモリイメージに存在するレジストリハイブをリストします。                                         |
| `windows.registry.hivescan.HiveScan`   | 特定のWindowsメモリイメージに存在するレジストリハイブをスキャンします。                                    |
| `windows.registry.printkey.PrintKey`   | ハイブまたは特定のキー値の下のレジストリキーをリストします。                                         |
| `windows.registry.userassist.UserAssist`| ユーザーアシストレジストリキーと情報を表示します。                                              |
| `windows.sessions.Sessions`            | 環境変数から抽出されたセッション情報を持つプロセスをリストします。                                       |
| `windows.skeleton_key_check.Skeleton_Key_Check`| スケルトンキーのマルウェアの兆候を探します。                                                |
| `windows.ssdt.SSDT`                    | システムコールテーブルをリストします。                                                   |
| `windows.statistics.Statistics`        | メモリ空間に関する統計情報をリストします。                                               |
| `windows.strings.Strings`              | stringsコマンドの出力を読み込み、それぞれの文字列がどのプロセスに属しているかを示します。                           |
| `windows.svcscan.SvcScan`              | Windowsサービスをスキャンします。                                                  |
| `windows.symlinkscan.SymlinkScan`      | 特定のWindowsメモリイメージに存在するリンクをスキャンします。                                      |
| `windows.vadinfo.VadInfo`              | プロセスメモリ範囲をリストします。                                                  |
| `windows.vadwalk.VadWalk`              | VADツリーをウォークします。                                                     |
| `windows.vadyarascan.VadYaraScan`      | YARAを使用して仮想アドレス記述子のメモリマップをスキャンします。                                      |
| `windows.verinfo.VerInfo`              | PEファイルのバージョン情報をリストします。                                               |
| `windows.virtmap.VirtMap`              | 仮想マップセクションをリストします。                                                 |
| `yarascan.YaraScan`                    | YARAルール（文字列またはファイル）を使用してメモリをスキャンします。                                |


## エントリーキーの永続化調査
レジストリは、いくつかの Windows オペレーティング システムに共通していますが、それらの間にいくつかの違いがあります。 
レジストリ ハイブは、データのバックアップを含む一連のサポート ファイルを含む、レジストリ内のキー、サブキー、および値のグループ

つまり、レジストリに設定された内容も調べることが可能。
スタートアップに設定されたバックドアを調べるには、メモリイメージからハイブリストのsoftwareのメモリ情報取得する。
```

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
```

softwareのレジストリキーの中にMicrosoft\Windows\CurrentVersion\Runが存在し、これが起動時に実行されるものが配置される。
例だと、オフセットは「0xd40ca703d000」であるから下記のように検索すると、
```

$ python3 vol.py -f  /ShareVM/memory.raw printkey --offset 0xd40ca703d000 --key "Microsoft\Windows\CurrentVersion\Run" 
Volatility 3 Framework 2.11.0
Progress:  100.00               PDB scanning finished                        
Last Write Time Hive Offset     Type    Key     Name    Data    Volatile

2021-04-06 01:01:27.000000 UTC  0xd40ca703d000  REG_EXPAND_SZ   \SystemRoot\System32\Config\SOFTWARE\Microsoft\Windows\CurrentVersion\Run       SecurityHealth  "%windir%\system32\SecurityHealthSystray.exe"   False
2021-04-06 01:01:27.000000 UTC  0xd40ca703d000  REG_SZ  \SystemRoot\System32\Config\SOFTWARE\Microsoft\Windows\CurrentVersion\Run       StartVPN        "C:\Users\Public\PSclient.exe -autorestart -relayserver 13.54.35.87:5555"       False
 ```

このようにVPNが張られる通信が発生するように仕込まれているのがわかる。  
